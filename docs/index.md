# Saleem's Productivity Tools

Last updated May 9, 2026

Here is the list of key tools in my workflow. If there are multiple to a category, the primary tool I use is listed first, and then there are use-case specific ones after that

---

**Things that are working**

## Mail

- AI Front End: Claude Code and Codex for email prioritization and drafting
- UI Front End: Gmail, Outlook
- Back End: Google, MS Office 365

May 2026 Note: I moved off Spark and Superhuman; I'm no longer looking for any advanced features in the email client given that I offload the complex tasks (like folder organization and e-mail rules to Claude & Codex) 

## Calendar

- Front End: Outlook
- Back End: MS Office 365 (for Family Calendar, IBM and public service accounts), Google Calendar (for  personal calendars and non-IBM work)

May 2026 Note: I moved off Fantastical, given that, like e-mail, I'm just looking for basic functionality, a consolidated view, and reliability in my calendar view

## LLM

My models of choice evolve every few days, so I'm putting a point-in-time view here

#### text / coding tasks
- personal / consumer uses — gpt 5.5 with low effort via codex
- work / IBM uses — opus 4.7 with high effort via claude code
- work / non-IBM uses — combinations of gpt 5.5 with low effort and opus 4.7 with medium effort 
- local / on-device — qwen 3.6 and gemma 4 (largest model that can run on given hardware I'm using)

#### image-gen tasks
- I don't have a model of choice yet, but I tend to use Replicate for my platform and utilize across flux, gpt and nano-banana

#### speech to text
- parakeet-english is still my default go-to alongside pyannote for diarization
- I have an eval framework that compares parakeet against the others of the top 4 — I use one of these others when I'm looking for higher quality and willing to compromise on speed — Cohere Transcribe, Mistral Voxtral, Granite Speech

## Note taking

#### text tasks

- Obsidian — I started moving almost all my note taking to Obsidian starting mid/late 2025, and have not looked back. I've sunset my uses for Evernote, Supernote
- Important Obsidian plugins in my workflow
	- Obsidian Web Clipper ([link](https://obsidian.md/clipper)) — to pull websites in as markdown
	- Git ([link](obsidian://show-plugin?id=obsidian-git))— for fast sync with a repo as I update files
	- Open in Github ([link](obsidian://show-plugin?id=open-in-github))— adds an option to open the given file on Github (easier to then share)
	- Open in Github ([link to official plugin](obsidian://show-plugin?id=open-in-github), [link to my fork](https://github.com/saleemh/obsidian-open-in-github-plugin)) — this adds a menu item when you right-click any file, that lets you open the file through a browser on Github. The fork I've linked is the version I use, where I also added a configurable capability to open files in Github Enterprise (as well as other custom Git URLs)
	- Kanban ([link](obsidian://show-plugin?id=obsidian-kanban))— comes in handy when I want a Kanban view (while still using markdown)
	- Tasks ([link](obsidian://show-plugin?id=obsidian-tasks-plugin))— fully functional task management system; has allowed me to move off of Cultured Code's Things app ecosystem (which I love, but doesn't allow easy manipulation through AI assistants)
	- BART ([link](obsidian://show-plugin?id=obsidian42-brat))—let's you test new obsidian plugins before publishing them (I do this when I customize the plugins for my own uses)
	- Marp Slides ([link](obsidian://show-plugin?id=marp-slides))— for slide viewing when I create marp-format markdown through other tools
	- Unofficial Supernote by Ratta Integration ([link](obsidian://show-plugin?id=supernote))— used with my e-ink notetaker to import into Obsidian

#### audio tasks
- SuperWhisper — my default for live-transcription (this is preferable to typing as its faster), and it works with the majority of the preferred text and speech-to-text models I mentioned in the LLM section above
- Custom software for meeting transcription & summarization (I've built this and use variants of it for all transcription & meeting note generation)
- Voice Notes — this is the basic audio recording app on iOS, MacOS, iPadOS and I've found it to be most reliable for recording and saving raw audio
- Loopback — for funneling audio to Voice Notes
#### note taking for specialized work
- LiquidText [link](https://www.liquidtext.net/) (mac & ipad only; researching & mind-mapping use case) — I only use this when I need to annotate & link across PDFs
- Zotero [link](https://www.zotero.org/)— for pulling together Research materials on any topic; integrates with Obsidian through a number of plugins
- Notability [link](https://notability.com/) (simple pdf markup, signatures)

## Task management

- Obsidian with Tasks plugin — this (along with task manipulation through Claude Code/Codex) is 90% of my task management

#### task management for specialized work
- AnyList [link](https://www.anylist.com/) (for groceries & shopping list use case, and shared w/ family)
- Notion (for trip planning use case; shifted off Trello to Notion in 2023-ish) 

## Development

- Claude Code with Claude model access via LiteLLM / AWS — this is the tooling I use for IBM work
- Cursor + Claude Code + Cursor — I use a combination of these tools for all non-IBM tasks, so that I don't have to hit token limits — I have $20/month accounts on those 3, and have been able to keep it that way rather than moving to the higher tier accounts for now. When I work across repo's, I prefer Cursor given its multi-repo workspace concept it adopts through VS Code
- iTerm — I use this for my MacOS shell
- Termius — I use this for my iOS/iPadOS Shell
- VNCViewer (on MacOS) and JumpDesktop (on iOS / iPadOS) for server access when I'm also using browser-control
- MCP Playwright — I use this open source project for browser-control tasks (versus the built-in capabilities that come through Codex and Claude), so that I can have better control and define my own workflows

## Physical Productivity Boosters Things

- Anker 6-in-1 USB C Hub ([Amazon](https://www.amazon.com/dp/B08C9HZ5YT)) — I carry this around everywhere and comes in handy almost every day
- Anker 25k wireless-chargeable battery pack ([Amazon](https://www.amazon.com/dp/B0DCBB2YTR)) — I also carry everywhere; has pass through charging and can charge a large laptop + 2 other devices simultaneously at near full speed
- Logitech Keys-to-Go 2 ([Amazon](https://www.amazon.com/Logitech-Portable-Wireless-Keyboard-Bluetooth/dp/B0D2FD5994))— this keyboard I also bring with me everywhere, and it supports 3 one-touch configs, which I have linked to my phone, ipad and laptop, for easy switching
- Neo65 Keyboard — this is my day-to-day keyboard; requires custom assembly. Parts = (1) Neo65 Cu Custom Mechanical Keyboard from QwertyKeys with a copper bottom, brass weight, tri-mode hotswap PCB, and PP plate, Gazzew Boba U4 Silent Tactile switches, and GMK key caps (note: still assembling but excited to start using it :))
- Moft Trackable Tripod Wallet ([Moft Site](https://www.moft.us/products/magsafe-tripod-wallet-stand-with-find-my?variant=42702829355095)) — works well with the keyboard, and easy to carry everywhere, and Moft iPad Dynamic Folio (this is an essential accessory for me; allows me to use my iPad in all the different environments I find myself in)
- Full Windsor Magnetic Flatware — I bring this to be able to use as utensils, comes in handy
- Logitech 4k brio camera — high quality and super portable, fits in one of those tiny pockets of a peak design tech bag
- EDC flashlight — high powered, tiny and easy to pocket
- Sony 1000XM6 — perfect for focus, calls, etc
- Logitech MX Master 4 — best mouse, and I also carry this around
- Leatherman Charge+TTI — the best pocketknife...
- PeakDesign — go-to brand for carrying all of above

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

- Chrome — my default
- Safari — backup
- (I've tried the genAI browsers, but the dev-tools and custom-plugin import ability of Chrome make it win for me)


---

**Things that aren't working really well yet, so trying to figure out best way**

## Personal finances

- Excel mostly (I've tried different tools but always keep coming back to Excel to manage finances)
- Also trying YNAB, but not much success yet

## Health & Wellness Tracking

- [No good default tool... this is a gap right now; I tried tools like MyFitnessPal, but nothing has integrated well into my life]
- Strava (tracking stats from runs & bike rides use case)
- Gaia Maps (tracking maps for hikes and bike rides)

## Family & Friend info management

- Cardhop and Contacts app via iCloud (for e-mail/phone & birthdays)
- Excel (physical addresses)
- Custom family tree app built on GrampsWeb — I am using this as a stop-gap to manage family tree information, because it's better than MacFamilyTree (which I used previously). I expect to move off this to pure markdown repository with time

## News

- The Economist, The Information, Pitchbook
- X / Google
- NYTimes, Slate, WSJ
- Gale (the text-based service through which I access The Economist)
- Apple News+ (the service through which I access WSJ)

## Messaging

- iMessage (only for ppl w/ iOS devices)
- WhatsApp (only for others using WhatsApp)
- Discord (for family)
- Slack (for IBM work)
- Google Chat (for non-IBM work)


---

## History

- 05/2026 — new pass; major changes in all categories, and consolidation into less tools
- 08/2025 — updated LLMs and cloud storage, added VPN section, tweaks to  note-taking, development
- 07/2025 — added obsidian, moft & LLM updates
- 06/2025 — updates across all categories
- 12/2024 — LLM updates, transcription tooling
- 11/2024 — expansion of notetaking tools, LLM updates
- 10/2024 — add LLM details, updates to notes
- 01/2022 — first iteration, includes mail/calendar/notes/tasks/vidconf/etc
