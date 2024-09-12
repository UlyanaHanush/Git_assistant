<p align="center">
 <img width="100px" src="https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white" align="center" alt="Learn GIT & Terminal" />
<img width="100px" src="https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white" align="center" alt="Learn GIT & Terminal" />
 <h2 align="center">Learn GIT & Terminal</h2>
 <p align="center">Beginner's Guide to Version Control & Command Line</p>
</p>
<p align="center">
<a href="/docs/readme_fr.md">Русский </a>
</p>

##Установка Git
git --version

А если команда не найдена, то воспользуйтесь этой:
xcode-select --install

#Работа с файлом настройки .gitconfig
git config --global user.name "Practicum"
git config --global user.email practicum@ya.ru

#Cписок всех свойств конфига
git config --list

#Чувствительность к регистру
git config --global core.ignorecase false

#Создание локального Git-репозитория.
1. Создать Папку
mkdir  Папка
cd Папка
git init

#«Разгитить» папку
rm -rf .git

#Создать/добавить или добавить все или добавить текущую папку/сохранить
touch file.txt 
git add file.txt или git add --all или git add .

#Делаем коммит
git commit -m "Коммит!"

> [Caution: git commit]
> ОБЯЗАТЕЛЬНО на английской раскладке :q! <!-- git попросит ввести название коммита в редакторе по умолчанию. Иногда в таком случае открывается редактор vim. Выйти из Vim. -->

##Рекомендации:
рассматреть подробно служебную информацию из папки .git

[![Ulyana's GitHub stats](https://github-readme-stats.vercel.app/api?username=anuraghazra)](https://github.com/anuraghazra/github-readme-stats)
