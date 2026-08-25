# AI Film Skills

Six reusable skills for AI film prompt development:

- `acting`: designs observable character performance, including objectives, tactics, beats, subtext, eye life, reactions, and voice consistency.
- `ai-cinematic-shot-designer`: designs camera language, framing, lenses, camera movement, blocking, transitions, and coherent shot lists.
- `cinedance-higgsfield`: converts a scene into a production-ready English prompt for Seedance 2.0 and Higgsfield Seedance.
- `lira-image-prompts`: writes and improves prompts for AI image generation and image editing workflows.
- `write-ai-video-lighting-prompts`: creates physically coherent lighting prompts and fixes common AI-video lighting failures.
- `write-fight-scene-prompts`: creates production-ready fight-scene prompts with clear choreography, impact, camera control, and continuity.

## Install

Copy the desired skill directory from `skills/` into your Codex skills directory:

```bash
cp -R skills/acting ~/.codex/skills/
cp -R skills/ai-cinematic-shot-designer ~/.codex/skills/
cp -R skills/cinedance-higgsfield ~/.codex/skills/
cp -R skills/lira-image-prompts ~/.codex/skills/
cp -R skills/write-ai-video-lighting-prompts ~/.codex/skills/
cp -R skills/write-fight-scene-prompts ~/.codex/skills/
```

Restart Codex or begin a new turn after installation so the skills can be discovered.

## Use

Invoke a skill explicitly in your request:

```text
Use $acting to design the performance for this dialogue scene.
Use $ai-cinematic-shot-designer to design the camera language for this scene.
Use $cinedance-higgsfield to turn this scene into a Seedance 2.0 prompt.
Use $lira-image-prompts to optimize this image prompt for Soul Cinema.
Use $write-ai-video-lighting-prompts to design the lighting for this video shot.
Use $write-fight-scene-prompts to write a controlled fight-scene prompt.
```

The skills may also activate automatically when a request matches their descriptions.

## Contents

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
