# Copilot Instructions for Player Re-Identification Project

<!-- Use this file to provide workspace-specific custom instructions to Copilot. For more details, visit https://code.visualstudio.com/docs/copilot/copilot-customization#_use-a-githubcopilotinstructionsmd-file -->

## Project Overview
This is a computer vision project for player re-identification in sports footage. The project uses:
- Python 3.8+
- OpenCV for video processing
- PyTorch for deep learning
- Ultralytics YOLOv11 for object detection
- scikit-learn for clustering and similarity matching

## Code Style Guidelines
- Follow PEP 8 conventions
- Use type hints for function parameters and return values
- Include docstrings for all classes and functions
- Use meaningful variable names that describe the purpose
- Add comments for complex algorithms and business logic

## Architecture Guidelines
- Keep detection, tracking, and re-identification as separate modules
- Use configuration files for hyperparameters
- Implement error handling for file I/O and model loading
- Make the code modular and testable
- Follow SOLID principles

## Domain-Specific Context
- Players can go out of frame and reappear
- Same player should maintain the same ID throughout the video
- Focus on robustness and real-time performance
- Consider sports-specific scenarios (occlusion, similar uniforms, etc.)
