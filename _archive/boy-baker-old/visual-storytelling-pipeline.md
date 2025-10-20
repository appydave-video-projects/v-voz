# Visual Storytelling Pipeline - Boy & Baker

## Pipeline Flow (ASCII Diagram)

```
IDEA (Compassion Story)
  │
  ▼
STORY + STYLE GUIDE
docs/script.md + docs/visual-styleguide.md
  │
  ▼
TIMESTAMP TRANSCRIPT ◄─────────────────────────┐
data/boy-baker.mp4.timestamps.txt            │
  │                                           │
  ▼                                           │
SHOTLIST (Updated Schema) ─────────────────────┤
data/boy-baker-shotlist.csv                   │
  │                                           │
  ▼                                           │
IMAGE & ANIMATION PROMPTS ─────────────────────┤
data/boy-baker-prompts-image.csv              │
data/boy-baker-prompts-animations.csv         │
  │                                           │
  ▼                                           │
UNIFIED DATA PROCESSOR ◄───────────────────────┘
tools/run-processor-debug.js
  │
  ▼
UNIFIED STORYLINE JSON
data/boy-baker-storyline.json (198KB)
  │
  ▼
REACT MICROAPP (Client Review)
[READY FOR DEVELOPMENT]
  │
  ▼
ANIMATED IMAGES (.mp4)
[IN PRODUCTION]
```

## Current File Status

### ✅ COMPLETED FILES:
- **IDEA**: Compassion story concept defined
- **STORY**: `docs/script.md` (core narrative)
- **STYLE GUIDE**: `docs/visual-styleguide.md` (1930s French village, characters, Studio Ghibli style)
- **TIMESTAMP TRANSCRIPT**: `data/boy-baker.mp4.timestamps.txt` (5.0KB) - 64 narrative segments with precise timing
- **SHOTLIST**: `data/boy-baker-shotlist.csv` (5.7KB) - Updated schema: `shot_no,setting,characters,visual_description,ambiance,establishing_shot,detail_shot`
- **IMAGE PROMPTS**: `data/boy-baker-prompts-image.csv` (43.2KB) - Schema: `processed,shot_no,variation_no,prompt`
- **ANIMATION PROMPTS**: `data/boy-baker-prompts-animations.csv` (7.2KB) - Schema: `shot_no,variation_no,prompt`
- **DATA PROCESSOR**: `tools/run-processor-debug.js` - Unifies all source files into single JSON
- **UNIFIED STORYLINE**: `data/boy-baker-storyline.json` (198KB) - Complete data structure for client review
- **ASSETS**: `assets/*.png` (existing character/scene images)

### 🔄 IN PRODUCTION:
- **REACT MICROAPP**: Client review interface (consumes unified JSON)
- **ANIMATED IMAGES**: Version 2 complete, undergoing refinement

### 📁 SUPPORTING FILES:
- `docs/visual-shotlist.md` - Human-readable shot descriptions
- `docs/visual-shotdeck.md` - Detailed production notes
- `---prompt.md` - Original prompt guidelines
- `script-v2.txt` - Alternative script version

## Data Schema Evolution

### Key Improvements:
- **Consistent Naming**: All files use `shot_no` and `variation_no` for cross-referencing
- **Snake Case Convention**: `setting`, `ambiance`, `establishing_shot`, `detail_shot`
- **Semantic Clarity**: Field names accurately reflect content (e.g., `setting` for location+details, `ambiance` for lighting+mood)
- **Unified Structure**: Single JSON contains all timestamps, shots, prompts, and metadata

## Pipeline Completion: ~90%

All foundational elements and data processing complete. Currently developing client review interface and finalizing animated video output.

## Next Steps:
1. **React Microapp Development** - Build client review interface
2. **Animation Production** - Generate final .mp4 videos
3. **Quality Assurance** - Client feedback and refinement cycle

The unified data structure enables rapid iteration and seamless handoff between creative and technical phases.