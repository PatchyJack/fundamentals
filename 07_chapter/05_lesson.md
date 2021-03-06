**WDI Fundamentals Unit 7**

---

##Publishing Work on GitHub

So far, we've been making changes "locally," editing files and repositories on our own computers.

To collaborate with others (and back up our files just in case our computer goes out of commission), we need to connect our local repository to a "remote" repository.

### What is GitHub?

GitHub is a company, famous for the platform it built to manage Git repositories in the cloud. On GitHub, developers can share their code, comment on it, and review code changes among one another. It's an implementation of the same Git software you installed on your computer, but it also comes with some additional features.

In a lot of ways, GitHub is like Dropbox.

You have a folder in the cloud, your *remote repo*, which syncs with your computer. You can share this remote repo with others, grant them special permissions, and view different versions of your files.

Below is what the GitHub interface looks like for a repo called `awesome-project`:

1) **Repo Name and Owner**: describes who owns the repository, the name of the repo, and whether the repo is public or private.

	![Repo Name and Owner](../assets/chapter2/username_github.gif)

2) **Overview**: displays the number of commits, branches, releases, and contributors to a particular repo. Choosing any one of these options will open a detailed view of your selection.

	![Overview](../assets/chapter2/overview_github.gif)

3) **Repo File Structure**: displays the contents of the repo. Selecting any file or folder will open a detailed view of that file and allow you to edit its content directly.

	![File Structure](../assets/chapter2/contents_github.gif)

4) **Fork Button**: allows you to copy a version of this repo (`user/awesome-project`) to your own GitHub account.

	![Fork button](../assets/chapter2/fork_github.gif)

5) **Side Bar**: allows you to respond to issues, create pull requests, and change the settings for this repo.

	![Side bar](../assets/chapter2/sidebar_github.gif)

There are many unique GitHub features crammed on this page, but we'll only be starting with three.

---

## Our GitHub Flow

There are a few different ways to work together on GitHub, and our class is going to use a specific order of operations to do so.

The GA Instructional Team has put together some resources for you in a repository on GitHub. You'll need to retrieve these files and save a copy on your computer using Git.

Eventually, when you've made changes that you'd like to share with our team, you can submit them back to us via our GitHub repo.

Our workflow looks like this:
![GitHub Workflow](../assets/chapter2/github_workflow.gif)
<br><br>

This workflow consists of the following steps:

1) Forking
2) Cloning
3) Editing
4) Committing
5) Pushing
6) Submitting a pull request

**Don't worry**, we're going to cover this process step by step, in plenty of detail.

### 1) Forking

Let's walk through an example. Consider a project like Node.js, a JavaScript framework you'll learn about in this course. Node.js is completely open source, which means that anyone can read (and even copy) the code that makes it work — including you! The source code is publicly available [here](https://github.com/joyent/node) on GitHub. If you visit the main repo, you'll see that there are more than 400 contributors who have committed changes to Node.js.

<br>
![Node.js Contributors](../assets/chapter2/node.png)
<br>

Although it is open source and anyone can read or contribute to its code, Node.js is **maintained** by a company called Joyent. Not all of these 400+ contributors have the ability to edit the original Joyent repo — that wouldn't be very efficient or safe. Someone could accidentally make a change that conflicts with someone else's contributions, causing the code to break. Changes need to be inspected and approved before they can officially be added to the project.

To create a copy of Joyent's repo, you would need to **fork** it by clicking the button we highlighted above.

![Forking GIF](../assets/chapter2/fork_node.gif)

> **CAUTION** Don't follow these steps just yet. Read this chapter, and then you'll have a chance to try it out yourself in the [Unit 2 Assignment](09_assessment.md).

"Forking" adds a copy of someone else's GitHub repo to *your* GitHub account.

The forked repo is not perfectly identical, but it includes all of the same source files, issues, and commit history.

By forking Joyent's repo, you can have a full working copy of the Node.js source code to play with. When you break something, which you will (everyone does), Node.js won't be affected.

### 2) Cloning

Next, you'll want to be able to edit the code.

To make a local copy of a fork, you'll need to open up the terminal and use a Git command.

You should navigate to the place where you'd like to store the repo and then type:

```
git clone https://url/to/clone
```

You can find the URL to clone on the right side of the forked repo on GitHub:

![Node.js Clone](../assets/chapter2/node_clone.png)

By issuing the clone command, you're asking GitHub via the command line for a copy of your remote repo, and this copy, or **clone**, ends up in your working directory.

> **HINT** If you're following along in Git Bash in Windows, the commands to copy and paste are a little different than the default Windows copy/paste commands. The command to copy is `control + insert`, and the command to paste is `shift + insert`.

### 3 & 4) Editing and Committing

We covered this in the previous section. As you complete the exercises in the rest of Fundamentals, you'll need to repeat this step frequently.

### 5) Pushing

Once you've committed the changes you've made to the code, your local repo will be different than your remote repo. To update your remote repo on GitHub, you have to **push** those changes using the Git command `git push origin master`.

Don't worry about the `origin` and `master` components just yet.

If you're curious, here's a brief overview:
* `origin` is a shortcut for the URL of your default remote repo (in this case, the repo on GitHub). You can have many remotes if you want, but we'll only be working with one in Fundamentals.
* `master` refers to the **branch** of your remote repo where you're currently adding changes. Again, for now, we'll only be working on the `master` branch.

### 6) Submitting a Pull Request

Once your changes are pushed to your remote repository on GitHub, you can notify the original repo owner of your changes by submitting a **pull request**.

A pull request is effectively saying "Hello, maintainer of project X, I made some changes here in my forked copy, and I think they're pretty good. You should add them to your repository." Pull requests are a GitHub feature, so you'll need to head back to the browser to make this happen.

We'll cover how to submit a pull request in a later chapter.


## Confused?

If you ever get stuck working with Git or GitHub, don't worry, you are NOT the first. When you don't understand something, we encourage you to follow this three-step process:

1) Search online for an answer via Google or [Stack Overflow](http://stackoverflow.com).
2) Ask classmates if they've solved a similar problem via [Slack](https://ga-students.slack.com/).
3) Seek out help from an instructor (they are also on Slack).

Trust us — you *will* get to the point where cloning and pushing are like breathing and sleeping.

---

[Here's another exercise for you](07_exercise.md) — give it a shot!
