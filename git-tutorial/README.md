We're going to try playing around with Git by having everyone mess around with this repository ("repo"). First everyone will clone the repo, and then submit a change.

# Fork & Clone the Repo
"Forking" a repo means making a copy of it. Conventionally, the original repo is referred to as `upstream`, while the fork is known as `origin`.

"Cloning" a repo means taking a snapshot of the code stored remotely (in this case on GitHub) and downloading it to your computer. The code stored on GitHub is `remote`, and the code on your computer is `local`.

## Create a directory to put the code into
Open up your terminal (⌘+Space and search for "Terminal").

1. Navigate to your root directory (`~/`), and create a folder named `code`.
    <details>
    <summary>Click the dropdown to see the commands (but try it yourself first!)</summary>

    ```
    cd ~/; mkdir code
    ```
</details>

2. Navigate into the `code` directory.
    <details>
    <summary>Click the dropdown to see the commands (but try it yourself first!)</summary>
    
    ```
    cd code
    ```
</details>

## Fork the Repo
Follow the directions [here](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/fork-a-repo#fork-an-example-repository) to fork and clone this repo. Instead of `Spoon-Knife`, you will be forking: https://github.com/rupalivohra/teched-cmd-git.

Complete the steps in "Fork an Example Repository" and "Keep Your Fork Synced."

### Tips
* When cloning, use the `HTTPS` link. You'll probably be prompted for your GitHub credentials, so make sure you have those handy!

# Submit Your First PR!
In this tutorial, you're going to learn how to do the following:
1) Create a `branch`.
2) Commit code.
3) Create & merge a pull request (PR).
4) *bonus: merge conflicts*.

## Create a Branch
The default branch on a repo is called "`master`" (to be defaulted to "`main`" later this year). You can see which branch you're on right now by entering `git branch` into the command line.

It's good practice to work off of feature branches and submit PRs to check your code into `master`. This allows an opportunity for other people to look at and comment on your changes ("do a code review"), and for you to make revisions until you're ready to check in your changes for everyone to use.

Create out a new branch:
`git checkout -b yourBranchName`

## Add to a File
Open up the file `oct09.txt`, and make a change to it. Add a line, make a joke, write a poem.

## Commit Your Changes
You can see the file you've changed on the command line. The change will show up in red with the word "modified" next to it, under a heading that says, "Changes not staged for commit":

`git status`

These changes are now `modified` and `unstaged`. To commit them, you must `stage` them:

`git add oct09.txt`

If you check `git status` again, you should see the file under the heading "Changes to be committed." You are ready to make the commit! Good commits have an informative message:

`git commit -m "Your awesome commit message goes here!"`

One more time, check out the `git status`. You'll see that "your branch is ahead of 'origin/featureBranchName' by 1 commit, and that those modified files are no longer listed out.

## Create a PR

### Push Your Code to Remote
The first time you push your code to `remote`, you will need to let Git know that you're creating a new branch on the remote. You can do that by doing the following:

`git push -u origin featureBranchName`

Any future time you want to push code, all you have to do is type `git push`.

### Make the PR
Go back over to `github.com` to the upstream repo. Follow the instructions [here](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request-from-a-fork) to submit your first PR!

### Merge Your PR
Wait for approval on your PR, and then "Squash and Merge" it (instructions [here](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/merging-a-pull-request)).

## Resolve Merge Conflicts
Merge conflicts happen when two people try and modify the same lines in a file at the same time. Since all of you are modifying the same file at once, it's very likely that whoever comes second will need to resolve merge conflicts.

There are some good instructions [here](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/resolving-a-merge-conflict-using-the-command-line) for resolving them.

