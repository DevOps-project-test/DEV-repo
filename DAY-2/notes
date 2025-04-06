# Difference Between `git add .` vs `git add *` and `git reset` vs `git revert` in Git

Git is a powerful version control tool that helps developers keep track of changes in their codebase. However, some Git commands can be confusing, especially when there are subtle differences in their usage. In this blog, we'll explain the differences between:

- **`git add .` vs `git add *`**
- **`git reset` vs `git revert`**

We will also include simple examples and flowcharts to help you better understand how each command works.

## Table of Contents:
1. [Introduction](#introduction)
2. [Difference Between `git add .` and `git add *`](#difference-between-git-add-and-git-add-)
3. [Difference Between `git reset` and `git revert`](#difference-between-git-reset-and-git-revert)
4. [Conclusion](#conclusion)

---

## Introduction

Git is an essential tool for version control, used by developers to manage and track changes in their code. Whether you are new to Git or a seasoned developer, it's important to know the subtle differences between similar commands.

In this blog, we’ll focus on the differences between two pairs of Git commands:
- **`git add .` vs `git add *`**
- **`git reset` vs `git revert`**

By the end of this post, you’ll have a clear understanding of when and how to use these commands with real-life examples.

---

## Difference Between `git add .` and `git add *`

Both `git add .` and `git add *` are used to stage files for commit, but they work differently. Here's a breakdown:

### `git add .`
- **What it does**: 
  - Stages all modified files, new files, and even deleted files in the **current directory** and all **subdirectories**.
  - It also includes **hidden files** (files that start with a dot `.`).

- **Example**: 
    ```bash
    git add .
    ```

    This command stages all files and directories (including hidden ones) in the current directory and subdirectories.

- **When to use**: 
  - Use `git add .` when you want to stage all changes (including new, modified, and deleted files) across the entire project directory, including any hidden files.

---

### `git add *`
- **What it does**: 
  - Adds all **non-hidden** files and directories in the current directory to the staging area.
  - **Does not include hidden files** (files starting with `.`).
  - It may also behave differently depending on the shell you're using (e.g., on Linux, it might skip directories).

- **Example**: 
    ```bash
    git add *
    ```

    This command adds all files and directories in the current directory but **won't add hidden files** or files in subdirectories.

- **When to use**: 
  - Use `git add *` if you are only concerned with adding **non-hidden files** in the current directory.

---

### Key Differences in a Flowchart:

```plaintext
+----------------------------+
|        git add .            |
+----------------------------+
| Stages files in the current|
| directory and all subdirs.  |
| Includes hidden files.      |
+----------------------------+

         |
         v

+----------------------------+
|        git add *            |
+----------------------------+
| Stages files in the current|
| directory only (excludes   |
| hidden files and subdirs).  |
+----------------------------+
Difference Between git reset and git revert
Both git reset and git revert are used to undo changes, but they behave in completely different ways. Let’s break them down:

git reset
What it does:

Moves the HEAD pointer to a previous commit.

It can modify the staging area (index) and the working directory depending on the flags used.

Types of reset:

--soft: Resets HEAD to the previous commit but keeps your changes staged.

--mixed (default): Resets HEAD, unstages changes but leaves them in your working directory.

--hard: Resets everything — HEAD, staging area, and working directory. All changes are lost!

Example:

bash
Copy
git reset --hard HEAD~1
This command will:

Move HEAD to the previous commit (HEAD~1).

Discard all changes (both staged and unstaged) in your working directory.

When to use:

Use git reset when you want to completely undo local changes or move your commit history backward. Be careful with --hard, as it can delete your work!

git revert
What it does:

Creates a new commit that undoes the changes introduced by a previous commit.

It does not change commit history, so the commit history remains intact.

This command is used to undo changes in a way that keeps the history clean, especially when you've already pushed commits to a shared repository.

Example:

bash
Copy
git revert <commit_hash>
This will create a new commit that undoes the changes made in the specified commit.

When to use:

Use git revert if you want to undo a commit that has already been pushed and you want to keep the history intact.

Key Differences in a Flowchart:
plaintext
Copy
+----------------------------+
|        git reset            |
+----------------------------+
| Resets the current branch   |
| to a specific commit.       |
| Can rewrite history (dangerous)|
+----------------------------+
         |
         v
+----------------------------+
|        git revert           |
+----------------------------+
| Creates a new commit that   |
| undoes a previous commit.   |
| History is preserved.       |
+----------------------------+
Conclusion
Quick Recap:
git add . vs git add *:

git add . stages all changes (including new, modified, and deleted files) in the current directory and subdirectories, including hidden files.

git add * stages only non-hidden files in the current directory.

git reset vs git revert:

git reset rewrites history by moving the HEAD pointer, which can be dangerous if done after pushing commits. It can discard changes in your working directory.

git revert creates a new commit that undoes changes, preserving history. It’s safe to use, especially for commits that have been pushed.

By understanding these commands, you'll be able to make better decisions when managing your code with Git. Use the appropriate command depending on the situation to ensure smooth collaboration and version control.

Happy coding! 😊

pgsql
Copy

This `.md` format is clean, easy to read, and beginner-friendly. It explains the c
