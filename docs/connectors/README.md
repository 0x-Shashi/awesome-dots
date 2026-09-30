# OpenAI Dots MCP Connectors Catalog

This catalog contains 150 verified, standardized Model Context Protocol (MCP) connector specifications adapted specifically for OpenAI Dots.

## Runtime Architecture

OpenAI Dots interacts with third-party tools via the Model Context Protocol (MCP). Each connector in this catalog defines:

1. Standard JSON-RPC tool endpoints discoverable by the GPT-6 Astra runtime.
2. Official OpenAI Dots Action Permission Modes:
   * Autonomous Execution: Read-only status checks and data queries.
   * Prompt-Initiated Execution: Pre-approved actions requested in the conversation.
   * Supervised Execution: Operations that pause for explicit user confirmation.
   * User Handoff: High-consequence operations (deletions, payments) requiring direct human completion.
3. Strict isolation of tokens, OAuth credentials, and API secrets.

## Complete Connector Index (150 Connectors)

| Connector | Category | Target Host | Action Count | Documentation |
| :--- | :--- | :--- | :--- | :--- |
| **Anthropic** | AI and Search | `api.anthropic.com` | 1 | [anthropic.md](anthropic.md) |
| **Beatoven** | AI and Search | `public-api.beatoven.ai` | 8 | [beatoven.md](beatoven.md) |
| **Black Forest Labs** | AI and Search | `api.bfl.ai` | 6 | [black-forest-labs.md](black-forest-labs.md) |
| **Brave Search** | AI and Search | `api.search.brave.com` | 2 | [brave-search.md](brave-search.md) |
| **Cartesia** | AI and Search | `api.cartesia.ai` | 5 | [cartesia.md](cartesia.md) |
| **Deepgram** | AI and Search | `api.deepgram.com` | 5 | [deepgram.md](deepgram.md) |
| **Deepl** | AI and Search | `api-free.deepl.com` | 4 | [deepl.md](deepl.md) |
| **Deepseek** | AI and Search | `api.deepseek.com` | 5 | [deepseek.md](deepseek.md) |
| **Elai** | AI and Search | `apis.elai.io` | 6 | [elai.md](elai.md) |
| **Elevenlabs** | AI and Search | `api.elevenlabs.io` | 5 | [elevenlabs.md](elevenlabs.md) |
| **Exa** | AI and Search | `api.exa.ai` | 2 | [exa.md](exa.md) |
| **Fal Ai** | AI and Search | `fal.run` | 6 | [fal-ai.md](fal-ai.md) |
| **Firecrawl** | AI and Search | `api.firecrawl.dev` | 6 | [firecrawl.md](firecrawl.md) |
| **Gemini** | AI and Search | `generativelanguage.googleapis.com` | 8 | [gemini.md](gemini.md) |
| **Heygen** | AI and Search | `api.heygen.com` | 6 | [heygen.md](heygen.md) |
| **Huggingface** | AI and Search | `huggingface.co` | 2 | [huggingface.md](huggingface.md) |
| **Hume Ai** | AI and Search | `api.hume.ai` | 4 | [hume-ai.md](hume-ai.md) |
| **Ideogram** | AI and Search | `api.ideogram.ai` | 7 | [ideogram.md](ideogram.md) |
| **Kling** | AI and Search | `api.klingai.com` | 6 | [kling.md](kling.md) |
| **Langfuse** | AI and Search | `cloud.langfuse.com` | 9 | [langfuse.md](langfuse.md) |
| **Luma** | AI and Search | `api.lumalabs.ai` | 7 | [luma.md](luma.md) |
| **Mistral** | AI and Search | `api.mistral.ai` | 8 | [mistral.md](mistral.md) |
| **Openai** | AI and Search | `api.openai.com` | 1 | [openai.md](openai.md) |
| **Openrouter** | AI and Search | `openrouter.ai` | 2 | [openrouter.md](openrouter.md) |
| **Perplexity** | AI and Search | `api.perplexity.ai` | 4 | [perplexity.md](perplexity.md) |
| **Playht** | AI and Search | `api.play.ht` | 5 | [playht.md](playht.md) |
| **Remove Bg** | AI and Search | `api.remove.bg` | 5 | [remove-bg.md](remove-bg.md) |
| **Replicate** | AI and Search | `api.replicate.com` | 5 | [replicate.md](replicate.md) |
| **Runway** | AI and Search | `api.dev.runwayml.com` | 6 | [runway.md](runway.md) |
| **Tavily** | AI and Search | `api.tavily.com` | 1 | [tavily.md](tavily.md) |
| **Vapi** | AI and Search | `api.vapi.ai` | 7 | [vapi.md](vapi.md) |
| **Xai** | AI and Search | `api.x.ai` | 4 | [xai.md](xai.md) |
| **N8N** | Automation | `your n8n instance host` | 7 | [n8n.md](n8n.md) |
| **Amadeus** | Business Services | `test.api.amadeus.com` | 5 | [amadeus.md](amadeus.md) |
| **Docusign** | Business Services | `demo.docusign.net` | 7 | [docusign.md](docusign.md) |
| **Lob** | Business Services | `api.lob.com` | 9 | [lob.md](lob.md) |
| **Printful** | Business Services | `api.printful.com` | 6 | [printful.md](printful.md) |
| **Shippo** | Business Services | `api.goshippo.com` | 7 | [shippo.md](shippo.md) |
| **Uber Direct** | Business Services | `api.uber.com` | 5 | [uber-direct.md](uber-direct.md) |
| **Cloudflare** | Cloud Infrastructure | `api.cloudflare.com` | 2 | [cloudflare.md](cloudflare.md) |
| **Digitalocean** | Cloud Infrastructure | `api.digitalocean.com` | 2 | [digitalocean.md](digitalocean.md) |
| **Flyio** | Cloud Infrastructure | `api.machines.dev` | 9 | [flyio.md](flyio.md) |
| **Netlify** | Cloud Infrastructure | `api.netlify.com` | 2 | [netlify.md](netlify.md) |
| **Railway** | Cloud Infrastructure | `backboard.railway.com` | 6 | [railway.md](railway.md) |
| **Render** | Cloud Infrastructure | `api.render.com` | 2 | [render.md](render.md) |
| **Triggerdev** | Cloud Infrastructure | `api.trigger.dev` | 7 | [triggerdev.md](triggerdev.md) |
| **Upstash** | Cloud Infrastructure | `*.upstash.io` | 3 | [upstash.md](upstash.md) |
| **Vercel** | Cloud Infrastructure | `api.vercel.com` | 3 | [vercel.md](vercel.md) |
| **Bluesky** | Communication | `bsky.social` | 7 | [bluesky.md](bluesky.md) |
| **Discord** | Communication | `discord.com` | 6 | [discord.md](discord.md) |
| **Front** | Communication | `api2.frontapp.com` | 8 | [front.md](front.md) |
| **Mastodon** | Communication | `your Mastodon instance host` | 6 | [mastodon.md](mastodon.md) |
| **Plain** | Communication | `core-api.uk.plain.com` | 6 | [plain.md](plain.md) |
| **Slack** | Communication | `slack.com` | 6 | [slack.md](slack.md) |
| **Telegram** | Communication | `api.telegram.org` | 3 | [telegram.md](telegram.md) |
| **X** | Communication | `api.x.com` | 6 | [x.md](x.md) |
| **Buzzsprout** | Content and Media | `www.buzzsprout.com` | 7 | [buzzsprout.md](buzzsprout.md) |
| **Canva** | Content and Media | `api.canva.com` | 11 | [canva.md](canva.md) |
| **Cloudinary** | Content and Media | `api.cloudinary.com` | 9 | [cloudinary.md](cloudinary.md) |
| **Descript** | Content and Media | `api.descript.com` | 8 | [descript.md](descript.md) |
| **Devto** | Content and Media | `dev.to` | 7 | [devto.md](devto.md) |
| **Figma** | Content and Media | `api.figma.com` | 4 | [figma.md](figma.md) |
| **Framer** | Content and Media | `api.framer.com` | 1 | [framer.md](framer.md) |
| **Opusclip** | Content and Media | `api.opus.pro` | 5 | [opusclip.md](opusclip.md) |
| **Pexels** | Content and Media | `api.pexels.com` | 9 | [pexels.md](pexels.md) |
| **Podbean** | Content and Media | `api.podbean.com` | 6 | [podbean.md](podbean.md) |
| **Spotify** | Content and Media | `api.spotify.com` | 10 | [spotify.md](spotify.md) |
| **Tiktok** | Content and Media | `open.tiktokapis.com` | 4 | [tiktok.md](tiktok.md) |
| **Transistor** | Content and Media | `api.transistor.fm` | 8 | [transistor.md](transistor.md) |
| **Twitch** | Content and Media | `api.twitch.tv` | 7 | [twitch.md](twitch.md) |
| **Unsplash** | Content and Media | `api.unsplash.com` | 8 | [unsplash.md](unsplash.md) |
| **Veed** | Content and Media | `the host you pass via --api-host` | 4 | [veed.md](veed.md) |
| **Webflow** | Content and Media | `api.webflow.com` | 9 | [webflow.md](webflow.md) |
| **Youtube** | Content and Media | `www.googleapis.com` | 7 | [youtube.md](youtube.md) |
| **Leaf Agriculture** | Data Services | `api.withleaf.io` | 10 | [leaf-agriculture.md](leaf-agriculture.md) |
| **Newsapi** | Data Services | `newsapi.org` | 2 | [newsapi.md](newsapi.md) |
| **Openweathermap** | Data Services | `api.openweathermap.org` | 2 | [openweathermap.md](openweathermap.md) |
| **Clerk** | Developer Tools | `api.clerk.com` | 6 | [clerk.md](clerk.md) |
| **Github** | Developer Tools | `api.github.com` | 4 | [github.md](github.md) |
| **Gitlab** | Developer Tools | `gitlab.com` | 4 | [gitlab.md](gitlab.md) |
| **Linear** | Developer Tools | `api.linear.app` | 3 | [linear.md](linear.md) |
| **Neon** | Developer Tools | `console.neon.tech` | 7 | [neon.md](neon.md) |
| **Posthog** | Developer Tools | `configurable` | 3 | [posthog.md](posthog.md) |
| **Sentry** | Developer Tools | `sentry.io` | 6 | [sentry.md](sentry.md) |
| **Supabase** | Developer Tools | `<ref>.supabase.co` | 3 | [supabase.md](supabase.md) |
| **Beehiiv** | Email and Marketing | `api.beehiiv.com` | 5 | [beehiiv.md](beehiiv.md) |
| **Buttondown** | Email and Marketing | `api.buttondown.com` | 6 | [buttondown.md](buttondown.md) |
| **Dub** | Email and Marketing | `api.dub.co` | 8 | [dub.md](dub.md) |
| **Kit** | Email and Marketing | `api.kit.com` | 7 | [kit.md](kit.md) |
| **Loops** | Email and Marketing | `app.loops.so` | 6 | [loops.md](loops.md) |
| **Postmark** | Email and Marketing | `api.postmarkapp.com` | 4 | [postmark.md](postmark.md) |
| **Resend** | Email and Marketing | `api.resend.com` | 2 | [resend.md](resend.md) |
| **Sendgrid** | Email and Marketing | `api.sendgrid.com` | 4 | [sendgrid.md](sendgrid.md) |
| **Alphavantage** | Finance and Commerce | `www.alphavantage.co` | 2 | [alphavantage.md](alphavantage.md) |
| **Etsy** | Finance and Commerce | `openapi.etsy.com` | 6 | [etsy.md](etsy.md) |
| **Gumroad** | Finance and Commerce | `api.gumroad.com` | 3 | [gumroad.md](gumroad.md) |
| **Lemon Squeezy** | Finance and Commerce | `api.lemonsqueezy.com` | 6 | [lemon-squeezy.md](lemon-squeezy.md) |
| **Mercury** | Finance and Commerce | `api.mercury.com` | 3 | [mercury.md](mercury.md) |
| **Paddle** | Finance and Commerce | `api.paddle.com` | 3 | [paddle.md](paddle.md) |
| **Patreon** | Finance and Commerce | `www.patreon.com` | 5 | [patreon.md](patreon.md) |
| **Polar** | Finance and Commerce | `api.polar.sh` | 7 | [polar.md](polar.md) |
| **Polymarket** | Finance and Commerce | `gamma-api.polymarket.com` | 9 | [polymarket.md](polymarket.md) |
| **Ramp** | Finance and Commerce | `api.ramp.com` | 8 | [ramp.md](ramp.md) |
| **Shopify** | Finance and Commerce | `<your-shop>.myshopify.com` | 6 | [shopify.md](shopify.md) |
| **Square** | Finance and Commerce | `connect.squareup.com` | 10 | [square.md](square.md) |
| **Stripe** | Finance and Commerce | `api.stripe.com` | 3 | [stripe.md](stripe.md) |
| **Wise** | Finance and Commerce | `api.wise.com` | 2 | [wise.md](wise.md) |
| **Ynab** | Finance and Commerce | `api.ynab.com` | 6 | [ynab.md](ynab.md) |
| **Tally** | Forms and Surveys | `api.tally.so` | 6 | [tally.md](tally.md) |
| **Typeform** | Forms and Surveys | `api.typeform.com` | 7 | [typeform.md](typeform.md) |
| **Aqara** | Hardware and IoT | `open-<region>.aqara.com` | 12 | [aqara.md](aqara.md) |
| **Ecovacs** | Hardware and IoT | `open.ecovacs.com` | 12 | [ecovacs.md](ecovacs.md) |
| **Google Nest** | Hardware and IoT | `smartdevicemanagement.googleapis.com` | 3 | [google-nest.md](google-nest.md) |
| **Home Assistant** | Hardware and IoT | `your instance host` | 3 | [home-assistant.md](home-assistant.md) |
| **Homey** | Hardware and IoT | `the host you pass via --host` | 3 | [homey.md](homey.md) |
| **Hubitat** | Hardware and IoT | `the host you pass via --host` | 3 | [hubitat.md](hubitat.md) |
| **Moonraker** | Hardware and IoT | `the host you pass via --host` | 11 | [moonraker.md](moonraker.md) |
| **Octoprint** | Hardware and IoT | `the host you pass via --host` | 14 | [octoprint.md](octoprint.md) |
| **Oura** | Hardware and IoT | `api.ouraring.com` | 6 | [oura.md](oura.md) |
| **Philips Hue** | Hardware and IoT | `derived from --host at runtime; the CLI refuses to send the key anywhere else` | 3 | [philips-hue.md](philips-hue.md) |
| **Prusa Connect** | Hardware and IoT | `connect.prusa3d.com` | 8 | [prusa-connect.md](prusa-connect.md) |
| **Rachio** | Hardware and IoT | `api.rach.io` | 7 | [rachio.md](rachio.md) |
| **Smartcar** | Hardware and IoT | `api.smartcar.com` | 10 | [smartcar.md](smartcar.md) |
| **Smartthings** | Hardware and IoT | `api.smartthings.com` | 11 | [smartthings.md](smartthings.md) |
| **Switchbot** | Hardware and IoT | `api.switch-bot.com` | 11 | [switchbot.md](switchbot.md) |
| **Tesla Fleet Api** | Hardware and IoT | `fleet-api.prd.na.vn.cloud.tesla.com` | 13 | [tesla-fleet-api.md](tesla-fleet-api.md) |
| **Tesla Powerwall** | Hardware and IoT | `fleet-api.prd.na.vn.cloud.tesla.com` | 8 | [tesla-powerwall.md](tesla-powerwall.md) |
| **Tuya** | Hardware and IoT | `openapi.tuyaus.com` | 7 | [tuya.md](tuya.md) |
| **Unifi Protect** | Hardware and IoT | `the host you pass via --host` | 3 | [unifi-protect.md](unifi-protect.md) |
| **Restream** | Other Services | `api.restream.io` | 7 | [restream.md](restream.md) |
| **Airtable** | Productivity | `api.airtable.com` | 4 | [airtable.md](airtable.md) |
| **Asana** | Productivity | `app.asana.com` | 4 | [asana.md](asana.md) |
| **Calcom** | Productivity | `api.cal.com` | 5 | [calcom.md](calcom.md) |
| **Calendly** | Productivity | `api.calendly.com` | 6 | [calendly.md](calendly.md) |
| **Clickup** | Productivity | `api.clickup.com` | 3 | [clickup.md](clickup.md) |
| **Coda** | Productivity | `coda.io` | 5 | [coda.md](coda.md) |
| **Letta** | Productivity | `api.letta.com` | 7 | [letta.md](letta.md) |
| **Mem0** | Productivity | `api.mem0.ai` | 9 | [mem0.md](mem0.md) |
| **Monday** | Productivity | `api.monday.com` | 4 | [monday.md](monday.md) |
| **Notion** | Productivity | `api.notion.com` | 8 | [notion.md](notion.md) |
| **Readwise** | Productivity | `readwise.io` | 5 | [readwise.md](readwise.md) |
| **Supermemory** | Productivity | `api.supermemory.ai` | 6 | [supermemory.md](supermemory.md) |
| **Ticktick** | Productivity | `api.ticktick.com` | 6 | [ticktick.md](ticktick.md) |
| **Todoist** | Productivity | `api.todoist.com` | 3 | [todoist.md](todoist.md) |
| **Zep** | Productivity | `api.getzep.com` | 6 | [zep.md](zep.md) |
| **Apollo** | Sales and CRM | `api.apollo.io` | 4 | [apollo.md](apollo.md) |
| **Ashby** | Sales and CRM | `api.ashbyhq.com` | 7 | [ashby.md](ashby.md) |
| **Attio** | Sales and CRM | `api.attio.com` | 6 | [attio.md](attio.md) |
| **Hubspot** | Sales and CRM | `api.hubapi.com` | 4 | [hubspot.md](hubspot.md) |
| **Pipedrive** | Sales and CRM | `{company}.pipedrive.com` | 5 | [pipedrive.md](pipedrive.md) |

## Integration Guide

To connect any connector to your Dot:
1. Ensure the server implements the specification defined in [docs/connector-blueprint.md](../connector-blueprint.md).
2. Register the MCP server in your ChatGPT Desktop settings or run it locally via `openai/tunnel-client`.
3. Set your target security boundary in [docs/starter-policy.md](../starter-policy.md).
