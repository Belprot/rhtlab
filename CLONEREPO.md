# Work on a github project

To work on a project with students, the better way is the following :

Teacher's part :
 - Create the main repository
 - Check if can access to the student's repository
 - Add file when needed
 - Download release if want an archive of the student's project at the end

 Student's part :
 - Fork the main repository
 - Add collaborator's (other member of the group and the teacher)
 - Create a personnal folder 
 - Copy working file inside
 
 **_&#9432;_** _Don't modify the file outside this folder (be carefull if modify other file, that will create conflict, but we can solve the conflict problem)._
 - Synch fork when it's needed (modification in main repository)
 - At the end of the project, publish a release 

# Student's part
Choose a member of the group to hold the file.
And this member will follow the step in [Student's part](#students-part)
## Fork repository

On github, click on `fork` to create a copie at this time with all history.

Under `Repository name*`, add your name or accronyme to the repo name.

## Add collaborators
Go :
`Settings`\ `Access` \ `Collaborators` \ `Manage Access`\ `Add people`

Add the other group members and project managers.

## Create a personnal folder and copy working file inside

To avoid all futur conflict, create a personnal folder, give it an explicit name, and copy inside all the file you want modify.

## Update fork repo

When you show on your repo that it is outdated, click on `Sync fork`

## End of project

At the end of the project, create a release and give to project managers the name of the release :
To do this : 
 - Click on `Create a new release`
 - Give a clear name and describe in few words the project.
 - Click on `Publish release` 
 - Send the name of the release.

# Clone Repository
To work locally on your computer, clone your fork repository.
- **Clone the project repository:**
  
  Create a folder (like git in exemple) and clone the repository inside 
  ```bash
  mkdir git 
  cd git
  git clone git@github.com:heig-vd-ie/rhtlab.git
  ```
  Type `yes`to accept the warning.

if we work with mamba, follow [Install Dependencies](#install-dependencies), to install all the good package.
# Install Dependencies
Three options : 
- WSL with python3.12-venv
- WSL with mamba/conda (if you have followed the tuto [INSTALL.md](INSTALL.md))
- Windows 10/11 with native venv module
## On WSL 
### With python3.12-venv
Use virtual environment with the module python3.12-venv
- If the module isn't installed, install with :
  ```bash
  sudo apt install python3.12-venv
  ```
- Then create the virtual environment, for this :
  - move to the project file
  - Confirme that the file .gitingore exit at the root of the project
- Create a virtual environment with the name `.venv`
```bash
python3 -m venv .venv
```
- Activate it
```bash
source .venv/bin/activate
```
- Install the depedencies with the requirement file :
  ```bash
  pip install -r requirements_linux.txt
  ```
### With conda package management
- Install packages from `environment.yml` into the `(base)` environnement :
  ```bash
  cd rhtlab
  mamba env update -n base --file environment.yml
  ```
## On windows 11
- Create a virtual environnement for the project, at the root of the project :
  ```bash
  python -m venv .venv
  ```
- Activate it
  ```bash
  .venv\Scripts\activate
  ```
- Then install the requirement file
  ```bash
  pip install -r requirements_windows.txt
  ```
---
