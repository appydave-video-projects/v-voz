# v-voz Video Projects

VOZ client video projects using the Storyline workflow (script-first narrative-driven content).

## Final Assets Directory

The `final/` directory stores **publishable final videos** ready for distribution.

**Naming convention**: `{project-name}-v{version}.mp4` (lowercase-kebab-case)

**Examples**:
```
project-name/
└── final/
    ├── project-name-v1.mp4          # First version
    ├── project-name-v2.mp4          # Revised version
    └── project-name-short-v1.mp4    # Short variant
```

**Git tracking**: Files in `final/` are tracked (exception to video ignore rules).

**When to use**:
- ✅ Final client deliverables
- ✅ Multiple versions for client review
- ✅ Platform-specific exports
- ❌ NOT for work-in-progress renders

## Storyline Workflow

VOZ projects follow a **script-first approach**:

1. Script development (`docs/script.md`)
2. Beat breakdown (`data/source/beats.json`)
3. Visual concept generation (`data/storyline.json`)
4. Scene image creation (`assets/scenes/`)
5. Animation and final render

**Key files**:
- `data/storyline.json` - Single source of truth for narrative structure
- `data/styleguide.md` - Visual direction and tone
- `docs/script.md` - Full narrative script
- `assets/scenes/` - Generated scene images

**Naming convention for scenes**: `{shot}-{variation}-{type}-{label}-{uuid}.png`

Example: `01-1-1-establishing-f4595985.png`

---

Last updated: 2025-10-21
