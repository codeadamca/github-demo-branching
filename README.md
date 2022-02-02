# github-demo

A demo GitHub repository for introducing students to Git and GitHub. 

## Initial Setup

There are two possible scenarios when setting up a project and a Git repository:

### Brand New Project

If you are starting a brand new project that does not have a GitHub repository you will need to follow these steps:

1. Register or login to your GitHub account.
2. Create a new GitHub repository. Give it a title using lowercase letters and dashes. Make it ```Public``` and Click ```Add a README file```.

IMAGE

3. On the new repository page click the green ```Code``` button and copy the repository URL.

IMAGE

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

### 
