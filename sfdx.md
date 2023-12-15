# Getting Started with SFDX

## Commands to Get Started

`sfdx force:auth -h`

- The -h flag allows us to get help with the sfdx force:auth command

`sfdx force:org:list`

- This command will list out all of the SFDX orgs we have attached to our org.

`sfdx force:auth:web:login -a trailhead`

- The -a flag lets us alias our devhub
  - The following command would alias our devhub as 'trailhead'
- Log into salesforce after
- This authorizes salesforce to work with the CLI

`sfdx force:auth:web:login -d -r https://cs215.salesforce.com/ -a test`

- The -r flag lets us specify a login url
- The -d flag lets us make thi

## Create an SFDX Project

`sfdx force:project:create -n trailhead-triggers`

- The -n flag allows us to name our project

  - The following command would name our project trailhead-triggers

- Creating a Project gives you a Scratch Definition for that org
  - Found in /{root}/config/project-scratch-def.json

`sfdx force:org:create -s -f`

- The -s flag makes it so that this is our default scratch org
- The -f flag makes it the scratch org is made with the scratch def file we specify

## Create Repo on IDE

`git init`

- Creates a repo

`git add .`

- Adds all files at . to current repo

`git status`

- Shows status of repo

`git commit -m 'init commit'`

- Pushes code to master, with the comment 'init commit'

## Create GitHub Repo

- Create repo on github w/ same name
- Follow the commands to push your committed code to the github repo

`git remote -v`

- Shows repos

## Create Scratch Org

- A disposable org to spin up for developing and testing on

`sfdx force:org:create -v nameofdevhub -a nameoforg -d numberofdaysactive -f destinationofconfigfile`

## Hub Org

- Very similar to Salesforce Developer Org
