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

## Merge vs Rebase vs Merge Fast-Forward

![image](https://github.com/luiscoco/Git_explained_with_images/assets/32194879/52794e94-2ecc-443c-875a-3021edaa3d56)

![image](https://github.com/luiscoco/Git_explained_with_images/assets/32194879/892c9f10-3ab1-413a-b038-6e657c526d83)

## Fast Forward step by step

Check out the target branch at commit C:

```bash
git checkout C
```

This puts you on the commit C of the target branch.

Merge the source branch:

```bash
git merge source_branch
```

Since this is a fast-forward merge and there are no divergent changes, Git will automatically move the target branch pointer forward to include the commits from the source branch.

After this step, your commit history would look like:

```rust
A->B->C->D->E
```

Verify the changes:

Review the changes using git log to ensure that everything looks good.

By checking out commit C of the target branch before the merge, you ensure that the fast-forward merge incorporates the changes from the source branch (D and E) onto the latest commit of the target branch (C).


## Merge step by step

In Git, merging is the process of combining changes from different branches. 

Let me walk you through a simple example.

Let's say you have a Git repository with two branches: master and feature_branch. 

The master branch is the main branch, and you've been working on a new feature in the feature_branch.

Now, you want to merge the changes from feature_branch into master.

Here are the steps:

### Switch to the master branch:

```bash
git checkout master
```

### Pull the latest changes from master:

```bash
git pull origin master
```

### Merge feature_branch into master:

```bash
git merge feature_branch
```

If there are no conflicts, Git will automatically perform the merge. However, if there are conflicts (i.e., changes in the same lines of the same file in both branches), Git will prompt you to resolve them.

### Resolve conflicts (if any):

Git will mark the conflicted areas in the files. 

Open the conflicted files, manually resolve the conflicts, and then:

```bash
git add <conflicted_file>
git merge --continue
```

### Commit the merge:

```bash
git commit -m "Merge feature_branch into master"
```

### Push the changes to the remote repository:

```bash
git push origin master
```

That's it! Now, the changes from feature_branch are merged into master.

It's a good practice to delete the feature branch after the merge if you no longer need it:

```bash
git branch -d feature_branch
```

## Rebase step by step

https://senali.hashnode.dev/git-rebase

Git rebase is a powerful command used to integrate changes from one branch into another. 

It works by moving or combining a sequence of commits to a new base commit. 

This can be useful for cleaning up your commit history, resolving conflicts, or keeping your feature branches up-to-date with the latest changes from the main branch.

Here's a simple example to illustrate how git rebase works:

Assuming your commit history looks like this:

Source Branch:

```css
A - B - C - D   (source_branch)
```

Target Branch:

```css
A - B - E - F - G   (target_branch)
```

Now, let's rebase the source branch (source_branch) onto the target branch (target_branch):

Make sure you are on the source branch at commit B:

```bash
git checkout source_branch
git reset --hard B
```

Now, you are on the source branch at commit B.

Start the rebase:

```bash
git rebase target_branch
```

During this step, Git applies commits A and B from the target branch.

Resolve any conflicts:

If there are conflicts, Git will pause and prompt you to resolve them. After resolving conflicts, continue the rebase:

```bash
git rebase --continue
```

This will apply commits C and D from the source branch.

Repeat step 3 until rebase is complete:

If there are multiple conflicts or if Git pauses for any reason, resolve the issues and continue the rebase until it's complete.

Switch to the target branch:

```bash
git checkout target_branch
```

Fast-forward the target branch:

Fast-forward the target branch to the new rebased source branch:

```bash
git merge source_branch
```

At this point, the target branch will include commits A, B, C, D from the source branch, and then commits E', F', G' from the original target branch.

Now, your main branch (target_branch) should have the desired commit sequence: A -> B -> C -> D -> E' -> F' -> G'. 

The original commits from target_branch (E, F, G) are replaced with the new ones from the rebase.

## Cherry-picking in Git

https://senali.hashnode.dev/git-cherry-pick

Cherry-picking in Git is a way to apply a specific commit from one branch to another. 

It's like saying, "I want this commit from that branch, but not the whole branch." Here's a simple explanation with examples:

Let's say you have two branches: feature-branch and main-branch. 

You've made some changes in feature-branch and want to bring just one commit from it into main-branch.

![image](https://github.com/luiscoco/Git_explained_with_images/assets/32194879/6da35b4b-0e71-45d9-83bb-38504e0c340c)

Find the Commit ID:

First, find the commit ID of the specific commit you want to cherry-pick. 

You can use git log to see the commit history.

```bash
git log
```
Note the commit ID (something like abcdef123456).

Switch to the Target Branch:

Make sure you are on the branch where you want to apply the commit, in this case, main-branch.

```bash
git checkout main-branch
```

Cherry-pick the Commit:

Now, use the git cherry-pick command followed by the commit ID.

```bash
git cherry-pick abcdef123456
```

Git will apply the changes from that specific commit to your current branch (main-branch).

Resolve Conflicts (if any):

If there are conflicts during the cherry-pick process, Git will pause and ask you to resolve them. 

After resolving, continue the cherry-pick process with:

```bash
git cherry-pick --continue
```

Or, if you want to cancel the cherry-pick:

```bash
git cherry-pick --abort
```

Finish:

Once there are no conflicts or conflicts are resolved, you have successfully cherry-picked the commit.

Remember, cherry-picking is a powerful tool, but use it wisely. 

It's good for picking specific changes, but avoid cherry-picking a large number of commits, especially if they are interconnected, as it might lead to a messy history.
