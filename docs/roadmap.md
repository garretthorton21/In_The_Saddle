# Roadmap: web prototype → UE5

The web prototype proved the **experience**. UE5 is where the systems get
real. Each prototype feature maps to a UE5 system below.

## Feature map

| Prototype | UE5 equivalent | Notes |
|---|---|---|
| 360° look from saddle | Camera component on rider's head, mouse-look | Third Person template's camera, repositioned |
| WASD riding | Character movement + horse anim Blueprint | Horse asset's locomotion blendspaces |
| Pause / ½× / 1× / 2× / 4× time | Global time dilation (`Set Global Time Dilation`) | Trivial in UE; UI buttons in UMG |
| Replay mode | **Hard.** UE has no built-in rewind. Options: (a) record transform snapshots each tick and scrub them (simple, memory-heavy); (b) deterministic re-simulation (complex). Start with (a), capped at N minutes. |
| Messengers carry orders/reports | AI controllers + navmesh; orders as data, delivery on arrival | Delay becomes physical distance/speed, exactly like the design doc |
| Visibility-masked tactical map | UMG widget + scene capture or fog-of-war material | Mask radius = the ¼-mile visibility setting from the design doc |
| Plain-language orders | Local command grammar now; LLM API later (server-side, never in-client) | The messenger delay already covers LLM latency — the design anticipated this |
| Enemy "ghosts" (last reported positions) | Decals/actors with fading opacity on the map | Straightforward once the map exists |

## Suggested build order

1. Valley + horse + riding (M1–M3). No game systems yet — just the feeling of
   sitting in the saddle and looking around.
2. Time controls + replay snapshot recorder.
3. One messenger: ride out, deliver a report, ride back. Prove the delay loop.
4. Visibility-masked map with ghost markers.
5. Plain-language order box wired to the messenger system.

## Deliberately deferred

- Real AI order understanding (needs a server + API key; the grammar
  stand-in carries the design until then).
- Multiplayer, mod support, the full customization suite from the design doc.
- C++ — Blueprints carry us until profiling says otherwise.
