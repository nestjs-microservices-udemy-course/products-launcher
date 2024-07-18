## Dev

1. Clone the repository
2. Create the .env based on the .env.example
3. Execute the command `docker compose up --build`

### Steps to create Git Submodules

1. Create a new repository on GitHub
2. Clone the repository on the local machine
3. Add the submodule, where `repository_url` is the repository url and `directory_name` is the name of the folder where you want to save the submodule (it must not exist in the project)
4. Add the changes to the repository (git add, git commit, git push)
   Ex:

```
git add .
git commit -m "Add submodule"
git push
```

5. Initialize and update Submodules, when someone clones the repository for the first time, they must run the following command to initialize and update the submodules

```
git submodule update --init --recursive
```

6. To update the sub-module references

```
git submodule update --remote
```

## Important!

If you are working on the repository that has the submodules, **first update and push** in the submodule and **then** in the main repository.

If you do it the other way around, you will lose the references of the submodules in the main repository and you will have to resolve conflicts.
