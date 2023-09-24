Module 1 - Understanding Git and Version Control
=================================================

Introduction to Version Control
-------------------------------
In the field of bioinformatics, understanding the principles of version control
is paramount. **Version control** allows you to track changes, collaborate with 
team members, and maintain a historical record of your work. **Git** is a 
distributed version control system that we will use for managing bioinformatics 
projects. It enables you to keep track of changes in your code and data, making 
it an indispensable tool for reproducible research.

Git Basics
----------
Before diving into Git, let's clarify some key concepts. A **repository** is a 
place where Git stores your project's files and the entire history of changes. 
Each **commit** represents a snapshot of your project at a specific point in
time. **Branches** allow you to work on different features or experiments
independently. **Merging** combines changes from different branches into one
cohesive project. You can also **clone** a repository to make a copy on your 
local machine and **fork** a repository on GitHub to contribute to someone 
else's project.

Setting Up Git
--------------
To get started with Git, you'll need to install it on your workstation and 
configure your username and email. Once you're set up, you can begin creating 
repositories to manage your bioinformatics projects.

.. admonition:: Task

   **Step 1: Install Git**
   
   Test if Git is installed on your workstation using ``git --version``. If Git is not 
   already installed on your  workstation, you'll need to install it. 
   The installation process may vary depending on your operating system.

   * Linux (Debian/Ubuntu):
      You can use the package manager to install Git:

      .. code-block:: bash

         sudo apt-get update
         sudo apt-get install git
   
   * macOS:
      Git can be installed via Homebrew:

      .. code-block:: bash

         brew install git
   
   **Step 2: Configure Git**
   
   After installing Git, you need to configure it with your name and email
   address, which will be associated with your commits:

   .. code-block:: bash
         
      git config --global user.name "Your Name"
      git config --global user.email "your.email@example.com"
   
   You can also configure other settings, such as your preferred text editor 
   and default branch name. Use the following commands to set these options:
   
   .. code-block:: bash
         
      git config --global core.editor "nano" 
      git config --global init.defaultBranch "main"
   
   **Step 3: Generate SSH Key**
   
   If you plan to use Git with remote repositories that require SSH 
   authentication (e.g., GitHub, GitLab), you should generate an SSH key and 
   add it to your SSH agent. 

   To generate an SSH key:

   .. code-block:: bash
         
      ssh-keygen -t ed25519 -C "your_email@example.com"

   Follow the prompts to save the key in the default location 
   (~/.ssh/id_ed25519).
   
   To add your SSH key to the SSH agent: 

   .. code-block:: bash

      eval "$(ssh-agent -s)"
      ssh-add ~/.ssh/id_ed25519

   **Step 4: Test Your Configuration**

   To test whether Git is configured correctly, run the following command:

   .. code-block:: bash

      git --version
   
   This should display the installed Git version. That's it! You've 
   successfully set up Git on your bioinformatics workstation. You can now 
   start using Git for version control in your bioinformatics projects.
