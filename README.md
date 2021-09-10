# Helpful Git References

## ProGIT (free) – Scott Chacon/Ben Straub
https://git-scm.com/book/en/v2

## Visual GIT Reference – Mark Lodato
https://marklodato.github.io/visual-git-guide/index-en.html

## Visual GIT Concepts with D3
http://onlywei.github.io/explain-git-with-d3/#

```git
## Initialize a REPO
git init - create repo, default is master

## Add files to stage
git add s1  - "add the file s1"
git add .   - "add all the files"
git add s*  - "add all the s's"

## Commit files to REPO
git commit -m "commit s1"  

## Display REPO log
git log

## Display REPO status
git status

## GIT Graph with detail
git log --all --decorate --oneline --graph

git add s2
git commit -m "commit s2"
git log --all --decorate --oneline --graph

git status

## Create New Branches
git branch SDN           - new branch SDN
git branch auth          - new branch auth
git checkout -b "dev"    - create "dev" and move pointer in one

## Display Branches
git branch   - shows all the branches  * next to branch checked out  AKA HEAD pointer
git log --all --decorate --oneline --graph

PS C:\classGitWork\gitDemoWork> git branch
* master

PS C:\classGitWork\gitDemoWork> git status
On branch master
nothing to commit, working tree clean

PS C:\classGitWork\gitDemoWork> git log --all --decorate --oneline --graph
* e3e9fd0 (HEAD -> master) cleanup
* cc0349b gitignore
* acaec7f add s2 edit s1
* bc256fd add s1
* c875341 update demo text
* 70a3f2e update Readme
* 9546741 commit demo
* 3a7ce05 Initial extend_project commit
* 47ee884 Initial Commit

PS C:\classGitWork\gitDemoWork> git branch SDN
PS C:\classGitWork\gitDemoWork> git branch auth
PS C:\classGitWork\gitDemoWork> git branch
  SDN
  auth
* master

## Switch Branches
git checkout SDN

git log --all --decorate --oneline --graph

git status

git add s1
or
git add s1 s2 s3
or
git add s*   (wildcard all s's)
or 
git add .    (all)

git commit -m "s1 for SDN"

git log --all --decorate --oneline --graph

git checkout auth

## Display Branches
git branch

git log --all --decorate --oneline --graph

## View Files
cat s1 - look at s1
cat s2 - look at s2

## Change Branches
git checkout SDN
git checkout auth

git status

git diff             --   shows us differences in staged items
git diff --staged   show us what we are about to commit

git log       - see commits
git log -p    - see what has changed

git rm s2     - removed s2 from working tree, removed from staged area
git commit    - detailed multiline commit message about delete

# working directory undo
git restore s1.yaml restore file to working directory
git restore --staged s1.yaml   to unstaged

# undo working tree Files
get reset head S1   -- unstaged s1 from the staging area
get checkout --s1  -- restore the working area with s1 from the history

get log --s2     - see what affects s2


.gitignore  - you don't need GIT to track files
add and commit this file like any other file 

Merging files

Fast-forward Merge
We want to commit changes of s1 to master branch and there is
a direct path, this is a fast-forward merge.

Detached HEAD
PS C:\classGitWork\gitDemoWork> git checkout 9546741
Note: switching to '9546741'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

HEAD is now at 9546741 commit demo
PS C:\classGitWork\gitDemoWork> git switch -
Previous HEAD position was 9546741 commit demo
Switched to branch 'master'
PS C:\classGitWork\gitDemoWork>

Could also "git checkout MASTER" again, or some other branch.
This will also move the head back to an undetached state.

```

<!-- Headings -->
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6

<!-- Italics -->
ITALICS
Use single asterisks   *to italicize text*
Or use single underscores _to italicize text_

<!-- Make your text strong -->
STRONG TEXT
You can use double asterisks **to make text strong**
Or use double underscores __to make text strong__

STRONG AND ITALIC
Use three asterisks or three understores
to make it ***strong and italic***
to make it ___strong and italic___

<!-- Strikethrough Some Text -->
STRIKETHROUGH
Use the double tildes   ~~to STRIKETHROUGH text~~ 

<!-- Horizontal Rule -->
HORIZONTAL RULE
Use triple underscores for Horizontal Rule
___

Also use triple hyphens for Horizontal Rule

---

<!-- ESC Characters to Display -->
DISPLAY MARKDOWN CHARACTERS
To show some of the characters, you can ESC them so they don't use Markdown.
\*Italics\*  shows you the asterisk w/o formatting
\#Heading\#  shows you the hashtag w/o formatting

<!-- Blockquotes -->
BLOCKQUOTES
> A horse is a horse is a horse of course.
> Noone can talk to a horse of course.

<!-- Links -->
BROWSER LINKS
***Name*** in brackets
***URL*** in parens
***Hover Over Text*** in quotes inside the parens
[Dunwoody Website](https://dunwoody.edu "Hover over link to see this title")

<!-- Unordered Lists  -->
UNORDERED LISTS
* One asterisk and space per item
* Item 2
* Item 3
    * Nest items with TAB asterisk space

<!-- Ordered Lists -->
ORDERED LISTS
1. One dot for item one
1. One dot for item two
1. One dot for item three


<!-- Images -->
IMAGES
![Markdown LOGO](https://markdown-here.com/img/icon256.png)

![Local LOGO](./logo.png)



# In-Class Activity A
* [ ] Create a new web project gitDemoWork in editor and initialize GIT into the project
  
* [ ] Create a file and name it git.html
  
* [ ] Copy the HTML5 code and do what is necessary to make an initial commit.
* [ ] Run the git status command and make sure your directory does not have untracked fi les.
* [ ] Run the commands to create a new branch called "extend_project" and switch to the new branch
* [ ] Add a new page to the "extend_project" branch and name it github.html
* [ ] Run the various commands to commit the new file and merge "extend_project" into
the master branch.
