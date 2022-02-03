# github-demo

This is a demo GitHub repository for introducing students to Git and GitHub. You will need a GitHub account to proceed. Make sure you [login](https://github.com/login) or [register](https://github.com/signup). 

Please take a moment to notice that the registration page acts like a command line! That's kind of awesome!

![GitHub Registration](https://raw.githubusercontent.com/codeadamca/github-demo/main/screenshot-register.png)

## Initial Setup

There are two possible scenarios when setting up a project and a Git repository:

### Brand New Project

If you are starting a brand new project that does not have a GitHub repository you will need to follow these steps:

1. Register or login to your GitHub account.

2. Create a new GitHub repository. Give it a title using lowercase letters and dashes. Make it ```Public``` and Click ```Add a README file```.

![New Repository](https://raw.githubusercontent.com/codeadamca/github-demo/main/screenshot-new-repo.png)

3. On the new repository page click the green ```Code``` button and copy the repository URL.

![Copy URL](https://raw.githubusercontent.com/codeadamca/github-demo/main/screenshot-code-url.png)

4. Open up the Terminal or Command Prompt. If you do not have Git installed, [download and install GIT](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

5. Navigate to the folder you want to place your project in. To navigate folders use the following commands:

```
# Change directoy
cd repository-name
# Go back a folder
cd ..
# Go to the root drive
cd /
```

6. In your working folder clone your new repository:

```
git clone https://github.com/<YourUserName>/<RepositoryName>
```

7. This will create a new folder using the repository name. Change the direftory to that new folder:

```
cd <repositoryName>
```

You are now setup and ready to follow the development cylcle instructions below.

### Existing Project

If the repositry already exists and you want to contribute to the project follow these steps:

1. Provide your uasername to the programmer who owns the project. The owner will need to login to their GitHub account and follow these steps:

 - Navigate to the repository
 - Click ```Settings```
 - Click ```Collaborators```
 - Click the ```Add People``` button
 - Enter the username
 - Click ```Add <UserName> to this repository```

![Collaborator](https://raw.githubusercontent.com/codeadamca/github-demo/main/screenshot-add-user.png)

2. You will receive an email with the invitation details. Click ```View Invitation``` in the email and then ```Accept Invitation``` in the browser. You are not a contributor!

3. Navigat to the repository. Click the ```Code``` button and copy the repositry URL. 

4. Open up the Terminal or Command Prompt. If you do not have Git installed, [download and install GIT](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

5. Navigate to the folder you want to place your project in. To navigate folders use the following commands:

```
# Change directoy
cd repository-name
# Go back a folder
cd ..
# Go to the root drive
cd /
```

6. In your working folder clone your new repository:

```
git clone https://github.com/<YourUserName>/<RepositoryName>
```

7. This will create a new folder using the repository name. Change the direftory to that new folder:

```
cd <repositoryName>
```

8. Your ```github-demo``` folder contains a lot of Git settings. You can view these settings using the following commands:

```
git config user.name
git config user.email
git config remote.origin.url
```

We need to add a Personal Access Token to the origin URL to make sure you are authorized. In your browser, go to GitHub, and follow these steps:

- Click on your profile avatar (top right)
- Click on ```Settings```
- Click on ```Developer Settings``` (last option)
- Click ```Personal Access Token```
- Click ```Generate New Token```
- Give the token a name, set the expiration to ```No Expiration```, and check off just ```repo```
- Copy your new token and save it somewhere, GitHub will not redisplay this token

![Personal Access Token](https://raw.githubusercontent.com/codeadamca/github-demo/main/screenshot-token.png)

In the terminal, run the following command to apply your Personal Access Token:

```
git remote set-url https://<PersonalAccessToken>@github.com/codeadamca/github-demo
```

You are now setup and ready to follow the development cycle instructions below!!

## Development Cycle

Now that you have access to the repository and a local copy, it's time to make some changes! 

Open up the IDE of your choice. I will be using [Visual Studio Code](https://code.visualstudio.com/). Using your IDE, open the folder that contains your repository. Also open up a terminal or command prompt and change the folder to the same repository. 

There are two primary methods of commiting a change to a repository:

### Directly to Main Branch

If you are working in a small group and everyone has access to the ```main``` branch, then group members can all make change and commit them directly to the ```main``` branch:

1. In the terminal check on the status of your local repository:

```
git status
```

You will be given a summary of which branch you are working on and a list of files that have been changed. At this point you should be on a branch called ```main``` and there should not be any changes that need to be commited. If there were changes, the files would be listed in red text.

```
On branch main
Your branch is up to date with 'origin/main'.
nothing to commit, working tree clean
```

2. Open up the files named ```main-content.md```. This is a [MarkDown](https://daringfireball.net/projects/markdown/) file! Using the table example, add a row with your name and a portfolio URL (if you have one).

3. In your terminal, commit the changes to the ```main``` branch:

```
git status
git add .
git commit -am "Add <Name> to content"
git push origin main
```

If someone has made changes since you last downloaded the content of the repository you will need to first update your local copy:

```
git pull origin main
```

Congratulations! You have officially contributed to the ```github-demo``` repository. Checn out your GitHub home page and view your contributions calendar. You have a green square!

### Pull Request

If one group member is responsible for merging all code, the other group members can make their code contributions and then submit pull requests. 

1. In the terminal, create a new branch:

```
git branch <BranchName>
```

2. Checkout the new branch:

```
git checkout <BranchName>
```

3. Open up the files named ```branch-content.md```. Using the table example, add a row with your name and a portfolio URL (if you have one).

4. Commit your changes:

```
git add .
git commit -am "Add <Name> to content"
git push origin <BranchName>
```

5. Your changes have been pushed to the <BranchName> branch in GitHub. You now need to create a ```Pull Request``` to request that your code be merged with the ```main``` branch. 
 
After pushing to <BranchName> you will receive a message like this:
 
 ```
 Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 608 bytes | 608.00 KiB/s, done.
Total 6 (delta 4), reused 0 (delta 0)
remote: Resolving deltas: 100% (4/4), completed with 3 local objects.
remote: 
remote: Create a pull request for 'reorder' on GitHub by visiting:
remote:      https://github.com/codeadamca/github-demo/pull/new/reorder
remote: 
To https://github.com/codeadamca/github-demo.git
 * [new branch]      reorder -> reorder
 ```
 
 Go to the recommended URL in a browser and click ```Create Pull Request```. 
 
 6. Now you can clean up your local repository:
 
 ```
 git checkout main
 git merge <BranchName>
 git branch <BranchName> -d
 ```
 
 Congratulations! You are ready to work in a team environment!
 
 ## Tutorial Requirements:

* [Visual Studio Code](https://code.visualstudio.com/) or [Brackets](http://brackets.io/) (or any code editor)
* [GitHub](https://github.com/)
* [Git](https://git-scm.com/)
* [MarkDown](https://daringfireball.net/projects/markdown/

<a href="https://codeadam.ca">
<img src="https://codeadam.ca/images/code-block.png" width="100">
</a>
