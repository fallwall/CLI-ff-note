git remote rm destination
https://help.github.com/en/articles/removing-a-remote


git remote add origin destination
https://articles.assembla.com/en/articles/1136998-how-to-add-a-new-remote-to-your-git-repo


$ git remote -v
# View current remotes
> origin  https://github.com/OWNER/REPOSITORY.git (fetch)
> origin  https://github.com/OWNER/REPOSITORY.git (push)
> destination  https://github.com/FORKER/REPOSITORY.git (fetch)
> destination  https://github.com/FORKER/REPOSITORY.git (push)

$ git remote rm destination
# Remove remote
$ git remote -v
# Verify it's gone
> origin  https://github.com/OWNER/REPOSITORY.git (fetch)
> origin  https://github.com/OWNER/REPOSITORY.git (push)
