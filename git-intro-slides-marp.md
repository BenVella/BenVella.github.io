---
marp: true
theme: marpit
---

# Git Introduction

A presentation on the basics, features, and use cases of Git.

---

# What is Git?

- Git is a distributed Version Control System (DVCS) designed to track changes in source code during software development.
- Git was created by Linus Torvalds in 2005 and has become the industry standard for version control.
- Git allows developers to collaborate on projects, maintain version history, and manage codebase modifications.

---
<style scoped>section { font-size: 30px; }</style>
# Git vs Perforce

- Primarily, Perforce is a Centralized Version Control System (CVCS) while Git is Distributed
- In theory, you can add other colleague's repos as remotes and directly push / pull on them

| Git | Perforce |
| --- | -------- |
| Works offline | Requires network connection |
| Stores full repository on each machine | Stores only working copy on each machine |
| Uses Branches and Commits | Uses Streams and Changelists |
| Requires LFS for file locking | Supports file locking natively |

---

# An example workflow of Perforce

- Do the usual addition of 

- Suppose you want to work on a new feature for your project.
- In Git, you would create a new branch from the main branch and work on it locally. You can commit, push, and pull changes as you wish. When the feature is ready, you can merge it back to the main branch.
- In Perforce, you would check out the files you want to modify from the server and work on them locally. You can shelve your changes to the server if you want to share them with others. When the feature is ready, you would submit your changes to the server.

---

# Git Features and Use Cases

- Git has many features that make it a powerful and versatile tool for software development.
- Some of the most important and commonly used features are:

  - Branching and Merging
  - Committing and Stashing
  - Pulling and Pushing
  - Rebasing and Resetting
  - Tagging and Cherry-picking

- Let's look at each feature and its use cases in more detail.

---

# Branching and Merging

- Branching is the process of creating a separate line of development from an existing branch.
- Merging is the process of combining the changes from one branch into another branch.
- Branching and merging allow developers to work on different features or bug fixes concurrently and integrate them seamlessly.
- Git supports multiple types of branches, such as:

  - Feature branches: for developing new features
  - Release branches: for preparing releases
  - Hotfix branches: for fixing urgent bugs
  - Support branches: for maintaining older versions

---

# Committing and Stashing

- Committing is the process of recording the changes made to the files in the repository.
- Stashing is the process of temporarily saving the changes made to the files without committing them.
- Committing and stashing allow developers to keep track of the changes made to the codebase and save them for later use.
- Git supports various options for committing and stashing, such as:

  - Adding a message to describe the commit
  - Amending the previous commit
  - Squashing multiple commits into one
  - Applying or dropping a stash

---

# Pulling and Pushing

- Pulling is the process of fetching and merging the changes from a remote repository to a local repository.
- Pushing is the process of sending and updating the changes from a local repository to a remote repository.
- Pulling and pushing allow developers to synchronize their changes with other developers and share them with the world.
- Git supports various protocols and platforms for pulling and pushing, such as:

  - HTTPS or SSH
  - GitHub, GitLab, or Bitbucket

---

# Rebasing and Resetting

- Rebasing is the process of changing the base of a branch from one commit to another commit.
- Resetting is the process of moving the current branch pointer to a different commit.
- Rebasing and resetting allow developers to modify the history of the project and undo or redo changes.
- Git supports various modes and options for rebasing and resetting, such as:

  - Interactive or automatic rebasing
  - Soft, mixed, or hard resetting
  - Preserving or discarding merges

---

# Tagging and Cherry-picking

- Tagging is the process of adding a label to a specific commit to mark it as a significant point in the project history.
- Cherry-picking is the process of applying the changes from a specific commit to another branch without merging the whole branch.
- Tagging and cherry-picking allow developers to identify and reuse important commits in the project.
- Git supports various types and options for tagging and cherry-picking, such as:

  - Lightweight or annotated tags
  - Signed or unsigned tags
  - Editing or dropping commit messages

---

# GitFlow Example

- GitFlow is a popular branching model for Git that defines a standard workflow for developing, releasing, and maintaining software.
- GitFlow involves the use of two main branches (main and develop) and three supporting branches (feature, release, and hotfix).
- Let's see how GitFlow works with a practical example.

---

# GitFlow Example: Creating a Feature Branch

- Suppose you want to work on a new feature for your project, called feature1.
- You would create a feature branch from the develop branch and work on it locally.
- You can use the git-flow extension to simplify the process:

```bash
git flow init # initialize git-flow
git flow feature start feature1 # create feature branch
# work on feature1
git flow feature finish feature1 # merge feature branch to develop
```

#GitFlow Example: Creating a Release Branch

- Suppose you want to prepare a new release for your project, called 1.0.0.
- You would create a release branch from the develop branch and work on it locally.
- You can use the git-flow extension to simplify the process:

```bash
git flow release start 1.0.0 # create release branch
# work on release
git flow release finish 1.0.0 # merge release branch to main and develop
```

# GitFlow Example: Creating a Hotfix Branch

- Suppose you want to fix a critical bug in your project, called bug1.
- You would create a hotfix branch from the main branch and work on it locally.
- You can use the git-flow extension to simplify the process:

```bash
git flow hotfix start bug1 # create hotfix branch
# work on bug1
git flow hotfix finish bug1 # merge hotfix branch to main and develop
```

# Using Git via CLI or GUI

- Git can be used via command line interface (CLI) or graphical user interface (GUI).

/ Both options have their advantages and disadvantages, and the choice depends on your personal preferences, needs, and goals.

- Some of the factors to consider are:

  - Availability and compatibility
  - Completeness and functionality
  - Visualization and interactivity
  - Documentation and support
  - Learning curve and productivity

# Using Git via CLI or GUI: Pros and Cons
|CLI |	GUI|
|---|---|
|Available and compatible with all environments and machines	| May not be available or compatible with some environments and machines
|Covers all Git features and commands|	May not cover all Git features and commands
|Lacks visualization and interactivity	|Provides visualization and interactivity
|Well documented and supported	|Poorly documented and supported
|Steep learning curve but allows for higher productivity ceiling|Gentle learning curve but restricted productivity

# Conclusion

- Git is a powerful and versatile tool for software development.
- Git has many features and use cases that enable collaboration, version control, and code quality.
- GitFlow is a popular branching model for Git that defines a standard workflow for developing, releasing, and maintaining software.
- Git can be used via command line interface (CLI) or graphical user interface (GUI), depending on your preferences, needs, and goals.

