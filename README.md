# Player Re-Identification System

A real-time player tracking and re-identification system for sports footage using YOLOv11 and computer vision techniques.

##  Overview

This system tackles the challenge of maintaining consistent player identities in sports videos, even when players temporarily leave and re-enter the frame. The solution combines object detection, feature extraction, and intelligent tracking algorithms to achieve robust player re-identification.

##  Challenge Objective

- **Input**: 15-second sports video (`data/15sec_input_720p.mp4`)
- **Goal**: Maintain consistent player IDs when players go out of frame and reappear
- **Real-world application**: Player tracking during sports events with camera movement and occlusions

##  Quick Start

### Prerequisites
- Python 3.8+
- CUDA-compatible GPU (recommended)
- 4GB+ RAM

### Installation

1. **Clone and navigate to the project:**
```bash
git clone https://github.com/Prathmesh-S27/sports-player-reidentification.git
cd sports-player-reidentification
```

2. **Install dependencies:**
```bash
pip install -r requirements.txt
```

3. **Download required files:**
```bash
python download_model.py
```

4. **Run the system:**
```bash
python -m src.main data/your_video.mp4 --save-comparison
```

##  Performance Results

**Current Performance on Challenge Video:**
-  **40% Re-identification Success Rate**: 4 out of 10 disappeared players successfully re-identified
-  **Perfect ID Stability**: When re-identification works, players maintain exact same ID
-  **Real-time Processing**: ~9-15 FPS on standard hardware
-  **Robust Feature Matching**: High confidence scores (0.96-0.99) for successful matches

##  Project Structure

```
sports-player-reidentification/
 src/                          # Core source code
    main.py                   # Main pipeline orchestrator
    detector.py               # YOLOv11 player detection
    feature_extractor.py      # Multi-modal feature extraction
    tracker.py                # Player tracking & re-identification
    visualizer.py             # Video annotation and visualization
    config.py                 # System configuration
 data/                         # Input videos (add your own)
 models/                       # AI models (auto-downloaded)
 output/                       # Generated results
 requirements.txt              # Python dependencies
 setup.py                     # Automated setup script
 download_model.py            # Model download utility
 test_system.py               # System validation tests
 README.md                    # This file
 TECHNICAL_REPORT.md          # Detailed technical analysis
```

##  Configuration

Key parameters can be adjusted in `src/config.py`:

```python
# Re-identification sensitivity
REID_CONFIG = {
    "similarity_threshold": 0.58,  # Lower = more lenient matching
    "memory_size": 150,           # Feature history length
}
```

##  Output Examples

The system generates two types of output:

1. **Tracked Video** (`*_tracked.mp4`):
   - Original video with colored bounding boxes
   - Unique ID numbers for each player

2. **Comparison Video** (`*_comparison.mp4`):
   - Side-by-side: Original vs Tracked
   - Perfect for analyzing system performance

##  Technical Details

See `TECHNICAL_REPORT.md` for detailed analysis including:
- Algorithm design decisions
- Feature extraction methodology
- Re-identification pipeline details
- Performance optimization strategies

##  License

This project is created for the player re-identification challenge assessment.

---

**Ready to track some players?** 
