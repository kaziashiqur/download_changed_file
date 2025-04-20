### Git Update Version Vs Old Version -> Only Updated file Zip
* At first, in old folder, run this command
```
git init
git add .
git commint -m "something"
```
* Then paste the .git file to the updated folder and run this command
```
git add .  
git commit -m "something"   
git archive --output=modified_and_added_files.zip HEAD -- $(git diff --name-only --diff-filter=AM HEAD~1..HEAD)  
git reset HEAD~1
```

### Thats all, now you can see the updated file zip named modified_and_added_filez.zip in the new folder
