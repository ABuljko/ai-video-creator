# 🎬 AI Video Creator

An autonomous AI storytelling system that generates narrated short videos with expressive voices, themed ambient sound effects, background music, and high-quality scene visuals. Ideal for creative, educational, and entertainment use cases.

---

## ✨ Overview

This project automatically generates **two themed cinematic videos per run**, using a combination of powerful open-source models. It combines text, image, and audio generation into a smooth video pipeline.

### 🧠 Core Components

- **Mistral-7B** – Structured story generation (6-sentence plot per theme)
- **Stable Diffusion** – High-resolution scene image generation
- **Bark** – Expressive text-to-speech narration
- **Stable Audio Open** – Ambient sound effects & background music
- **MoviePy** – Final video assembly with transitions and overlays

---

## 🎥 Features

- ✅ Generates two unique **30-second** MP4 videos per execution
- ✅ Supports various **themes** like *Dark Fantasy*, *Medieval*, etc.
- ✅ Scene-by-scene synchronization:
  - 🖼️ Image
  - 🗣️ Narration
  - 🌌 Ambient SFX
  - 📝 Subtitle
- ✅ 🎵 Title screen with background music
- ✅ ✨ Smooth transitions, stylized subtitles, expressive voice
- ✅ 💻 Works offline (with local models) or in **Google Colab** (T4/A100 GPU)

---

## ⚙️ Requirements

- **Python**: 3.9+
- **GPU**: NVIDIA GPU with CUDA 12.1 support  
  *(recommended: T4, A100, or equivalent – ~16GB VRAM preferred)*

---

## 🧩 Python Libraries

Install all dependencies using pip or Colab:

```bash
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
pip uninstall -y sentence-transformers
pip install --quiet git+https://github.com/Stability-AI/stable-audio-tools.git
pip install --upgrade --quiet --no-deps protobuf==5.29.1 einops
pip install transformers==4.41.2
pip install diffusers==0.27.2
pip install bitsandbytes==0.43.1
pip install accelerate==0.30.1
pip install moviepy==1.0.3
pip install soundfile==0.12.1
pip install pydub==0.25.1
pip install git+https://github.com/suno-ai/bark.git
pip install peft==0.9.0
pip install huggingface_hub==0.25.2
apt-get install -y imagemagick
apt-get install -y fonts-dejavu-core
pip install numpy==1.26.4
```

---

## ▶️ How to Run

1. **Clone the repository** and navigate to the project folder:

   ```bash
   git clone https://github.com/your-username/AI_video_creator.git
   cd AI_video_creator
   ```

2. **Install all dependencies** (as shown above).

3. **Download models**:
   - Place Mistral, Stable Diffusion, and Bark models into your local cache
   - Optionally set environment variables like `HF_HOME`, `TORCH_HOME`, etc.

4. **Run the project**:

   ```bash
   jupyter notebook AI_VIDEO_CREATOR.ipynb
   # or convert to script:
   python AI_VIDEO_CREATOR.py
   ```

5. **Output location**:

   All generated files (videos, images, audio, logs) will be saved in the `output/` folder.

---

## 🗂️ Output Structure

```plaintext
output/
├── dark_fantasy_01.mp4
├── medieval_01.mp4
├── logs/
├── frames/
├── audio/
└── metadata/
```

Each video includes:

- 📽️ Title screen with background music
- 🖼️ 6 scene images (~5s each)
- 🗣️ Narration per sentence
- 🌌 Ambient sound effects per scene
- 📝 Subtitle overlays

🎬 **Total duration per video**: ~30 seconds

---

## 📌 Notes & Tips

- 💾 Ensure at least **15–20GB of free VRAM** and **disk space** for caching models and temporary files.
- 🌐 Most models are fully offline, but Stable Audio Open may need internet access in Colab.
- 🛠️ Use `HF_HOME`, `TRANSFORMERS_CACHE`, `TORCH_HOME`, etc., to manage model paths and avoid C: drive overload.
- 🎨 You can customize themes, narration style, or visual filters in `config.py` or main generation logic.

---

## 🙏 Credits

- 🤗 [Hugging Face Transformers](https://huggingface.co)
- 🎨 [Stability AI - Stable Diffusion](https://stability.ai)
- 🔊 [Stability AI - Stable Audio Open](https://stability.ai)
- 🗣️ [Suno AI - Bark TTS](https://github.com/suno-ai/bark)
- 🎞️ [MoviePy](https://zulko.github.io/moviepy/)
- 🧠 [Mistral-7B](https://mistral.ai)

