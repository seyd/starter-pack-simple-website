# Review generated document

> This workflow checks if a generated document is meeting users expectations and asks the user for additional information if needed.

## Instructions for the agent

- This workflow is used after the generation of a new document <document name> (mentioned in the context before)
- Say to the user that a new document has been generated and recommend to open/read and review it and print the link to the document in the chat with icon 📄 <document name> (and src of the link will point to the exact path of the document in the project starting with `/doc/...`) and add text "(click to open)"

- Stop here and ask the user:

  ```
  ## ❓ Is the document meeting your expectations and what you had in mind?
  - ✅ "Yes" - to continue the process
  - ✏️ "No, let's change...." - to change the document
  ```

- If the user responds with "No, let's change....", ask the user what he wants to change.

- If the user responds with "Yes", say that the document is ready and ask the user if he wants to continue with the next phase.
