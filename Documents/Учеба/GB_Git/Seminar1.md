# Работа с Git и GitHub
## 1. Проыерка наличия установленного гида
В терминале выполнить команду 'git version'
Если Git установлен, появится сообщение о версии, иначе будет сообщение об ошибке.
## Установка Git
Загружаем последн.. версию с сайта [Установка Git](https://git-scm.com/downloads).
Устанавливаем последнюю версию по умолчанию.
## 3. Настройка Git
При первом использовании Git необходимо представиться.
Для этого нужно ввести в терминале 2 команды:
```
git config --global user.name "Ваше имя английскими буквами"
git config --global user.emal "Ваша почта@example.com"
```
## 4. Инициализация репозитория
В терминале переходим к папке, в которой хотим создать репозиторий. Выполняем команду 
```
git init
```
## 5. Запись изменения в репозиторий
Чтобы просмотреть изменения, вызывается команда:
```
git diff 
Для выхода из списка нажмите клавишу "q".
```
Чтобы проверить статус репозитория используйте команду:
```
git status 
```
После внесения изменений, необходимо добавить все файлы проекта в репозиторий. Для это используйте команду 
```
git add . или git add --all
NB! все без исключения файлы будут добавлены.
```
Если нужно добавить конкретный файл, то используйте команду 
``` git add <Имя_файла>
```
Теперь создаем комит, обязательно с комментарием в кавычках:
```
git commit -m "<комментарий>"
```

Поздравляем, ваш первый комит создан!

## 6. Просмотр истории комитов
Чтобы посмотреть историю комитов, используйте команду:
```
git log 
```
появятся созданные версии комитов с данными об авторе и файле.
```
Например: commit 00acc1e0646799c1a89ae80f5c8e05073ed1bcc4
Author: Alex <aleksabdra.majerus@gmail.com>
Date:   Thu Jul 13 00:20:27 2023 +0200

где 00acc1e0646799c1a89ae80f5c8e05073ed1bcc4 - номер комита
```

Для более локоничной визуализации можно воспользоваться командой 
```
git log --oneline
```
Тогда информация о файлах будет сокращена и отобразиться в строковом виде.
```
Например:
0de0451 initialization
00acc1e how to download
7b5bc50 how to download

первый столбик - номера комитов
```

## 7. Перемещение между сохранениями
Чтобы перемещаться между файлами для начала проверьте статус последнего командой:
```
git status
```
Далее:
1. Убедитесь, что все изменения добавлены в комит.
2. Воспользуйтесь пунктом 6 для вызова списка всех файлов.
3. Скопируйте первые 4 цифры номера комита и вставьте их в команду
```
git checkout <первые четыре цифры комита>
```
Произойдет переход к нужной версии файла.

Чтобы вернуться к последней версии, наберите команду:
```
git switch master или git switch main
```
Также можно перейти в другую версию командой
```
git switch - c <первые четыре цифры комита>
```

Надеюсь, что эта информация была вам полезна. Удачи!