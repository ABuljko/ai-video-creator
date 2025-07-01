# 🎬 AI Video Creator

## 🚀 Overview

**AI Video Creator** is a fully automated pipeline that generates short, high-quality narrated videos based on themed AI-generated stories. By combining cutting-edge models for text, image, and audio generation, this project delivers cinematic video experiences using only prompts and local compute.

## ✨ Features

- 🎭 **Story Generation**  
  Uses **Mistral-7B** to craft compelling, structured short stories (6 sentences each) based on randomly selected themes like *Dark Fantasy* or *Medieval Adventure*.

- 🖼️ **Image Generation**  
  Generates vivid, high-resolution scene visuals with **Stable Diffusion** for each line of the story.

- 🗣️ **Voice Narration**  
  Converts text to expressive speech using **Bark**, providing lifelike storytelling voices with emotional tone.

- 🌌 **Ambient Sound & Music**  
  Adds thematic **ambient sound effects** per scene and **background music** throughout the video using **Stable Audio Open**.

- 🎞️ **Video Assembly**  
  Merges scenes, narration, subtitles, and sound using **MoviePy**, producing two cinematic 30-second videos per execution.

## 🛠️ Requirements

- Python 3.10+
- CUDA-enabled GPU for acceleration
- Required models:
  - Mistral-7B (LLM for storytelling)
  - Stable Diffusion (image generation)
  - Bark (narration)
  - Stable Audio Open (sound effects & music)
- Python dependencies:
  - `torch`, `transformers`, `diffusers`, `moviepy`, `torchaudio`, `numpy`, etc.

> ℹ️ All models run locally. Ensure enough VRAM and disk space is available.

## ▶️ How to Run

1. Clone the repository and navigate to the project directory.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Download required models and place them in appropriate cache directories (or configure environment variables).
4. Run the notebook `AI_VIDEO_CREATOR.ipynb` or convert it to a Python script:
   ```bash
   jupyter notebook AI_VIDEO_CREATOR.ipynb
   # or
   python AI_VIDEO_CREATOR.py
   ```
5. Output videos will be saved in the `output/` directory.

## 🎥 Output

Each run produces **two unique MP4 videos** featuring:

- 📽️ Title screen
- 🖼️ 6 scene images (5 seconds each)
- 🗣️ Narration synced with subtitles
- 🌌 Scene-specific ambient SFX
- 🎶 Background music

> Total duration per video: **~30 seconds**

## 🙏 Credits

- 🤗 [HuggingFace Transformers](https://huggingface.co)
- 🎨 [Stability AI - Stable Diffusion](https://stability.ai)
- 🗣️ [Suno AI - Bark TTS](https://github.com/suno-ai/bark)
- 🔊 [Stability AI - Stable Audio Open](https://stability.ai)
- 🎞️ [MoviePy](https://zulko.github.io/moviepy/)

---

> Created with ❤️ using the power of local AI models and a bit of cinematic magic.
