```
git add .  
git commit -m "immediate"   
git archive --output=modified_and_added_files.zip HEAD -- $(git diff --name-only --diff-filter=AM HEAD~1..HEAD)  
git reset HEAD~1
```
