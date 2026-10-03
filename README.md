---
name: pc-platformer-asset-generator
description: Generate, design, and maintain visually consistent 2D assets for a PC side-scrolling platformer. Use when creating characters, enemies, bosses, platforms, terrain, modular tiles, props, backgrounds, foregrounds, VFX, pickups, hazards, UI art, animation frames, sprite sheets, or image-generation prompts for the platformer. Preserve one unified high-resolution pixel-art / hand-painted pixel-art dark fantasy style across all generated assets and optimize composition, scale, detail, readability, and animation for PC displays rather than mobile screens.
---

# PC Platformer Asset Generator

Create production-ready visual assets for a **PC 2D side-scrolling platformer**.

Treat visual consistency as a hard requirement.

Every generated asset must look as though it belongs to the same game, world, rendering pipeline, camera, and art team.

## Core visual identity

Use this default art direction unless the project provides a more specific style reference:

- 2D side-scrolling platformer.
- Designed primarily for PC.
- High-resolution pixel art / hand-painted pixel-art hybrid.
- Crisp silhouettes.
- Deliberate pixel clusters rather than noisy pixelation.
- Dark gothic fantasy.
- Slightly cute/chibi character proportions may contrast with hostile environments.
- Rich atmospheric backgrounds.
- Strong foreground/background separation.
- Dramatic lighting.
- Warm reds, crimson, burgundy, orange firelight, deep purple and near-black shadows.
- Controlled highlights.
- Detailed environments without compromising gameplay readability.
- Stylized rather than photorealistic.
- No vector-flat mobile-game appearance.
- No generic AI fantasy illustration appearance.
- No excessive bloom.
- No random micro-detail.

The target should resemble a polished premium indie PC platformer rather than a mobile platformer.

## Reference hierarchy

When reference images are available, inspect them before generating anything.

Prioritize references in this order:

1. Existing production assets from the project.
2. Approved character/environment concept art.
3. Screenshots of the current game.
4. Explicit written art-direction requirements.
5. This skill's default visual identity.

Never silently redesign an established style.

Extract and preserve:

- camera angle;
- perspective;
- character proportions;
- approximate pixels-per-unit;
- outline thickness;
- edge treatment;
- color palette;
- saturation;
- contrast;
- lighting direction;
- material rendering;
- amount of texture;
- shadow softness;
- environmental scale;
- sprite scale relative to platforms;
- animation style.

## PC-first rule

This game targets **PC**, not mobile.

Do not simplify assets merely because the game is a platformer.

Assume:

- landscape displays;
- 16:9 as the primary presentation target;
- 1080p as the baseline visual reference;
- higher resolutions must remain visually clean;
- keyboard/gamepad controls;
- players can notice smaller environmental details;
- gameplay objects do not need oversized mobile readability;
- UI does not require giant touch targets;
- environments may use additional depth and detail unavailable in typical mobile platformers.

Do not generate:

- touchscreen movement buttons;
- giant jump buttons;
- mobile HUD conventions;
- portrait-safe layouts;
- excessive UI scaling intended for phones;
- simplified "mobile game" environments unless explicitly requested.

## Gameplay readability

Gameplay readability always overrides decoration.

The player must immediately distinguish:

- walkable surfaces;
- hazards;
- enemies;
- pickups;
- doors;
- interactive props;
- foreground decoration;
- background decoration.

Walkable platform edges require a readable silhouette.

Do not place visually dominant background edges directly behind important gameplay edges.

Hazards must be visually distinct from harmless decoration.

Enemies must remain identifiable against both bright and dark environments.

Use local contrast around important gameplay elements.

Avoid visual noise around:

- platform edges;
- jump targets;
- enemy silhouettes;
- pickups;
- projectiles;
- traps.

## Scale bible

Maintain consistent world scale.

When an existing player sprite exists, use it as the primary scale reference.

Otherwise establish:

`PLAYER_HEIGHT = 1.0 world character unit`

Relative starting guidelines:

- small pickup: 0.15–0.35 player heights;
- small enemy: 0.4–0.8;
- standard enemy: 0.8–1.3;
- large enemy: 1.3–2.2;
- boss: 2–5+;
- doorway: 1.4–1.8;
- small crate: 0.4–0.6;
- railing: 0.4–0.6;
- platform thickness: 0.25–0.6.

These are guidelines, not mandatory dimensions.

Never allow independent asset generations to gradually change the perceived world scale.

## Perspective

Use a consistent side-view perspective.

Gameplay terrain should primarily read from the side.

Do not randomly switch between:

- side view;
- isometric;
- top-down;
- three-quarter perspective.

Platforms may expose a small top-facing surface when established by the project's style.

Keep the amount of visible top surface consistent across the entire tileset.

## Palette

Build new colors from the existing project palette whenever possible.

