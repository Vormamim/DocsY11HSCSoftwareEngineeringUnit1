---
icon: book-open
---

# Git

Git is a **distributed version control system** created by Linus Torvalds in 2005 for development of the Linux kernel.

**Git** is a widely used version control system designed to handle everything from small to very large projects with speed and efficiency. Created by Linus Torvalds in 2005, Git is unique because it is a **distributed system**, meaning every developer has a full copy of the project’s history. This makes Git particularly resilient, as each repository can function independently, even without internet access.

## Key Git Terminology and Commands

1.  **Repository (Repo)**: A repository is the main project folder where Git tracks all changes. It’s the database for all project files and change history.

    `git init`
2.  **Commit**: A commit is a record of changes made to the code. Each commit is like a snapshot of the project at a specific point in time.

    `git commit -m "Describe the changes made"`
3.  **Branch**: A branch is a separate line of development in Git. The default branch is typically `main` or `master`. Developers can create branches to develop features without impacting the main codebase.

    `git branch new-feature`
4.  **Merge**: Merging is the process of combining changes from one branch into another, typically from a feature branch into the main branch.

    `git merge new-feature`
5.  **Push**: This command uploads changes from a local repository to a remote repository, making them available for others.

    `git push origin main`
6.  **Pull**: Pulling fetches updates from a remote repository and merges them into the local repository.

    `git pull origin main`

## Illustrative Example

Consider a project where three developers—Alice, Bob, and Charlie—are working on a web application. Each developer works on a different feature in a separate branch. Alice works on `navbar-feature`, Bob on `login-feature`, and Charlie on `signup-feature`. Using Git, each developer can work independently and commit changes without affecting the main branch. When Alice finishes her feature, she can merge it back into the main branch without disrupting the others.

{% embed url="https://www.youtube.com/watch?embeds_referring_euri=https://se.eforge.online/&source_ve_path=OTY3MTQ&v=hwP7WQkmECE" %}
Git Explained in 100 Seconds
{% endembed %}

## Git Features

**Version Control**: Git helps in managing different versions of a document, a set of files, or an entire project. It records changes over time, allowing you to view specific versions later.

**Distributed**: Every developer's working copy of the code is also a repository that can contain the full history of all changes.

* **Branching and Merging**: Git allows multiple developers to work simultaneously on different branches, maintaining different features or tasks, and then merge these changes into a main branch.
* **Data Integrity**: Git uses a data model that ensures the cryptographic integrity of every part of your project. Each file and commit is checksummed and retrieved by its checksum.
* **Speed and Efficiency**: Git is known for its performance. Operations like branching, merging, and comparing past versions are very fast.
* **Staging Area**: A unique feature of Git is the staging area or index. This is an intermediate area where commits can be formatted and reviewed before completing the commit.

**Free and Open Source**: Git is available freely under the GNU General Public License (GPL).
