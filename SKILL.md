---
name: seeker-codex
description: Create anything with The Seeker, an open-source sci-fi brand whose code, art, music and lore anyone may use and sell. Games in any genre and on any platform, 2D or 3D art, rigged models, music, interactive apps, websites, tools, merch, promo material and stories. Also play, run, change and contribute to its projects (the Rust game the-seeker and the SEEKER browser music studio), and build its collectibles, Planetary Guardians (Bitcoin ordinals) and SEEKER NET (Robinhood Chain), into a work by reading public chain data, never writing to it. Use whenever someone mentions The Seeker, Theorem, Guardians, SEEKER NET or the 48 Hz tuning, or wants to make, remix, fork or contribute to anything Seeker-related, including people with no coding experience.
---

# The Seeker Codex

The Seeker is an open-source creative brand: a science-fiction universe about curiosity, transformation, mathematics and cosmic horror, whose trunk is a free 2D metroidvania. Its code, art, music and lore are open to everyone, commercial use included. Its collectibles live on public blockchains, and their holders are the game masters of the shared world, like the Gamemakers of *The Hunger Games* reshaping the arena while everyone else plays. What holders do on-chain can change every work that reads it, while anyone can play and create without owning anything.

With this skill you help anyone, from a seasoned developer to someone who has never installed a programming language, make something new in that universe, use and change what already exists, and contribute back.

**How to work:**

1. **Read the sources** (section 1). The repositories are the source of truth; this file is a map of them.
2. **Understand the person and the goal** (section 2), then **choose the simplest path that can deliver it well** (section 3).
3. **Give the work the Seeker's character** (sections 4 and 5).
4. **Bring in the collections wherever they deepen the work** (section 6).
5. **Build the smallest complete version, look at it or listen to it, then grow it.**
6. **Finish properly:** credit, licenses, and a way to share it (sections 9 to 12).

## 1. Read the sources first

