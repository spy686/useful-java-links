    git clone --bare git@git.test.com:my-repo-a.git
    git fetch origin
    git remote add new-origin git@git.test.com:my-repo-b.git
    git push --mirror new-origin
    git remote rm origin
    git remote rename new-origin origin

Источник: https://www.smashingmagazine.com/2014/05/moving-git-repository-new-server/
