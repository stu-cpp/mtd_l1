# mtd_l1
modern technologies in development, Lab1

---

## 1. SSH-ключ

1. Сгенерируйте SSH-ключ алгоритмом Ed25519.
Как это сделать, можно прочесть в статье [Generating a new SSH key and adding it to the ssh-agent](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).
1. Добавьте ключ в аккаунт GitHub (см. [Adding a new SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) и [Testing your SSH connection](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/testing-your-ssh-connection)). Сделайте клон этого репозитория, используя SSH
1. Публичный ключ положите в папку `ssh_keys`.
Имя файла должно быть `id_ed25519.pub`
1. Сгенерируйте отпечаток (fingerprint) ключа и скопируйте в файл `id_ed25519_fingerprint.txt`
1. сделайте commit и push

## 2. Добавление кода

1. Создайте в папке `src` подпапки `lab1`, `lab2`, ..., `lab6`, куда положите код лабораторных прошлого семестра (можно просто файлы `lab<x>.c`, если в лабораторной всего один файл кода).
Не следует помещать бинарные и конфигурационные файлы проектов.
1. Создайте файл `src/CMakeLists.txt`, где задайте как минимум 2 компилируемых target'а: один должен собирать бинарник шестой лабораторной, второй - бинарный файл, соответствующий коду в `task3.c`.
По желанию также можно создать таргеты для других лабораторных
1. сделайте commit и push

## 3. Ветвление

В этом задании работаем с файлом `task3.c`

1. Сделайте ветку `refactor/rename_a` и в ней переименуйте переменную `a`, дав ей любое другое имя. Откройте Pull Request в ветку `main`, но не вливайте изменения
1. Сделайте другую ветку из ветки `main` (`refactor/a_type`), где измените тип переменной `a` с `int` на `unsigned int`. Также откройте Pull Request и влейте `refactor/a_type` в `main`
1. Влейте ветку `main` в ветку `refactor/rename_a`, не открывая Pull Request (просто у себя через терминал), сделайте push
1. Влейте оставшийся Pull Request в `main`

---
После выполнения всех заданий откройте pull request в базовый репозиторий.
Убедитесь, что CI успешно проходит (это означает, что первое задание выполнено верно).

