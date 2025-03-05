If getting `git` permission denied errors (change ownership of the `.git` directory to user instead of root):

```
  sudo chown -R $USER:$USER .git
```
