---
title: Статьи Git | Составление файла .gitignore
keywords: файл .gitignore
sidebar: articles_sidebar
folder: articles
permalink: articles-git-gitignore.html
summary: false
toc: false
---

## Общее описание

Файл .gitignore предназначен для исключения из индексации Git файлов и папок проекта.

Размещаться этот файл может в любой папке проекта и количество этих файлов в разных папках не ограничено. 
Зона действия файла распространяется от папки в которой он лежит и на все вложенные файлы и папки.

Чаще всего файл .gitignore помещают в корневую папку проекта и от нее настраивают необходимые исключения для Git.

## Примеры работы с файлом .gitignore

* Добавить в исключения папку

```
# только папку example в корне проекта
/example
# аналогично
/example/
# аналогично
/example/*
```

**!!!Внимание:** разница между записями ```/example/``` и ```/example/*``` в том, 
что при выполнении команды ```git clean -df``` при записи ```/example/*``` будет удалена и папка example, а в случае с ```/example/```
будут удалены файлы в папке example, сама же папка удалена не будет.

