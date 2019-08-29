to add node_modules/ to .gitignore with one liner:

```
touch .gitignore && echo "node_modules/" >> .gitignore
````

if it's already added to .git
```
git rm -r --cached node_modules && touch .gitignore && echo "node_modules/" >> .gitignore
```
