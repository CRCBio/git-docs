Module 3 - Branching and Merging
================================

Understanding Branches
----------------------
Branching is a powerful feature in Git that allows you to work on different
aspects of your bioinformatics project in isolation. Each branch is like a 
separate line of development, which is incredibly useful when working on
multiple features or experiments simultaneously. You can create branches using 
the ``git branch`` command and switch between them using ``git checkout``.

Switching and Merging Branches
------------------------------
Merging is the process of combining changes from one branch into another. When 
you've completed a feature or experiment on a branch, you can merge it into the 
main project branch. This integration of changes is done using the ``git merge``
command. However, conflicts may arise if changes in one branch conflict with 
those in another. Git provides tools to resolve these conflicts and ensure a 
smooth merge.

.. admonition:: Task

   **Step 1: Ensure You're on the Main Branch**
   
   Before creating new branches, ensure you are on the main branch. You can 
   check your current branch using the following command:
   
   .. code-block:: bash
      
      git branch
    
   If you're not on the main branch, switch to it:

   .. code-block:: bash
      
      git checkout main

   **Step 2: Create a New Branch**
   
   To create a new branch, use the ``git checkout -b`` command followed by the 
   name of the branch you want to create. For example, to create a branch for 
   sequence alignment:

   .. code-block:: bash
         
      git checkout -b feature/sequence-alignment

   This command both creates the new branch and checks it out, switching you to 
   the new branch. 
   
   **Step 3: Work on Your Task**
   
   Now that you're on the ``feature/sequence-alignment`` branch, you can start 
   working on your sequence alignment task. Make changes, add files, and commit 
   your work as needed using standard Git commands:

   .. code-block:: bash
         
      # Make changes to files
      # Add changes to the staging area
      git add .
      # Commit your changes with a descriptive message
      git commit -m "Implement sequence alignment feature"

   **Step 4: Create and Switch to Another Branch**

   To work on another task, such as ``feature/data-visualization``, you can 
   create and switch to a new branch in the same way as in Step 2:

   .. code-block:: bash

      git checkout -b feature/data-visualization

   Now, you're on the ``feature/data-visualization`` branch, and you can make 
   changes specific to this task. Again, use standard Git commands to make 
   changes and commit as needed.

   **Step 5: Switch Between Branches**

   You can switch between branches at any time using the ``git checkout``
   command:

   .. code-block:: bash

      # Switch back to the "feature/sequence-alignment" branch
      git checkout feature/sequence-alignment

   **Step 6: Merge Your Work**

   Once you've completed the tasks on your feature branches and tested them 
   thoroughly, you can merge them back into the main branch:

   .. code-block:: bash

      # Switch to the main branch
      git checkout main
      # Merge the feature/sequence-alignment branch into main
      git merge feature/sequence-alignment
 
   Repeat the merge process for the ``feature/data-visualization`` branch or 
   any other feature branches you've created.

   **Step 7: Delete Feature Branches**

   After merging your changes, you can delete the feature branches if you no 
   longer need them:

   .. code-block:: bash

      # Delete the feature/sequence-alignment branch
      git branch -d feature/sequence-alignment
      # Delete the feature/data-visualization branch
      git branch -d feature/data-visualization
 
   Creating separate branches for different tasks helps you keep your codebase 
   organized and allows for concurrent development of multiple features or bug 
   fixes. It also makes it easier to isolate and test changes before merging 
   them into the main branch.