# Contributing

## Request for Changes/ Pull Requests

You first need to create a fork of the [webannoyances](https://github.com/Laniksj/webannoyances/) repository to commit your changes to it. Methods to fork a repository can be found in the [GitHub Documentation](https://docs.github.com/en/get-started/quickstart/fork-a-repo).

Then add your fork as a local project:

```sh
# Using HTTPS
git clone https://github.com/LanikSJ/webannoyances.git

# Using SSH
git clone git@github.com:LanikSJ/webannoyances.git
```

> [Which remote URL should be used ?](https://docs.github.com/en/get-started/getting-started-with-git/about-remote-repositories)

Then, go to your local folder

```sh
cd webannoyances
```

Add git remote controls :

```sh
# Using HTTPS
git remote add fork https://github.com/YOUR-USERNAME/webannoyances.git
git remote add upstream https://github.com/LanikSJ/webannoyances.git


# Using SSH
git remote add fork git@github.com:YOUR-USERNAME/webannoyances.git
git remote add upstream git@github.com/LanikSJ/webannoyances.git
```

You can now verify that you have your two git remotes:

```sh
git remote -v
```

## Receive remote updates

In view of staying up to date with the central repository :

```sh
git pull upstream main
```

## Choose a base branch

Before starting development, you need to know which branch to base your modifications/additions on. When in doubt, use main.

| Type of change                |           | Branches              |
| :------------------           |:---------:| ---------------------:|
| Documentation                 |           | `main`              |
| Bug fixes                     |           | `main`              |
| New features                  |           | `main`              |
| New issues models             |           | `YOUR-USERNAME:patch` |

```sh
# Switch to the desired branch
git switch main

# Pull down any upstream changes
git pull

# Create a new branch to work on
git switch --create patch/1234-name-issue

# Make your changes and run the checksum script
./scripts/checksum-sort.sh filters/webannoyances.txt
```

Check [ultralist.txt](https://github.com/LanikSJ/webannoyances/blob/master/ultralist.txt) or any of the sublists to make sure your changes are added.

Commit your changes, then push the branch to your fork with `git push -u fork` and open a pull request on [the webannoyances repository](https://github.com/LanikSJ/webannoyances/) following the template provided.
