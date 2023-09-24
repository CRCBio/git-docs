Module 6 - Troubleshooting
==========================

Common Git Issues
-----------------
Common Git issues include conflicts during merges, accidentally deleted files, 
or mistakenly committed sensitive data. Learning how to resolve these issues 
and understanding Git's "undo" mechanisms, such as ``git reset`` and ``git 
revert``, can help you maintain the integrity of your bioinformatics projects.

#. Merge Conflicts

   * Merge conflicts occur when Git is unable to automatically merge changes 
     from different branches due to conflicting edits in the same part of a 
     file. This often happens when multiple collaborators work on the same file 
     simultaneously.
   * To resolve merge conflicts, open the conflicted file(s) in a text editor 
     and manually edit the conflicting sections to resolve differences. Then, 
     commit the resolved file(s) and complete the merge process.
   * In the conflict marker section, you'll see your changes (above =======) 
     and the conflicting changes from the other branch (below =======). Edit 
     the content to keep the desired changes and remove the conflict markers.
   
   .. code-block:: bash

      <<<<<<< HEAD
      This is your change
      =======
      This is their change
      >>>>>>> branch-name

#. Accidentally Deleted Files

   * You might inadvertently delete a file that is still needed in your 
     project. Git will recognize this as an untracked deletion.
   * If you realize that a file was mistakenly deleted, you can use the ``git 
     checkout`` command to restore the deleted file from the last committed 
     state.
   * This command will restore the deleted file to its last committed state.

   .. code-block:: bash

      git checkout path/to/deleted_file.py
   

#. Mistakenly Committed Sensitive Data

   * You accidentally committed sensitive data, such as passwords, API keys, 
     or confidential information, to your Git repository.
   * To remove sensitive data from the Git history, you can use the ``git 
     filter-branch`` command. Once the data is removed, force-push the updated 
     history to the remote repository. Be cautious when using this method, as 
     it can affect collaborators.
   * Confirm the name of the sensitive file you want to remove. In this 
     example, we'll assume it's named sensitive_data.txt.
   
   .. code-block:: bash

      git filter-branch --tree-filter 'rm -f sensitive_data.txt' HEAD
      git push --force origin <branch_name>   

#. Undoing Commits with ``git reset`` and ``git revert``

   * You may need to undo one or more commits due to errors, changes in 
     project direction, or other reasons.
   * Git provides two primary mechanisms for undoing commits: ``git reset`` 
     and ``git revert``.
   * ``git reset`` allows you to move the branch pointer to a previous commit, 
     effectively removing all commits after it. This can be a destructive 
     operation, so use it with caution.
   * ``git revert`` creates a new commit that undoes the changes made by a 
     specific commit, leaving a clear history. This is the safer option when 
     working with shared repositories.

   .. code-block:: bash

      git log  # Find the commit hash you want to undo
      git revert <commit-hash>
   