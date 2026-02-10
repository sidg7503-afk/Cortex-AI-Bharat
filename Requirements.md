# Requirements Specification for Cortex AI
**Version:** 1.0
**Status:** Draft

## 1. User Interaction
* **WHEN** the student uploads a physics diagram image **THE SYSTEM SHALL** use Optical Character Recognition (OCR) to extract visual elements and text labels.
* **WHEN** the student asks a question in Hindi/Hinglish **THE SYSTEM SHALL** detect the language and respond in the same dialect using NLP translation layers.
* **WHEN** the student requests a "Lecture" **THE SYSTEM SHALL** generate a structured summary with LaTeX-formatted equations.

## 2. System Architecture
* **WHEN** the internet bandwidth is below 500Kbps **THE SYSTEM SHALL** switch to "Text-Only Mode" to preserve data.
* **WHEN** a query is flagged as "Complex Reasoning" (e.g., Rotational Dynamics) **THE SYSTEM SHALL** route the prompt to the DeepSeek/Reasoning model agent.
* **WHEN** the user completes a quiz **THE SYSTEM SHALL** update the local XP database and unlock the next difficulty tier.

## 3. Compliance & Safety
* **WHEN** the user inputs non-educational queries **THE SYSTEM SHALL** refuse the response and redirect to the syllabus.
