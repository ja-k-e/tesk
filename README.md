# tesk
**Comment-based task management for developers.**

The idea for tesk is simple. Use comments in code to create and complete tasks for a project while making more meaningful commits. It is like TDD and Git had a baby for task management.

## Example Markup 

**Yet-to-be completed tasks:**

Write tasks in your code with comments like `/* @tesk: do all the things */`, `# @tesk: do all the things`, `<!-- @tesk: do all the things -->`, or `// @tesk: do all the things`

**Completed tasks:**

The removal of the `@tesk:` flag turns completed tasks into well-documented code: `/* do all the things */`

**A task with more urgency:**

Add priority to a task by adding `@` symbols: `/* @@@tesk: do all the things */`

## Process
- Comment task(s) in your code: `/* @tesk: do all the things */`
- Complete task(s) in your code: `/* do all the things */`- 
- Parse your app from your project directory: `$ tesk --parse`
- tesk adds and commits *tesk-specific* changes to your git repository with descriptive commit messages and descriptions.
  - no more "what am I committing again?? WIP."
- Tasks become well-written markup and `.md` documentation
  - everyone is happy and understands what's going on.
 
## Eventually
- tesk will exist.
- tesk will render project-level html overviews on parse`$ tesk --pars
- tesk will include support for documentation `.md` files to manage global and directory-level tasks
	- one required global `README.md` file
	- optional directory-level `README.md` files
- tesk will optionally generate task-named `.tesk` files in a project-level tesk directory, using the file browser as a todo list for easy hide/reveal reference in any text editor that has a file browser.
	- imagine expanding a tesk directory at the root of your project with the following contents:
		- .tesk_completed (collapsed directory)
		- `___body_styles_style.css.tesk`
		- `___global_typography_style.css.tesk`
		- `__container_styles_style.css.tesk`
		- `_implement_analytics_index.html.tesk`
- tesk will include role assignments: `/* @tesk --DavyCrockett: do all the things */`
