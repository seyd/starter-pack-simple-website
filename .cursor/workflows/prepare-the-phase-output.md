# Prepare the phase output

## Instructions for the agent

- validate if the answers are consistent, understandable, clear and not contradicting each other (if so, point it out and ask additional questions)

- check if the requirements (answers) are not coliding with the constrains of this starter pack (if so, point it out and ask if user wants continue or change the previous answers)

- **create a compact Markdown summary** of all answers and:

  - use plain text (no tables)
  - summarize the answers to the output template described in section "Output template" below
  - use Markdown headings & bullet lists, do not use tables

- **enhance the output** with the following:

  - Evaluate the answer on Accuracy, Completeness, Clarity, and Tone.
  - For each dimension, give a 1-5 score and 1-2 sentences explaining the score.
  - List concrete suggestions, not just general remarks.
  - Spawn multiple critics with different specialties.
  - Have the Author incorporate every critic's point.
  - Fix the grammar and improve the phrasing (if needed).
  - Update the output document as many times as needed.

- **IMPORTANT**: don't forget toalways follow the workflow [update-tasks.md](/.cursor/workflows/update-tasks.md)
  (except for the phase "0. Disclaimer" - do not create task file for this phase)
