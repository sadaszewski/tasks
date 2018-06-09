# tasks
Yet another simple command line task manager

Sitting in a single stand-alone Python file named "t" you will find a very basic command line task manager. Just download it anywhere (e.g. to your project diretory) and make it executable. You can also add it to system path. Depending on location you can call it as ./t or simply t. It will store its data in the "tasks" file in the working directory.

Task data:
- Serial identifier (an always increasing number - 1, 2, 3, etc.)
- Dates of all state transitions (added, finished, cancelled, etc.)
- Task description

Supported task states:
- Pending
- Finished
- Cancelled
- Removed

Syntax:
- Add task: ./t Task description does not have to be quoted
- Edit description for task with id 1: ./t -e 1
- Finish task with id 1: ./t -f 1
- Cancel a task: ./t -c 1
- Restore a cancelled task: ./t -r 1
- Print pending tasks: ./t
- Print finished (done) tasks: ./t -d
- Print cancelled (postponed) tasks: ./t -p
- Print tasks in any state: ./t -A
- Remove a task completely (its ID will remain reserved): ./t -x 1

Features:
- Color output (green - done, red - pending, magenta - cancelled)
- Output date of last transition, ID and description

Sample output:

![Sample output](https://github.com/sadaszewski/tasks/raw/master/Screen%20Shot%202018-06-09%20at%2013.21.44.png)
