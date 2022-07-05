# devops-netology
edit 1
added gitignore

Will be ignored all directoreis, files and file types including wildcards wich are listed
in this file .gitignore e.g. local directories, .tfstate files, crash logs, tfvars files, override
files, CLI configuration files.

# Задание по лекции ветвление в Git
https://github.com/wittmann-spb/devops-netology

# Домашнее задание к занятию «2.4. Инструменты Git»

1. Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.

ОТВЕТ: можно git show, но имхо удобнее

$ git log aefea -n 1

commit aefead2207ef7e2aa5dc81a34aedf0cad4c32545

Author: Alisdair McDiarmid <alisdair@users.noreply.github.com>

Date:   Thu Jun 18 10:29:58 2020 -0400



    Update CHANGELOG.md

2. Какому тегу соответствует коммит 85024d3?

ОТВЕТ: (tag: v0.12.23)
$ git show 85024d3
commit 85024d3100126de36331c6982bfaac02cdab9e76 (tag: v0.12.23)

3. Сколько родителей у коммита b8d720? Напишите их хеши.

ОТВЕТ:
git show --pretty=format:' %P' b8d720

Хэши

56cd7859e05c36c06b56d013b55a252d0bb7e158

9ea88f22fc6269854151c571162c5bcf958bee2b

4. Перечислите хеши и комментарии всех коммитов которые были сделаны между тегами v0.12.23 и v0.12.24.

ОТВЕТ:
git log v0.12.23..v0.12.24 --oneline

Хэши + комментарии

33ff1c03b (tag: v0.12.24) v0.12.24

b14b74c49 [Website] vmc provider links

3f235065b Update CHANGELOG.md

6ae64e247 registry: Fix panic when server is unreachable

5c619ca1b website: Remove links to the getting started guide's old location

06275647e Update CHANGELOG.md

d5f9411f5 command: Fix bug when using terraform login on Windows

4b6d06cc5 Update CHANGELOG.md

dd01a3507 Update CHANGELOG.md

225466bc3 Cleanup after v0.12.23 release

5. Найдите коммит в котором была создана функция func providerSource, ее определение в коде выглядит так func providerSource(...) (вместо троеточего перечислены аргументы).

ОТВЕТ:

git log -S'func providerSource(' --oneline

8c928e835 main: Consult local directories as potential mirrors of providers

6. Найдите все коммиты в которых была изменена функция globalPluginDirs.

ОВТЕТ:

git grep 'func globalPluginDirs'

git log -L :'func globalPluginDirs':plugins.go --oneline

commit 8364383c3 - создана

commit 66ebff90c - изменена

commit 41ab0aef7 - изменена

commit 52dbf9483 - изменена

commit 78b122055 - изменена

7. Кто автор функции synchronizedWriters?

ОТВЕТ:

git log -S'func synchronizedWriters(‘ --pretty=format:'%h - %an %ae'

bdfea50cc - James Bardin j.bardin@gmail.com

5ac311e2a - Martin Atkins mart@degeneration.co.uk

git show bdfea50cc - удалена

git show 5ac311e2a - создана

автор:

Martin Atkins mart@degeneration.co.uk

# Домашнее задание к занятию "3.1. Работа в терминале, лекция 1"

https://github.com/wittmann-spb/devops-netology/edit/main/hw3-1.md
