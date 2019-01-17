# Atom-Github-OSX
Connecting Atom to GitHub OSX


## Step 1 - GitHub: Create New Repsoitory
Copy Text from resulting screen. Will look like:
echo "# $repositoryname" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:$Username/$repositoryname.git
git push -u origin master

## Step 2 - OSX Terminal
Navigate to directory you wish to work from
Paste the text from Step 1 and hit enter

## Step 3 - Atom Editor
Open new project directory
Create a GIT Repo (Ctrl+Shift_9)
Push to Github (Bottom menu)

# note
You may need to adjust the github.com address depending on the key being used
