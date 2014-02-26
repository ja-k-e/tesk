# tesk
**Comment-based task management for developers.**

The idea for tesk is simple. Use comments in code to create and complete tasks for a project while making more meaningful commits. Think TDD for tasks.

## Example Markup 

**Yet-to-be completed tasks:**

Write tasks in your code with comments like `/* @tesk: do all the things */`, `# @tesk: do all the things`, `<!-- @tesk: do all the things -->`, or `// @tesk: do all the things`

**Completed tasks:**

The removal of the `@tesk:` flag turns completed tasks into well-documented code: `/* do all the things */`

**A task with more urgency:**

Add priority to a task by adding `@` symbols: `/* @@@tesk: do all the things */`

## Process
- Comment task(s) in your code `/* @tesk: do all the things */`
- Complete task(s) in your code `/* do all the things */`
- Parse your app from your project directory `~ tesk parse`
- tesk adds and commits *tesk-specific* changes to your git repository with descriptive commit messages and descriptions.
  - no more "what am I committing again?? WIP."
- Tasks become well-documented markup
  - everyone is happy and understands what's going on.
 
## Eventually
- tesk will exist.
- tesk will render project-level html overviews on parse
- tesk will somehow allow for global task creation (a project-level tesk file?)
- tesk will optionally generate task-named files in a project-level tesk directory, using the file system as a todo list (for easy hide/reveal reference in any text editor that has a file browser).
- tesk will include role assignments /* @tesk #DaveyCrockett: do all the things */`
