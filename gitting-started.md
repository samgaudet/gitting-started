# Gitting started

This guide assumes that you have created a GitHub account, and have access to the terminal on your computer. If for some reason Git is not already installed on your computer, you can follow these instructions [here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).

## Background

Git allows us to control and track the version history of components in a project. Said more eloquently than I could come up with:

> A version control system, or VCS, tracks the history of changes as people and teams collaborate on projects together. As the project evolves, teams can run tests, fix bugs, and contribute new code with the confidence that any version can be recovered at any time. Developers can review project history to find out:
>
> - Which changes were made?
> - Who made the changes?
> - When were the changes made?
> - Why were changes needed?

## Alternatives to this guide

I am not the first person or the last person to write about working with Git. Here are a number of other guides that may be helpful to read in tandem, or in replacement, of this one!

[GitHub: _Git Handbook_](https://guides.github.com/introduction/git-handbook/)  
[HubSpot: _An Intro to Git and GitHub for Beginners (Tutorial)_](https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners)

## Background

## Creating a repo

"Repo" is short for repository (not for [repossession](https://m.media-amazon.com/images/M/MV5BNzdkMzVhNTgtMjlhNC00M2JkLWI3MzktYzdkNzYxNTk1NjcwXkEyXkFqcGdeQXVyMTQxNzMzNDI@._V1_SY1000_CR0,0,653,1000_AL_.jpg)). A repo is a folder in which we will store the files associated with a project.

### Creating a repo in GitHub

To create a repo in GitHub, begin by navigating to your profile. From here, click the "Repositories" tab in the navigation, where you will then see a green button labeled "New". Click this button, which will bring you to a page where you can create a new repo (alternatively, just follow this [link](https://github.com/new)).

There are a few options on this page:

- _Owner_: the parent account of the repo&mdash;for personal use, there will likely only be one option, which is your account.
- _Repository name_: the name of your project, which will be used as the repo (folder) name.
- _Description_ (optional): an optional description of your project that will be used in the generated README for the repo if you so choose.
- _Public_ or _Private_: the visibility of your repo&mdash;from GitHub:

```
public: Anyone on the the internet can see this repository. You choose who can commit.
private: You choose who can see and commit to this repository.
```

_Options for repos if you are **not** importing an existing repo_

- _Initialize this repository with a README_: whether or not GitHub will automatically add your first file (a markdown file called _README_) to a new repo.
- _Add .gitignore_: a dropdown of language-specific `.gitignore` files&mdash;let's talk more about this [later]().
- _Add a license_: a dropdown of prewritten licenses&mdash;we will also talk about this one a bit more [later]().

Once you have given the repo a name and selected the relevant options to your project, click on "Create repository" and be amazed! The repo is now available on GitHub at:

```
https://github.com/<owner>/<repo-name>
```

### Creating a repo locally

Once you have made a new folder for your project locally&mdash;either by right-clicking to create a folder, or by using something like `mkdir` in terminal&mdash;you will need to initialize the folder as a git repo. You can do this by running the `git init` command from within the folder. This will look something like this:

```
samgaudet:GitHub samgaudet$ mkdir gitting-started
samgaudet:GitHub samgaudet$ cd gitting-started
samgaudet:gittin-started samgaudet$ git init
```

_**`# TODO`**_ finish up this section and talk about uploading an existing repo :)

## General development workflow

Let's assume you have followed the steps above and setup a GitHub repo, or are contributing to a project that has an existing GitHub repo. I find working with Git as a developer on its simplest form to be like following a cooking recipe (there is a _ton_ more nuance that one can choose to learn about Git, but it should not stop you from getting started making commits).

### Branches

When working collaboratively, branches can be a helpful way of organizing changes, and are likely required by your organization's development workflow. A branch is an offshoot of the master tree&mdash;a version of the current project that you can add to, subtract from, or generally modify.

Critical in working with git branches well, is picking a good name for your branch. In general it may be helpful to include details such as your name or initials, a ticket number or other identifier that could be linked to a project management system, and a brief description of the changes on the branch. In my work, I use the following convention:

```
<initals>_
```
