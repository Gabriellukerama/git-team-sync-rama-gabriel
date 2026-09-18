1. What did the rejected push error message tell you, and why did it happen?
The rejected push error message indicated a non-fast-forward push rejection, which informed me that my local branch was behind the remote branch on GitHub.
This happened because another commit had already been pushed to the remote repository from Clone B, making my local history in Clone A outdated.

2. What's the actual difference between how you resolved Task 3 (merge) vs Task 4 (rebase)?
In Task 3, resolving with a merge created a dedicated merge commit that explicitly preserved both independent feature branches and joined their histories together.
In Task 4, resolving with a rebase placed my local unpushed commit directly on top of the fetched remote commit, creating a single linear commit history without creating a merge commit.

3. What one habit would have avoided both rejected pushes in this lab?
Running `git fetch` or `git pull --rebase` before writing new local commits or attempting to push would have prevented both push rejections.

4. Which approach - merge or rebase - would you default to on a shared team branch, and why?
I would default to merging on a shared team branch because it preserves the authentic history without rewriting existing commits. Rebasing re writes commit history,
which can cause severe sync conflicts and broken histories for other team members working on the same branch.
