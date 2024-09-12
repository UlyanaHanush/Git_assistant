<p align="center">
 <img width="100px" src="https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white" align="center" alt="Learn GIT & Terminal" />
<img width="100px" src="https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white" align="center" alt="Learn GIT & Terminal" />
 <h2 align="center">Изучите GIT & Терминал</h2>
 <p align="center">Руководство для начинающих по Контролю версий и Командной строке</p>
</p>
<p align="center">
<a href="/README.md">English</a>
</p>

<p align="center">Обратите внимание, что переводы документации могут быть устаревшими; постарайтесь использовать английскую документацию, если это возможно.</p>

# Оглавление <!-- omit in toc -->

- [Установка Git](#установка-git)
    - [Установка Git](#установка-git)
    - [Работа с файлом настройки .gitconfig](#работа-с-файлом-настройки-.gitconfig)
    - [Cписок всех свойств конфига](#список-всех-свойств-конфигаs)
    - [Чувствительность к регистру](#чувствительность-к-регистру)
    - [Создание локального Git-репозитория](#создание-локального-git-репозитория)
    - [Создать Добавить Сохранить](#создать-добавить-сохранить)
    - [Делаем коммит](#делаем-коммит)
- [Рекомендации](#рекомендации)
- [Генерация SSH-ключа](#генерация-ssh-ключа)
- [Добавляем SSH-ключ в GitHub аккаунт](#добавляем-ssh-ключ-в-github-аккаунт)

# Установка Git
git --version

А если команда не найдена, то воспользуйтесь этой:  
xcode-select --install  

# Работа с файлом настройки .gitconfig
git config --global user.name "Practicum"  
git config --global user.email uluana.hanush@gmail.com  

# Cписок всех свойств конфига
git config --list  

# Чувствительность к регистру
git config --global core.ignorecase false  

# Создание локального Git-репозитория
Создать Папку:  
mkdir  имяПапки  
cd имяПапки  
git init  

«Разгитить» папку:  
rm -rf .git  

# Создать Добавить Сохранить
touch file.txt   
git add file.txt или git add --all или git add .  

# Делаем коммит
git commit -m "Коммит!"  

> [!WARNING]\
> ОБЯЗАТЕЛЬНО на английской раскладке :q! <!-- git попросит ввести название коммита в редакторе по умолчанию. Иногда в таком случае открывается редактор vim. Выйти из Vim. -->

# Рекомендации:
рассматреть подробно служебную информацию из папки .git

# Генерация SSH-ключа

Откройте Terminal и введите команду:  
ssh-keygen -t ed25519 -C "<ВАШ EMAIL при регистрации в GitHub>"  

Дальше команда предложит ввести путь до папки, где нужно сохранить ключ:  
Enter file in which to save the key (/Users/practicum/.ssh/id_ed25519)    
Рекомендую согласиться с предложенным вариантом — просто нажмите Enter.  

Ввести парольную фразу для файла:  
Enter passphrase (empty for no passphrase)  
Этот пароль будет нужен каждый раз, когда вы попробуете распечатать часть ключа.  
Программа предлагает создавать ключ и без пароля; чтобы пропустить шаг, нажмите Enter.  
Дальше выполните команду, которая добавит ключ SSH-агенту (программа, которая запоминает ваш приватный SSH-ключ и автоматически подставляет его при подключении к серверу через SSH) и сохранит его в связке ключей (Keychain):  
ssh-add --apple-use-keychain ~/.ssh/id_ed25519  
Теперь скопируйте публичный ключ id_ed25519.pub в буфер обмена:  
pbcopy < ~/.ssh/id_ed25519.pub  

# Добавляем SSH-ключ в GitHub аккаунт 

*  Зайдите на GitHub и перейдите в Settings (Настройки).  
*  В левом меню выберите SSH and GPG keys.  
*  Нажмите New SSH key или Add SSH key.  
*  В поле Title введите название ключа (например, название вашего компьютера).   
*  В поле Key вставьте ключ из буфера обмена горячими клавишами Cmd + V.  
*  Нажмите Add SSH key.  


![Ulyana's GitHub stats](https://github-readme-stats.vercel.app/api?username=ulyanahanush\&show_icons=true\&theme=radical)
