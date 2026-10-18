# The Seeker Codex

One file that teaches any AI agent [The Seeker](https://github.com/TheSeekerGame/the-seeker), the open-source sci-fi brand: its universe and themes, its art style and palette, its 48 Hz tuning, where all its art and code live, how to run and change its projects, and how to bring its collectibles into anything by reading the chain. Give [SKILL.md](SKILL.md) to your agent and make whatever you want, even if you have never written code.

## Use it

**Claude Code.** Install it once for every project:

```sh
git clone https://github.com/TheSeekerGame/seeker-codex ~/.claude/skills/seeker-codex
```

Claude then uses it whenever a task involves The Seeker. For a single project, clone it into that project's `.claude/skills/` folder instead.

**Claude apps.** Download this repository as a ZIP and upload it in the app's settings, under Skills.

**Other agents that read skills.** Put the `seeker-codex` folder wherever the agent loads skills from; its documentation says where.

**Any other AI chat.** Attach `SKILL.md`, or paste its contents at the start of the conversation.

Then say what you want to make. For example:

- "I've never coded. Help me play The Seeker on my laptop."
- "Make a browser game where Planetary Guardians change form when their holders change their padding."
- "Build a page that shows every activated SEEKER NET seeker, updating live."
- "Compose a track in the Seeker tuning and export the stems."
- "Turn the Seeker sprite into a rigged 3D model."
- "Design a poster of Guardian #1 exactly as it looks right now."

## What you can make with it

- **Games** in any genre and on any platform: 2D or 3D, browser or desktop, single-player or multiplayer, set in The Seeker's universe or only in its style.
- **Art:** pixel art, illustrations, rigged 3D models, voxel figures, animations, built from the game's and the collections' art or new art in their style.
- **Music and sound** in the Seeker tuning, with [SEEKER](https://theseekergame.github.io/seeker-audio/), the browser music studio, or any instrument that can be tuned.
- **Interactive apps, tools and websites**, from live dashboards of the collections to toys and generative art.
- **Merch, prints and promo material:** print-ready files, posters, trailers, social images.
- **Tabletop games and stories** in the universe.
- **Playing, modding and contributing** to The Seeker's own projects, with a guided setup for people who have nothing installed.

## The collections

Works can read Planetary Guardians (Bitcoin ordinals) and SEEKER NET (Robinhood Chain) straight from public APIs, so when a holder changes a Guardian's look or a seeker's charge moves, every game and artwork that reads them changes too. Holders become the game masters of the shared world. Integrations only ever read the chain: nobody connects a wallet or makes a transaction, and nobody needs to own anything to play.

## Always current

The codex is a map, not a copy. It sends agents to read the live repositories ([the-seeker](https://github.com/TheSeekerGame/the-seeker), [collections](https://github.com/TheSeekerGame/collections), [seeker-audio](https://github.com/TheSeekerGame/seeker-audio)) before they start, so it keeps up as the projects change.
