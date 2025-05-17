# Git Commands

git clone <repo>
description: Creates a copy of a remote repository on your local machine

git add <files>
description: Stages changes for commit, preparing files to be included in the next commit

git commit -m "<commit message>"
description: Records staged changes to the repository with a descriptive message

git fetch
description: Downloads objects and refs from remote repository without merging changes

git pull --ff-only
description: Fetches from remote repository and merges changes into current branch

git push
description: Uploads local repository commits to the remote repository

git log
description: Shows commit history with details like author, date, and commit messages

git status
description: Displays working directory state and staging area status

git branch
description: Lists, creates, or deletes branches

git checkout
description: Switches between branches or restores working tree files

# Git LFS Commands

git lfs locks
description: Lists currently active file locks in the repository

git lfs lock
description: Places a lock on a file to prevent others from modifying it

git lfs unlock
description: Removes a lock from a previously locked file
