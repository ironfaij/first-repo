# first-repo
This is my first repo.<br>
my name is faijan
=========================================================================

GIT:- it is a version control system tool and VCS means it track changes in code. it is a software that runs in our laptop/pc.
      git is a free and open source distributed VCS that is responsible for everything github in our local machine.

----------------------------------------------------------------------------

GITHUB:- it is a website that allow developer's to store or manage there code using git.
         in git & github folders are called repository.

------------------------------------------------------------------------------

IN This ydi kisi changes ko confirmed save kiya jata hai to use commit kha jata hai
1. in github ydi ham save karte hai to direct commit kar sakte hai
2. in git ki madad se ydi save karna hai to ye two step process hoti hai (1) add (2) commit

--------------------------------------------------------------------------------

TO CHECK GIT VERSION:
git --version

--------------------------------------------------------------------------------

# local machine ko github account se jodne ke liye 
CONFIGURING GIT:-
                Configuring git means joingin our local system to github account by using following syntax
                git config --global user.name"your name"
                git config --global user.email"your email which is create github account"
                git config --list (aapne kya kya joda hai dekhne ke liye)

----------------------------------------------------------------------------------
# Clone and status command
CLONE:-
      cloning (copy)  a repo. on our local machine
      git clone <-repo. link->

STATUS:-
        to check our code status
        and in this 4 type of status (1) unmodified (2) modified (3) staged (jab add ki ai ja chuki ho or commit karna baki ho) (4) untracked (new or updated file jiske bare me git ko pta na ho)

        git status

-----------------------------------------------------------------------------------
# change directory
CD:-
    folder ke andar folder me jane ke liye syntax
        cd <-folder name->
    folder se bahar aane ke liye syntax 
        cd ..

----------------------------------------------------------------------------------
# Add & Commit
ADD:-
    adds new or changed files in your working directory to the git staying area
        git add <-file name-> (for single files)
        git add . (for all file ko ek sath add karne ke liye)

COMMIT:-
        confirmed save karne ke liye (it is a record of change)
        git commit -m "any message"

-----------------------------------------------------------------------------------
# push command
push:-
    upload local repo contant to remote(github) repo.
    git push origin main 
        where origin= repo name
        and main= branch name

---------------------------------------------------------------------------------
# Nya folder (repo) create karne ke liye
syntax:- 
        mkdir <-repository name->

-------------------------------------------------------------------------------
# ydi local machine par koi nya folder(repo) bnate hai to use git ki repo bnane se github account par upload karne tak ki process
STEPS:-
(1) sabse pehle ek folder create karenge local machine par
    mkdir <-repository name->
(2) folder ko git ki repo bnana
    git init
(3) uske andar kiye gaye changes ko add or commit karna padega
    git add .
    git commit -m "some message"
(4) local machine se github par upload karne ke liye
    ek new repo github par create karna hogi or wha se uska link copy kar lenge
    then,

        git remote add origin(or repo name) <-repo link->
        git remote --v(to verify remote)
        git push origin main (ydi ye bar bar pura nhi likhna ho ek  hi file ke liye to ham ise ek bar is trah likh denge [git push -u origin main] fir keval esa likh sakte hai {git push})

--------------------------------------------------------------------------------
# Git branches
GIT COMMAND'S:-
                git branch  (to check branch)
                git branch -m <-branch new name-> (to change branch name)
                git checkout <-branch name-> (to jump another branch)
                git checkout -b <-branch name-> (to create new branch)
                git branch -d <-branch name-> (to delete a branch) [run time par jis branch par hote hai use delte nhi kar sakte hai]

---------------------------------------------------------------------------------
# alag alg branch ke code ko merge karne ke liye
WE HAVE 2 WAYS
(1) WAY 1:-
            through github by pull request(PR)

YDI PR KE THROUGH MERGE KARTE HAI TO CAHNGES GITHUB ACCOUNT PAR TO HO JATE HAI BUT LOCAL MACHINE PAR NHI DIKHTE HAI TO UN UPDATES KO LOCAL MACHINE PAR LANE KE LIYE HAM PULL COMMAND USE KARTE HAI
(used to fetch and download contant from a remote repo and immediatly update the local repo to match that contant)

    git pull origin main


(2) WAY 2:-
            by local machine
            git diff <-branch name->
            git merge <-branch name->

--------------------------------------------------------------------------
# merge conflict

ydi do brancho me ek hi jgah par changes yani ek hi line me change kiya jata hai to git confuse ho jata hai ki konsa statment rakhna hai to ise merge conflict ki proble kehte hai

----------------------------------------------------------------------------
# undoing changes

undoing changes matlab jo bhi changes ham karte hai unhe undo karna
ham jantE hai ki change 2 tarike ke hote hai yha (1)add (2) commit

case 1. ydi mene add kar diya hai (staged change)
    git reset <-file name->
    git reset (for all file's)
case 2. ydi mene commit bhi kar diya hai (for one commit)
    git reset HEAD~1
case 3. multiple commit ko undo karne ke liye
    git reset <-HASh address->

permanently reset karne ke liye yani ki abhi tak kabhi ise commit hi na kiya gya ho 

    git reset --hard <-HASh address->

-------------------------------------------------------------------------------
# HASH ADD. KO DEKHNE KE LIYE

    git log

-----------------------------------------------------------------------------
# FORK
A fork is a new repo that shares code and visibility settings with the original "upstream" repo.
that means fork is a rough copy.