# Git sync for Insomnia

This plugin can sync service calls of a project to git and pull from it.
Currently, the plugin does not support branches, it only uses the default branch.
Conflicts get solved on overwrite basis only.
You can decide if you want to send your local version to server, or overwrite your local changes with the current server version.
Therefore, it is a good idea to always pull before doing changes.

## Insomnia Documentation:
* https://docs.insomnia.rest/insomnia/introduction-to-plugins

# Usage

## Save project in GIT for the first time

1. Create a GIT Repository on your GIT instance

## Custom changes (MUST READ)

If these steps are not followed, you will not be able to use this fork of the plugin.

First of all, you must create a branch by the name `insomnia` in your repo, preferably using following way:

```
  git checkout --orphan insomnia
  git rm -rf .
  touch .gitignore
  git add .
  git commit -m "First commit"
  git push -u origin insomnia
```
After that, follow remaning steps below.

2. Set Repository URL: click on project name in Insomnia > Set GIT Repository URL
3. Click on project name in Insomnia > Push to GIT Repository

## Import from Server

1. Create a project with the same name as used before
2. Set Repository URL: click on project name in Insomnia > Set GIT Repository URL
3. Click on project name in Insomnia > Pull from GIT Repository

## Notes about custom changes

Changes in this fork allow the insomnia workspace to be saved in a git branch by the name `insomina` in your project repo. The advantage of that is the insomnia branch does not contain any other project file, and only the wokrspace json. So using this fork of plugin makes it a bit easier for me to keep insomnia workspace within the main project repo, without affecting any of the project files.
