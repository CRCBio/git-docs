Module 4 - Collaborating with GitHub
====================================

Introduction to GitHub
----------------------
Collaboration is at the heart of bioinformatics research, and GitHub is a 
platform that facilitates collaboration on code and data. GitHub acts as a 
central hub for hosting Git repositories and provides tools for team 
collaboration, code review, and project management. To begin collaborating with
GitHub, you'll first need to create an account on the platform. 

Forking and Cloning Repositories
--------------------------------
Once you're logged in, you can start by **forking** an existing repository. 
Forking essentially creates a copy of the repository in your own GitHub 
account. This allows you to work on the project independently and make changes 
without affecting the original repository.

After forking, you'll want to bring the repository to your local machine. This 
is done using the ``git clone`` command, followed by the URL of your forked 
repository on GitHub. Cloning sets up a local copy of the repository on your 
computer, enabling you to work on it just like any other Git repository.

.. admonition:: Task

   **Step 1: Find the Repository to Fork**
   
   Navigate to the GitHub repository of the tool you want to customize. Use 
   the search bar or go directly to the repository's URL.

   **Step 2: Fork the Repository**
   
   On the top-right corner of the repository's page, you'll see a "Fork" 
   button. Click this button to create a fork of the repository in your GitHub 
   account.

   **Step 3: Clone Your Fork Locally**

   Now that you have a fork of the repository in your GitHub account, you need 
   to clone it to your local machine to start making customizations.

   1. Clone your forked repository using the ``git clone`` command, replacing 
      ``<your_username>`` with your GitHub username and ``<repository_name>`` with 
      the name of the forked repository:
   
   .. code-block:: bash

      git clone https://github.com/<your_username>/<repository_name>.git

   2. Change into the cloned directory:

   .. code-block:: bash

      cd <repository_name>

Pushing and Pulling Changes
---------------------------
As you make changes to your local copy, you'll want to keep your fork on 
GitHub up to date. This is achieved using the ``git push`` command, which 
uploads your local changes to your forked repository on GitHub. Conversely, 
you can use ``git pull`` to retrieve changes made by others from the remote 
repository.

.. admonition:: Task
   
   **Pushing Changes with** ``git push``
   
   After making changes to your repository, you'll want to upload those 
   changes to your repository on GitHub using ``git push``.
   
   .. code-block:: bash

      git push origin <branch_name>

   **Pulling Changes with** ``git pull``
   
   To retrieve changes made by others from the remote repository, you can use 
   the ``git pull`` command. First, ensure you're on the branch where you want 
   to incorporate the changes. You can use ``git checkout <branch_name>`` to 
   switch to the appropriate branch if needed.
   
   .. code-block:: bash

      git pull origin <branch_name>

   
Pull Requests
-------------
In a collaborative bioinformatics project, you'll often need to request that 
your changes be integrated into the main project. This is done through a "pull 
request." A pull request is a request to merge your changes from your forked 
repository into the original repository. It allows for discussion and code 
review before merging. You can create a pull request on GitHub, describe your 
changes, and request that someone else review and approve your work.

.. admonition:: Task
   
   **Step 1: Find the Repository to Fork**
   
   Once you've made changes and pushed them to your GitHub forked repository, 
   you can begin the pull request process.

   #. Visit your forked repository on GitHub.
   #. Switch to the branch you just pushed using the branch switcher on the 
      repository's main page.
   #. Click the "New Pull Request" button.
   #. You will be prompted to choose the base repository and branch (the 
      repository and branch you want to merge your changes into) and the 
      compare repository and branch (your fork and the branch with your 
      changes).
   #. GitHub will display the changes you've made. Review them to ensure they 
      look correct.
   #. Provide a title and description for your pull request. Be clear and 
      descriptive about the changes you've made.
   #. Optionally, you can assign reviewers, request feedback, and label your 
      pull request to provide more context.
   #. Click the "Create Pull Request" button to submit your pull request.

   **Step 2: Collaborate and Review**
   
   Collaborators or maintainers of the repository will review your pull 
   request. They may request changes or ask for more information.

   **Step 3: Address Feedback (if needed)**
   
   If there are changes requested, make the necessary changes locally, commit 
   them, and push them to your branch on GitHub. The pull request will be 
   automatically updated.
   
   **Step 4: Merge the Pull Request**

   Once your pull request is approved and the required changes are made, a 
   repository collaborator can merge your changes into the main codebase.