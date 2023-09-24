Git Cheatsheet
==============

Here are some common Git commands and examples of their usage:

``git init`` - Initializing a New Git Repository
------------------------------------------------
**Usage:** This command initializes a new Git repository in the current
directory, allowing you to start version controlling your project.

.. code-block:: bash

   mkdir my_project
   cd my_project
   git init

``git clone`` - Cloning a Remote Repository
-------------------------------------------
**Usage:** Clone an existing Git repository from a remote server, creating a 
local copy for you to work on.

.. code-block:: bash

   git clone https://github.com/username/repo.git

``git status`` - Checking the Status of Your Repository
-------------------------------------------------------
**Usage:** View the current state of your repository, including which files are
modified, staged, or untracked.

.. code-block:: bash

   git status

``git add`` - Staging Changes
-----------------------------
**Usage:** Stage changes for the next commit. You can specify files or use
``.`` to stage all changes.

.. code-block:: bash

   git add file.txt

``git commit`` - Committing Changes
-----------------------------------
**Usage:** Create a new commit to save the staged changes with a descriptive 
commit message.

.. code-block:: bash

   git commit -m "Added feature X"

``git branch`` - Managing Branches
----------------------------------
**Usage:** List, create, or delete branches. Use ``-a`` to list remote branches.

.. code-block:: bash

   git branch feature-branch

``git checkout`` - Switching Between Branches
---------------------------------------------
**Usage:** Switch to a different branch. You can also use this command to
create a new branch with the ``-b`` flag.

.. code-block:: bash

   git checkout feature-branch

``git merge`` - Merging Branches
--------------------------------
**Usage:** Merge changes from one branch into another. Usually used to integrate 
feature branches into the main branch.

.. code-block:: bash

   git checkout main
   git merge feature-branch

``git pull`` - Updating Your Local Repository
---------------------------------------------
**Usage:** Fetch and merge changes from a remote repository. Equivalent to ``git 
fetch`` followed by ``git merge``.

.. code-block:: bash

   git pull origin main

``git push`` - Pushing Changes to a Remote Repository
-----------------------------------------------------
**Usage:** Upload your local commits to a remote repository, making your changes
available to others.

.. code-block:: bash

   git push origin main

``git log`` - Viewing Commit History
------------------------------------
**Usage:** View a log of all commits in the current branch, including commit 
messages, authors, and commit hashes.

.. code-block:: bash

   git log

``git diff`` - Viewing Changes Between Commits
----------------------------------------------
**Usage:** Compare differences between two commits, branches, or the working
directory.

.. code-block:: bash 

   git diff HEAD~1..HEAD

``git stash`` - Temporarily Stashing Changes
--------------------------------------------
**Usage:** Temporarily save your uncommitted changes to work on something else, 
then reapply the changes later.

.. code-block:: bash

   git stash

``git remote`` - Managing Remote Repositories
---------------------------------------------
**Usage:** List, add, or remove remote repositories that your local repository
can interact with.

.. code-block:: bash

   git remote add upstream https://github.com/upstream/repo.git