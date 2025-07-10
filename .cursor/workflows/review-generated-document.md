# Review generated document

> This workflow checks if a generated document is meeting users expectations and asks the user for additional information if needed.

## Instructions for the agent

- This workflow is used after the generation of a new document <document name> (mentioned in the context before)
- Say to the user that a new document has been generated and recommend to open/read and review it.

- Stop here and ask the user:

  ```
  ## ❓ Want you review the document in editor by yourself?
  - ✅ "Yes, continue" - I have already reviewed the document and want to continue the process
  - 👀 "No, print it here" - to print the document in the chat
  ```

  - If the user responds with "Yes", continue the process.
  - If the user responds with something like "No, print it here", print the document in the chat in formatted markdown and then continue the process.

- Stop here and ask the user:

  ```
  ## ❓ Is the document meeting your expectations and what you had in mind?
  - ✅ "Yes" - to continue the process
  - ✏️ "No, let's change...." - to change the document
  ```

- If the user responds with "No, let's change....", ask the user what he wants to change.

- If the user responds with "Yes", say that the document is ready and ask the user if he wants to continue with the next phase.
