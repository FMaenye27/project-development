# Basic Code Development Repo: Project Development

## Project Development Getting Started
Just a starter on going project meant to test functionality and grow

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
