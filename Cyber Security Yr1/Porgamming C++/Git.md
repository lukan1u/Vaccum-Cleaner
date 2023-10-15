---
Date: 2023-10-15T14:46:00
Summary:
---
# All git stuff
---
#settings #uwe #git #cplusplus 
Table of contents >>> 
Previous page >>> 
Next Page >>>

## How to set up and connect git repos with tokens
---
- `gh auth login`


https://docs.github.com/en/get-started/getting-started-with-git/caching-your-github-credentials-in-git
- How to generate the tokens:
https://www.youtube.com/watch?v=ytSoabxSQ6E


## How to merge to git repos
---
If you want to merge `project-a` into `project-b`:

```bash
cd path/to/project-b
git remote add project-a /path/to/project-a
git fetch project-a --tags
git merge --allow-unrelated-histories project-a/master # or whichever branch you want to merge
git remote remove project-a
```
