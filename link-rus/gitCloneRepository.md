Есть некоторый репозиторий с ветками master и develop:

    git@git.test.com:my-repo-a.git
    
Есть также пустой репозиторий:

    git@git.test.com:my-repo-b.git
    
Как полностью перенести репозиторий a в b?
Под полностью подразумевается, что должны сохраниться все ветки и все коммиты.

**Answer:**

    git clone --bare git@git.test.com:my-repo-a.git
    git fetch origin
    git remote add new-origin git@git.test.com:my-repo-b.git
    git push --mirror new-origin
    git remote rm origin
    git remote rename new-origin origin

Источник: https://www.smashingmagazine.com/2014/05/moving-git-repository-new-server/
