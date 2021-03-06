**WDI Fundamentals Unit 7**

---

## Get Started with Git

###Initialize a Repository

To turn an ordinary directory into a Git repository (or *repo*, for short), you have to **initialize** the repository. This just means adding a hidden folder called `.git/` to your project folder, which contains all the data Git needs to operate.

Simply change your working directory to the folder you'd like to track, and run the command:

```
$ git init
```
> **CAUTION** Do not execute this command in your **home directory**! It will make it difficult to work with any other repositories. Use `pwd` to check your location if you're unsure.

When you take a look at your working directory in the GUI, you probably won't see any additional files, because (if you remember from Unit 6) hidden files are not visible on your computer by default. To see the `.git/` directory, you need to run `ls -a` from the command line.

If you delete the hidden `.git` directory, you will effectively "uninitialize" your repository and lose the data Git has collected for you.

> **CAUTION** You should never manually change the internal contents of your `.git` directory, unless your name is Linus Torvalds.

### Saving Changes to Your Project

Unfortunately, it's not enough to simply house your files in a repo. Like the terminal, Git doesn't make any assumptions about the changes you want to save or when you want to save them — you need to explicitly tell it what to do.

Suppose that we want to work on a blog post for General Assembly, so we create a directory on our desktop called "GA-Blog," and run `git init` from inside that directory. At the moment, this project is empty. We can confirm this by running `git status`, which asks Git to give us an update on the status of our project.

```
$ git status
```

We should get a response like this:

![Git Status of GA-Blog](../assets/chapter2/git_status.gif)

Each "save" we make to our repository is called a **commit**. The message above tells us that our project has no unsaved changes.

Let's go ahead and make a new text file called `post.txt` inside of `GA-Blog` using the `touch` command.

```
$ touch post.txt
```

Now, let's check our Git status:

![Git Status of GA-Blog](../assets/chapter2/git_status_untracked.gif)

Git has identified that a change has been made: There is now a file in our repo. However, it does not know if we want to save that change right now. To add this change to our next commit, we can run the command:

```
$ git add post.txt
```
The changes we've just made have now been *staged*, or added to the list of changes that will be officially saved with our next commit. However, this list is not final, and any of these changes can be taken off the list, or *unstaged*. If we run `git status` again, we'll see that the addition of `post.txt` is staged and ready to be committed:

![Git Status of GA-Blog](../assets/chapter2/git_status_staged.gif)

> **NOTE** Sometimes, you'll want to save *all* of the changes to files that have been made inside your repo. Instead of specifying a unique file, you can write `git add .`. This will add all of the files in the working directory to the next commit. Be careful, however, when using `git add .` — you could accidentally add files with sensitive information.

Once we're ready to officially record this version of our project, we can type:

    $ git commit -m "created a new post.txt file"

The `-m` option allows you to include a message describing the changes you made for your collaborators — or your future self. These should be short but descriptive, clearly indicating what changes each commit makes to the project.

###The Git Staging Area

One of the unique features of Git is its "Staging Area." Git allows you to add changes to the local repo in two steps:

```
$ git add <your-file-name>
$ git commit -m "message"
```

Why stage? So that, if you make multiple changes, you can commit them separately or all at once. (Basically, it exists to help you better organize your project history).

![Git Staging Area](../assets/chapter2/add_commit.png)



### Your Commit History

When you're farther into your project and have made many commits to your repository, you may want to look back and see a timeline of your changes. Git allows you to view a list of commits, along with the date the commit was submitted, the author of the commit, the commit message, AND a unique number to identify the commit by, known as an SHA. This unique number allows Git to remember each commit. (A 40-digit code is easier for Git than "Version1.txt" or "Draft-01-2014.txt").

To view the timeline of changes, you can run:

```
 $ git log
```

This will yield a list of entries that looks like this:

```
commit 6d33f525a09b9918f75188db164ea2722039830b
Author: Sarah <sarah@gmail.com>
Date:   Wed Jan 28 17:44:03 2015 -0500

    added a new post

```

Each of these entries represents a commit for this project and provides other useful information including: when the commit was made; who made the commit; and, if a message was included, a description of the code being committed.

---

[Here are some more exercises to help you practice.](04_exercise.md)
