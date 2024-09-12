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
- [Клонируем репозиторий](#клонируем-репозиторий)
- [Ветки](#ветки)
- [Делаем Pull Request](#делаем-pull-request)

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

![Зайдите на GitHub и перейдите в Settings](https://github.com/UlyanaHanush/Git_assistant/blob/main/image/Image.png)

*  В левом меню выберите SSH and GPG keys.

![В левом меню выберите SSH and GPG keys](https://github.com/UlyanaHanush/Git_assistant/blob/main/image/Image-2.png)
  
*  Нажмите New SSH key или Add SSH key.  

![Нажмите New SSH key или Add SSH key](https://github.com/UlyanaHanush/Git_assistant/blob/main/image/Image-3.png)

*  В поле Title введите название ключа (например, название вашего компьютера).  

![В поле Title введите название ключа](https://github.com/UlyanaHanush/Git_assistant/blob/main/image/Image-4.png)
 
*  В поле Key вставьте ключ из буфера обмена горячими клавишами Cmd + V.  

*  Нажмите Add SSH key.  

# Клонируем репозиторий
Откройте терминал и перейдите в папку проектов  

*  Откройте ваш проект в GitHub, нажмите зелёную кнопку Code и скопируйте SSH-адрес проекта

![Откройте ваш проект в GitHub, нажмите зелёную кнопку Code и скопируйте](https://github.com/UlyanaHanush/Git_assistant/blob/main/image/gitClon.png)

Откройте терминал и перейдите в папку проектов:
git clone git@github.com:<ВАШ НИКНЕЙМ>/first-project-git.git second-project-git
cd second-project-git  

Перед выполнением git pull убедитесь, что ваша рабочая версия чиста, то есть все изменения зафиксированы: сделан commit.  
Иногда после выполнения git pull могут возникнуть конфликты слияния, если одни и те же части кода были изменены локально и в удалённом репозитории. В таком случае Git попросит вас разрешить эти конфликты перед тем как продолжить.  

> [!WARNING]\
> Перед выполнением git pull убедитесь, что ваша рабочая версия чиста, то есть все изменения зафиксированы: сделан commit. Иногда после выполнения git pull могут возникнуть конфликты слияния, если одни и те же части кода были изменены локально и в удалённом репозитории. В таком случае Git попросит вас разрешить эти конфликты перед тем как продолжить.  

# Ветки

git branch — просматриваем ветки проекта  
git branch <название_ветки>: создаём ветку  
git checkout <название_ветки>: переключаемся между ветками  

Можно создать ветку и сразу начать в ней работать  
git checkout -b another_branch  

Сливаем ветки  
git merge new_branch  

последние изменения из основной ветки в удалённый репозиторий   
git push -u origin main 

необязательно переходить в ветку, чтобы запушить её  
git push -u origin merge-request 

# Делаем Pull Request

*  Перейдите на страницу репозитория и выберите вкладку Pull requests и нажмите зелёную кнопку New pull request. Выберите названия веток:  ветка «куда» (в которую пулл-реквест будет осуществлён) и ветка «откуда» (из которой будет идти пулл-реквест).

![Перейдите на страницу репозитория и выберите вкладку Pull requests и нажмите зелёную кнопку New pull request](https://github.com/UlyanaHanush/Git_assistant/blob/main/image/pullRequest.png)

В окне отобразятся добавленные коммиты и их изменения. Нажмите Create pull request.  
Заполните поля с названием и описанием пулл-реквеста. Нажмите Create pull request.  
Теперь вы или ваши коллеги могут перейти на вкладку Files changed (англ. «изменённые файлы»), чтобы оставить свои комментарии — провести ревью.  
Осталось только нажать Merge pull request (англ. «принять запрос на изменения»). Это объединит ветку с вашими изменениями и ветку main.  

![Ulyana's GitHub stats](https://github-readme-stats.vercel.app/api?username=ulyanahanush\&show_icons=true\&theme=radical)
