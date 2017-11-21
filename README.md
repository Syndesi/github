# How tu use GitHub

Prerequisites: The following commands require the program git, which you can get [here](https://git-scm.com/downloads) or as part of the [GitHub Desktop](https://desktop.github.com/) program.

## Clone a repository

```shell
git clone https://github.com/Syndesi/github
```

After that GitHub will copy everything and save it in a newly generated folder, *github*.

## Keep the local repository up-to-date

Because good software will get updated, your local repository will get outdated at some point. To avoid this you can download all changes automatically. Just open the Shell/Terminal in your *github*-folder and execute this command:

```shell
git pull
```

## Force a local update

Should there be errors, e.g. because an updated file would erase your changes, you can force GitHub to overwrite your local files. Execute therefore this command in the *github*-folder:

```shell
git fetch --all
git reset --hard origin/master
```

## Upload your changes to the GitHub repository

First at all, you need the permission to do that. You can get it from the project owner.<br>
If you got it, then execute the following commands:

```shell
git add .
git commit -m ‘describe your update here’
git push -u origin master
```

## Don't upload changes to one specific file in the repository (e.g. config-file)

To have a file in the repo which can be modified, but not uploaded again, use the following command:

```shell
git update-index --assume-unchanged FILE_NAME
```

Remove this behavior with this command:

```shell
git update-index --no-assume-unchanged FILE_NAME
```

## Create a new branch

```shell
git checkout -b [name_of_your_new_branch]
```

## Change working branch

```shell
git checkout [name_of_your_new_branch]
```

## Upload to different branch

```shell
git push origin [name_of_your_new_branch]
```

## Merge branches

```shell
git checkout master
git merge --squash dev
```


## List all branches

```shell
git branch
```

## Delete branch locally

```shell
git branch -d [name_of_your_new_branch]
```

## Force deleting branch locally

```shell
git branch -D [name_of_your_new_branch]
```

## Delete branch on Github

```shell
git push origin :[name_of_your_new_branch]
```

---
[Used this tutorial for reference](https://github.com/Kunena/Kunena-Forum/wiki/Create-a-new-branch-with-git-and-manage-branches).
