

# Steps to Create a Parent Repo with Submodules

Create the Parent Repository

On GitHub, create a new repository (e.g., parent-repo).
Clone it to your local machine:
sh
git clone https://github.com/your-username/parent-repo.git
cd parent-repo
Add Submodules (Sub-repos)

To add a submodule, use:

sh
git submodule add https://github.com/username/sub-repo.git path/to/sub-repo how can i move on

Here’s how you can move forward and successfully set up a parent repository with submodules, step by step:

## **1. Create the Parent Repository**

- On GitHub, create a new repository (e.g., `parent-repo`).
- Clone it to your local machine:

```sh
git clone https://github.com/your-username/parent-repo.git
cd parent-repo
```


## **2. Add Submodules**

- Make sure the repositories you want to use as submodules already exist on GitHub (or another Git server)[^6].
- In your parent repo directory, add a submodule using:

```sh
git submodule add https://github.com/username/sub-repo.git path/to/sub-repo
```

    - Replace `https://github.com/username/sub-repo.git` with the actual URL of the submodule repo.
    - Replace `path/to/sub-repo` with the folder name or path you want the submodule to appear in (or omit for default)[^2][^5][^6].


## **3. Commit Submodule Changes**

- After adding a submodule, Git will create a `.gitmodules` file and the submodule directory.
- Add and commit these changes:

```sh
git add .gitmodules path/to/sub-repo
git commit -m "Add submodule sub-repo"
```


## **4. Push to GitHub**

- Push your changes to your parent repo on GitHub:

```sh
git push
```


## **5. Working With Submodules**

- When you clone the parent repo in the future, initialize and fetch submodules with:

```sh
git clone https://github.com/your-username/parent-repo.git
cd parent-repo
git submodule update --init --recursive
```

- If you make changes inside a submodule, you must push those changes from within the submodule directory to its own repository[^3][^5].


## **Summary Table**

| Step | Command/Action |
| :-- | :-- |
| Clone parent repo | `git clone <parent-repo-url>` |
| Add submodule | `git submodule add <sub-repo-url> <path>` |
| Commit changes | `git add .gitmodules <path>`<br>`git commit -m "Add submodule"` |
| Push to GitHub | `git push` |
| Initialize submodules | `git submodule update --init --recursive` |


---

**Key Points:**

- Each submodule must be a separate repository and have its own remote.
- Changes to submodules must be committed and pushed from within the submodule directory.
- The parent repository only tracks the submodule’s commit reference, not its content[^3][^5][^6].

If you need help with a specific step or run into an error, just ask!

<div style="text-align: center">⁂</div>

[^1]: parent-

[^2]: https://git-scm.com/book/en/v2/Git-Tools-Submodules

[^3]: https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/How-to-add-submodules-to-GitHub-repos

[^4]: https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/The-git-submodule-add-example

[^5]: https://www.atlassian.com/git/tutorials/git-submodule

[^6]: https://blog.bitsrc.io/how-to-utilize-submodules-within-git-repos-5dfdd1c62d09

[^7]: https://stackoverflow.com/questions/68343998/how-to-make-the-parent-git-folder-always-point-to-latest-commit-whenever-there-i

[^8]: https://stackoverflow.com/questions/1777854/how-can-i-specify-a-branch-tag-when-adding-a-git-submodule

[^9]: https://chrisjean.com/git-submodules-adding-using-removing-and-updating/

[^10]: https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/How-to-clone-a-git-repository-with-submodules-init-and-update

[^11]: https://www.reddit.com/r/git/comments/edn49q/how_to_add_existing_local_git_repo_as_a_submodule/

