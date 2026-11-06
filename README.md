
# Отчёт по лабораторной работе №6: Система контроля версий

**Цель лабораторной работы:** изучение базовых возможностей системы управления версиями, опыт работы с Git API, опыт работы с локальным и удаленным репозиториями.

## 1. Снимки экрана

**1. Настройка клиента Git и клонирование репозитория:**
![Настройка имени, почты и клонирование](Lab6/sc1.png)

**2. Форк личного репозитория на GitHub:**
![Репозиторий на GitHub](Lab6/sc2.png)

**3. Граф веток и история коммитов:**
![Результат команды git log](Lab6/sc3.png)

## 2. Лог команд

```bash
git config --global user.name "4514 Удалый В. П."
git config --global user.email "work2show@gmail.com"
git config --list
cd ~/Labs
git clone https://github.com/GigglyArtist/LR6.git
cd LR6
ls
git status
git pull
git branch
git checkout -b feature
git add hello.txt
git commit -m "Добавил текст в ветку feature"
git checkout master
git add hello.txt
git commit -m "Добавил конфликтный текст"
git log --oneline --graph --all
git merge feature
git add hello.txt
git commit -m "Разрешен конфликт слияния"
git branch -d feature
git branch
echo "Строка для первого коммита" >> hello.txt
git add hello.txt
git commit -m "Добавил первую строку"
echo "Строка для второго коммита" >> hello.txt
git add hello.txt
git commit -m "Добавил вторую строку"
echo "Строка для третьего коммита" >> hello.txt
git add hello.txt
git commit -m "Добавил третью строку"
git log --oneline
git revert HEAD --no-edit
git log --oneline
git checkout -b report
```
