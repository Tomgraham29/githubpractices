# Setting Up Git in MATLAB and Creating a New GitHub Repository

## Introduction

Version control is an essential aspect of collaborative software development. Git is a widely-used version control system that allows you to track changes, collaborate with others, and manage your codebase effectively. In this guide, we will walk you through the process of setting up Git in MATLAB and creating a new GitHub repository for an existing directory of files.

## Prerequisites

1. **MATLAB Installed**: Ensure that MATLAB is installed on your computer. If not, you can download it from the [official MATLAB website](https://www.mathworks.com/products/matlab.html).

2. **GitHub Account**: Create a GitHub account if you don't have one. You can sign up at [GitHub](https://github.com/).

3. **Git Installed**: Install Git on your machine. You can download it from the [official Git website](https://git-scm.com/).

## Steps

### Step 1: Initialize a Git Repository

1. Open MATLAB and navigate to the directory containing your existing MATLAB files.

2. Open the MATLAB Command Window.

3. Initialize a new Git repository using the following command:

    ```matlab
    system('git init');
    ```

### Step 2: Create a `.gitignore` File

Create a `.gitignore` file to specify files and directories that should be ignored by Git. This file helps avoid tracking unnecessary files, such as temporary files or build artifacts. Create the file using MATLAB or a text editor and add entries for files or directories you want to ignore.

Example `.gitignore` file:

```plaintext
*.mat
*.fig
*.p
/private/
```

### Step 3: Stage and Commit Changes

1. Stage your files for commit:

    ```matlab
    system('git add .');
    ```

2. Commit the changes:

    ```matlab
    system('git commit -m "Initial commit"');
    ```

### Step 4: Create a New GitHub Repository

1. Go to [GitHub](https://github.com/) and log in to your account.

2. Click on the "+" sign in the upper right corner and select "New repository."

3. Fill in the repository name, add a description, and configure other settings.

4. Click on "Create repository."

### Step 5: Connect Local Repository to GitHub

1. Copy the repository URL from your GitHub repository.

2. In MATLAB, add the remote repository:

    ```matlab
    system('git remote add origin <repository_url>');
    ```
	note: github now uses ssh as the only accepted credentials, using the https:// url will default to asking for login credentials and fail. 
	For more information about setting up ssh visit githubs documentation: https://docs.github.com/en/authentication/connecting-to-github-with-ssh
3. Push your local changes to GitHub:

    ```matlab
    system('git push -u origin master');
    ```

Now, your MATLAB files are version-controlled with Git, and changes can be tracked on GitHub.

## Conclusion

Congratulations! You have successfully set up Git in MATLAB, initialized a new Git repository, and connected it to a new GitHub repository. You can now manage your MATLAB codebase efficiently using Git version control.
