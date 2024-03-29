# cs600f2019-project1-starter

This repository contains the starter for project one (proposal template)
in Computer Science 600 Fall 2019. The main directory of this repository
contains the LaTeX source code for a project that is designed for use with [GitHub
Classroom](https://classroom.github.com/). To learn more about the course in
which these assignments were completed, please visit the [Computer Science Thesis Fall 2019 Allegheny College GitHub
Organization](https://github.com/allegheny-computer-science-thesis-2019).

The LaTeX file in this repository is automatically compiled with [Travis
CI](https://travis-ci.org/), thus ensuring that it compiles correctly and,
moreover, that a PDF of the project proposal is available in your GitHub
repository whenever a commit is tagged for a release. Additionally, you can use
a LaTeX compilation command like `pdflatex` or `latexmk` to compile the provided
LaTeX file on your local workstation.

## Introduction

This assignment requires a researcher to write a LaTeX document, stored in the
file `senior_thesis_proposal.tex` that proposes all of the key aspects of a
senior thesis research project. Please refer to the source code in this file for
an explanation of the components of a senior thesis proposal and the way in
which you create them in LaTeX.

Your course instructor will reduce a researcher's grade for this assignment if
the pdf of your completed proposal document has not been properly released before the
assignment's due date on October 16, 2019 at 11:59 pm. Unless
you provide the course instructors with documentation of the extenuating
circumstances that you are facing, no late work will be considered towards your
grade for this project.

## Learning

If you have not done so already, please read all of the relevant [GitHub
Guides](https://guides.github.com/) that explain how to use many of the features
that GitHub provides.

## Travis

This assignment uses [Travis CI](https://travis-ci.com/) to automatically run
the checking programs every time you commit to your GitHub repository. The
checking will start as soon as you have accepted the assignment, thus creating
your own private repository, and the course instructor enables Travis for it. If
you are using Travis for the first time, you will need to authorize Travis CI to
access the private repositories that you created on GitHub. You will partially
complete this authorization by following intuitive steps in your web browser.
You will also need to type the command `travis login --pro` in your terminal
window when you are in the root of your GitHub repository.

## Security

In order for Travis to automatically upload a PDF, called
`senior_thesis_proposal.pdf`, to GitHub when you tag the commit, you need to
created your encrypted access token. To complete this task you must type the
command `travis setup releases --com --force` in your GitHub repository for this
assignment. Then, when prompted, please type your username and password for
GitHub. When asked to give the filename, you can type
`_build/senior_thesis_proposal.pdf`. When asked if you want to deploy from a
specific repository, you can respond with the answer of "no". Finally, when
this tool asks if you want to use encryption, please answer with a "yes".

Now, you should have a `.travis.yml` file with a secure access token for your
GitHub repository for this assignment. Use a text editor to edit this file and
place the following lines of code at the bottom of it. Please note that you must
preserve the spacing in the following code segment when you paste it into your
own `.travis.yml` file. Now, you should be ready to perform a commit with tags
and see your PDF uploaded to GitHub!

```
  skip_cleanup: true
  on:
    tags: true
```

## Tagging

Since this repository primarily contains LaTeX source code, the Travis CI
configuration for it will compile the source code and automatically release a
PDF of the main file whenever the last commit is associated with a [Git
Tag](https://git-scm.com/book/en/v2/Git-Basics-Tagging). As such, this will
cause a PDF file to become available in the listing of the "Releases" listing
for this repository. All release numbers for your writing in this repository
should adhere to the [Semantic Versioning](http://semver.org/) standard that
all GitHub projects are asked to adopt.

Please note that the faculty members who read the PDF that is generated from the
LaTeX source code will only do so by downloading the "tagged" release of the
file `senior_thesis_proposal.pdf` that has a version number greater than
1.0.0. That is, if your commit is tagged with
`senior_thesis_proposal-jjumadinova-1.0.0`, then the file
`senior_thesis_proposal.pdf` should be available for download in the
"Releases" tab in your GitHub repository for this project under the name
`senior_thesis_proposal-jjumadinova-1.0.0`.

Once you have finished making a single small change to the
`senior_thesis_proposal.tex`, you should commit your file using a `git
commit` command. Now, to create your first tag for this repository you could
type `git tag senior_thesis_proposal-jjumadinova-0.1.0`. Of course, you should
substitute your user name for `jjumadinova` when you create the tag. At this point,
you are ready to push your changes with the appropriate tag by typing the
command `git push -u origin master --tags`. After waiting for a period of time,
you should see that your GitHub repository features a new release of the
document that you must create for this project.

When you make subsequent changes to your files and perform commits and you are
ready to release a new version of `senior_thesis_proposal.pdf`, then you should
again tag your work &mdash; before running a push &mdash; with a tag that
adheres to the [Semantic Versioning](http://semver.org/) standard. Each time
that you correctly execute this sequence of commands you will release a new
version of your document to GitHub that is easily accessible as a PDF to you and
to your first and second readers. If you are unable to create a tagged release
using the automated system that Travis provides you can manually create one by
using GitHub's web interface; to adopt the manual approach please click the
"Draft a new release" button in the Releases tab of your GitHub repository.

## Updates

If a course instructor updates the provided material for this assignment and
you would like to receive these updates, then you can type this command in the
main directory for this assignment:

```
git remote add download git@github.com:allegheny-computer-science-thesis-2019/cs600f2019_proposal.git
```

You should only need to type this command once; typing the command additional
times may yield an error message but will not negatively influence the state of
your repository. Now, you are ready to download the updates provided by the
course instructor by typing:

```
git pull download master
```

This second command can be run whenever a course instructor needs to provide you
with new source code for this assignment. However, please note that, if you have
edited the files that the course instructor updated, running the previous
command may lead to Git merge conflicts. If this happens, you may need to
manually resolve them with the help of the instructor or a teaching assistant.

## Problems

If you have found a problem with this assignment's provided source code, then
you can go to the [Computer Science 600 Project 1
Starter](https://github.com/allegheny-computer-science-thesis-2019/cs600f2019_proposal)
repository and create an issue by clicking the "Issues" tab and then clicking
the green "New Issue" button. To ensure that your issue is properly resolved,
please provide as many details as is possible about the problem that you
experienced.

Please note that these assignment sheets have been developed and tested on an
Ubuntu 18.04 workstation running a recent version of LaTeX that was manually
installed using the TeXLive installer. It is also worth noting that you can
compile the `senior_thesis_proposal.tex` file using LaTeX development tools
such as `latexmk` or `pdflatex`. If you are unable to compile this file with
your development tools and your execution environment, then please open a new
issue and we will attempt to resolve your concerns.

Students who find, and use the appropriate GitHub issue tracker to correctly
document, a mistake in any aspect of this laboratory assignment will receive
free laptop stickers and extra credit towards their grade for it.

## Assistance

If you are having trouble completing any part of this project, then please talk
with your first reader. In particular, if you have questions about your research project, please
see your first reader. Alternatively, you may ask questions in the Slack
team for this course.
