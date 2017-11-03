[Wiki Homepage](index.md)
# Github 

## Starting a New Project
1. Create a new repository on GitHub. Do not initialize with README/etc.
2. In terminal, navigate to working directory of the project
3. `$ git init`
4. `$ git add .`
5. `$ git commit -m "Commit Message"`
6. Note URL from the top of the GitHub repository's Quick Setup page.
7. `$ git remote add origin www.url.git`
8. `$ git remote -v`
9. `$ git push origin master`

## Un-sync a File
`$ git rm --cached filename.ext`

## Sync repository (push changes from local machine --> GitHub)
1. `$ git add .`
2. `$ git commit -m "Commit Message"`
3. `$ git push origin master`

Simple bash script to save a little typing:
```bash
#!/bin/sh
git add .
git commit -m "automated commit $(date +%Y%m%d)"
git push origin master
```

---
##### References

[Adding an Existing Project to Github](https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/)

---
This page was last updated: Wed 01 Nov 2017 09:41:56 AM EDT 
