# ComfyUI on Amazon SageMaker AI Studio - Global Version

## Project Information

**Author:** Hyunsoo Kim  
**Position:** Senior GenAI Specialist SA at AWS  
**Version:** Global English Version  
**Last Updated:** August 2025

## Project Overview

This repository provides a comprehensive guide for installing and running ComfyUI on Amazon SageMaker AI Studio. The project has been fully translated from Korean to English to serve a global audience.

## Key Features

- **Complete English Documentation**: All Korean comments, explanations, and documentation have been translated to English
- **SageMaker Integration**: Optimized for AWS SageMaker AI Studio environment
- **Automated Setup**: Streamlined installation process with minimal manual intervention
- **Professional Workflows**: Pre-configured workflows for product image generation
- **GPU Optimization**: Configured for GPU-enabled instances (recommended: ml.g5.2xlarge)

## Repository Structure

```
comfyui_on_SageMakerAI/
├── README.md                    # Main documentation (English)
├── ComfyUI_ModelPrep.ipynb     # Environment setup and model preparation
├── ComfyUI_Start.ipynb         # Server startup and access instructions
├── workflow_temp/              # Pre-configured workflow examples
├── input_img/                  # Sample images for workflow testing
├── img/                        # Documentation screenshots
└── PROJECT_INFO.md             # This file
```

## What's New in Global Version

1. **Language Conversion**: All Korean text converted to English
2. **Enhanced Documentation**: Improved explanations for international users
3. **Code Comments**: All code comments translated to English
4. **User Interface**: Instructions updated for English-speaking users
5. **Author Attribution**: Updated with proper author information

## Technical Requirements

- **Instance Type**: ml.g5.2xlarge (recommended)
- **Storage**: Minimum 100GB for model storage
- **Python**: 3.8+ with GPU support
- **CUDA**: Compatible GPU drivers

## Quick Start

1. Launch SageMaker AI Studio with GPU-enabled instance
2. Clone this repository
3. Run `ComfyUI_ModelPrep.ipynb` to set up environment
4. Run `ComfyUI_Start.ipynb` to start the server
5. Access ComfyUI through the provided proxy URL

## Support

For technical support or questions about this implementation, please refer to the detailed documentation in the README.md file.

## License

This project follows the same license terms as the original ComfyUI project.

---

**Note**: This is the global English version of the original Korean repository, adapted for international users while maintaining all original functionality.
