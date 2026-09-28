# UCI Kit Mouse (2026-2027 Ver.)

This repository contains:
 - A template kit mouse project with KiCad
 - Short installation guide for the overall project
 - Helpful Git Commands

> [!IMPORTANT]
> Contents here are summarized from [IEEE@UCI Micromouse Website](https://ieee.ics.uci.edu/micromouse/mm_index.html).
> More details of the tools installed will be under "Modules" and "Lectures."

## Prerequistes


### KiCad
> [!NOTE]
> All teamates should install the same version of KiCad, preferably the newest
> stable release here: https://www.kicad.org/download/. 
> Files modified from newer versions can no longer be read by older versions.

*The installation guide will be using KiCad ver. 10.5*

<details>
<summary><b>Windows</b></summary>

1. Download and Launch the installer: https://www.kicad.org/download/windows/

<img src="img/kicad-windows1.png" width="500">


2. Select **Next** 2 times, and give permissions to the installer.

3. At "Choose Components," make sure all check boxes are selected 
(should be default)

<img src="img/kicad-windows2.png" width="500">

4. Select **Next**, and then install.
</details>

<details>
<summary><b>macOS</b></summary>

1. Download the installer: https://www.kicad.org/download/macos/

2. Double-click `kicad-unified-universal-#.#.#.dmg` file in finder

<img src="img/kicad-mac1.png" width="600">

3. Click and drag the `KiCad.app` to Application folder.

<img src="img/kicad-mac2.png" width="300">


4. Close the window, and Eject the `.dmg` file from Finder.

<img src="img/kicad-mac3.png" height="300">
</details>

<details>
<summary><b>Linux</b></summary>
Install as an AppImage or use your desired package manager. <br></br>

> [!NOTE]
> KiCad does not support Wayland,
> but the AppImage version defaults to Wayland instead of 
> Xwayland under GTK3. Installing via PPAs instead defaults to Xwayland, 
> likely bringing graphical bugs.

</details>

---
### Git
Check if Git is installed with this command:
```sh
git --version
```

If git is missing, here are official steps in 
[installing Git](https://git-scm.com/install/), and
a recommended step-by-step installation will be provided below.


<details>
<summary><b>Windows</b></summary>

1. Install **Git for Windows** from this link: [https://git-scm.com/install/windows](https://git-scm.com/install/windows).

<img src="img/git-windows0.png" width="550">

2. After installing the executable, give the installer permissions.

<img src="img/git-windows1.png" width="400">

3. Select **Next** 4 times, and reach "Choosing the default editor used by Git"

<img src="img/git-windows3.png" width="600">

Choose your favorite editor, and after setup you can still change the 
default editor with this command:
```sh
git config --global core.editor "editor-name"
```

4. Select **Next** to "Adjusting the name of the initial branch in 
new repositories"
- Use default branch name as `main`, since GitHub defaults to `main` as well.

<img src="img/git-windows4.png" width="600">


5. Keep selecting **Next** and finish installing.



</details>

<details>
<summary><b>macOS</b></summary>

Install **Xcode Command Line Tools** from Apple for `git` and other tools:
```sh
xcode-select --install
```
... and more info about what is downloaded is [here](https://developer.apple.com/documentation/xcode/installing-the-command-line-tools/).


If you prefer installing ONLY `git` with `homebrew`, here is the command:
```sh
brew install git
```
</details>

<details>
<summary><b>Linux</b></summary>

Install `git` with package manager or build from source, 
as seen from this site: [https://git-scm.com/install/linux](https://git-scm.com/install/linux).
</details>

---


#### Setting up GitHub Authentication

Source: [https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-authentication-to-github](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/about-authentication-to-github)

After installing git, you need to configure a few things before being
able to edit your remote repositories on GitHub.

> [!NOTE]
> If Authentication is via GitHub Desktop, Git environment (in cli) does
> not also get authentication.
<details>
<summary><b>GitHub Desktop</b></summary>
Source: 

[https://docs.github.com/en/desktop/installing-and-authenticating-to-github-desktop/authenticating-to-github-in-github-desktop](https://docs.github.com/en/desktop/installing-and-authenticating-to-github-desktop/authenticating-to-github-in-github-desktop)

1. Install and Run GitHub Desktop: https://desktop.github.com/download/

2. Login or Create your GitHub account, and authorize access:

<img src="img/github-desktop1.png" width="600">

<img src="img/github-desktop2.png" width="300">

3. Setup your Git Username and Email
   - Select "Configure Manually" if `user.email` 
     and `user.name` have been setup before

<img src="img/github-desktop3.png" width="600">

</details>

<details>
<summary><b>GitHub CLI</b></summary>

Source: 
 - https://cli.github.com/manual/gh_auth_login
 - https://docs.github.com/en/github-cli/github-cli/quickstart#prerequisites
<br></br>
1. Install GitHub CLI with this link: https://cli.github.com/
2. Follow the prompts below:
   - Authentication with HTTPS, so authentication automatically
       used for HTTPS repo clones
   - `.gitconfig` will be modified

<img src="img/github-cli1.png" width="800">


</details>

<details>
<summary><b>Personal Access Tokens</b></summary>

Source: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens
</details>


---


#### Other Git Tools
For a GUI experience, try out these software:
 - Connecting GitHub to VS Code, and utilizing [Source Control](https://code.visualstudio.com/docs/sourcecontrol/overview)


## Cloning This Repository

<details>
<summary><b>GitHub Desktop</b></summary>

Source: [https://docs.github.com/en/desktop/adding-and-cloning-repositories/cloning-a-repository-from-github-to-github-desktop](https://docs.github.com/en/desktop/adding-and-cloning-repositories/cloning-a-repository-from-github-to-github-desktop).

1. At the top of this page, click the green button labled **<> Code**

<img src="img/clone1.png" width="600">

2. Then select **Open with GitHub Desktop**

<img src="img/github-desktop-clone1.png" width="500">

3. Choose where the local Clone Repo location, and then press **Clone**

<img src="img/github-desktop-clone2.png" width="500">

</details>

<details>
<summary><b>On Terminal</b></summary>

Source: [https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository).

1. At the top of this page, click the green button labled **<> Code**

<img src="img/clone1.png" width="600">

2. Copy the clone link as HTTPS

<img src="img/clone2.png" width="500">

3. Open your terminal, change directory to somewhere you want to put your 
local repository in.

4. Type `git clone`, then paste and run the command:
```sh
$ git clone https://github.com/Maahi-V/26-27-UCI-Kit-Micromouse.git
>   Cloning into '26-27-UCI-Kit-Micromouse'...
>   remote: Enumerating objects: 135, done.
>   remote: Counting objects: 100% (135/135), done.
>   remote: Compressing objects: 100% (78/78), done.
>   remote: Total 135 (delta 69), reused 118 (delta 52), pack-reused 0 (from 0)
>   Receiving objects: 100% (135/135), 3.28 MiB | 12.25 MiB/s, done.
>   Resolving deltas: 100% (69/69), done.
```
</details>




## Push Local Repository into a GitHub Remote Repository (Initial)

<details>
<summary><b>GitHub Desktop</b></summary>

1. Find you local git repository in your file manager, and make sure you 
   have hidden files enabled
   - Windows: In File Explorer, go to View -> Show -> Hidden Items
   - macOS: In finder, use `Cmd + Shift + .` to show hidden files

<img src="img/new-repo4-1.png" width="500">

<img src="img/new-repo4-2.png" width="500">

2. Delete the `.git` folder (contains the local repo edit history) and 
   revert the local repository back to a normal folder
   - After cloning the repository, it still has commits made by other 
     people. To start fresh, these commits needs to be deleted

3. GitHub Desktop should now have an error popup, and **"Remove"** this repo
   to stop tracking it

<img src="img/new-repo-desktop1.png" width="700">

4. Select **Add an Existing Repository from your Local Drive...**

<img src="img/new-repo-desktop2.png" width="700">

5. Find the location of the local repo (default location is `~/Documents/GitHub/`), and
   press **Add Repository**

<img src="img/new-repo-desktop3.png" width="400">

6. Now select **create a repository**

<img src="img/new-repo-desktop4.png" width="400">

7. GitHub Desktop automatically fills out everything required. Keep
   everything as default and select **Create Repository**

<img src="img/new-repo-desktop5.png" width="400">

8. After creation, GitHub Desktop would automatically create a commit.
   Select the **Publish repository** to create a new remote repo

<img src="img/new-repo-desktop6.png" width="600">

9. Insert a name and description of the project, and select **Publish Repository**

<img src="img/new-repo-desktop7.png" width="400">

10. Now you can view your repository on browser as well

<img src="img/new-repo-desktop8.png" width="600">


</details>



<details>
<summary><b>With `github.com` and Terminal</b></summary>

1. Go to your GitHub Dashboard (at [https://github.com/](https://github.com/) and login),
and press the **+** button, then **New repository**

<img src="img/new-repo1.png" width="500">

2. Configure your repository to whatever you like, just make sure
   these 2 settings are set (since cloned repo already has a README
   and `.gitignore` configured)

<img src="img/new-repo2.png" width="500">

3. Now you should see **Quick Setup**, but the local repository
   needs to be modified a bit before being pushed to the remote
   server.

<img src="img/new-repo3.png" width="700">

4. Go back to your local git repository, and make sure you have
   hidden files enabled
   - Windows: In File Explorer, go to View -> Show -> Hidden Items
   - macOS: In finder, use `Cmd + Shift + .` to show hidden files

<img src="img/new-repo4-1.png" width="500">

<img src="img/new-repo4-2.png" width="500">

5. Delete the `.git` folder (contains the local repo edit history) and 
   revert the local repository back to a normal folder
   - After cloning the repository, it still has commits made by other 
     people. To start fresh, these commits needs to be deleted

6. Copy-paste this command to create a new local git repository: 
```
git init
git add -A
git commit -m "First Commit"
```

7. Then go back to GitHub, and copy-paste the commands under 
 **…or push an existing repository from the command line**

<img src="img/new-repo5.png" width="700">

8. Reload the GitHub page, and your remote repository should now
   show up


</details>


> [!TIP]
> Update and personalize this README page! Feel free to edit/replace 
> the README.md to be about your project instead.


## Push Local Edits to Remote Repository

When sharing edits to other teamates, users have to use `git push` 
push/share their local edits to the remote repository. 

Teamates then need to use `git pull` to obtain 
the new edits to their local repository.

The example below has the following local edits:
 - `README.md` file modified
 - New file `temp.txt`

When pushing edits to the remote server, *you can control what remote file
gets updated* by staging the local files you want to be updated.

In this example ONLY the `README.md` edits are shared, 
and `temp.txt` is not shared.

<details>
<summary><b>GitHub Desktop</b></summary>
1. GitHub Desktop should have an overview of the local edits made.

Here is `README.md`

<img src="img/push-desktop1.png" width="700">

... and here is `temp.txt`

<img src="img/push-desktop2.png" width="700">

2. Only the `README.md` file should get updated, so unstage `temp.txt` 
   by unchecking this box at the left

<img src="img/push-desktop3.png" width="700">

The bottom **Commit 2 files to main** button should now change to **Commit 1 file to main** instead

<img src="img/push-desktop4.png" width="200">

3. Write a Commit Message and Description, and press **Commit 1 file to main** 
   to create a new commit
   - Commits are saved as an edit history
   - Use commits as a checkpoint completed, and to organize the work you made
   - This commit is only recorded locally
   - Commit Summary: Write a concise change made, and easy to understand
   - If needed, add more details in Commit Description

<img src="img/push-desktop5.png" width="300">


Edits from `temp.txt` has not been recorded/commit, so GitHub Desktop
still display the file

<img src="img/push-desktop6.png" width="700">

4. Now push your local commits to origin (the remote server)
 - Recommended to push multiple commits at once, instead of commit once then immediately push.
 - It is easier to fix mistakes in local commits that are not pushed yet, 
   or to squash multiple local commits into one for a cleaner commit history

<img src="img/push-desktop7.png" width="700">



</details>

<details>
<summary><b>On Terminal</b></summary>

1. Check overall status of the local repo with `git status`
 - Modified File: File already on remote server, but locally is edited
 - Untracked files: New file not tracked by remote server
```
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	temp.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

2. Only stage `README.md` with `git add <file>`
 - Also you can stage all files with `git add -A`
```
$ git add README.md
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	temp.txt
```

3. Create a commit with `git commit`, and use `-m` to append the commit
   message
```
$ git commit -m "Modified README.md"
[main 7311eae] Modified README.md
 1 file changed, 1 insertion(+)
```

Now local repo should be ahead of `origin/main` (since local repo has newer commits than remote repo),
and `temp.txt` is not included in the commit
```
$ git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	temp.txt

nothing added to commit but untracked files present (use "git add" to track)



$ git whatchanged
commit 7311eae2b4a877c8229590e44fe4e0f08f418967 (HEAD -> main)
Author: Justin Chen <justin7.chen@gmail.com>
Date:   Mon Sep 28 00:05:22 2026 -0700

    Modified README.md

:100644 100644 404fe81 91129e9 M        README.md
```

4. Now push your local edits to remote server with `git push`
```
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 279 bytes | 279.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/hippoBus/testin.git
   0ab9dcf..7311eae  main -> main
```


</details>


## Pull Remote Edits to Local Repository

<details>
<summary><b>GitHub Desktop</b></summary>

1. If available, select **Fetch Origin** to check if there are any new
   remote edits

<img src="img/pull-desktop1.png" width="700">

2. Detected that the remote repository is updated, button becomes **Pull Origin**

<img src="img/pull-desktop2.png" width="700">

3. Now the local repository is updated. Check **History** to see what
   edits are made

<img src="img/pull-desktop3.png" width="700">

</details>



<details>
<summary><b>On Terminal</b></summary>

1. Check if there are any remote changes with `git fetch`
  - No changes, `git fetch` results without any output
```
$ git fetch
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 908 bytes | 151.00 KiB/s, done.
From https://github.com/hippoBus/testin
   7311eae..97050af  main       -> origin/main
```

2. Obtain new changes and rebase to edits in `origin/main` with `git pull`
```
$ git pull
Updating 7311eae..97050af
Fast-forward
 README.md | 3 +--
 1 file changed, 1 insertion(+), 2 deletions(-)
```


</details>


## Helpful Git Commands

For more details, use the `man git` command or use the official
documentation: [https://git-scm.com/docs](https://git-scm.com/docs).
```sh
git status
```

```sh
git log
```

```sh
git reflog
```

```sh
git fetch
```

```sh
git pull
```

```sh
git add
```

```sh
git diff
```

```sh
git push
```

```sh
git rebase
```

```sh
git branch
```

```sh
git switch
```

```sh
git checkout
```

## How to Submit on Canvas/Gradescope

