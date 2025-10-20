# The Point

Created: 2025-10-08

## Project Structure

This project follows the unified storyline structure:

- **assets/**: Visual assets (characters, artifacts, scenes)
  - **characters/**: Character design images
  - **artifacts/**: Props and artifact references
  - **scenes/**: Generated scene images (UUID-based naming)
- **data/**: Working data files
  - **storyline.json**: Main storyline data structure
  - **styleguide.md**: Visual style guide
  - **source/**: Transcripts and source data (words.json, beats.json, etc.)
- **docs/**: Creative documentation (notes, etc.)
- **video/**: Video assets (source files, generated animations, etc.)

## File Naming Conventions

### Images (assets/scenes/)
Pattern: `{beat:2d}-{concept:1d}-{variation:1d}-{label}-{uuid:8}.{ext}`

Example: `01-1-1-establishing-a3f7b2c9.png`
- `01` = Beat number (2 digits)
- `1` = Concept number within beat (1-9)
- `1` = Variation number (1-9)
- `establishing` = Semantic label
- `a3f7b2c9` = 8-digit UUID (permanent file identity)

### Videos (video/animations/)
Pattern: `{beat:2d}-{concept:1d}-{variation:1d}-{video:1d}-{label}-{uuid:8}.mp4`

Example: `01-1-1-1-dolly-in-f6d3e8a1.mp4`
- `01` = Beat number
- `1` = Concept number
- `1` = Variation number
- `1` = Animation/video number (1-9)
- `dolly-in` = Animation type/label
- `f6d3e8a1` = 8-digit UUID (permanent file identity)

### Why UUIDs?
- **UUID = permanent identity**: Never changes, survives reordering
- **Prefix = position hint**: Shows approximate location in sequence
- **Enables flexible reordering**: Move concepts in UI without renaming files
- **Human-friendly browsing**: Position prefix makes filesystem navigation easy

For detailed UUID strategy, see: `storyline-app/docs/requirements-epic-5.3-project-structure.md`

## Getting Started

1. Add source video to `video/source/`
2. Run Whisper transcription (instructions TBD)
3. Edit `data/styleguide.md` with your visual style
4. Open storyline app and create beats from transcript

## Next Steps

- [ ] Add source video/audio
- [ ] Create transcript with Whisper
- [ ] Define visual style guide
- [ ] Create beats from transcript
- [ ] Generate visual concepts
- [ ] Create image variations
