# AI Film Skills

A collection of reusable Codex skills for AI filmmaking and video production, covering character performance, cinematic camera language, Seedance video prompts, image prompts, video lighting, and fight-scene design.

## Skill Guide

### [`acting`](skills/acting/SKILL.md) — Character Performance and Behavior

**[Use Cases]** Design character acting profiles, dialogue scenes, conflict scenes, emotional close-ups, and ensemble reactions for AI video. It also helps fix stiff expressions, dead eyes, mechanical gestures, and performances that merely display emotions.

**[How to Use]** Invoke `$acting` and provide the character's identity, relationships, current situation, and what the character wants from another person in the scene. You may also include dialogue, shot duration, reference tags, or an existing prompt.

**[Output]** An English acting paragraph ready to insert into a video prompt. Depending on the request, it can also produce a master acting profile, a scene-specific performance adaptation, a locked voice prompt, or a performance diagnosis.

### [`ai-cinematic-shot-designer`](skills/ai-cinematic-shot-designer/SKILL.md) — Cinematic Shot Prompts

**[Use Cases]** Design or improve shot angles, framing, camera height, perspective, lens behavior, camera movement, blocking, transitions, and coherent shot lists. It is also useful for fixing confused viewpoints, unmotivated camera movement, and unclear spatial relationships.

**[How to Use]** Invoke `$ai-cinematic-shot-designer` and provide the scene, narrative purpose, subject positions, shot duration, and desired rhythm. You may attach reference images, an existing prompt, or specific camera requirements.

**[Output]** A cinematic camera-language prompt for AI video models or a structured shot list. The result may include composition, optics, camera paths, blocking, timed beats, transitions, and continuity checks.

### [`cinedance-higgsfield`](skills/cinedance-higgsfield/SKILL.md) — Seedance and Higgsfield Video Prompts

**[Use Cases]** Convert scene ideas, script excerpts, or existing prompts into executable prompts for Seedance 2.0 and Higgsfield Seedance. It supports continuous takes, dialogue scenes, multi-character blocking, action shots, and controlled multi-shot sequences.

**[How to Use]** Invoke `$cinedance-higgsfield` and provide the current shot's event, active characters, and duration. When using references, explain what each `@tag` represents and add any dialogue, lighting, or camera-movement requirements.

**[Output]** A structured English video-generation prompt that may include active references, first-frame occupancy, spatial blocking, gaze lines, optics, camera behavior, action timing, physics, lighting, audio, and targeted failure-prevention locks.

### [`lira-image-prompts`](skills/lira-image-prompts/SKILL.md) — AI Image Prompt Optimization

**[Use Cases]** Write, improve, or diagnose prompts for characters, environments, props, and image edits across Higgsfield Soul, Soul Cinema, Nano Banana Pro, Seedream, GPT Image, and related image workflows.

**[How to Use]** Invoke `$lira-image-prompts`, state whether the task is a new generation or an edit, and provide the target model, subject, environment, composition, lighting, palette, and elements that must change or remain unchanged. Include the source image for editing tasks.

**[Output]** A recommended model route, a production-ready English image prompt, and relevant platform-setting notes. Image-editing tasks receive explicit `CHANGE` and `PRESERVE EXACTLY` instructions.

### [`write-ai-video-lighting-prompts`](skills/write-ai-video-lighting-prompts/SKILL.md) — AI Video Lighting Prompts

**[Use Cases]** Design cinematic lighting with clear sources, direction, falloff, and spatial depth; maintain lighting continuity across shots; or fix flat illumination, sourceless light, exposure jumps, flicker, inconsistent shadows, and excessive glow.

**[How to Use]** Invoke `$write-ai-video-lighting-prompts` and provide the scene, time of day, weather, subject positions, practical or natural light sources, and intended mood. For troubleshooting, include the current prompt, a reference frame, and the observed lighting failure.

**[Output]** A lighting-control block ready for an AI video prompt, covering source motivation, direction, intensity, color temperature, subject-background separation, exposure strategy, atmospheric media, continuity locks, and targeted local constraints.

### [`write-fight-scene-prompts`](skills/write-fight-scene-prompts/SKILL.md) — AI Film Fight-Scene Prompts

**[Use Cases]** Design hand-to-hand combat, chases, weapon fights, group battles, mech combat, creature fights, and battlefield action. It also helps fix confused choreography, teleporting characters, body intersections, changing weapons, weak impacts, and uncontrolled camera shake.

**[How to Use]** Invoke `$write-fight-scene-prompts` and provide the fighters, location, duration, combat style, weapons, intended outcome, and key actions. You may also include character references, camera requirements, an existing prompt, or specific failures to correct.

**[Output]** A production-ready English fight-scene prompt that may include spatial relationships, action beats, attack-and-defense causality, impact physics, camera choreography, character and weapon consistency, environmental interaction, continuity constraints, and silent quality checks.

## Install

Copy the desired skill directories into your Codex skills directory:

```bash
cp -R skills/acting ~/.codex/skills/
cp -R skills/ai-cinematic-shot-designer ~/.codex/skills/
cp -R skills/cinedance-higgsfield ~/.codex/skills/
cp -R skills/lira-image-prompts ~/.codex/skills/
cp -R skills/write-ai-video-lighting-prompts ~/.codex/skills/
cp -R skills/write-fight-scene-prompts ~/.codex/skills/
```

Restart Codex or begin a new conversation turn after installation so the skills can be rediscovered.

## Usage Examples

Invoke a skill explicitly with `$skill-name`:

```text
Use $acting to design the performance for this dialogue scene.
Use $ai-cinematic-shot-designer to design the camera language for this scene.
Use $cinedance-higgsfield to turn this scene into a Seedance 2.0 prompt.
Use $lira-image-prompts to optimize this image prompt for Soul Cinema.
Use $write-ai-video-lighting-prompts to design the lighting for this video shot.
Use $write-fight-scene-prompts to write a controlled fight-scene prompt.
```

Codex may also invoke a skill automatically when a request matches its description.

## Repository Structure

```text
skills/
├── acting/
│   └── SKILL.md
├── ai-cinematic-shot-designer/
│   ├── agents/
│   ├── references/
│   └── SKILL.md
├── cinedance-higgsfield/
│   └── SKILL.md
├── lira-image-prompts/
│   └── SKILL.md
├── write-ai-video-lighting-prompts/
│   ├── agents/
│   ├── references/
│   └── SKILL.md
└── write-fight-scene-prompts/
    ├── agents/
    └── SKILL.md
```

## Note

`lira-image-prompts` refers to additional `references/*.md` material that was not included in the original source package. Its core instructions remain available in `SKILL.md`, but those optional extended references are not part of this repository.
