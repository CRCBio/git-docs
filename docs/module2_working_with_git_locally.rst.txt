Module 2 - Working with Git Locally
=================================================

Initializing a Git Repository
-----------------------------
The first step in using Git for bioinformatics is to initialize a Git
repository. This is essentially telling Git to start tracking changes in your
project. You can do this with the ``git init`` command in your project's
directory. This command creates a hidden directory called ".git" that stores
all the version control information.

Tracking Changes
----------------
Once you have initialized a repository, you can start tracking changes to your
files. The ``git status`` command shows you the current state of your repository,
including which files have been modified. To include changes in your next
commit, you'll use the ``git add`` command to stage them. Finally, you commit 
your staged changes with ``git commit``, providing a meaningful message to 
describe the changes you made.

.. admonition:: Task

   **Step 1: Set Up a Local Directory**
   
   Choose or create a directory on your bioinformatics workstation where you 
   want to store your project files. This will be your local project directory.
   
   .. code-block:: bash
      
      mkdir my_project
      cd my_project

   **Step 2: Initialize a New Git Repository**
   
   Inside your project directory, initialize a new Git repository using the 
   following command:

   .. code-block:: bash
         
      git init
   
   This command will create a hidden ``.git`` directory in your project 
   directory, which stores all the information needed for version control.
   
   **Step 3: Create and Add Project Files**
   
   Create and add your bioinformatics project files to the local repository. 
   You can use the ``git add`` command to stage files for tracking:

   .. code-block:: bash
         
      git add file1.py   # Stage a specific file
      git add .          # Stage all files in the directory

   **Step 4: Commit Your Changes**

   Commit the staged changes with a descriptive message:

   .. code-block:: bash

      git commit -m "Initial commit: Added project files"

   This creates a snapshot of your project's state at this point.

   **Step 5: Set Up a Remote Repository**

   To collaborate with others or back up your project, you can set up a remote 
   Git repository. This step must be performed if you plan on using GitHub.

   #. Create an empty repository on GitHub.
   #. Copy the URL of your remote repository. It may look something like 
      ``git@github.com:username/repo.git`` 
   #. Add the remote repository to your local Git configuration using the 
      following command:

   .. code-block:: bash

      git remote add origin git@github.com:username/repo.git

   **Step 6: Push Your Local Repository to the Remote**

   If you set up a remote repository, you can push your local repository to it 
   to create a backup or share your work with others:

   .. code-block:: bash

      git push -u origin main
 
   Replace ``main`` with the appropriate branch name if you're using a 
   different branch.

   Your project repository is now set up locally and configured with a remote 
   repository. You can continue working on your project, commit changes 
   locally, and push them to the remote repository if needed. Collaborators can 
   clone the remote repository to access the project and contribute to it.