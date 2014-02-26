# tesk
**Comment-based task management for developers.**

The idea for tesk is simple. Use comments in code to create and complete tasks for a project.

## example markup 

### yet-to-be completed tasks
`/* @tesk: do all the things */`, `# @tesk: do all the things`, `<!-- @tesk: do all the things -->`

### to complete a task
remove `@tesk:` flag from `/* @tesk: do all the things */`: result `/* do all the things */`

### a task with more urgency
`/* @@tesk: do all the things */`

## process
- Comment task(s) in your code `/* @tesk: do all the things */`
- Complete task(s) in your code `/* do all the things */`
- Parse your app from your project directory `~ tesk parse`
- tesk adds and commits *tesk-specific* changes to your git repository with descriptive titles
  - no more "what am I committing again?? WIP."
- Tasks become well-documented markup
  - everyone is happy and understands what's going on.
 
## eventually
- tesk will exist.
- tesk will render project-level html overviews on parse
- tesk will optionally generate task-named files in a project-level tesk directory, using the file system as a todo list (for easy reference in any text editor that has a file browser).
- tesk will include role assignments /* @tesk #DaveyCrockett: do all the things */`
