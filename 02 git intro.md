# 2. Git Intro

In this chapter, we'll learn how to create a git repository and keep track of changes to our documents using commits.

## Opening the git client

The git client we'll be using to manage our document history is called **GitFiend**. Its icon is a little purple owl. You can open it by clicking the start menu (1), typing 'gitfiend' (2) (note that it's all one word), and selecting the owl icon that comes up (3) :

![image-20230427160606408](assets\git-gui-open.png)

## Creating a new repository

A repository is a folder within which Git will track file changes.

From the start screen of GitFiend, click `Create` (circled in red):

![image-20230427160824772](assets\git-create-1.png)

The next window will ask you to name the repository. First, make sure the repository will be created on your computer's desktop by confirming that the `Location` text ends with `Desktop\`. If it doesn't, click `Browse` and select the desktop folder (1) . Regardless, enter a name for your repository (2) and then click `Create Repo` (3):

![image-20230427160915833](assets\git-create-2.png)

This will create a new, empty folder on our desktop that we can put files in just like any regular old folder. GitFiend will now show us the repository "history", which is currently empty:

![image-20230427161220576](assets/git-history-empty.png)

Let's take a look at the repository using Windows Explorer. Minimize the `Git Fiend` window, and find the folder on your desktop that GitFiend just created. Its name will be the same thing you entered in the `Name` box when creating a new repository. Double-click it to open it:

![image-20230427161640037](assets/git-desktop-repo.png)

![image-20230427161735617](assets/empty-repo.png)

Any files we place in here will be monitored by GitFiend. Note the folder `.git`, which is the location that `GitFiend` actually stores the modification history and settings for the repository. In general, we don't want to open or modify the `.git` folder. Doing so could corrupt our document histories.

## Adding files

Let's move our markdown file into the repo!

Click the markdown file we saved on the desktop (1), and copy it by pressing `Control + C`. Then, click the repository folder area (2) and paste the file by pressing `Control + V`:

![image-20230427162133073](assets/image-20230427162133073.png)

Alternatively, you could move the file in by clicking and dragging. If you added any images to your markdown document, make sure you copy/move them into this folder as well.

Now, let's return to GitFiend. We can see that it has observed new files in the repository. Click the area circled in red for details:

![image-20230427162431302](assets/git-new-files.png)

Indeed, the files it sees are the ones we just copied into our repository folder. The green "`A`"s indicate these files are brand new to the repository and have no prior history recorded by Git:

![image-20230427162509040](assets/git-new-files-2.png)

Let's click the `Changes` button at the top of the screen  (1) to see more details. We can select specific files form the pane on the left (2), and see a description of what about them has changed on the right (3):

![image-20230427162803914](assets/git-changes-pane.png)

In this case, since they're new to the repository, GitFiend is telling us that every line of text is a new addition (highlighted in green).

We can record the state of the folder at this moment in history by giving it a description in the bottom left (1) and clicking the `Commit` button  (2):

![image-20230427163045048](assets/git-commit-1.png)

GitFiend will now return to the `Commits` screen, which shows our repository history. We can see that this version of the repository is now present in the timeline:

![image-20230427163134503](assets/git-timeline.png)

You can view the details about this "commit" (this moment in history) by clicking the commit description and then clicking the expand button in the top-right of the commit box, circled in red:

![image-20230427163432950](assets/git-commit-deets.png)

From here, we see a read-only version of that "`Changes`" screen we were just using. We can always return to the timeline of changes by clicking "`Commits`" at the top of the screen, circled in red here:

![image-20230427163531511](assets/image-20230427163531511.png)

## Making Changes

Let's see how Git keeps track of file changes.

Start by opening GhostWriter, selecting the File menu (1) and selecting Open (2):

![image-20230427163706449](assets/image-20230427163706449.png)

Find your repository folder, navigate into it, and then open the markdown file you placed in there:

![image-20230427163808231](assets/image-20230427163808231.png)

Make sure that you're opening the file in the git repository, and not a copy somewhere else on your computer. You can be sure by checking that the `".git"` folder is also present on the file selection screen.

Now, let's change an existing line of text in the file. Select some text in the source pane on the left, change it, and then save the document by pressing `Control + S`:

![image-20230427164050947](assets/git-mod-file.png)

GitFiend has observed the change! Go back to the GitFiend window, make sure `Commits` is selected at the top, and then click `2 Changed Files` to view change details:

![image-20230427164234511](assets/changes.png)

We'll see a yellow `M` indicating that our markdown file has been altered, and also a new file ending in `.backup` has appeared. This is Ghostwriter helpfully keeping a backup of our document in case we shut our computer down without saving, which leads to an important point: **this backup file is a feature of Ghostwriter, not Git**, and so if we use other tools to edit our Markdown this backup file likely won't appear.

Anyway, let's take a closer look at our changes by clicking the 'Changes' button at the top:

![image-20230427164550995](assets/image-20230427164550995.png)

From this "changes" screen, we can see that the old version of the line was deleted (the red highlighted region), and the new version of the line was added (the green region). This view of the file and how it has changed is called a "**diff**" (short for "difference").

Let's commit this change. Using the checkboxes next to filenames and individual changes, we can choose what parts of these modifications we want Git to remember at this moment in history, and what parts we want it to ignore.

Let's tell it *not* to remember Ghostwriter's backup file by unchecking the filename ending with ".backup" in the file list (1). Then, let's write a quick commit message (2) and click the commit button (3):

![image-20230427165019219](assets/git-new-commit.png)

Return to the `Commits` screen by click the button at the top of the window. Now we can see there are two commits in our repository's history:

![image-20230427165122482](assets/image-20230427165122482.png)

Clicking on them will show what changes were made at that point in time.