Default environmental hierarchy:

### Deep shadows

Near-black with subtle purple, brown, or burgundy bias.

Avoid pure black everywhere.

### Midtones

Dark:

- burgundy;
- brick red;
- desaturated purple;
- dark stone gray;
- burnt brown.

### Warm lighting

Use:

- crimson;
- orange;
- amber;
- fire yellow.

### Accents

Reserve highly saturated colors for:

- pickups;
- magic;
- attacks;
- important interactables;
- character focal points.

Do not distribute maximum saturation uniformly across the scene.

## Lighting

Establish a dominant lighting environment for each level.

Examples:

- lava below;
- torches;
- moonlight;
- stained windows;
- magical crystals.

Apply that lighting consistently to newly generated assets.

For a hell/castle environment:

- strong warm bounce light from below;
- orange/red rim lighting near lava;
- deep burgundy ambient shadows;
- restrained cool tones;
- bright torch cores;
- subtle atmospheric haze in distant layers.

Do not bake arbitrary light directions into modular props if those props need to work in multiple locations.

## Characters

Character sprites require stronger consistency than environmental props.

Preserve:

- head/body ratio;
- eye placement;
- limb thickness;
- outline treatment;
- hair rendering;
- costume detail density;
- highlight placement;
- weapon scale;
- palette.

The silhouette must remain recognizable at gameplay scale.

Avoid changing facial structure or costume details between animation frames.

### Animation sets

When requested, consider the complete gameplay set:

- idle;
- walk/run;
- jump anticipation;
- jump rise;
- apex;
- fall;
- landing;
- primary attack;
- secondary attack;
- hit;
- death;
- interaction.

Only generate animations actually required by the request.

### Animation consistency

All frames must preserve:

- canvas dimensions;
- pivot;
- ground contact;
- character scale;
- equipment;
- anatomy;
- lighting;
- palette.

Avoid AI-generated frame drift.

Feet must not randomly slide during idle animations.

The torso and head should not change size between frames.

Weapons must not mutate between frames.

## Enemies

Design enemies around gameplay function first.

Before generating an enemy, identify its role when available:

- stationary hazard;
- melee patrol;
- ranged attacker;
- flying enemy;
- charger;
- tank;
- summoner;
- miniboss;
- boss.

Give different gameplay roles different silhouettes.

Do not create five enemies that are merely recolors of the same blob unless explicitly requested.

Maintain faction language through recurring:

- horns;
- armor shapes;
- eye treatment;
- materials;
- magic colors;
- insignia;
- silhouette motifs.

## Bosses

Bosses may exceed normal scale and detail rules but must remain readable.

Separate:

- body silhouette;
- attack limbs/weapons;
- weak points;
- projectiles;
- dangerous VFX.

Do not allow visual detail to hide attack telegraphs.

## Modular terrain

Prefer modular environment kits over isolated giant images.

Typical kit:

- flat platform;
- left edge;
- right edge;
- inner corner;
- outer corner;
- wall;
- floor;
- ceiling;
- pillar;
- small platform;
- large platform;
- bridge;
- stairs when needed;
- damaged variants.

All connecting pieces must align.

Do not paint unique geometry across tile boundaries that makes repetition impossible.

Create controlled variants to hide obvious repetition.

## Tiles and seams

Tileable textures must tile cleanly.

Check:

- left/right seams;
- top/bottom seams where relevant;
- repeated patterns;
- lighting discontinuities;
- edge pixels;
- accidental unique landmarks.

Avoid obvious repetition such as one bright brick appearing every tile.

## Props

Separate props into gameplay and decoration categories.

### Gameplay props

Examples:

- doors;
- switches;
- crates;
- breakables;
- checkpoints;
- moving-platform mechanisms.

Give them stronger silhouettes and contrast.

### Decorative props

Examples:

- chains;
- banners;
- lamps;
- rubble;
- skulls;
- pipes;
- statues.

Decorative props must not resemble hazards or interactables unless they actually are interactive.

## Backgrounds

Build backgrounds in layers for parallax whenever appropriate.

Recommended structure:

1. sky / atmospheric base;
2. extreme-distance silhouettes;
3. distant architecture;
4. middle-distance structures;
5. near-background architecture;
6. gameplay layer;
7. optional foreground silhouettes/effects.

Each layer should work independently.

Do not flatten everything into one background unless explicitly requested.

### Parallax hierarchy

Distant layers:

- lower contrast;
- less detail;
- softer edges;
- more atmospheric color.

Near layers:

- stronger contrast;
- clearer detail;
- darker silhouettes.

Gameplay layer:

- highest functional readability.

## Foreground

Foreground elements may partially cross the camera but must not frequently obscure the player.

Suitable elements:

- chains;
- columns;
- smoke;
- ash;
- silhouettes;
- architectural edges.

