# In The Saddle — Unreal Engine 5

A natural-language wargame where the commander **lives** the battle: 360° view
from the saddle, time controls (pause / slow / fast / replay), fog of war
through the commander's own eyes, messengers that physically carry orders and
reports, and orders typed in plain words.

This repo is the UE5 home of the project. The playable web prototype
(`in-the-saddle` artifact) proved the experience; this is where the real
thing gets built with proper 3D assets.

## Getting started (your steps)

You need a Windows PC, an Epic Games account, and ~60 GB of free disk.

1. **Install the Epic Games Launcher** — https://www.epicgames.com/store/download
2. **Install Unreal Engine 5** (latest 5.x) from the launcher's Unreal Engine tab.
   Big download; let it run.
3. **Claim the free stuff** (see [docs/asset-wishlist.md](docs/asset-wishlist.md)):
   - In-engine: Quixel Bridge + Megascans (free environment assets).
   - On Fab: this month's free packs at https://www.fab.com/limited-time-free —
     claim them even before you need them, they're yours forever.
4. **Create the project**: in UE5, New Project → Games → **Third Person** →
   Blueprint → name it `InTheSaddle`. This template is our starting skeleton.
5. **Clone this repo** next to (or into) your project folder for the docs,
   roadmap, and asset notes. Docs live here; the `.uproject` lives wherever
   you created it.

## Steal with pride

Don't build what Epic gives away (full list in
[docs/asset-wishlist.md](docs/asset-wishlist.md)):

- **Environment**: Quixel Megascans (free, in-engine via Bridge) — the valley,
  trees, grass, ground detail.
- **Reference architecture**: Lyra Starter Game (free sample in the launcher) —
  read it, don't build on it.
- **The horse** (the crux asset): paid Fab packs exist with full rider
  animation sets; there's also a free Horse Kit template on itch.io. Decision
  deferred until the valley exists.

## Milestones

- **M0** — Third Person template opens, press Play, character runs around. ✅
  (do this first, it validates the whole toolchain)
- **M1** — A valley: landscape + Megascans trees/grass, atmospheric lighting.
- **M2** — A horse standing in the valley. Then: riding it.
- **M3** — Camera locked to the rider's head, 360° look.
- **M4** — Port the web prototype's systems: time controls, messengers,
  visibility-masked map. See [docs/roadmap.md](docs/roadmap.md).

## Learning path (no UE experience required)

- Epic's "Your First Hour in Unreal Engine 5" (free, on the Epic Developer
  Community) — do this before touching the project.
- Then: the Third Person template's Blueprints — open the character Blueprint
  and read it like source code. Blueprints first, C++ later (or never).
