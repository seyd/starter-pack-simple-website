# Check thinking model

> This workflow checks if a thinking model is in use and recommends one to the user if not

## Instructions for the agent

- Write which model you currently use and state if is explicitly defined as a thinking model.

- Check if you see thinking processes in the previous context/conversation.

- If you are not sure if you are using thinking model (even the model name match thinking model, but it is not explicit stated, and thinking processes are missing), ask user if he uses a thinking model and if not, offer the recommended thinking model to the user.

  - Stop here and ask the user:
    ```
    Please respond with:
    - ⚠️ "Continue" - to continue the process without thinking model (not optimal)
    - ❌ "Stop" - to stop here and start again with thinking model (you have to set it in the chat)
    ```

- if you see "Recommended model" or "Preferred model" in your context, recommend this one.

- do not write anything at all (but current model name) if user is using the thinking model, just continue
