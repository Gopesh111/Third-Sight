# Third Sight – Assistive Multimodal AI System

Third Sight is a **multimodal AI assistant** designed to help users—especially persons with disabilities—interact with their environment using **vision, speech, and gestures**.
The system combines **computer vision, large language models, and neural audio pipelines** to enable real-time, hands-free interaction.

This project focuses on **agentic AI workflows**, real-time perception, and accessibility-driven design.

---

## Problem Statement

Many assistive systems rely on a single modality (only voice or only vision), which limits usability in real-world environments.
Users with visual, speech, or motor impairments require an **adaptive system** that can understand **intent**, reason over **multiple inputs**, and respond naturally.

Third Sight addresses this by integrating:
- Vision-based perception
- Gesture-based interaction
- Voice-driven reasoning and feedback

---

## Key Capabilities

- Multimodal reasoning using LLMs
- Real-time object detection and gesture recognition
- Hands-free and accessibility-focused interaction
- Agent-based task execution using tool selection
- Low-latency audio feedback loop

---

## System Overview

User Input (Voice / Gesture / Visual Context)
↓
Agentic AI Brain
↓
Tool Selection & Reasoning
↓
Vision / Speech / Gesture Modules
↓
Audio Feedback to User


---

## Core Components

### 1. Multimodal Reasoning & Agentic Behavior

At the core of Third Sight is an autonomous **AI Brain** that manages tasks based on user intent.

- Uses **Llama-3** to interpret user queries
- Determines whether the request requires:
  - Visual context
  - Gesture input
  - Clipboard or screen data
- Dynamically triggers tools such as:
  - Webcam frame capture
  - Screenshot analysis
  - Clipboard reading
- Sends visual data to **Gemini 1.5 Flash** for high-level semantic understanding

This design demonstrates **agentic workflows**, tool usage, and reasoning-based orchestration across models.

---

### 2. Real-Time Computer Vision (Edge-Ready)

Third Sight includes two optimized vision pipelines designed for real-time performance.

#### Object Perception
- Uses **YOLOv8** for object detection
- Identifies items in the user’s environment
- Optimized using frame-skipping logic for low latency
- Suitable for edge and real-time scenarios

#### Gesture-Based UI
- Built using **MediaPipe**
- Applies custom **Euclidean distance geometry**
- Recognizes hand gestures for:
  - Non-verbal commands
  - Accessibility control
  - Interaction for mute users

---

### 3. Neural Audio Pipeline

To ensure smooth and natural interaction, the system uses a **split-audio architecture**.

- **Speech-to-Text**
  - Uses **Faster-Whisper**
  - Runs locally for privacy-focused transcription

- **Text-to-Speech**
  - Uses **Amazon Polly (Neural Engine)**
  - Produces natural, human-like voice output

- Multi-threading is used so that:
  - Vision processing does not block audio response
  - User experience remains real-time and responsive

---

## Tech Stack

**Languages & Frameworks**
- Python
- TensorFlow
- PyTorch

**Computer Vision**
- YOLOv8
- OpenCV
- MediaPipe

**AI & Reasoning**
- Llama-3
- Gemini 1.5 Flash

**Audio Processing**
- Faster-Whisper
- Amazon Polly (Neural TTS)

**System Design**
- Multi-threading
- Agent-based orchestration

---

## Accessibility & Use Cases

- Assistive AI for visually impaired users
- Gesture-based interaction for mute users
- Hands-free environmental awareness
- Smart human-computer interaction
- AI-powered accessibility research

---



## Future Improvements

- Support for additional gesture vocabularies
- On-device deployment optimization
- Multilingual speech support
- Integration with AR devices
- Expanded domain-specific agents

---



