# Database Designer Dot Skill

Relational schema design - normalization, keys, constraints, and evolution - use when modeling data or reviewing a schema.

## Skill Metadata

* Identifier: `dots-skill-database-designer`
* Category: Engineering
* Target Engine: GPT-6 Astra (OpenAI Dots)
* Primary MCP Dependency: `dots-mcp-custom`

## Standing Responsibility Prompt

Paste this instruction into your OpenAI Dot conversation to assign this background responsibility:

```text
Act as my Database Designer specialist. Monitor relevant incoming events, perform analysis autonomously, and draft recommendations in my activity log. Pause and ask for my confirmation before modifying any external records.
```

## Governance and Permission Mapping

| Action Phase | Operation | Assigned Permission Mode |
| :--- | :--- | :--- |
| Ingestion | Scanning feeds, reading logs, and inspecting state | Autonomous Execution |
| Processing | Running local transforms, filtering, and drafting | Autonomous Execution |
| Verification | Compiling candidate recommendations and reports | Prompt-Initiated Execution |
| Modification | Committing changes, dispatching messages, or updating records | Supervised Execution |
| Destruction | Deleting records, purging branches, or revoking access | User Handoff |

## Operational Instructions

## Overview

Good schema design is decided once and paid for (or repaid) forever. This skill
covers the principles behind durable relational schemas: normalization done
pragmatically, key selection, constraints as documentation, and how to evolve a
schema without downtime.

## When to use

- Designing a new database schema from requirements
- Reviewing an existing schema for design smells
- Deciding between surrogate keys (UUID/serial) and natural keys
- Planning zero-downtime migrations for a live database
- Choosing data types (timestamps, money, enums, JSON columns)

## Core concepts

**Normalize to 3NF by default, denormalize with evidence.** First normal form
(atomic values, no repeating groups), second (no partial dependencies), third
(no transitive dependencies) eliminate update anomalies. Denormalize only for a
measured query problem - a cached count or a materialized summary - never
preemptively.

**Keys carry meaning.** Primary keys should be stable, unique, and meaningless
if possible: surrogate integer/UUID keys survive business-rule changes that
natural keys (email, username, SKU formats) do not. Foreign keys enforce
referential integrity - declare them; the database is the last line of defense
against orphaned rows.

**Constraints are executable documentation.** `NOT NULL`, `UNIQUE`, `CHECK`, and
foreign keys encode business rules where they cannot be bypassed. Application
code changes; constraints persist. Prefer the database enforcing "an order must
have a customer" over hoping every code path remembers.

**Choose types deliberately.** Money `NUMERIC`/`DECIMAL`, never float.
Timestamps timezone-aware types, stored in UTC. Enums real enum types or
check constraints for closed sets; lookup tables when the set may grow or needs
metadata. Text with a known max bounded `VARCHAR`; unbounded `TEXT`.

**Design for evolution.** Every table gets `created_at`/`updated_at` (or
equivalent); soft-delete vs hard-delete is decided per entity; large tables get
their growth strategy up front (partitioning by time, archival policy).

## Practical workflow

1. **Extract entities and relationships** from requirements; write one sentence
 per entity describing its lifecycle (created when? deleted ever?).
2. **Sketch the ER model** - entities, cardinalities, and which side owns the
 relationship. Resolve many-to-many with explicit join tables (they always
 grow attributes later: `created_at`, role, ordering).
3. **Pick keys and types** per the concepts above; name conventions consistently
 (`id` PK, `<entity>_id` FK, `*_at` timestamps).
4. **Add constraints** for every invariant you can state: uniqueness, non-null,
 checks (`CHECK (price >= 0)`), foreign keys with explicit `ON DELETE` behavior.
5. **Review for smells:** god tables (30+ columns doing three jobs), polymorphic
 associations without discipline, nullable FKs that mean two things, missing
 indexes on FK columns.
6. **Plan migrations as expand-then-contract:** add the new column/table 
 dual-write backfill in batches switch reads drop the old. Never rename
 or drop in the same deploy that stops using them.

## Common pitfalls

- **Natural primary keys** (email, phone, government IDs) - they change, they get
 reused, they leak PII into every join and log. Use surrogates; unique-constrain
 the natural key.
- **No foreign keys "for performance"** - the integrity cost dwarfs the tiny
 write overhead; orphaned data is far more expensive than FK checks.
- **Nullable columns with ambiguous meaning** - does `NULL shipped_at` mean "not
 shipped" or "unknown"? Document it or split the state explicitly.
- **Storing lists as comma-separated strings** - violates 1NF, unqueryable,
 unindexable. Use a join table or a proper array/JSON type with a GIN index.
- **Big-bang migrations** - renaming a column and deploying the code that uses
 the new name simultaneously guarantees downtime or errors; expand-contract
 instead.
- **Forgetting the read path** - a perfectly normalized schema that requires
 12 joins for the homepage needs a read model (view, materialized view, or
 cache), designed deliberately rather than discovered in production.


## Safety Boundaries

1. Read-Only Default: Background research and status checks proceed autonomously.
2. Supervised State Changes: Any action that publishes content or alters shared state requires explicit sign-off.
3. Secret Scrubbing: Credentials and API tokens must never be rendered in output logs.
