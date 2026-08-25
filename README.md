# AI Film Skills

Three reusable skills for AI film prompt development:

- `acting`: designs observable character performance, including objectives, tactics, beats, subtext, eye life, reactions, and voice consistency.
- `cinedance-higgsfield`: converts a scene into a production-ready English prompt for Seedance 2.0 and Higgsfield Seedance.
- `lira-image-prompts`: writes and improves prompts for AI image generation and image editing workflows.

## Install

Copy the desired skill directory from `skills/` into your Codex skills directory:

```bash
cp -R skills/acting ~/.codex/skills/
cp -R skills/cinedance-higgsfield ~/.codex/skills/
cp -R skills/lira-image-prompts ~/.codex/skills/
```

Restart Codex or begin a new turn after installation so the skills can be discovered.

## Use

Invoke a skill explicitly in your request:

```text
Use $acting to design the performance for this dialogue scene.
Use $cinedance-higgsfield to turn this scene into a Seedance 2.0 prompt.
Use $lira-image-prompts to optimize this image prompt for Soul Cinema.
```

The skills may also activate automatically when a request matches their descriptions.

## Contents

```text
skills/
├── acting/
│   └── SKILL.md
├── cinedance-higgsfield/
│   └── SKILL.md
└── lira-image-prompts/
    └── SKILL.md
```

## Note

`lira-image-prompts` refers to additional `references/*.md` material that was not included in the original source package. Its core instructions remain available in `SKILL.md`, but those optional extended references are not part of this repository.
