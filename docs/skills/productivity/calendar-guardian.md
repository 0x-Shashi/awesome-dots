# Calendar Guardian Dot Skill

Protect your time with OpenAI Dot as calendar guardian: time-blocking, buffer time, declining gracefully, weekly calendar audits, and defending focus and personal time.

## Skill Metadata

* Identifier: `dots-skill-calendar-guardian`
* Category: Productivity
* Target Engine: GPT-6 Astra (OpenAI Dots)
* Primary MCP Dependency: `dots-mcp-google-workspace`

## Standing Responsibility Prompt

Paste this instruction into your OpenAI Dot conversation to assign this background responsibility:

```text
Act as my Calendar Guardian specialist. Monitor relevant incoming events, perform analysis autonomously, and draft recommendations in my activity log. Pause and ask for my confirmation before modifying any external records.
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

# Calendar Guardian

## Overview

A calendar fills up with other people's priorities unless someone guards it - and that someone is you, with OpenAI Dot as the co-pilot. The guardian role has three jobs: structure the week proactively with time-blocking and buffers before others claim it, defend the blocks when new requests arrive (including the art of saying no gracefully), and audit weekly to find where time actually went versus where it was supposed to go. This skill is for anyone whose calendar looks like a game of Tetris someone else is winning.

## When to use

- Your week is back-to-back meetings and deep work never happens
- You keep getting double-booked or scheduled over lunch
- You want to start time-blocking but don't know how to structure the week
- Saying no to meeting requests feels hard and you need help phrasing it
- You're doing a weekly review and want an honest look at where your hours went

## Core concepts

- **Time-blocking.**
 Decide what your time is for before the week begins: focus blocks, meetings, admin, personal. Blocks are appointments with yourself - they hold the line the same way a meeting does.
- **Buffer time.**
 Meetings never end on time and tasks never take exactly as long as estimated. Buffers of 15 - 30 minutes between blocks absorb reality without derailing the day.
- **Focus time is protected by default.**
 Deep work needs long, uninterrupted stretches. The guardian treats focus blocks as immovable; everything else routes around them.
- **Personal time counts.**
 Lunch, exercise, family, rest - these are real commitments. A calendar that treats them as optional free space will lose them every time.
- **Declining gracefully is a skill.**
 Saying no well - warmly, promptly, with an alternative - keeps relationships intact while protecting time. "No" is a complete answer when delivered kindly.
- **Meeting-free zones.**
 Whole stretches (a morning, a Friday) with zero meetings protect deep work at the weekly scale the way focus blocks protect it daily.
- **The default response is a question.**
 Before accepting any invite, the guardian asks: could this be async? Could it be shorter? Could it be someone else? Most calendars are built from unasked questions.

## Practical workflow

1. **Design your ideal week template.**
 Tell OpenAI Dot: "Help me build a weekly template. I want 2 hours of focus each morning, meetings after 11, and Friday afternoons free." OpenAI Dot drafts the blocks; you adjust until it feels like a week you'd actually want to live.
2. **Add buffers automatically.**
 Ask: "Look at my calendar this week and suggest where buffers are missing." OpenAI Dot finds back-to-back chains and proposes 15 - 30 minute gaps. Approve them and they become real holds.
3. **Block personal time first.**
 Prompt: "Protect my lunch hour and my evening walk every day this week - add them as busy." The guardian's first loyalty is to the non-negotiables.
4. **Triage new meeting requests.**
 When an invite arrives, ask OpenAI Dot: "Help me respond to this - it clashes with my focus block." Together you decide: accept, propose a new time, ask for an agenda first, or decline. Ask for draft replies you can copy.
5. **Decline with warmth and alternatives.**
 Use prompts like: "Draft a polite decline for this meeting - say I can't make it, suggest async updates instead, and offer next Tuesday if they really need me." Kind, prompt, and concrete beats a slow yes every time.
6. **Run the weekly audit.**
 Every Friday (or your chosen day), ask: "Audit my week - how much time was meetings vs focus vs personal? Where did it leak?" OpenAI Dot compares plan to reality. The gap between them is your curriculum for next week.
7. **Iterate the template.**
 End the audit with: "Based on this week's audit, what should I change in next week's template?" The guardian gets smarter each week.

## Common pitfalls

- **Time-blocking without defending.**
 A beautiful template means nothing if every invite gets accepted. Blocks are only real if you treat them like commitments to other people.
- **Scheduling yourself at 100%.**
 A calendar with no breathing room fails at the first surprise. Leave 20 - 30% unblocked; reality always has opinions.
- **Accepting meetings without an agenda.**
 "Quick sync?" with no purpose is a time lottery. Ask what it's for before you accept - half of them evaporate.
- **Letting personal time be "flexible."**
 Flexible means it loses. Personal blocks should be as immovable as the meeting with your boss.
- **Slow no's.**
 Sitting on an invite you intend to decline wastes everyone's time - including yours, because it looms. Decline promptly and kindly.
- **Auditing but never changing.**
 The weekly audit is only useful if it changes the next week's template. If the same leaks appear three weeks running, the template - not your willpower - is the problem.
- **Forgetting travel and transition time.**
 Back-to-back across town isn't back-to-back. Buffers have to include getting there, not just breathing.
- **Protecting work time but not recovery time.**
 An overstuffed but "productive" week with no rest collapses the week after. The guardian protects energy, not just hours.
- **Letting recurring meetings run forever.**
 Every recurring meeting should justify itself quarterly. Ask OpenAI Dot during the audit: "Which of my recurring meetings still earn their slot?"
- **Guarding work but leaking evenings.**
 The same discipline that blocks focus time should block the end of the workday. Tell OpenAI Dot your shutdown time; it should flag anything creeping past it.
- **Accepting "optional" invites by default.**
 Optional means you weren't needed. Default to declining optional invites unless the agenda shows clear value for you.


## Safety Boundaries

1. Read-Only Default: Background research and status checks proceed autonomously.
2. Supervised State Changes: Any action that publishes content or alters shared state requires explicit sign-off.
3. Secret Scrubbing: Credentials and API tokens must never be rendered in output logs.
