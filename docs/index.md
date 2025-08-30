# Saleem's Productivity Tools

Last updated Aug 28, 2025

Here's the list of key tools in my workflow. If there are multiple to a category, the primary tool I use is listed first, and then there are use-case specific ones after that

---

**Things that are working**

## Mail

- Front End: Spark, iOS Mail (where Spark isn't supported use case)
- Back End: Google (for personal accounts), MS Office 365 (for work accounts)

## Calendar

- Front End: Fantastical
- Back End: MS Office 365 (for Family Calendar and work accounts), Google Calendar (for individual personal calendars)

## LLM — Updated Aug 28

- gpt-5-thinking as my default/go-to
- sonnet 4 through claude-code+cursor for coding tasks and uses of long-term memory
- parakeet-english for on-device automatic speech transcription (using Superwhisper front-end)
- grok 3/4 for things that are happening real time, and in-car use
- gpt-oss-20b for on-laptop/confidential work
- (note I recognize gemini is really good, but the ux/ui bothers me so i only use it when i have to, like for youtube summarization or making storybooks)

## Note taking

### Note taking without grounding material

- Obsidian — recently started using this, and it has quickly become my go-to for most on-the-fly note taking and drafting
- iA Writer — I use this for converting markdown files to PDF, and also working with markdown files across the various file stores I use (i.e. OneDrive, Working Copy, GDrive, ShellFish, iCloud)
- Claude Code — When I mix note taking with research, I use a combination of text-editing in iA Writer + direct edits from the AI with Claude Code
- ~~Evernote (I've used this since 2008 for all general note taking... it would take a lot to move me off this as the primary note taking tool) — Aug2025 UPDATE: I've now completed a move off Evernote fully to Obsidian; using [evernote2obsidian](https://github.com/AltoRetrato/evernote2obsidian) and [evernote-backup](https://github.com/vzhd1701/evernote-backup/)~~
- SuperNote (for pen-based note-taking & journaling) — I use the SuperNote Nomad, which is nice... but if I had to replace now, I would probably get the ReMarkable Pro given the color screen and reading light
- ~~LiveScribe (OCR & search across paper notes use case)~~ — deprecated as of early 2023 given switch to SuperNote (and I think I left my Livescribe in a cafe recently anyway)

### Note taking with audio grounding material

- SuperWhisper — new default for meeting transcription & summarization; almost as good as Notability, but also allows for fully on-device execution and custom-LLM use. Also includes speaker-differentiation capabilities
- Notability — secondary option for meeting transcription & summarization, in those situations where there is no confidential information shared. Has good transcription quality (uses OpenAI in background; better that what I've seen through Apple Intelligence + Adobe Premiere Pro), and is differentiated in that it ties the transcription based on timepoints, to your typed/handwritten notes. Still has gaps in that (1) it doesn't support on-device transcription, and (2) no speaker-differentiation capabilities
- Loopback — for funneling audio to Notability where relevant
- Apple Notes — for transcription when there's an on-device requirement or when I need to transcript through a phone call (and then I use Llama with Ollama or LMStudio for generating the meeting notes)

### Note taking with PDF grounding material

- LiquidNotes (mac & ipad only; researching & mind-mapping use case) — moved out of "Notes" category, because Researching now has a category of its own tools
- Zotero — for pulling together Research materials on any topic — integrates well with LiquidText and Consensus
- Consensus.app (for finding relevant research to a given topic) — June 2025 update: I use this less and less, as the Deep Research capabilities from OpenAI are getting better... so I suspect I'll take this off the list by the end of the year
- NotebookLM — for summarizing text into audio
- Notability (simple pdf markup, signatures)

## Image / Video tasks

- Gemini vue 3 for new video generation
- Flux-context-max on Replicate for image optimization
- King AI for existing-image to video conversion

## Task management

- Things
- AnyList (for groceries & shopping list use case, and shared w/ family)
- Microsoft Todo (for shared tasks w/ family use case, mainly accessed through iOS Reminders & Fantastical)
- Notion (for trip planning use case; shifted off Trello to Notion in 2023-ish) — I also use Notion AI but it's pretty bad compared to just directly using GPT models and copying responses back into Notion

## Development

- ~~VS Code~~ (moved off as of late 2023; my development needs aren't super intense, but Cursor + Claude Code still works better)
- Cursor + Claude Code — I use a combination of both these tools. I tend to use Cursor for the IDE and tab-completion when I'm doing direct edits, and I tend to use Claude Code for planning and AI-led coding tasks
- Working Copy — I use this tool daily on iOS and iPad for sync'ing active GitHub projects I'm working on (for code but mostly for research/learning tasks)

## Physical Productivity Boosters Things

- Anker 5k wireless-chargeable battery pack with built-in kickstand (i bring 1-2 of these with me at all times given it comes in handy so often)
- Logitech Keys-to-Go 2 (this keyboard I also bring with me everywhere, and it supports 3 one-touch configs, which I have linked to my phone, ipad and laptop, for easy switching)
- Moft snap tripod for iPhone (works well with the keyboard, and easy to carry everywhere), and Moft iPad Dynamic Folio (this is an essential accessory for me; allows me to use my iPad in all the different environments I find myself in)
- Full Windsor Magnetic Flatware (I bring this to be able to use as utensils, comes in handy)
- Logitech 4k brio camera (high quality and super portable, fits in one of those tiny pockets of a peakdesign tech bag)
- EDC flashlight (high powered, tiny and easy to pocket)
- Sony 1000XM6 (perfect for focus, calls, etc)
- Logitech MX Master 3S (best mouse I've used, and I also carry this around)
- Leatherman Charge+TTI (the best pocketknife...)
- PeakDesign (go-to brand for carrying all of above)

## Legal Services

- Notarize.com for digital Notary

## Video conferencing

- Zoom
- Teams (for work use cases)
- FaceTime (for personal & 1x1)
- Google Meet (for kids' activities use case)
- OBS Studio for video stream manipulation alongside above video-conferencing services (e.g. for cropping/zooming video)

## TextExpander

- Paste for iOS/MacOS
- (I've fully moved off TextExpander and aText which is what I used before; Paste solves all use cases for me)

## Screenshot / Screen Recording

- Cleanshot — default for MacOS — this is by far the best I've seen; 'scrolling screenshot' is killer feature
- Tailor — default for iOS

## Cloud Storage

- OneDrive
- GitHub for folders with mostly markdown and code
- ShellFish —  an iPhone/iPad app that lets me expose GitHub repos through the iOS/iPadOS file system
- rclone for working across cloud storage on linux
- Google Photos (for pictures use case, esp now w/ Ask Photos)
- iCloud (for device backup use case)
- SmugMug (for large home video storage and some photo album curation)
- Box / Dropbox (for IBM / Town use cases)

## VPN

- Tailscale — I install Tailscale on the devices where I need a personal VPN, and I have it running with an exit note on my Ubuntu Linux VPS (which is hosted on GoDaddy, and also the place I do development, host websites, etc); this gives me the security I need for VPN and doesn't cost anything (versus solutions like NordVPN that come with a cost)

## SW Licenses & Password Management

- 1Password

## Window & Action Bar Management (MacOS)

- Bartender (for managing action bar icons) — I expect to move off this after Tahoe is released
- ~~Magnet~~ — deprecated in 2024 because its now built into Sonoma

## Browsers

- Safari — this is my default
- Chrome — for web apps like Outlook
- Dia — I use this a GenAI browser in those situations where I'm going to be focused on 'web browsing' as an activity

---

**Things that aren't working really well yet, so trying to figure out best way**

## Browser-Use Agents

- Browser-Use (It's open-source and runs on laptop, which is great, but doesn't work all that well. Main issue that it doesn't let the user pause and take over the screen mid-execution)
- Claude Computer-Use (This works better than anything else I've used, but it just chews through $ and is also slow. As this gets cheaper and better, it would be positioned to be my chosen option (until the on-laptop tool gets better)

## Personal finances

- Excel mostly (I've tried different tools but always keep coming back to Excel to manage finances)
- Also trying YNAB, but not much success yet

## Health & Wellness Tracking

- [No good default tool... this is a gap right now; I tried tools like MyFitnessPal, but nothing has integrated well into my life]
- ~~Peloton (cycling use case)~~ — deprecated in early 2024, moved to LifeTime app since this tech is tied to whatever the subscription is for
- Strava (tracking stats from runs & bike rides use case)
- Gaia Maps (tracking maps for hikes and bike rides)

## Family & Friend info management

- ~~MonicaHQ (for cataloging events use case)~~ — deprecated in 2022; didn't work out
- Contacts app via iCloud (for e-mail/phone & birthdays)
- Excel (physical addresses)
- MacFamilyTree (for family history & connections ) — i really dislike this because they keep making me pay for a new version, but there's nothing that's decent out there instead

## News

- The Economist
- X / Google
- NYTimes, Slate, WSJ
- Gale (the text-based service through which I access The Economist)
- Apple News+ (the service through which I access WSJ)

## Messaging

- iMessage (only for ppl w/ iOS devices)
- WhatsApp (only for others using WhatsApp)
- Discord (for family)
- Slack (for IBM work)

## Documents & presentations

- MS Office
- ~~Dropbox Paper (for town work) — deprecated as of 2021~~
- ~~Box Notes (for ibm work) — deprecated in Nov 2024; worked fine but we moved off Box~~

---

## History

- 08/2025 — updated LLMs and cloud storage, added VPN section, tweaks to  note-taking, development
- 07/2025 — added obsidian, moft & LLM updates
- 06/2025 — updates across all categories
- 12/2024 — LLM updates, transcription tooling
- 11/2024 — expansion of notetaking tools, LLM updates
- 10/2024 — add LLM details, updates to notes
- 01/2022 — first iteration, includes mail/calendar/notes/tasks/vidconf/etc
