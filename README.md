mkdir ExamTP1
cd ExamTP1
git clone https://github.com/USERNAME/ExamTP1.git
cd ExamTP1

echo *.jpeg > .gitignore
git add .gitignore
git commit -m "gitignore"

echo test > image.jpeg

git checkout -b journal1

nano taches.txt
git add taches.txt
git commit -m "tache1"

nano taches.txt
git add taches.txt
git commit -m "tache2"

git checkout main

nano taches.txt
git add taches.txt
git commit -m "tache2-3"

git merge journal1
nano taches.txt
git add taches.txt
git commit -m "resolve"

git log --oneline --graph --decorate

git checkout journal1
nano taches.txt
git add taches.txt
git commit -m "tache4"

nano taches.txt
git add taches.txt
git commit -m "tache5"

git checkout main
git merge --squash journal1
git commit -m "squash merge"

git push origin main
git push origin journal1
