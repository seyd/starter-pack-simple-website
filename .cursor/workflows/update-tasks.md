# Update TASKS.md

> This workflow is used to update the file `TASKS.md` with the new information
> and create a new task detail file for the task if it does not exist,
> storing the task details and the log of the task in the file.

## Instructions for the agent

- read the file `TASKS.md` and find the current task you are working on

- if the task is not found, create a new one with the new information

- if the task has no id yet, create a new unique id for the task as `task-00X` starting from 001 and incrementing by 1 the biggest task number in the file

- create a new file in the folder `/docs/tasks/` with the name of the task id and create a link to the task in the file `TASKS.md` with the following format:

  ```
  - [**[task-00X](/docs/tasks/task-00X.md)**] <task name>
  ```

  **Important**: the link must start with `/docs/tasks/` (to function properly) and the file must be in the folder `/docs/tasks/`!

- In the new task detail file:

  - add the main header with the task id and the task name (e.g. `# task-00X <task name>`)

  - analyze the current context and write the task details in the new file

  - create a task break down in the file with the following format (if not already present):

    ```
    ## 🔨 In Progress

    ## 📋 Todo

    ## ✅ Done
    ```

- add the task to the appropriate section in the file `TASKS.md`

- if the task is already in the file `TASKS.md`, update the task with the new information

- after finishing the task:

  - write summary of the task to the task detail file

  - move the task in the file `TASKS.md` to the section `✅ Done` and add the date and time of completion

  - **IMPORTANT:** always ask for current date and time with a shell command

  - order the tasks in the `✅ Done` section by date of completion (by datetime asc), so add new tasks at the end of the section
