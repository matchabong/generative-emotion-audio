# generative-emotion-audio
# Facial Expression Sonification Prototype

A real-time interactive system that maps facial landmarks and emotional data to generative audio parameters. This project explores Human-Computer Interaction (HCI) by integrating computer vision APIs with the Max/MSP audio environment.

## 🔎 Project Overview
This prototype was designed to test the latency and creative potential of driving audio synthesis using live biometric data. It functions by capturing video input, analyzing facial expressions (Joy, Sadness, Anger) via a Face API, and converting that JSON data into MIDI/audio control signals within Max/MSP.

**Key Concept:** Transforming visual emotional data into an auditory experience ("Sonification").

## ⚙️ Technical Architecture
The system operates as a data pipeline:

1.  **Input:** Live webcam feed.
2.  **Processing:** Face API (External Service) detects landmarks and emotion probabilities.
3.  **Data Parsing:** JSON response is parsed and filtered.
4.  **Synthesis:** Data is routed into **Max/MSP** patches to control:
    * **Tempo/BPM:** Controlled by "Arousal" or active movement.
    * **Scale/Harmony:** Mapped to dominant emotion (e.g., Joy -> Major Scale).

## 🛠️ Tech Stack
* **Computer Vision:** Face API (REST/WebSocket integration)
* **Audio Synthesis:** Max/MSP (Cycling '74)
* **Data Format:** JSON

## 🚀 Features
* **Real-Time Mapping:** Low-latency translation of visual cues to audio events.
* **Generative Structure:** The music is not pre-recorded; it is generated live based on the user's current expression.

## 📝 Acknowledgements & Credits
This project focuses on **system integration** and **multimedia prototyping**.
* Core Max/MSP patches adapted from open-source structures by fdb.
* Modifications made to customize data parsing logic and audio output parameters.

## 🔮 Future Improvements
* Replace external API with a local Python/OpenCV script to reduce latency.
* Expand emotion mapping to include micro-expressions.
