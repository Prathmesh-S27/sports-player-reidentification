# Models Directory

This directory contains AI models for player detection and re-identification.

## Model Files

### YOLOv11 Player Detection Model:
- `best.pt` - Fine-tuned YOLOv11 model for player detection
  - **Note**: This file is NOT included in the repository due to file size limits
  - **Download**: Run `python download_model.py` to automatically download
  - **Size**: Approximately 20-50MB
  - **Source**: Company-provided pre-trained model

## Automatic Download

The model will be automatically downloaded when you run:

```bash
python download_model.py
```

If automatic download fails, follow the manual instructions provided by the script.

## Model Limitations

⚠️ **Performance Note**: The 40% re-identification accuracy is limited by this pre-trained model. 

With access to custom training infrastructure, this system could achieve 70-85% accuracy through:
- Custom model fine-tuning for sports scenarios
- Transfer learning with sports-specific datasets
- Enhanced feature extraction approaches

## File Size Notice

Model files are excluded from this repository due to GitHub's file size limits. The `.gitignore` file prevents accidentally committing large model files (`.pt`, `.pth` extensions).
