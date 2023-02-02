# Basic Code Development Repo: Project Development

## Project Development Getting Started
Just a starter on going project meant to test functionality and grow. Please add more projects to it!

## What needs to be done:
- Develop a project concept
- Setup local repos
- Establish appropriate branches
- Add code!!!!


## Some Set Up Instructions

### Useful configurations to help with development

Try following to get a terminal that displays some useful visuals to help with git

```bash
cd ~
git clone https://github.com/magicmonty/bash-git-prompt.git
```
This should display something like this:

Cloning into 'bash-git-prompt'...
remote: Enumerating objects: 1788, done.
remote: Counting objects: 100% (46/46), done.
remote: Compressing objects: 100% (33/33), done.
remote: Total 1788 (delta 24), reused 17 (delta 13), pack-reused 1742
Receiving objects: 100% (1788/1788), 511.73 KiB | 18.95 MiB/s, done.
Resolving deltas: 100% (1070/1070), done.

Then follow up with performing the following:

```bash
echo 'GIT_PROMPT_ONLY_IN_REPO=1' >> ~/.bashrc
echo 'GIT_PROMPT_THEME=solarized_ubuntu' >> ~/.bashrc
echo 'GIT_PROMPT_SHOW_UPSTREAM=1' >> ~/.bashrc
echo 'source ~/bash-git-prompt/gitprompt.sh' >> ~/.bashrc
source ~/.bashrc
```

Once this is done, change directories to any of your local repos. You should now see the prompt with a more descriptive display.

If you would like an easy way to see commit history, perform the following:

```bash
git config --global alias.lga "log --graph --oneline --all --decorate"
```

Then type:

```bash
git lga
```
It should look like this:
NOT MEANT TO COPY

```bash
* ae1cfae (HEAD -> development, origin/development, origin/HEAD) updated README.md to make it easier to clone the repo
*   bed39d4 Merge branch 'development' of https://github.com/FMaenye27/project-development into development
|\  
| * 4f42fd3 Create CODEOWNERS
* | 45ad007 updated README.md with additional setup information
|/  
* c7eabdf (freds_local) Updated README.md to remove additional header
* 8800f35 Updated README.md file
* bb8eef2 (origin/master) Initial commit
```

### If you would like to get a local clone to start coding, run this:

```bash
git clone https://github.com/FMaenye27/project-development.git
``` 

### Create a local branch

```bash
git checkout -b <new_branch_name_here>
```


