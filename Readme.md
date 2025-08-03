# Research text to speech technologies from srt file

This notebook implements a pipeline for converting subtitle files (SRT format) to natural-sounding speech audio. It utilizes the TTS library to generate speech from text segments and combines them with proper timing to match the original subtitle timing.

## Overview

The notebook provides functionality to:

1. Parse SRT subtitle files
2. Generate speech for each subtitle segment using various TTS models
3. Adjust speech speed to match subtitle timing
4. Combine all segments into a continuous audio file

This approach is useful for creating voiceovers for videos, generating audio versions of subtitled content, or creating accessible versions of media

## Dependencies

The implementation relies on the following libraries:

-   `srt`: For parsing SRT subtitle files
-   `torch`: PyTorch for deep learning operations
-   `coqui-tts`: Text-to-Speech library for generating speech
-   `pydub`: For audio processing and manipulation
-   `IPython.display`: For audio playback in the notebook

## Key Components

### SRT Parsing

The notebook provides functionality to parse SRT subtitle files, extracting timing information and text content.

### Text-to-Speech Generation

Multiple TTS models are supported:

-   English TTS model
-   Vietnamese TTS model
-   Multilingual model with support for different voices

### Audio Processing

The system intelligently:

-   Adjusts speech speed to match subtitle timing
-   Handles silences between subtitles
-   Combines multiple audio segments into a continuous track

# Experimentation Guidelines

This section provides guidelines on how to experiment with and extend this notebook for your text-to-speech projects.

1. **Setup Environment**:

    - Create your virtual environment: `python3 -m venv venv`
    - Install dependencies: `pip3 install -r requirements.txt`

2. **Prepare Your SRT Files**:

    - Place your SRT files in the `srt/` directory
    - Ensure they're properly formatted and encoded (UTF-8 recommended)

3. **Basic Usage**:
    - Run the example code cell to convert an SRT file to audio:
        ```python
        create_audio_from_srt("srt/your_file.srt", "output_filename.wav")
        ```
    - Listen to the generated audio to evaluate quality
