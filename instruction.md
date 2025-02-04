# **Инструкция для работы с Git**

![logo](git.jpg)


## Что такое Git

Git - это одна из реализаций систем контоля версий

## Инициализация пользователя

Чтобы ининциализировать пользвателя, ввести имя и адрес электронной почты, нужно ввести команды:

    git config --global user.name "..."

    git config --global user.email "...@...."

## Подготовка репозитория

Чтобы создать (инициализировать) новый репозиторий в текущей  папке, нужно ввести в терминале команду: 

    git init


## Добавление изменений в репозиторий

Для добавления изменений в репозиторий введите команду:

    git add ./ имя файла

## Проверка статуса репозитория

Для проверки подготовленных, неподготовленных, неотслеживаемых файлов нужно ввести команду

    git status


## Создание коммитов

для создания коммитов используйте команду

    git commit -m ".."

### Просмотр истории коммитов 

для просмотра коммитов в хронологическом порядке используйте комманду

    git log

### Переход между коммитами

для переключения между коммитами используйте комманду

    git checkout 

### Просмотр разницы между коммитами

Для просмотра разницы между коммитами используйте команду:

    git diff

## Ветвления

Ветки нужны для того, чтобы программисты могли вести совместную работу над проектом и не мешать друг другу при этом.
При создании проекта, Git создает базовую ветку. Она называется master веткой. Она считается центральной веткой, т.е. в ней содержится основной код приложения.

### Просмотр существующих веток

Для  просмотра списка всех существующих веток, введите команду:

    git branch


### Создание новых веток

Для создания новой ветки, нужно ввести команду:

    git branch <имя ветки>

### Удаление веток

Чтобы удалить ветку, нужно ввестти команду:

    git branch -d <имя ветки>

Если вы завершили работу над веткой и объединили её с основной, можно её удалить без потери истории. Однако, если выполнить команду удаления до слияния — в результате появится сообщение об ошибке. Этот защитный механизм предотвращает потерю доступа к файлам.

### Слияние веток

Для того, чтобы влить другую ветку в текущую нужно:

- переключиться на ту ветку, **куда** мы вливаем
- ввести команду слияния, указав ту ветку, **которую** вливаем:

    git merge <имя ветки>

### Просмотр всех коммитов всех веток

Для просмотра всех коммитов всех веток, введите команду:

    git log --all --oneline --graph
    
### Создание нового удаленного репозитория

Удаленный репозиторий, который хранится в облаке имеет ряд преимуществ.

### Клонирование

Клонирование - это когда вы копируете удаленный репозиторий к себе на локальный ПК. Это то, с чего обычно начинается любой проект. При этом вы переносите себе все файлы и папки проекта, а также всю его историю с момента его создания. Чтобы склонировать проект, сперва, необходимо узнать где он расположен и скопировать ссылку на него. Можно командой:

    git clone <ссылка>

### Отправка изменений в удаленный репозиторий

Для отправки изменений в удаленный репозиторий используйте команду:

    git push

### Запрос изменений с сервера

Если вы сделали изменения в вашем удаленном репозитории, другие пользователи могут скачать изменения при помощи команды:

    git pull
### Переход от удаленного репозитория.

Перейтит от удаленного репозитория внутри папки к другому можно с помощью команды:

    СD <имя репозитория>