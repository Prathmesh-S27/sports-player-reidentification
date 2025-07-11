# Data Directory

This directory should contain your input video files for player re-identification.

## Required Files

### For Challenge Demo:
- `15sec_input_720p.mp4` - The 15-second challenge video
  - **Note**: This file is NOT included in the repository due to GitHub file size limits (>25MB)
  - **Source**: Obtain from the original challenge provider
  - **Size**: Approximately 30-40MB

### For Your Own Videos:
- Place any `.mp4`, `.avi`, or other video files here
- Supported formats: MP4, AVI, MOV, MKV

## Usage

```bash
# Run with challenge video (after placing it here)
python -m src.main data/15sec_input_720p.mp4 --save-comparison

# Run with your own video
python -m src.main data/your_video.mp4 --save-comparison
```

## File Size Notice

⚠️ **Large video files are excluded from this repository** due to GitHub's 25MB file size limit.

The `.gitignore` file is configured to ignore common video formats:
- `*.mp4`
- `*.avi` 
- `*.mov`
- `*.mkv`

This prevents accidentally committing large files to the repository.
