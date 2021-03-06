cli = command line interface
git bash in windows

/ = root directory
~ = home directory (alt 126)

prompt = name of PC + username + $
working directory = directory you're currently in

command + (maybe)flags + (maybe)arguments

## COMMANDS

pwd = displays path / prints the current working directory 
clear

ls = lists files and folders in the current directory
with flags:
ls -a = lists hidden and unhidden files
ls -al = lists details for the hidden and unhidden files

cd = change directory
alone goes to home directory
with argument of directory you want to visit
cd .. one level above current working directory

mkdir = make directory (create new folder)
argument is name of created directory

touch = create an empty file
argument is name of created file

cp = copy
argument 1 = file I want to copy; argument 2 = directory where I want to place it
cp -r = recursive flag
arguments are the file you want to copy and the one you want ot place it into

rm = remove / delete
argument is the name of the file you want to delete
rm -r = recursive delete of all files in a directory (careful, no chance to undo)

mv = move (or rename)
arguments are the name of the file and the folder it goes to
for rename: arguments are the old name of the file and the new name of the file

echo = print whatever argument you provide
date = gives you the date and time of when you request it


### EN GIT LOCAL

1. abro git bash
2. mkdir ~/test-repo
3. cd ~/test-repo

### En github
- fork el repositorio de otro usuario
- luego para hacer copia local:
$ git clone (y argumento de la dirección web del repositorio)

## BASIC GIT COMMANDS I WILL USE ON COURSE

A. ADDING (from workspace to index)
- using a local repository already under version control:
git add . = adds new files in folder to track (you should be currently on that directory).
git add -u = update tracking for files that changed names / were deleted
git add -A = both previous

B. COMMITING (from index to local repo)
git commit -m "message" (message = useful description of what u did)
This updates local repo, not remote repo on Github

C. PUSHING (from local repo to remote)
git push

D1. BRANCHES (other version of same -collaborative project- directory where you can make changes independently)
git checkout -b branchname = create a new branch
git brach = see in which branch you are
git checkout master = switch back to master branch type

D2. PULL (if you forked someone's repo or branched your own)
On github (web) and not on local git, you choose the branch and press the 'compose a pull request' button. The branch owner is notified and can see changes, if appropriate and interesting for them, they can merge.

### Help:
- git documentation (http://git-scm.com/doc)
- github help (https://help.github.com)
- google or stack overflow (adviced)

## BASIC MARKDOWN
Text file (ex. readme.md), used in reproducible research course

### Markdown syntax 

Headings:
## secondary heading: ##
### tertiary heading: ###
* for each item in a dotted list: *

MD button in Rstudio has a quick markdown guide on R
------

## INSTALL R PACKAGES

a <-available.packages () = y luego:
a = lista todos los que hay, son 5200

install.packages("slidify") = instala slidify
install.packages(c("slidify", "ggplot2", "devtools"))

library(ggplot2) = load package ggplot2 once installed into R (if you have all dependency packages)
search() = see all of the functions part of the package you've just loaded with 'library'

List of packages: http://cran.r-project.org/web/views/
List of packages for social sciences: http://cran.r-project.org/web/views/SocialSciences.html
List of packages for psychometrics: http://cran.r-project.org/web/views/Psychometrics.html

## INSTALLING RTOOLS
(only needed for 'DEVELOPING DATA TRIALS' course)
use latest version for your R version (choose right .exe file)
Once you have Rtools, in RStudio:
find.package("devtools") = check if you have it
install.packages("devtools") = download if you don't yet have it
library(devtools) = install it
find_rtools() = you should see TRUE printed on screen if it was installed properly.
---

## DATA SHARING:
- github.com (small)
- figshare.com (larger)

##OTROS

* Need to be careful with data-dredging when doing data mining (test lots of hypoteses in the same set of data, some will be false-true correlations at the 5% or 1% error margin: http://en.wikipedia.org/wiki/Data_dredging)
* Data tidying: http://vita.had.co.nz/papers/tidy-data.pdf and video: http://vimeo.com/33727555
* The unreasonable effectiveness of data https://www.youtube.com/watch?v=yvDCzhbjYWs
