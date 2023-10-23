# Git_explained_with_images
Git is a distributed version control system (DVCS) that helps developers track changes in their source code during software development. 

It was created by Linus Torvalds in 2005 and has become the most widely used version control system in the world.

![image](https://github.com/luiscoco/Git_explained_with_images/assets/32194879/ee332fc6-e851-4858-a2c1-e543e3ad33a8)

## Git key concepts:

### Version Control

Git allows developers to keep track of changes in their codebase over time. This includes modifications, additions, and deletions of files.

### Distributed

Git is a distributed version control system, meaning that each developer has a complete copy of the entire repository on their local machine. This allows for offline work and collaboration without a centralized server.

### Repositories

A Git repository is a collection of files and the entire history of changes made to those files. It can exist locally on a developer's machine or remotely on a server.

### Commits

A commit is a snapshot of the changes made to the files in a repository at a specific point in time. Each commit has a unique identifier.

### Branching

Git uses branches to allow developers to work on features or fixes in isolation. Branches can be created, merged, and deleted, enabling parallel development.

### Merging

Merging combines changes from different branches. Developers can merge changes from a feature branch back into the main branch, for example.

### Pull Requests (or Merge Requests)

In collaborative development, developers propose changes to a repository through pull requests. This allows for code review before changes are merged into the main branch.

### Remote Repositories

Git supports working with remote repositories. Developers can clone repositories, fetch changes from remote repositories, and push changes to them.

### Staging Area

Before committing changes, developers can stage specific changes for inclusion in the next commit. This allows for more control over the commit process.

### Tagging

Git allows developers to create tags for specific commits, marking them as important points in the project's history, such as releases.

Git is widely used in the software development industry and is a crucial tool for collaboration, tracking changes, and ensuring code stability. 

It is supported by various platforms, including GitHub, GitLab, and Bitbucket.

![image](https://github.com/luiscoco/Git_explained_with_images/assets/32194879/f3376228-5f35-41ec-a45e-1bc74c779fb9)


## Main actions in Git

### Repository (Repo):

Think of a repository as a folder that contains all your project files and the entire history of changes.

### Working Directory:

This is your current project state—what you see and work on.

### Staging Area (Index):

Before committing changes, you add them to the staging area. It's like preparing a package to be sent.

### Commit:

Committing is like taking a snapshot of your project at a specific point. It records changes you've made in the staging area.

### Branch:

Imagine branches as different parallel universes. Each branch can have its own changes without affecting the others. The main branch is usually called "master" or "main."

### Merge:

Merging is combining changes from one branch into another. It's like bringing changes from a parallel universe back to the main one.

### Pull Request:

In collaborative projects, a pull request is a way to propose changes to the main branch. Others review the changes before merging.

### Clone:

To clone a repository is like copying the entire project and its history to your machine.

### Fetch:

Fetching gets the latest changes from a remote repository but doesn't apply them to your working directory.

### Pull:

Pull is like fetching and then automatically merging the changes into your working directory.

### Push:

Pushing is sending your committed changes to a remote repository, making them available to others.

## Main Git commands

main Git commands along with examples:

### git init:

Initialize a new Git repository.

```bash
git init
```

### git clone:

Clone a repository into a new directory.

```bash
git clone <repository_url>
```

### git add:

Add changes to the staging area.

```bash
git add <file_name>
```

### git commit:

Commit changes with a message.

```bash
git commit -m "Your commit message"
```

### git status:

Show the status of changes as untracked, modified, or staged.

```bash
git status
```

### git log:

Display the commit history.

```bash
git log
```

### git branch:

List, create, or delete branches.

```bash
Copy code
git branch
git branch <branch_name>
git branch -d <branch_name>
```

### git checkout:

Switch branches or restore working tree files.

```bash
git checkout <branch_name>
```

### git merge:

Merge changes from one branch into another.

```bash
git merge <branch_name>
```

### git pull:

Fetch from and integrate with another repository or a local branch.

```bash
git pull origin <branch_name>
```

### git push:

Update remote refs along with associated objects.

```bash
git push origin <branch_name>
```

### git remote:

Manage connections to remote repositories.

```bash
git remote -v
```

### git fetch:

Download objects and refs from another repository.

```bash
git fetch origin
```

### git diff:

Show changes between commits, commit and working tree, etc.

```bash
git diff
```

These are some fundamental Git commands. Keep in mind that Git has a rich set of commands and options to handle various scenarios in version control.

## How Create a repo on the command line

```
echo "# TestRepo" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/luiscoco/TestRepo.git
git push -u origin main
```

## Push an existing repository from the command line

```
git remote add origin https://github.com/luiscoco/TestRepo.git
git branch -M main
git push -u origin main
```

## Merge vs Rebase

![image](https://github.com/luiscoco/Git_explained_with_images/assets/32194879/52794e94-2ecc-443c-875a-3021edaa3d56)

