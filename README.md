# Git Racer: A merge race detector

When you've got a lot of people working in a codebase, there is often more than
one person working in the same area. When this happens, weather you like it or
not you're in a merge race. First person to merge to master wins, and you have
to resolve that conflict.

This is a script that checks branches that have happened since you branched,
and tells you if any of them are in conflict with yours.

## Usage

Navigate to the repository that you're working in, checkout the branch you're
keen on...

```bash
cd $MY_REPO
git fetch --all
git checkout $MY_BRANCH
```

Now run this snazzy command...

```bash
git race
```

And you should get some output like...

```
Danger! Merge race in progress
* Conflict: HEAD with origin/ticket-840, last authored by Base Master Cylinder <mr@basemaster.co.nz>
* Conflict: HEAD with origin/ticket-246, last authored by Flappy Mc Flapjack <flappy@lumberjacks.com>
```

## Installation

TODO
