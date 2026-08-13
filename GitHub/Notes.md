git --version

git config --global user.name "Your UserName"
- Set your name
- Tells Git: "Whenever I save changes, show this name as the author."

git config --global user.email "Your email"
- Set your email
- Tells Git: "Use this email when recording my changes."

git config --global --list
- Check your settings
- Shows what Git currently knows about you.

git init
- Start Git in a folder
- Tells Git: "Start tracking this project."

git status
- Check what's happening
- Asks Git: "What files changed?"

git add .
- Prepare files to be saved
- Tells Git: "I want to save all current changes."

git commit -m "Comment"
- Save a snapshot
- Tells Git: "Take a snapshot of everything I added."

git branch -M master/main


git remote add origin git@github.com:Supriya117104/Python.git


git remote -v


git remote set-url origin https://github.com/Supriya117104/Python.git


git push -u origin master/main


Remove-Item -Recurse -Force .git