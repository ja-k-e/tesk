# tesk
**Comment-based task management for developers.**

The idea for tesk is simple. Use comments in code to create and complete tasks for a project.

## example markup 
### yet-to-be completed tasks (in different languages)
`/* @tesk: do all the things */`, `# @tesk: do all the things`, `<!-- @tesk: do all the things -->`
### a completed task
`/* do all the things */`
### a task with less urgency
`/* @@tesk: do all the things */`

## process
- Write task(s) in your code `/* @tesk: do all the things */`
- Parse your app from your project directory `~ tesk parse`
- tesk automatically adds and commits *tesk-specific* changes to your git repository with descriptive titles
  - no more "what am I committing again?? WIP."