Everything lives at [github.com/TheSeekerGame](https://github.com/TheSeekerGame). Any file can be read at `https://raw.githubusercontent.com/TheSeekerGame/<repository>/main/<path>`.

| Repository | What it holds |
| --- | --- |
| [`the-seeker`](https://github.com/TheSeekerGame/the-seeker) | The game, its design vision and lore, every art and audio asset, and the documentation |
| [`collections`](https://github.com/TheSeekerGame/collections) | Planetary Guardians and SEEKER NET: every art layer, the exact rules that assemble them, and how to read their live state from public APIs |
| [`seeker-audio`](https://github.com/TheSeekerGame/seeker-audio) | SEEKER, a music studio in the browser where every note is a harmonic of 48 Hz. Live at [theseekergame.github.io/seeker-audio](https://theseekergame.github.io/seeker-audio/) |
| [`community-games`](https://github.com/TheSeekerGame/community-games) | Games made in the universe, one folder each, with readable source. Live at [theseekergame.github.io/community-games](https://theseekergame.github.io/community-games/) |
| [`theseekergame.github.io`](https://github.com/TheSeekerGame/theseekergame.github.io) | The published [documentation](https://theseekergame.github.io/doc/) and [API reference](https://theseekergame.github.io/api/theseeker_game/), generated from `the-seeker`. Read it, never edit it |

**Always read these before starting, whatever the work:**

| File | Why |
| --- | --- |
| `the-seeker/README.md` | What the game is and how to run it |
| `the-seeker/docs/design/lore.md` | The universe, its themes (giving without a transaction among them), mathematics as experience, and the questions it deliberately leaves open |
| `the-seeker/docs/design/open-brand.md` | What is open, under which licenses, how holders act as game masters, every collection, and the ways a work can relate to the canon |
| `the-seeker/docs/design/art-direction.md` | The rules of the art and the exact palette |
| `the-seeker/LICENSE.md` | Licenses and the attribution line |
| `collections/README.md`, `collections/guardians/README.md`, `collections/SEEKER_NET/README.md` | The collectibles, and how any client reads their live state |

**Read these too when the work touches them,** and skip the rest: a project without sound has no need for `seeker-audio`, and one that never touches the game's code has no need for `AGENTS.md`.

| Work | Read |
| --- | --- |
| The game's code, a mod, or a contribution | `the-seeker/AGENTS.md` (the instruction file for AI agents: source map and the rules every change keeps), `the-seeker/CONTRIBUTING.md`, `docs/architecture/`, `docs/authoring/` |
| Game design and mechanics | `docs/design/mechanics/` (start with its `README.md`), `docs/design/audience.md` |
| Music, sound, timing | `docs/authoring/music.md`, `docs/authoring/SeekerTuning48hz.tun`, `docs/architecture/timing-and-audio.md`, `seeker-audio/README.md` |
| Sprites and animation | `docs/authoring/animations.md`, `docs/authoring/animation-reference.md`, `docs/authoring/assets.md` |
| Caves, terrain, backgrounds | `docs/architecture/level-generation.md` |
| SEEKER NET at contract level | `collections/SEEKER_NET/contracts/README.md` and `contracts/src/` |
| A game, toy or interactive piece | Games in `community-games` that resemble it, for ideas and context (section 3) |

**How to read them:**

- **With a shell:** clone what you need, for example `git clone --depth 1 https://github.com/TheSeekerGame/collections.git`. For `the-seeker`, run `git lfs install` first (section 7), or its art arrives as placeholders.
- **With web access only:** fetch the raw URLs. The game's images, audio, fonts and level projects are stored in Git LFS: `raw.githubusercontent.com` returns a text pointer of about 130 bytes for them, and `https://media.githubusercontent.com/media/TheSeekerGame/the-seeker/main/<path>` returns the real file. Nothing in `collections` uses LFS. List a folder with `https://api.github.com/repos/TheSeekerGame/<repository>/contents/<path>`.
- **Without web access:** work from this file, tell the person so, and ask them to paste whatever else you need.

**The sources evolve.** Read them fresh at the start of every project rather than relying on an earlier read. Where they disagree with this file, follow them and mention the difference to the person. The core (themes, art style, the tuning, the collections' on-chain rules) rarely changes; paths, features and numbers change more often. The endpoints, sizes and code in this file were checked in October 2026. In the game, code and assets define current behavior and design pages record intent. Where the design pages and the collections READMEs differ about the collectibles, the READMEs are current.

## 2. Work with the person

Find out, briefly: what they want to make and why, who it is for, where it should run or exist (a browser, a phone, a desktop, print, a shop), how experienced they are, which computer they use and what is installed on it, and any deadline or budget. Ask only what changes the plan. If the request is open-ended, propose a concrete concept in a sentence or two and start.

**For someone new to all of this:**

- Use plain words, and explain a term the first time it appears.
- Check instead of assuming. With a shell, run `git --version`, `python3 --version` or `node --version`; otherwise ask them to.
- Prefer results that need nothing installed: a web page opened by double-clicking, a link, an image, a PDF.
- Go one step at a time. Before each command, say what it does. Give exact text to copy for their operating system, and confirm each step worked before the next.
- Ask before installing software, creating accounts, spending money, or publishing anything. They decide.
- Keep the work in one clearly named folder and tell them where it is.
- Show results early: open the page, show the image, play the sound.
- If you cannot write files, give each file whole in one block and say how to save it: in a plain-text editor (Notepad on Windows; TextEdit on a Mac after Format → Make Plain Text), with a name ending in `.html`.

**For someone experienced:** match their tools and pace, and skip the explanations.

**Always** build the smallest version that is complete and good, then grow it, and say plainly what you checked and what you could not: a still image does not prove an animation works, and a passing test does not prove how something sounds or feels.

## 3. Choose a path

| They want | Start with | Needs |
| --- | --- | --- |
| To play The Seeker | Build it from source (section 7) | Git, Git LFS and Rust; about 500 MB to download and several GB of disk |
| Music in the Seeker tuning | [SEEKER](https://theseekergame.github.io/seeker-audio/): ✦ surprise, edit, share the link (it carries the whole song), export stems | A browser |
| A browser game, toy or interactive piece (2D) | One self-contained HTML file: a canvas and plain JavaScript, with a library from a CDN only when it clearly helps | A browser |
| A 3D experience in the browser | One HTML file with three.js | A browser |
| A larger 2D or 3D game for desktop, mobile or consoles | Godot (free, approachable, exports everywhere), Bevy and Rust like the main game, or a fork of `the-seeker` | The engine |
| Multiplayer | Shareable links for turn-based or asynchronous play, which need no server (SEEKER's song links show how). Real-time play needs a relay or host (WebRTC peer-to-peer, or a hosting service); choose one with the person. Chain data is still read by each client directly | Depends |
| Pixel art, sprites, icons | Draw in code (canvas, or Python with Pillow), or in Piskel (in the browser), Aseprite or LibreSprite | A browser or the editor |
| 3D models, rigs, figures | Blender (free), with the 2D art as reference; export glTF for games, STL or 3MF for printing | Blender |
| Illustrations, posters, cards, comics, zines | Integer-scaled pixel art or vector SVG; PDF for print | A browser |
| Animation, trailers, promo clips | Frames rendered in code or captured from the game, assembled with ffmpeg; music from SEEKER stems | ffmpeg (optional) |
| Merch | Print-ready files (section 5) for a print-on-demand shop the person chooses | A browser |
| A website | Static HTML and CSS, hosted on GitHub Pages, itch.io or similar | A browser |
| A tabletop game | Printable rules and cards (HTML to PDF), perhaps with a companion web page that reads the chain | A browser |
| Tools, bots, dashboards | A web page first; a script only if it must run unattended | Depends |
| A change to the game or a contribution | Sections 7, 8 and 11 | Git, Rust |

**Look at similar games.** The games in `community-games` are worth reading when they resemble the work: how they look, play and are built gives ideas and context. Soundings, for example, is a 3D ice-fishing game in three.js with a pixel look, the Seeker and SEEKER NET seekers as 3D characters, live chain reads and music in the 48 Hz tuning. Their code is MIT OR Apache-2.0, so anything useful can also be reused, with credit (section 9).

Favor formats that open anywhere (HTML, PNG, SVG, PDF, WAV or FLAC, glTF), few dependencies, and no build step for small web projects. A single HTML file opened straight from disk can call every public API and art host named in this file, because they allow requests from any page; the one exception is the Magic Eden ord mirror, which serves only native programs. A few browser features need a local server: audio worklets, for example, do not run from `file://`. `python3 -m http.server 8000` serves a folder at `http://localhost:8000`. Python comes with Apple's command line tools on a Mac (section 7); on Windows, install it from [python.org](https://www.python.org/downloads/).

## 4. The world and its spirit

`lore.md`, `open-brand.md` and `art-direction.md` are the full account; this is the essence for when you cannot read them.

### The universe

- **Theorem** is a vast organization devoted to discovering and formalizing knowledge across the universe. **Seekers** are its explorers, and Seeker is a role, not a species: humans, aliens and machines alike become one. The seekers of SEEKER NET, for example, are tiny computer-like robots.
- **The Codex** is Theorem's shared archive; a Seeker reaches it through the visor to scan, record and analyze. **Attunement** is the ability to sense the frequencies and structures of other beings and of the cosmos. Seekers travel and work alone.
- **The planet** is icy and almost implausibly rich. Life shelters in caves beneath the ice that grow warmer, stranger, more beautiful and more dangerous with depth. Scientists, opportunists, caretakers and worshippers have come too. Something near the core seems to call.
- **Guardians** are ancient alien demigods who watch over the planet. Their origins are a mystery.

The main story's twists and ending are deliberately unpublished. Do not invent them as canon or claim to reveal them; a new work finds its own answers. A work can continue the canon, extend it compatibly, fork it openly, or only borrow the style. All are welcome; say which one it is. None of the lore is required: one borrowed idea, such as the frozen planet, Theorem or the 12-based tuning, is enough to build on.

### The Seeker character

The main game's protagonist is one particular Seeker. Use this description only in works that include them; any other Seeker can look like anything.

- **A mysterious hooded explorer.** A small figure wrapped head to toe in a hooded cloak of muted, sandy gold, in the spirit of the hooded and cloaked wanderers of *Star Wars* and *Dune*. Inside the hood there is only darkness and a single pale slit of light, the visor through which they reach the Codex; the face is never shown. Dark legs show beneath the cloak, which streams behind them when they run.
- **A backpack that grows.** They usually carry a dark, compact backpack that grows as they gather, in three sizes from small to large (`the-seeker/assets/items/equipment/backpack1.png` to `backpack3.png`). The game swaps sizes as more materials fill it, and the pack trails the body slightly, hovers at rest and shakes while running (`game/src/game/player/equipment.rs`).
- **In the original game** they are about 12 pixels tall, and their sprites are in `the-seeker/assets/animations/player/`. Their gold is the warm accent described under Visual grammar.

### What it explores

- **Permutations of existence.** Seeing ultraviolet is one way to exist, thinking as a swarm another, living beneath an ocean of ice a third. Combined, they make an existence no one has had. A permutation counts when it changes behavior, perception, material, rhythm or what becomes possible next; a renamed item or a recolor does not.
- **Recursion.** The result of a process becomes an ingredient of the next pass: encounter, inhabit or transform, act, provoke a response, find a new possibility. Finite, legible rules can suggest the infinite; never promise literal infinity.
- **Expansion and simplicity.** One path leads toward more knowledge, abilities and possibility; the other toward humility, service and letting go. Both must be genuinely attractive, and neither may be made obviously foolish. Avoid moral lectures.
- **Recording versus experiencing.** Is recording something the same as understanding it, and understanding a creature the same as becoming it? Who benefits from what Theorem collects?
- **Giving without a transaction.** When a work lets someone give, restrain or let go, keep the act real: no hidden reward, virtue meter or reimbursement.
- **Mathematics as experience.** A triangle can be three connected points or a felt experience, as red feels unlike green. Let people feel how primes differ from even numbers or Fibonacci growth from a fractal, without lecturing them.
- **Mixed feelings.** Awe, loneliness, tenderness and unease together. The horror is quiet: vastness, indifference, beauty that asks something in return. Ordinary life (trade, play, care, family, cooking) makes the cosmic scale land.

**Tone:** quiet, vast, meditative, eerie, precise, beautiful. Alien but coherent, mysterious but never random. Show rather than explain. Avoid generic neon cyberpunk, gore for its own sake, quirky whimsy, exposition dumps, and creatures that exist only as enemies.

### Resonance: everything from one fundamental

Derive time, pitch and space from one root so that the whole work resonates. People should rarely notice it; it should simply feel synchronized. The values below are the game's. Translate them into whatever units suit the medium (meters, centimeters, grid cells, bars), or choose another fundamental when a work has reason to: the principle is coherence from one root, not the number 12 itself. Authored poses can step at 12 per second while motion, input and display stay smooth.

| Element | Value | Relation |
| --- | --- | --- |
| Animation | 12 frames per second | The fundamental, 12 |
| Pitch reference | 48 Hz, in any octave | 12 × 4 |
| Simulation tick | 96 Hz | 8 ticks per animation frame |
| Tempo | 90 BPM (1.5 Hz) | 8 animation frames per beat |
| Spatial module | 6 units (the game's 6 × 6 px tiles) | 12 ÷ 2 |
| Character height | 12 units (the game's 12 px Seeker) | Two modules |

**The tuning rule:** every pitch is `48 Hz × X / 2^N` for whole numbers X and N, so its denominator is a power of two: 9/8, 19/16, 13/8, 3/2 and 7/4 belong; 4/3 and 6/5 do not. Every note is then a harmonic of 48 Hz or of one of its lower octaves, folded into the octave needed. The default **Seeker palette** is 1, 9/8, 19/16, 21/16, 3/2 and 7/4 (48, 54, 57, 63, 72 and 84 Hz, repeating at every octave). This is just intonation, not twelve-tone equal temperament: use explicit frequencies or a microtuning-capable instrument. Tempos follow the same rule (`2880 × X / 2^N` BPM). Unpitched sound, noise and silence are free.

Lock periodic events to one shared clock so they agree in phase as well as rate. Five- and seven-step motifs realign every 35 steps, Fibonacci numbers (1, 1, 2, 3, 5, 8, 13…) can size phrases or rooms, and prime multiples of the base unit can size platforms. If something is called fractal, it must actually repeat an operation. Judge the result by looking and listening: correct arithmetic does not make a piece good.

### Patterns for interactive work

These are directions, not a checklist: use those that fit the work, and a racing game or a puzzle may need none of them. `docs/design/mechanics/` shows where the game stands on each.

- **Become, don't just collect.** Learning from a creature means temporarily taking on its movement, attacks or senses, sharing the creature's own mechanic, not firing a reskinned projectile.
- **The world answers.** Creatures adapt to how someone plays, legibly, opening new possibilities and leaving more than one response. Never build an omniscient counter that deletes a playstyle.
- **Materials remember.** How something happened changes what it yields: a bat wing, a frozen bat wing, a ruptured bat wing.
- **Prefer combinations to catalogs, and an ecology to an enemy list.** Connect beings through heat, food, shelter, predators and offspring; not everything is hostile.
- **The landscape takes part.** Spikes grow and routes shift, while essential paths stay viable and changes stay understandable.
- **Iterations remember.** If the world changes between runs, derive the change from what the last journey actually did, not from a fresh random seed.
- **Choices cost something real.** A path of restraint or letting go must not be quietly repaid.
- **Scope the first build around one loop that closes:** one form to become, one transformation, one adaptation, one new possibility.

## 5. Art

### Visual grammar

These hold in any medium: 3D, illustration, film, print, physical objects and pixel art alike. They describe the brand's look, not one game's.

- **One clear focal point.** Every image or scene has a subject that reads at a glance, set apart by value, color and placement. Give it a color nothing around it shares. In works that include the Seeker character, that is its muted gold: keep it the only yellowish thing in view, so it stays visible wherever it goes.
- **Color follows place.** The planet's frozen surface and upper caves are cold, pale and muted; deeper down it grows warmer, stranger and more exotic, and so do its colors. A work set elsewhere sets its own temperature. Whatever the palette, keep color purposeful: calm, restrained fields, clear value structure, and a few strong accents that lead the eye.
- **Silhouette first:** a few decisive features, then detail. Backgrounds stay simpler and quieter than the subject.
- **No outlines.** Form comes from adjacent masses of color and value, dark internal structure and selective pale rims, not a contour drawn around everything.
- **Depth from layering:** overlapping masses, atmosphere and haze, and distance that grows paler and quieter, as if lit from far openings.
- **Disciplined light** reveals form and leads the eye. Glow and bloom stay sparing so shapes survive.
- **Mineral and strange forms:** ice, mineral, fungal, mycelial, root, shell and modular structures, and organic shapes nobody can name. Strangeness deepens the farther a work goes.
- **Seeker technology** is dark, minimalist sci-fi fused with the organic: mostly black, with black organic detail and a pale core of light. The tether node is the example, a metal stake wrapped by a parasitic vine that roots into rock.
- **Families of beings** share a resemblance and diverge through mutation. Guardians combine dark modular bodies, pale eyes and rims, and suspended orbs; SEEKER NET's seekers are tiny computer-like robots.

**When the work is pixel art,** the game's own craft rules apply as well: compact clusters, crisp native edges, integer scaling with nearest-neighbor sampling only, purposeful negative space, dither for gradients and atmosphere, and parallax layers. Never mix pixel sizes: the world, its characters and effects, and the interface with its icons and text all share one pixel resolution on screen, with no piece drawn finer or coarser than the rest and none scaled down or by fractions. Mixed pixel sizes look broken even when every piece is fine on its own. The game draws its assets fully lit and lets the renderer darken the scene afterwards. Other media express the same ideas through their own techniques.

### Palette

Exact sRGB values sampled from the game's art, which so far covers the icy surface, the ice caves and the tundra below them. Pick a coherent subset per scene. Deeper regions grow warmer and more exotic: extend the palette that way with the same discipline. A new world can shift its hues entirely, toward a desert, an ocean or a nebula, as long as the relationships hold: restrained fields, clear value structure, and a few accents that lead the eye.

| Family | Colors |
| --- | --- |
| Seeker gold and deepest shadow | `#B9A87B` `#6B6258` `#2D2E33` `#0F0E16` `#FFFFFF` |
| Ice-cave stone | `#181C20` `#20242A` `#353E50` `#4F5D73` `#667389` `#94A6B1` |
| Dark creature bodies | `#181C20` `#262B32` `#313C43` `#3F4D5B` `#4F5D73` `#C2C9C9` |
| Pale shells | `#353B44` `#465B7D` `#627594` `#7B92A9` `#97ACB0` `#C2C9C9` |
| Minerals and snow | `#50607C` `#758399` `#94A6B1` `#C4CED4` `#EDF0F1` |
| Cold luminescence (sparingly) | `#698F9B` `#7BACBC` `#91CBDE` `#D6EDF5` |
| Tundra stone | `#21252C` `#2A2F32` `#353E50` `#3E545B` `#4F7368` `#557C70` `#8CA893` |
| Moss, bark and earth | `#1C1D22` `#353B44` `#49573D` `#61554C` `#796E58` `#6A7972` `#779051` `#8CA893` `#C2C9C9` |
| Living accents | `#696E49` `#8C9245` `#AD2E41` `#AF634B` |
| Atmospheric distance | `#5D666D` `#6C7983` `#83909C` `#8D9FAA` `#A1B2BB` `#B0C3CD` `#CFDDE4` `#D4E6EC` `#F5FAFD` |
| Neutral figure | `#010202` `#282E3C` `#5E6970` `#7E8991` `#F6FAFD` |
| A character who stands apart | `#000000` `#172808` `#654170` `#4C5C8C` `#5B8399` |
| Void | `#151515` |
| Interface | panel `#04060A` at 92%, well `#12151D`, empty well `#0B0D13`, line `#29303E`, text `#F0F2E8`, muted `#8A919E`, disabled `#454A4F`, positive `#ABE3D9`, negative `#E84D3D` |

### Where the art is

Use, remix and build on all of it. The game's art is CC BY 4.0 and the collections' art MIT OR Apache-2.0 (section 9).

| Location | Contents |
| --- | --- |
| `the-seeker/assets/animations/` | Every animated sprite sheet, one folder per character: `player/` (movement, sword, hammer, bow, skills, particles, sparks); creatures `bats/`, `spider/`, `opi/`, `squid/`, `buzzer/`, `tentacle/`, `void/`, `yak/`; people `collector/`, `exiled1/`, `monk/`, `observers/`, `vagrant/`; `objects/` (capsule, tent, tether node); `intro/` (the landing cinematic); `numbers/`. Each sheet's `.anim.toml` gives its frames, timing and events. `Name__r1c15__90x90.png` means 1 row of 15 cells, each 90×90 px. Magenta pixels in a sheet are collision masks, not art |
| `the-seeker/assets/levels/tiles/` | Terrain, platforms, decorations, near backgrounds and entities per biome (`ice_biome/`, `tundra_biome/`), and the auto-tiling tilesets and prop sheets in `ldtk_rules/` |
| `the-seeker/assets/levels/surface/` | The planet's surface: sky, clouds, far range, hills, crater rim |
| `the-seeker/assets/levels/background_bank/` | Generated middle and far cave backgrounds |
| `the-seeker/assets/items/` | 12×12 icons: creature drops, equipment, passives, weapons. `equipment/backpack1.png` to `backpack3.png` are the Seeker's backpack in its three sizes |
| `the-seeker/assets/ui/game/` | Skill icons, HUD, toolbar frames, key hints |
| `the-seeker/assets/fx/`, `assets/font/` | Fog and effect textures; the `PixelFont2.png` bitmap font and the Tektur typeface (SIL OFL) |
| `the-seeker/tools/` | Source art and exemplars (`source_art/`, `backgrounds/source/`, `surface_art/`) and `generate_*.py` scripts that place art pixel by pixel in code. Edit the script, not its output |
| `the-seeker/assets/audio/` | The game's sound effects and music (FLAC) |
| `collections/guardians/assets/` | Guardian layers: 15 backgrounds, 15 orbs, 37 eyes, and all 1,843 body states in four SVG bundles. `guardians.py` assembles any Guardian at any padding |
| `collections/SEEKER_NET/layers/` | Seeker layers: 16 monitors, 32 eyes, 14 floating objects, 10 hats, 7 flank and 7 back add-ons, 8 backgrounds, the uncharged screens and shades, 20 colorways, and animated strips. `seeker.py` draws any token |
| On-chain and Arweave | Each Guardian's live look at `https://ordinals.com/content/<inscription id>`; SEEKER NET's finished art on Arweave (each token's URLs are in `SEEKER_NET/lists/tokens.csv`) |

The PNGs under `assets/levels/chunks/` and `secret_rooms/` are level layouts, not artwork. Game art is 6 px tiles and a 12 px Seeker; sprite cells such as 48×48 are canvases, not body sizes. Guardians and seekers are 54×54 pixel art, shown at 20× (1080 px) in their collections.

### Into any medium or style

Every piece of this art can become something else: a rigged 3D character, a voxel model, a vector illustration, a painting, a plush, a 3D-printed Guardian, an animated short, a garment. Keep what makes it the Seeker's: silhouette and proportions, the palette's relationships (restrained fields, clear values, a few accents that lead the eye), no outlines, readable masses, and the quiet, strange mood. Keep pixelation only when the work wants it.

- **In 2D pixel-art games:** Guardians and seekers can come alive through procedural animation of their separate layers: an orb that drifts, eyes that blink or follow, a body that breathes, add-ons that sway, every move in whole-pixel steps. SEEKER NET already ships animated versions of every monitor, eye and add-on in `collections/SEEKER_NET/layers/animated/` (strips of 86×86 frames at 50 ms each, with a `.json` describing each motion), ready to use. To keep everything on the pixel grid, render at native resolution, scale up by whole numbers with nearest-neighbor sampling, and snap positions to whole pixels. The Seeker's own pixel-perfect renderer does exactly this in Bevy and can be reused: see the pixel-perfect rules in `AGENTS.md` and `game/src/camera/scale.rs`, `game/src/graphics/pixel_view.rs` and `game/src/graphics/pixel_perfect.rs`.
- **Fitting a game's palette:** when a Guardian or seeker clashes with a game's palette, shift its colors slightly toward the game's ramps, keeping values, silhouette and traits recognizable, so a holder still knows their piece at a glance. Seekers make this easy: their six color roles (lid, front body, body shadow, screen-inset shadow, secondary plate, indicator light) are mapped per colorway in `collections/SEEKER_NET/layers/colorways.json`, so a game can add its own mapping. Guardian bodies take their colors from palette variables inside their SVG bundles, and the other Guardian layers are small PNGs that can be remapped color by color.
- **To 3D and rigs:** use the sprite as orthographic reference and its animation sheet for poses and timing. Block out the forms in Blender, keeping the source's proportions (the Seeker, for example, is two modules tall, its head and visor reading at a glance). Take material colors from the palette, flat or lightly textured. Rig with an armature (Rigify suits humanoids), key the poses from the sheet at 12 frames per second with holds, and export glTF (`.glb`) for three.js, Godot or Bevy, or FBX for other tools. For printing, export STL or 3MF and thicken thin parts. Guardians and seekers also convert naturally to voxels: one 54×54 layer at a time, extruded by depth.
- **To vector and print:** one SVG square per pixel stays crisp at any size; traced shapes give a smoother style. Raster prints use integer scaling only: a 54 px Guardian at 20× is 1080 px, about 9 cm at 300 dpi, so larger prints should use SVG. Check colors in a proof, since print shifts them.
- **With AI image or 3D generators:** give them the original asset as reference, then check the result against the palette and rules above and fix what drifts.

## 6. The collections: holders are the game masters

### The idea

The brand's collectibles live on public blockchains, and a work can read their current state at any moment. When a holder changes a Guardian's look or a seeker's charge moves, every game, app and artwork that reads the chain shows it, single-player games included, because all of them read the same public source of truth. Nobody needs a server of ours. Holders shape the world everyone plays in; players need to own nothing.

**Bring the collections into whatever you make, wherever they fit and deepen it.** Nothing about how to use them is fixed. The best integrations make a work more interesting and richer in meaning: they belong to its fiction and its systems instead of being bolted on, and the work is complete and good for someone who owns nothing and never thinks about a blockchain. If an integration would hinder the work, leave it out or make it smaller.

### Rules for every integration

- **Read only, never write.** Never ask anyone to connect a wallet, sign anything, send or approve a transaction, or reveal a seed phrase or private key. Never call a contract function that changes state. SEEKER NET's `activate`, `activateMany` and `refreshTokens`, for example, are transactions even though anyone may send them. Reading needs nothing but public APIs, so it is seamless and free.
- **No server of your own is needed.** Each client reads the public APIs below directly and caches what it learns.
- **Never gate or sell the core experience.** Holding nothing must still mean the whole game. Influence belongs to holders' on-chain choices; it must never become pay-to-win.
- **Reading cannot prove who someone is.** Anyone can type anyone's public address, so never tie an advantage to claiming ownership. Let anyone meet, choose or bring along any Guardian or seeker (they are all public art) and let its live on-chain state decide what it does, or let world-level changes come from what holders actually do on-chain.
- **Be legible and fair.** Show where an influence comes from ("Guardian #12 changed form two blocks ago"), and apply changes at natural boundaries (a new run, a new region, a new session), never mid-jump.
- **Degrade gracefully.** Ship a snapshot or keep a cache, keep working offline, and show "last seen" times instead of pretending stale data is live.
- **For shared worlds, pin the inputs:** the same chain state and the same mapping version must give the same world in every copy.
- **No financial claims.** The collectibles are art and membership, not investments.

### Planetary Guardians (Bitcoin ordinals)

333 alien demigods, inscriptions `0000038e69f964da83318a45cd892abffbc63f73e0d08436d2ade37f5d8b3000i0` to `…i332`. Each has a fixed four-letter code, and its look comes from its **padding**: the value in sats of the Bitcoin output that holds it. A holder changes the look by moving the Guardian into an output of a different value; the change appears with the next Bitcoin block (about ten minutes). The selection rules come from the latest inscription on sat `1051634999999999`, which is how the collection can gain new looks later. Layers are background, orb, body and eyes, all 54×54, drawn in that order. `collections/guardians/README.md` has everything: endpoints, mirrors, caching, rate limits and the exact rules.

```js
// Browser-ready: a Guardian's current look, from public ord servers. Nothing to install.
const ORD = 'https://ordinals.com';   // mirror: https://static.unisat.io (and, outside browsers, https://ord-mirror.magiceden.dev)
const KIT = 'https://raw.githubusercontent.com/TheSeekerGame/collections/main/guardians/data/';
const json = url => fetch(url).then(r => { if (!r.ok) throw new Error(`${url}: ${r.status}`); return r.json(); });

function select(code, padding, rules) {   // the on-chain renderer's own rule, in double arithmetic
  let amount = padding;
  return [...code].map((letter, layer) => {
    const group = rules[layer][letter.charCodeAt(0) - 65];
    const r = amount % group.length;
    amount = Math.floor(amount / group.length);
    return group[r];
  });
}

async function guardianLook(id) {
  const [collection, config, inscription] = await Promise.all([
    json(KIT + 'collection.json'),                  // id -> {number, code}
    json(`${ORD}/r/sat/1051634999999999/at/-1`),    // the current selection rules
    json(`${ORD}/r/inscription/${id}`),             // value = padding, output, address
  ]);
  const rules = await json(`${ORD}/content/${config.id}`);   // about 1 MB: cache it
  const layers = select(collection[id].code, inscription.value, rules).map(ref => `${ORD}/content/${ref}`);
  return {padding: inscription.value, output: inscription.output, layers};
}

async function drawGuardian(canvas, layers) {   // pixel-identical to the on-chain renderer
  const load = src => new Promise((ok, fail) => {
    const img = new Image(); img.crossOrigin = 'anonymous'; img.onload = () => ok(img); img.onerror = fail; img.src = src;
  });
  const images = await Promise.all(layers.map(load));
  canvas.width = canvas.height = 54;               // scale up in CSS with image-rendering: pixelated
  const ctx = canvas.getContext('2d');
  ctx.imageSmoothingEnabled = false;
  images.forEach(img => ctx.drawImage(img, 0, 0, 54, 54));
}

// Guardians at a Bitcoin address: where every Guardian sits, matched against the address's unspent outputs.
async function guardiansAt(address) {
  const where = new Map();
  for (let page = 0, more = true; more; page++) {
    const d = await json(`${ORD}/r/children/1eab87f0048147a37b3be9f0f35227c77a7b258ce37ef1cf4a0e7adb16b20f5ei0/inscriptions/${page}`);
    d.children.forEach(c => where.set(c.output, c.id));
    more = d.more;
  }
  const utxos = await json(`https://mempool.space/api/address/${address}/utxo`);
  return utxos.map(u => where.get(`${u.txid}:${u.vout}`)).filter(Boolean);
}
```

The four children pages also give the whole collection's current outputs at once; an output's value never changes, so look up only outputs you have not seen. Check `/r/blockheight` every minute or two and refresh only when it changes. Native programs can use the same requests, or the kit's Python tools (`guardians.py`, `live.py`) and local art.

### SEEKER NET (Robinhood Chain)

2,222 tokens on Robinhood Chain (chain ID 4663), contract `0x5aC790269A6c71a51Ba68BF6a3a2647F86788792`. Every seeker charges continuously at 50 a day. Moving one keeps 75% of its charge and splits the other 25% among all the other seekers still charging. At 9,000 charge it activates for good and becomes an animated GIF. **Discharge** is what its last move gave away and **Uplink** everything it has given; both exist only while it is dormant. Its picture is one of six uncharged stages (one per 1,500 charge) until it activates. The art can grow too: the renderer contract can gain new traits, so read `renderer()` rather than keeping its address. `collections/SEEKER_NET/README.md` has every read, batching, polling, events and rate limits.

```js
// Browser-ready: live SEEKER NET data from a public RPC. Fallback RPC: https://robinhood.drpc.org
const RPC = 'https://rpc.mainnet.chain.robinhood.com';
const SEEKER_NET = '0x5aC790269A6c71a51Ba68BF6a3a2647F86788792';
const MULTICALL3 = '0xcA11bde05977b3631167028862bE2a173976CA11';
const word = n => BigInt(n).toString(16).padStart(64, '0');

async function ethCall(to, data) {
  const r = await fetch(RPC, {method: 'POST', headers: {'content-type': 'application/json'},
    body: JSON.stringify({jsonrpc: '2.0', id: 1, method: 'eth_call', params: [{to, data}, 'latest']})});
  const {result, error} = await r.json();
  if (error) throw new Error(error.message);
  return result.slice(2);
}

// One seeker, exactly as marketplaces see it: name, picture URL, traits, Status, Charge, Discharge, Uplink.
async function seeker(token) {
  const renderer = '0x' + (await ethCall(SEEKER_NET, '0x8ada6b0f')).slice(-40);   // renderer()
  const hex = await ethCall(renderer, '0x8f7bb179' + word(token));               // tokenJSON(token)
  const at = parseInt(hex.slice(0, 64), 16) * 2, length = parseInt(hex.slice(at, at + 64), 16);
  const bytes = Uint8Array.from(hex.slice(at + 64, at + 64 + length * 2).match(/../g), h => parseInt(h, 16));
  return JSON.parse(new TextDecoder().decode(bytes));
}

// The same one-argument read for many tokens in a single request, through Multicall3.aggregate3.
async function perToken(target, selector, ids) {
  const call = id => word(target) + word(0) + word(96) + word(36) + (selector.slice(2) + word(id)).padEnd(128, '0');
  const body = ids.map(call), heads = body.map((_, i) => word(32 * ids.length + i * 192));
  const hex = await ethCall(MULTICALL3, '0x82ad56cb' + word(32) + word(ids.length) + heads.join('') + body.join(''));
  const at = i => BigInt('0x' + hex.slice(i * 64, i * 64 + 64));
  const base = Number(at(0)) / 32;
  return ids.map((_, k) => {
    const t = base + 1 + Number(at(base + 1 + k)) / 32;
    return at(t + Number(at(t + 1)) / 32 + 1);    // each answer as a 256-bit number
  });
}

// SEEKER NET tokens held by an address: ownerOf for all 2,222, in two requests.
async function seekersOf(address) {
  const owned = [];
  for (let first = 1; first <= 2222; first += 1111) {
    const ids = Array.from({length: Math.min(1111, 2223 - first)}, (_, i) => first + i);
    const owners = await perToken(SEEKER_NET, '0x6352211e', ids);               // ownerOf(id)
    ids.forEach((id, k) => { if (owners[k] === BigInt(address)) owned.push(id); });
  }
  return owned;
}
```

`chargesOf(1, 2222)` returns every token's charge and status in one call (the SEEKER NET README decodes it). Between reads, charge only grows by 50 a day until someone moves a seeker, so a client can extrapolate and re-read every minute or so.

### Ideas, as examples only

- **A Guardian that molts in every world.** A boss or shrine guardian whose form, element and moves follow its live look: when its holder changes its padding, it has transformed the next time anyone meets it. Its body category could set how it moves and its orb what it guards.
- **Migrations.** A Guardian sent to a new address wanders to a new region of the planet, and players everywhere discuss where it went.
- **The network as weather.** The total charge of SEEKER NET is the planet's aurora, tide or season; every move, which strengthens all the others, sends a visible pulse through the world.
- **Activated seekers as companions.** Activated seekers drift through a game as tiny robot allies, scouts or Codex terminals, and dormant ones as dark husks that light up stage by stage.
- **Power-ups from the network.** A seeker's charge fuels a power-up, its stage unlocks an ability, its activation turns it into something new. Anyone can pick any seeker, so the advantage comes from the seeker's live state, not from owning it. Uplink measures what a seeker has given away, so it can shape how it helps others (its light spreading to allies, say) rather than paying its own holder back, in keeping with giving without a transaction.
- **A shared daily world.** Today's caves are seeded from the latest block hash and the collections' current state, so everyone explores the same planet today, single-player.
- **Music from the chain.** Each seeker is a harmonic of 48 Hz; activated ones sound, dormant ones hum quietly at their charge; a Guardian's code and padding choose a SEEKER mood and seed.
- **A living artwork.** A poster, mural, screensaver or website that redraws itself as Guardians change and seekers activate, or a print edition "as of block N".
- **A game master's console.** Show a holder what their Guardian would look like at any padding, using the kit's rules, before they decide anything. The tool only reads; any change they make happens in their own wallet.
- **Tabletop.** A companion page reads the chain at the start of each session, and the campaign's Guardians and the network's weather follow.

### The other collections

[The Seeker](https://ord.net/collection/the-seeker) (the development diary, on Bitcoin since 2023) and [Planetary Primes](https://ord.net/collection/planetaryprimes) (mathematical artifacts on prime-numbered sats) are also part of the brand, but have no kit yet. They can be read through the same ord recursive endpoints once their inscription IDs are known; Possible roles include Primes seeding a region's geography.

## 7. Play and change The Seeker

The game is a Rust and Bevy desktop metroidvania. There are no prebuilt downloads: build it from source. It needs Git, Git LFS (for the art and audio) and Rust. The download is about 500 MB, the build needs several GB of disk, and the first build takes a long time; later ones are quick. Continuous integration builds it on Linux; macOS and Windows are supported by Bevy but not built by continuous integration. Use each tool's official installer page, since install commands change.

**macOS**

1. Install Apple's command line tools: `xcode-select --install`.
2. Install Git LFS: install Homebrew from [brew.sh](https://brew.sh), then `brew install git-lfs`.
3. Install Rust from [rustup.rs](https://rustup.rs): `curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh`. Then open a new terminal window.

**Windows**

1. Install Git for Windows from [git-scm.com](https://git-scm.com/), which includes Git LFS.
2. Download and run `rustup-init.exe` from [rustup.rs](https://rustup.rs), and accept its offer to install the Visual Studio C++ build tools. Then open a new terminal window.

**Linux (Debian or Ubuntu; other distributions have equivalent packages)**

1. `sudo apt-get install git git-lfs build-essential pkg-config libx11-dev libasound2-dev libudev-dev libwayland-dev libxkbcommon-dev`
2. Install Rust from [rustup.rs](https://rustup.rs), then open a new terminal.

**Then, everywhere:**

```sh
git lfs install
git clone https://github.com/TheSeekerGame/the-seeker.git
cd the-seeker
cargo run
```

`SEEKER_SKIP_INTRO=1 cargo run` skips the landing cinematic. In the game, C shows the controls; the README lists them. To update later, run `git pull` and `cargo run` again.

**If something goes wrong:**

- Errors about images or audio that cannot be read mean the LFS files arrived as pointers: run `git lfs install` and then `git lfs pull` inside the folder.
- `clippy-driver` not found: `rustup component add clippy`. The build runs Clippy as part of every compile.
- A linker error on Windows means the C++ build tools are missing; on Linux, a missing system library means the packages above are missing.
- Send the full error text to whoever is helping; it usually names the cause.

**To change the game,** read `AGENTS.md` (the source map and the rules every change preserves) and `CONTRIBUTING.md` first. `AGENTS.md` is the repository's instruction file for AI agents; read it yourself even if your tool did not load it on its own. Its key rules: never run `cargo fmt`, since the code is not rustfmt-formatted; test with development builds, not `--release`; keep gameplay tuning, units, timing and asset bindings unless changing them is the point; keep generic code in `engine/` and game rules in `game/`; check with `cargo check`, `cargo test --workspace` and `cargo clippy --workspace --all-targets -- -D warnings`; play anything you can see or hear; and update the documentation the change affects. New art follows `docs/authoring/assets.md` and `animations.md` (PNG, a `.anim.toml` per sheet, a grid encoded in the filename); new audio is FLAC in the tuning. A personal variant lives on a fork or branch; sharing it as a fork is welcome.

## 8. Other projects to use and change

**SEEKER, the music studio** ([open it](https://theseekergame.github.io/seeker-audio/)): ✦ surprise writes a song in one of eleven styles, the spiral plays notes, layers and patterns edit it, share copies a link that contains the whole song, rec records a WAV, and the menu exports stems for a video or a game. To change it, clone `seeker-audio`, run `python3 -m http.server 8000` in its folder, and open `http://localhost:8000` (audio worklets do not run from `file://`). Produce every pitch through `js/tuning.js`, never from raw frequencies; raise `GENERATOR_VERSION` in `js/generate.js` when generation changes; run `npm test` (Node 18 or newer); and listen to anything that affects the sound. A fork can publish itself with GitHub Pages.

**The collection kits** (`collections`, Python and Pillow; seekers also need numpy):

```sh
python guardians.py render --id <inscription id> --padding 1000 --scale 20 --output guardian.png
python live.py --id <inscription id>      # in guardians/: its current padding and layers
python3 seeker.py 1895                     # in SEEKER_NET/: token 1895 at its live charge
python3 live.py                            # in SEEKER_NET/: every token's live state, as JSON
```

## 9. Licenses and credit

| Repository | Licenses |
| --- | --- |
| `the-seeker` | Code and technical documentation: MIT OR Apache-2.0. Art, animation, audio, lore and design: CC BY 4.0. Fonts: SIL OFL 1.1 |
| `seeker-audio` | Code: MIT OR Apache-2.0. Artwork: CC BY 4.0 |
| `collections` | Everything, art included: MIT OR Apache-2.0. Bundled third-party contract libraries keep their own notices |
| `community-games` | As `the-seeker`: code MIT OR Apache-2.0, project assets CC BY 4.0, fonts SIL OFL 1.1. Each game's `licenses/` holds the notices of what it bundles (three.js, for example) |

Anyone may use, remix and sell what they make, commercially too. CC BY asks for credit, a link to the license, and a note of changes. The line from `LICENSE.md`:

> Includes or adapts assets from The Seeker by The Seeker contributors, licensed CC BY 4.0: https://creativecommons.org/licenses/by/4.0/ . Original project: https://github.com/TheSeekerGame/the-seeker . Changes were made where applicable.

Credit The Seeker in every work, never present a work as an official release of the project unless it is one, and keep third-party material under its own terms. When in doubt, read the license files; this is not legal advice.

## 10. Safety

- Never ask for, accept or store seed phrases, private keys or passwords. If someone offers one, tell them to keep it private.
- Never connect wallets, request signatures or send transactions, in anything you build or anything you do.
- Public addresses and token IDs are all reading needs. Do not link addresses to real identities.
- Promise nothing about prices, value or returns.
- Do not impersonate the project's team, and be wary of anything that asks for payment or keys in The Seeker's name.
- Ask before publishing, posting, opening pull requests, buying or ordering anything.

## 11. Contribute back

Code, art, music, levels, documentation, bug reports and playtesting are all welcome in `the-seeker`, `seeker-audio` and `collections`, and finished browser games in `community-games` (one folder each, every path relative, as its `README.md` describes). The best ideas from forks can flow back into the originals.

1. **Talk first about anything large:** open an issue or a draft pull request describing the idea.
2. **Fork the repository and make a focused branch,** one topic per pull request.
3. **Follow the repository's rules:** `CONTRIBUTING.md` and `AGENTS.md` for the game; for `seeker-audio`, `npm test` and listening; for everything, the design pages, so the work fits the vision and the art direction.
4. **Verify:** run the checks, play or listen, and update the documentation the change affects.
5. **Describe the pull request:** what changed and why, which checks ran, and what was or was not playtested.

High quality and alignment with the vision decide what is merged; maintainers review every pull request. For someone new: they need a free GitHub account; forks and pull requests can be made on the website, with GitHub Desktop, or with the `gh` tool. Ask the person before opening a pull request in their name, and never push to someone else's repository without permission. Asset contributions to the game are licensed CC BY 4.0, and maintainers may also relicense them under CC0 (see `LICENSE.md`).

## 12. Before you call it done

- **Feel:** does it feel like The Seeker (vast, precise, quietly strange) beyond names and references?
- **Its own life:** does it have its own world and meaning rather than retelling the main game?
- **Experience:** is it compelling without a lore lecture, and does its focal subject read at a glance?
- **Permutation:** do variations change something that matters? Does at least one loop close?
- **Mathematics:** are the claimed ratios, sequences and transformations actually present?
- **Craft:** have you looked at the rendered result and listened to the actual sound?
- **Collections:** if they are in it, do they deepen the work, read only, survive being offline, and leave the work whole for someone who owns nothing?
- **Openness:** is The Seeker credited, and are licenses and the work's own sources clear?
- **The person:** can they open, run or use it on their own machine? Do they know where the files are, what was verified and what was not, and what they could do next?

## 13. Field notes

Findings from earlier works, each with the context it came from. They are not rules: they help works that share that context, and the rest of this file always takes precedence.

### SEEKER NET seekers as 3D characters

**Context.** A 3D browser game built with three.js (October 2026), in which seekers follow the player and work as fishing devices: Soundings, whose working code is `community-games/soundings/src/actors/seekerbot.js` (the seekers) and `objects.js` (their floating objects). These notes help any work that shows seekers as 3D models; works in 2D or print need none of it.

- **Size.** Seekers read as characters at about half the Seeker's height, and as props when much smaller. With a 1.6 m Seeker, that is about 2 cm per art pixel: a seeker of 35 to 40 px then stands about 0.8 m tall.
- **The art is an oblique view, so plain extrusion only looks right from the front.** Each monitor shows its front face, a lid (the top face, three or four rows receding up and to the left) and a dark bevel (the left face, five to ten columns). Rebuild it as a box:
  1. Classify each base pixel once by its master color role and where it sits: lid (`T` and `R`, from the top down), bevel (`D`, `Z`, `L` and `K`, left of the front), front everything else. Do it per base in the master colors, where the roles are unambiguous, then shift the result by each token's base offset.
  2. Extrude the front face back to a depth of about one and a half times the bevel's width, and wrap the lid art onto the top face and the bevel art onto the left side, sampling them along the receding direction. Give the right side and the back the front's edge colors and the bevel's dark.
  3. Set the black screen one voxel deep, with the eyes (or the battery) on it.
  4. Place each add-on at its depth. The art draws every part shifted up and to the left by how far back it sits, so undo that shift for its depth: the hat moves down and right by half the lid's height and half the bevel's width and sits on the box at mid-depth; the back add-on moves by the full lid and bevel and goes behind the back face; the flank pieces move by half and sit at the sides at mid-depth. The floating object is the exception: model it (below).
- **Give the depth something to show.** A box that only extends the front face looks like a slab from every other angle. Behind the screen, add the tapered housing of a tube monitor (about half the box's depth, stepping in a little on each side), vent slots across its top and down its sides, screws at the back corners, a grille on the lid, rubber feet and a power cable out of the back, all in darker shades of the seeker's own casing.
- **Model the floating object; never extrude it.** The 14 objects in `collections/SEEKER_NET/layers/objects` (Keyboard, Classic, Compact and Split Keyboard, Numpad, Mouse, Trackball, Joystick, Gamepad, Fader Deck, Dial Deck, Datasette, Floppy Drive, Codex Slate) are drawn in the same oblique view as the monitors, and a tray, a tilt or an extrusion of their pictures keeps that drawn perspective: it looks warped from any angle. Build each kind once, as the thing itself:
  1. Read its real proportions off the art. Its true width is the picture's width less the slant (about one pixel per receding row), its true depth about twice its receding rows (an oblique view halves depth), its thickness the rows of its front edge. A keyboard comes to about 22 × 9 × 2 voxels, a mouse 7 × 10 × 4, a floppy drive 19 × 12 × 4.
  2. Use the layer's own colors. In every token checked, the object's pixels match the master layer whatever the colorway, so one model per kind serves all 2,222 seekers; only its position shifts, by a pixel at most. The pale rim `#8ea6db` and the bevel shades `#6c78a2` and `#48557e` along every object's edges are the drawing's edge light: leave them out of the model, or use the pale one for a faint dashed ring underneath, which reads as the field it floats on.
  3. Detail it at one voxel per art pixel: keys on every other voxel, staggered row to row, so the dark plate shows between them (it reads as a keyboard at a glance), and a space bar; lights as single lit voxels; dials as plus-shaped caps with a pointer; fader caps on dark slots; a cassette window with two spools; a disk slot; lines of glyphs on a dark screen; a mouse's button split, wheel, and cable running back to the seeker. Shells read better as rounded rectangles stepping in toward a hump than as stacked ellipses, which look lumpy at this size.
  4. Place it from the token's art: centred under the picture's front edge (its bottom two rows), two or three voxels in front of the screen, its body (the slab, not a joystick's stick or a trackball's ball) just under the monitor's feet. Anchored at the bottom of the picture's bounding box instead, it hangs far below, because the drawn top face makes the picture several times taller than the slab. Leave room in the voxel grid's depth for it.
- **Start from the parts, not the finished picture.** The engine's `layers(t)` in `collections/SEEKER_NET/engine/final.py` returns every part already placed and recolored, in paint order; the finished picture has lost what lies behind each part.
- **Rig them by part.** Keep the floating object, back add-on, body, flank, head and eyes as separate meshes so each can move on its own, stepping on the 12 fps grid: the object drifts on its own, slower than the rest, the head sways, the flank pieces lift, and the eyes blink and glance toward what the seeker watches. Light the eyes, and let the screen cast a little light on what is around it.
- **Float, and move calmly.** Close to the ground, seekers look as if they drag; about 0.35 m above the snow (0.6 m with a Propeller or Thruster Pods), they float. Hopping and fast bobbing read as frantic, even comic. A breath of about 2 cm every five seconds, and a glide with a slight forward lean while following, read as calm. Keep quick movement for moments that mean something: a bite at its hole, an Overdrive, a surge.
- **Voxels with greedy meshing** keep each seeker to a few hundred triangles: only faces between filled and empty cells, with coplanar same-colored neighbors merged.
- **Dormant pictures** are the seeker darkened by one flat shade per stage, with the battery icon in place of the eyes; in 3D that is a tint on the body and the battery as the lit layer on the screen.
- **In the work's own palette.** Snap the art's colors, and every shade derived from them (the darker casing behind the screen), to the work's palette by nearest color in OKLab, so seekers sit in the scene rather than on top of it. Keep the exact colors only for checking pictures against the collection's checksums.
- **Portraits at one pixel per art pixel.** Crop a portrait to the seeker's own bounds: a fixed crop cuts off tall hats and antennas. Never scale the art down. A crop of the head alone (26 × 26 px from 14, 12) works as a small icon, with the whole seeker shown beside its details.
- **Check each kind on its own.** Render every floating object (and every base) alone, with a close camera from the front and a little above, into a labeled contact sheet: a scene with all of them at a distance hides what is wrong. A still image does not prove the motion.

### Interfaces in games

**Context.** Soundings again (October 2026), a pixel-art 3D game whose interface went through many rounds of a player's notes. These notes help any game or interactive work with a HUD, menus or dialogue.

- **Pixel art is a choice, not a requirement.** An interface can just as well be clean type, flat color and vector shapes. Whatever its style, it must be intentional and well crafted: clear at a glance, calm rather than busy, every element earning its place.
- **Nothing overlaps anything.** Windows never stack on one another or sit over the HUD; the HUD steps back while a window is open. Floating prompts and cards find a place that covers neither the character nor what the player is looking at. Crowded marks, on a compass for example, keep their icons and drop their labels rather than drawing over each other.
- **Design decisions over text.** Explain through play: let a new ability happen once on its own so the player sees what it does, show a key only where it can be used, and show an effect where it acts. Don't announce every event in a notice, which reads like output logs: one notice at a time, and only what matters. A short line of words is fine where a choice needs it, but a paragraph is a sign the design has not done its job.
- **One thing selected, one place for its words.** A menu reads best as a few short tabs, a grid of clear icons, one detail area for whichever entry is selected, and the actions that entry allows. Fit it on one screen without scrolling, so nothing is ever cut off. Show progress as a visible track of steps or numbers rather than describing it in paragraphs.
- **Every interface works by keyboard as well as by pointer,** with the same few keys everywhere to move, choose and close, and a click beside a window never closes it.
