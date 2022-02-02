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

You are now setup and ready to follow the development cylcle instructions below.

## Development Cycle

Now that you have access to the repository and a local copy, it's time to make some changes!

Open up the IDE of your choice. I will be using [Visual Studio Code](https://code.visualstudio.com/). Using your IDE open the folder that contains your repository. Also open up a terminal or command prompt and change the folder to the same repository. 

1. In the terminal check on the Git status of your code:

```
git status
```

You will be given a summary of which branch you are working on and a list of files that have changed. At this point you should be on the branched called ```main``` and there should not be any changes that need to be commited. If there were changes, the files would be listed in red text.

```
On branch main
Your branch is up to date with 'origin/main'.
nothing to commit, working tree clean
```

