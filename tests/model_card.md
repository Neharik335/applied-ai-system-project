# Model Card: Game Glitch Investigator

## Project Summary
Game Glitch Investigator is a Streamlit-based number guessing game enhanced with Retrieval-Augmented Generation (RAG). Users can play the game and ask questions about the rules or bugs, with the AI retrieving relevant info from project documentation. The project demonstrates AI-assisted development, debugging, and explainability.

## AI Collaboration Reflection
- **Helpful Suggestion:** The AI recommended modularizing game logic and adding a retrieval feature for user questions, which improved code structure and user experience.
- **Flawed Suggestion:** The AI initially suggested using advanced NLP for retrieval, which was unnecessary for this project’s scope; a simple keyword search was more effective.

## Limitations & Biases
- The RAG feature relies on keyword matching and may miss context or nuance in user queries.
- Answers are only as good as the documentation provided; incomplete or biased docs can affect output.

## Reliability & Testing
- 3/3 unit tests for game logic pass (see tests/test_game_logic.py).
- Logging and error handling are implemented for both game logic and retrieval.
- Manual and automated tests confirm the system is robust for its intended use.

## Responsible AI Considerations
- Potential misuse: If harmful content is added to documentation, the retriever may surface it. Mitigation: review and version-control docs, filter user input.
- Surprises: Vague questions often returned no results, highlighting the need for clear queries and documentation.

## Human Evaluation
- All AI outputs were reviewed for accuracy and relevance. The system performs well when queries are clear and documentation is accurate.

---
This model card documents the design, limitations, and responsible use of the Game Glitch Investigator AI system.