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

git clone https://github.com/USERNAME/ExamTP1.git ExamTPL1
cd ExamTPL1

git config --global user.name
git config --global user.email

git log

nano app.py
git add app.py
git commit -m "add app.py"

nano app.py
git add app.py
git commit -m "add average"

git log --oneline

git commit --amend -m "add sum and average"

git checkout -b feature-stats

nano app.py
git add app.py
git commit -m "add max"

git checkout main

nano app.py
git add app.py
git commit -m "update app.py"

git merge feature-stats

nano app.py
git add app.py
git commit -m "resolve conflict"

git checkout -b feature-min

nano app.py
git add app.py
git commit -m "add min"

git commit --amend -m "fix indentation"

git rebase -i HEAD~2

git checkout main
git rebase feature-min

git push origin main
git push origin feature-stats
git push origin feature-min
