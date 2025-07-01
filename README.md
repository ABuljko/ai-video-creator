# AI Video Creator

## Overview

This project uses AI models to automatically generate short, narrated videos with thematic content. It combines story generation, image synthesis, voice narration, and audio mixing into a single pipeline.

## Features

- **Story Generation**: Uses Mistral-7B to create structured, themed stories.
- **Image Generation**: Stable Diffusion generates high-quality scene visuals.
- **Narration**: Bark provides expressive text-to-speech narration.
- **Ambient Sound**: Stable Audio Open generates theme-specific sound effects and music.
- **Video Compilation**: MoviePy combines all assets into synchronized videos with subtitles and transitions.

## Requirements

- Python 3.10+
- CUDA-compatible GPU (for local inference)
- Models: Mistral-7B, Stable Diffusion, Bark, Stable Audio Open
- Dependencies: torch, moviepy, transformers, diffusers, etc.

## How to Run

1. Install the required dependencies (see `requirements.txt` or the notebook).
2. Run the notebook or convert it into a script.
3. The system generates two 30-second themed videos with narration, ambient sound, and synchronized visuals.

## Output

- 2 MP4 videos with:
  - Title screen
  - 6 image scenes (5 seconds each)
  - Expressive narration
  - Ambient SFX per scene
  - Background music

## Credits

- [HuggingFace Transformers](https://huggingface.co)
- [Stability AI - Stable Diffusion](https://stability.ai)
- [Suno AI - Bark TTS](https://github.com/suno-ai/bark)
- [MoviePy](https://zulko.github.io/moviepy/)

