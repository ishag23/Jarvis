# Jarvis-Style Desktop Automation 🎙️

A Python-based desktop automation project that detects a **double clap through the microphone** and triggers a Jarvis-style welcome experience.

The project can:

* 🎙️ Detect double-clap gestures using the microphone
* 🎵 Open and control Spotify
* 🌐 Open Chrome windows
* 🤖 Launch Claude and other configured web applications
* 🗣️ Generate a personalized welcome message using ElevenLabs
* ⚙️ Automatically select a working microphone when the default device is silent
* 🔧 Provide configurable audio detection and automation settings

## Tech Stack

* Python
* SoundDevice
* ElevenLabs API
* Chrome automation
* Spotify
* python-dotenv

## How It Works

The application continuously listens to the microphone and detects significant audio spikes. When two claps are detected within the configured time window, it triggers the Jarvis-style desktop workflow.

Configuration such as clap sensitivity, cooldown time, microphone selection, ElevenLabs voice, and URLs can be customized through environment variables and constants in `jarvis.py`.

## Setup

```bash
python -m pip install -r requirements.txt
```

Create a `.env` file and add your ElevenLabs credentials:

```env
ELEVENLABS_API_KEY=your_key_here
ELEVENLABS_VOICE_ID=your_voice_id_here
```

Then run:

```bash
python jarvis.py
```

## Configuration

The project supports configuration for:

* Clap detection sensitivity
* Microphone/input device
* Detection cooldown
* Audio sample rate
* ElevenLabs voice and model
* Welcome audio caching
* Chrome window size and URLs

See the project README for detailed configuration and troubleshooting instructions.
