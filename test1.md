VCS -\> Version Controller System Remote -\> Server GitHub - remote git
lab -\> remote every id keep the refrence of the previous one the last
commited stage is called head cat `<file name>`{=html} this will tell us
the contain of that file head file will tells us in which branch we are
now what git do : it just kept the changes or track what we just changed

what is git and GitHub Rough Notes

Git: git works locally it does not know that there is a server and all
those things. Jab ye banatha just for locally and independent software.
:::::----\>\>\>\>\>the problem statement for git is how we can track our
code locally and changes also.

git add `<file name>`{=html} means staging area. Means these changes are
ready to commit. git will remember the given files like git add
hello.txt if we are using git add . it means git will track all files
and folders in that directory and track the changes what will gona made
inside that folder. what are the changes done by a developer those thing
will go to a staging area. after this command

git log means what are the changes are done it will tell us. it will
commit history what it will return commit id, Author, date with time,
and commit massage

git commit -m "Your massage" (-m is use for massage) when we do this
command or perform then it checks the staging areas git commit -am
"massage" this will do the git add . and git commit -m "msg" both at a
time

git status it just tell us that sis there any changes are made need to
commit or everything is commited

git log -oneline this will give the data of each commit in a single line
with sorted id of each commit how it works --when we execute git log
then it will go to the HEAD file in .git folder lets say we are in main
branch --after that it will go to the refs folder inside that it will go
to the heads folder inside that main file which contain the last
commited id which means the Head node --but till now we dont get the
actual data we just got the head id or hash --after that .git folder
have a object named folder inside it git creates folder with the first 2
latter of the commited id and inside that it create a file named the
rest of the commited id and inside that it stores the author commited
massage changes and previous commit id to read this file we simply run
git cat-file -p commit id (-p for prettier ) --After getting the head we
can simply go back because git internally use linked list means through
the current id data we can go to the previous commits and we can read
those also

git revert `<commited id>`{=html} it will remove the added thing or we
can simply say that (current - added things or changed things in that
commit) it will create a new commit with the commit massage and the head
will transfer to the current commited node ( core logic is that what
ever the changes we did that will come back and what we have added the
will removed) just removed that changes made in that commit and all
changes will be there

git reset --hard `<commited id>`{=html} this will move the head to that
commited id means it will delete the data till that commited id if we
are not using the hard then it will take all chnages to the staging area
and unable us to commit once again and if we are using the --hard then
it will delete all thing and go to the given commited id

git branch this will gives us in which branch we are now like in main
branch

git diff `<before commit id>`{=html} `<after commit id>`{=html} this
command will gives us what are the changes are done or what are the
difference between those commits

if there is a bug then if i want to know that what are the changes are
done then i can just do the git diff the current commit id and the
previous one id then it will tell me what are the changes done and where
