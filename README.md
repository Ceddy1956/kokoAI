# kokoAI
## License & Attributions

The **Ember & Moss Sanctuary** application code, procedural 2D artwork, Web Audio synthesizer, and the **Koko** character are dedicated to the public domain under **CC0 1.0 Universal** (see `LICENSE`).

Core Features

Koko is a zero-dependency, single-file web application that merges procedural graphics and custom audio synthesis with a privacy-first, empathetic conversational UI.

Privacy-First State Management & Ethical Architecture

Engineered to prioritize user safety and emotional well-being, the application utilizes a bifurcated memory model to prevent traumatic feedback loops commonly found in conversational agents:

Local State Persistence: Non-sensitive user preferences (e.g., UI themes, routine configurations, benign identifiers) are securely stored via localStorage.

Session-Bound Context: Volatile data, including emotional disclosures and trauma-related themes, are strictly confined to temporary memory and programmatically wiped upon page reload.

Deterministic Safety Guardrails: A hardcoded interception layer (detectCrisisLanguage) preempts the standard AI processing pipeline. If self-harm or crisis language is detected, the application immediately drops character to surface the 988 Suicide & Crisis Lifeline.

Zero-Dependency Procedural Rendering Engine

High-Performance Canvas Loop: A custom HTML5 Canvas engine maintains a 60 FPS rendering cycle entirely without external game libraries or graphic dependencies.

Real-Time Environmental Simulation: Features procedural weather cycles (clear, rain, snow, storm), continuous day/night transitions, and physics-driven particle systems (e.g., wind drift on sky lanterns).

State-Driven Visuals: User interactions dynamically scale environment variables, such as fireIntensity, which mathematically alters flame rendering and particle emission rates.

Procedural Web Audio Synthesizer

Algorithmic Sound Generation: Operates entirely without static audio assets. All ambient audio is generated natively using the Web Audio API.

State-Reactive Audio Context: Utilizes white noise buffers and dynamic bandpass filters to synthesize wind, rain, and campfire crackles that map proportionally to the visual state of the environment.

Context-Aware Conversational Engine

Heuristic Narrative Tracking: Employs regex-based continuity checks (isLikelyKokoFollowUp) to parse conversational fragments, allowing the engine to maintain narrative threads across multiple discrete user inputs.

Therapeutic Framework Integration: Routes high-stress emotional domains (e.g., grief, burnout) through a programmed implementation of Hoppe's 6-stage active listening model (reflecting, clarifying, validating).

Scalable Dataset Integration: Architected to interface with a 120k+ combined NLP dataset (ESConv, EmpatheticDialogues, GoEmotions). Includes highly compressed Base64 GZIP and array fallbacks to maintain deep emotional reasoning capabilities in offline or lightweight environments.

Interactive Grounding & Wellness Mechanics

Actionable UI Elements: Integrates tangible self-care tracking (hydration, medication, stretching) and interactive character commands directly into the core loop.

Visual Grounding Exercises: Features a Safe Space overlay utilizing CSS/Canvas animations to guide users through the 5-4-3-2-1 anxiety reduction technique and box breathing.

Proactive Engagement System: An autonomous background timer monitors user activity; if idle, the application triggers gentle, non-intrusive prompts related to hydration, breathing, or previously saved interests.

Recent Architecture Updates

Volatile State Decoupling: Completely decoupled stressEvents and themesRaised from persistent storage to enforce strict session-only emotional memory boundaries.

Bounded Short-Term Memory: Implemented getRecentConversationContext() to maintain a rolling cache of the last 6 conversational turns, significantly reducing contextual hallucination and improving dialogue fluidity.

Dynamic Prompt Injection: Upgraded the chooseGentleQuestion logic to actively weave identified conversational themes into the response string, transitioning from generic active listening to context-specific validation.

Offline Data Compression: Embedded the EMNLP core dataset array and Base64 GZIP EmpatheticDialogues strings directly into the source file, eliminating external network dependencies for baseline emotional reasoning.

Dataset Credits & Acknowledgements

Koko's emotional reasoning and conversational routing are powered by several open-source academic datasets. The architecture utilizes these corpora to advance empathetic AI and structural active listening:

ESConv (Emotional Support Conversation): (Liu et al., 2021) - Provides the foundational structure for Koko's counseling-style empathy and problem-exploration framework.

EmpatheticDialogues: (Rashkin et al., 2019, Facebook AI Research) - Enables the engine to accurately recognize underlying emotional states and generate validating, context-appropriate responses.

DailyDialog: (Li et al., 2017, EMNLP) - Supplies high-quality human conversational pairs to manage natural, everyday small talk when the user is not in distress.

GoEmotions: (Demszky et al., 2020, Google Research) - Acts as the primary sensory engine for detecting and categorizing complex or mixed emotional signals across 27 distinct emotion categories.


This project includes locally embedded retrieval examples from the following research datasets, which remain subject to their respective academic licenses:
* **ESConv (Emotional Support Conversation):** Liu et al. (2021), *"Towards Emotional Support Dialog Systems"*, ACL. Licensed under [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/).
* **EmpatheticDialogues:** Rashkin et al. (2019), *"Towards Empathetic Open-domain Conversation Models"*, ACL.
* **DailyDialog:** Li et al. (2017), *"DailyDialog: A Manually Labelled Multi-turn Dialogue Dataset"*, IJCNLP
