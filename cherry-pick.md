#cherry-pick

git checkout master

git cherry-pick commit1

git cherry-pick commit1 commit2

** If the cherry picking gets halted because of conflicts, resolve them and

git cherry-pick --continue

git cherry-pick --abort