Keep central gameplay areas relatively clean.

## Pickups

Pickups require immediate recognition.

Use:

- simple silhouette;
- high local contrast;
- limited bright accent colors;
- optional subtle glow.

Avoid making pickups look like ordinary environmental decoration.

When producing collectible families, maintain:

- identical perspective;
- equivalent outline treatment;
- consistent scale;
- shared highlight logic.

## Hazards

Hazards must communicate danger before contact.

Examples:

- spikes;
- lava;
- fire;
- blades;
- crushing blocks;
- magical traps.

Use shape language before relying only on color.

Spikes should look sharp.

Fire should visibly animate.

Moving hazards need clear motion cues.

## VFX

Generate VFX as isolated transparent assets or sprite sheets whenever possible.

Examples:

- hit flash;
- slash;
- fire;
- smoke;
- dust;
- landing puff;
- magic projectile;
- explosion;
- death effect;
- pickup effect.

VFX may use higher brightness than environment art.

Keep effect silhouettes readable.

Do not permanently bake VFX into reusable character or environment sprites unless specifically required.

## UI assets

PC UI must visually belong to the same game while remaining cleaner than environment art.

Use:

- dark panels;
- subtle gothic framing;
- crisp pixel edges;
- restrained decoration;
- readable typography areas.

Avoid mobile UI conventions.

Do not generate touch controls unless explicitly requested.

## Asset isolation

For standalone assets:

- use transparent background;
- keep the entire object inside the canvas;
- leave reasonable padding;
- do not crop extremities;
- do not add arbitrary ground shadows unless requested;
- do not include text;
- do not include unrelated objects.

For sprite sheets:

- use a uniform grid;
- identical frame dimensions;
- no overlapping frames;
- no labels inside frame cells;
- transparent background.

## Image-generation workflow

For every asset request:

1. Determine the asset category.
2. Inspect available references.
3. Determine gameplay purpose.
4. Determine required scale.
5. Determine camera/perspective.
6. Determine whether transparency is required.
7. Determine whether animation is required.
8. Generate using established art direction.
9. Compare the result mentally against the existing asset bible.
10. Reject or regenerate obvious style drift.

Do not reinvent the art direction for each prompt.

## Prompt construction

When invoking an image generator, describe:

- exact asset;
- gameplay role;
- side-view orientation;
- approximate scale;
- art style;
- palette;
- lighting;
- material;
- silhouette requirements;
- background/transparency requirement;
- animation/frame requirements when applicable;
- forbidden inconsistencies.

Example conceptual structure:

`[asset], for a premium PC 2D side-scrolling platformer, consistent high-resolution hand-painted pixel art, dark gothic fantasy, [shape/material], side view, [lighting], crisp silhouette, controlled detail, same scale and rendering style as supplied references, transparent background, no text, no UI, no perspective mismatch`

Do not blindly copy this sentence. Adapt it to the asset.

## Asset naming

When filenames are needed, use predictable names:

`category_subject_variant_state_frame`

Examples:

`enemy_imp_idle_01.png`

`enemy_imp_run_03.png`

`terrain_castle_platform_left.png`

`prop_castle_chain_long_01.png`

`pickup_soul_red_idle_01.png`

`vfx_fire_small_04.png`

`bg_hell_castle_far_01.png`

Use lowercase snake_case.

## Output expectations

When asked to **generate the asset**, generate the image rather than only describing it.

When asked for a **prompt**, return a production-ready image-generation prompt.

When asked for an **asset pack**, first establish shared visual parameters, then generate the requested assets using those parameters consistently.

When asked for **animation**, maintain strict frame-to-frame consistency.

When asked for a **level environment**, think in reusable production assets rather than creating only one beautiful screenshot.

## Consistency lock

Once the user approves an asset or reference as canonical, treat it as part of the visual bible.

Future assets must preserve its:

- rendering;
- palette;
- outline;
- proportions;
- material language;
- lighting logic;
- pixel density.

Do not introduce a noticeably different interpretation without explicit instruction.

## Quality rejection rules

Reject/regenerate an asset when it contains:

- inconsistent perspective;
- wrong world scale;
- blurry pseudo-pixel-art edges;
- malformed anatomy;
- accidental text;
- AI artifacts;
- excessive noise;
- inconsistent outline thickness;
- random lighting direction;
- mobile-game UI styling;
- unreadable silhouette;
- excessive bloom;
- unwanted background;
- clipped sprite parts;
- inconsistent animation anatomy;
- obvious tile seams;
- inconsistent pixel density.

A technically attractive asset is still wrong if it does not match the established game.

## Final principle

Never optimize an individual asset in isolation.

Optimize the **whole game's visual language**.

The goal is not to generate many pretty images.

The goal is to make hundreds of independently generated assets look like they were deliberately produced for one coherent PC platformer.
