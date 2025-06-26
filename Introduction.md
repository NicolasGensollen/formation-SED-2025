# Introduction

## Who is this tutorial for?

The purpose of this tutorial is to show you the basics of how to develop software in Python.

Although it is quite general, the target audience consists of recently recruited individuals at the Aramis team. This means that this tutorial is opinionated on a lot of subjects, as it conveys the software development process that we have implemented within the team. There are a lot of ways to do what is described in this guide, and we do not proclaim our methods to be better, but we have organized our activities around tools and conventions that you need to learn and respect if you want to contribute during your time at Aramis.

Even though the tutorial doesn't require much to be followed, it is assumed that the reader has a Mac computer and possesses basic knowledge about:

- using the terminal
- using git (at least the basic commands)
- Python (the code will be pretty basic, but some basic knowledge is required)

If this is not your case, you will find more details and resources in the welcome guide. Make sure to read and practice those before coming back to this page.

## Why this tutorial?

When developing software in Python, there are a lot of options to choose from. A few years ago, the main software projects of the team were using very different tools and conventions:

|     | Clinica | ClinicaDL | Leaspy |
| -------- | ------- | ------- | ------- |
| Hosting platform  | GitHub | GitHub | GitLab |
| Project specifications | pyproject.toml | pyproject.toml | setup.py |
| Dependency managment | Poetry | Poetry | requirements.txt |
| Unit tests | NO | NO | YES |
| CI | Jenkins | Jenkins | gitlab-ci |
| releasing | Poetry | Poetry | twine |
| Formatter and Linter | Black | Black | None |

To be able to contribute to different projects within the ARAMIS team, engineers had to learn many different skills and technologies. In June 2025, this has been unified, and things now look like this:

|     | Clinica | ClinicaDL | Leaspy |
| -------- | ------- | ------- | ------- |
| Hosting platform  | GitHub | GitHub | GitHub |
| Project specifications | pyproject.toml | pyproject.toml | pyproject.toml |
| Dependency managment | Poetry | Poetry | Poetry |
| Unit tests | YES | YES | YES |
| CI | GitHub actions | GitHub actions | GitHub actions |
| releasing | Poetry | Poetry | Poetry |
| Formatter and Linter | Ruff | Ruff | Ruff |

First of all, all projects are using the same set of tools. Second, this set of tools is much smaller than before (things like Jenkins, twine, gitlab-ci have disappeared). This is great news for all those joining the team who want or need to contribute.

The goal of this tutorial is to introduce you to this set of tools, show you how they work, and explain the conventions we use. This will help us maintain this coherence within projects.

## How is the tutorial structured?

In this tutorial, we will build a small Python library from scratch as a toy example. The tutorial is organized in 6 chapters:

**Chapter 1** starts by providing information about the GitHub organization named "Aramis". It then moves on to the creation of a new repository for the Python library that will be developed. If you develop during your time at Aramis, you will be working within this organization a lot.

**Chapter 2** explains how to manage a project using Poetry and how to structure a repository. We will talk about dependencies and how to manage them effectively using Poetry.

**Chapter 3** is about planning a project. We won't jump right away into coding, but we will try to design a basic roadmap for a project and formalize it with issues and milestones. We will then start implementing the first features and see how to write unit tests to make sure the code is working.

**Chapter 4** is a key chapter because it introduces the different tools and concepts required to automate things. We will see how to use Ruff and GitHub actions to automatically format and lint our code. We will also learn how to perform automated code testing using GitHub Actions.

**Chapter 5** is about documentation. It starts by presenting the concept of Test Driven Development and then presents the tools to generate documentation for a package. We will present various tools to produce a good-looking documentation. We will also introduce readthedocs, a platform to build and host documentation. Finally, we will automate the documentation build and deployment steps.

**Chapter 6** is about releasing the code. We will see what a release is, how a Python package can be distributed and installed, and the main reference to publish Python packages: Pypi. We will publish the toy example to "test Pypi" and automate the publication step.

At the end of the tutorial, you will have a solid understanding of the way people of Aramis work on software. You will be able to navigate the team's public software and understand its structure, the purpose of the different files, and so on.
