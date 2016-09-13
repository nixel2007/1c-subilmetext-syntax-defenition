# 1c-syntax

[![Join the chat at https://gitter.im/xDrivenDevelopment/1c-syntax](https://badges.gitter.im/xDrivenDevelopment/1c-syntax.svg)](https://gitter.im/xDrivenDevelopment/1c-syntax?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Build Status](https://travis-ci.org/xDrivenDevelopment/atom-language-1c-bsl.svg?branch=master)](https://travis-ci.org/xDrivenDevelopment/atom-language-1c-bsl)
[![Build status](https://ci.appveyor.com/api/projects/status/y42clq0jgf3vth2c/branch/master?svg=true)](https://ci.appveyor.com/project/nixel2007/atom-language-1c-bsl/branch/master) (atom-grammar-test)

Syntax definition rules for 1C:Enterprise 8 for tmLanguage-based text editors (Sublime Text, Atom and VS Code).

## Цель репозитория
Данный репозиторий создан для консолидации работ по развитию пакетов, добавляющих поддержку языка 1С:Предприятие 8 для текстовых редакторов [Atom](https://atom.io/), [Sublime Text](http://www.sublimetext.com/) и [Visual Studio Code](https://www.visualstudio.com/en-us/products/code-vs.aspx).  
Под каждый из редакторов создан отдельный репозиторий и опубликован соответствующий пакет на площадке распространения пакетов:

| Репозиторий | Пакет |
|:---:|:---:|
| [Sublime Text](https://github.com/xDrivenDevelopment/sublime-language-1c-bsl) | [Package control](https://packagecontrol.io/packages/Language%201C%20(BSL)) |
| [Atom](https://github.com/xDrivenDevelopment/atom-language-1c-bsl) | [Atom.io/packages](https://atom.io/packages/language-1c-bsl) |
| [VS Code](https://github.com/xDrivenDevelopment/vsc-language-1c-bsl) | [Marketplace](https://marketplace.visualstudio.com/items/xDrivenDevelopment.language-1c-bsl) |

Разработка описания грамматики языка на основе [формата TextMate](http://manual.macromates.com/en/language_grammars) ведется в специальном [YAML-файле](https://github.com/xDrivenDevelopment/1c-syntax/blob/master/1c.YAML-tmLanguage), описание которого и примеры использования вы можете найти [здесь](http://docs.sublimetext.info/en/latest/extensibility/syntaxdefs.html).

## Связи с другими проектами

Проект 1c-syntax не органичивается репозиториями с описанием грамматики. В рамках наших активностей так же выполнялись/выполняются работы по направлениям:

* Подсветка синтаксиса для Github: библиотека [linguist](https://github.com/github/linguist)
* Подсветка синтаксиса GitLab: библиотека [rouge](https://github.com/jneen/rouge) и братский проект [1c-syntax-for-GitLab](https://github.com/karnilaev/1c-syntax-for-GitLab)
* Подсветка синтаксиса в редакторе Ace: репозиторий [ace](https://github.com/ajaxorg/ace)
* Запуск скриптов OneScript в редакторе Atom: пакеты [atom-script](https://github.com/rgbkrk/atom-script) и [atom-build](https://github.com/noseglid/atom-build)

Планируются работы по направлениям:
* Подсветка синтаксиса в редакторе CodeMirror - для поддержки подсветки в git-сервере BitBucket
* Обновление подсветки в редакторе Highlight.js - для улучшенной поддержки подсветки в git-сервере Gogs и приведения идентификаторов языка к единому виду

## Дополнительные возможности

Помимо, собственно, грамматики, мы пытаемся добавить в редакторы дополнительные
возможности, которые могут упростить работу с 1С.  
На данный момент список таких фич выглядит вот так:

| Функциональность \ Поддержка в редакторах | [Atom](https://github.com/xDrivenDevelopment/atom-language-1c-bsl) | [Sublime Text](https://github.com/xDrivenDevelopment/sublime-language-1c-bsl) | [VS Code](https://github.com/xDrivenDevelopment/vsc-language-1c-bsl) |
|---|:---:|:---:|:---:|
| Подсветка текста запроса внутри модуля и отдельно | Есть | Есть | Есть |
| Блочное комментирование через `//` | Есть | Есть | Есть |
| Список процедур и функций текущего файла | Есть | Есть | Есть |
| Список процедур и функций рабочего каталога | Есть | Есть | Есть |
| Переход к определению процедур и функций | Есть | Есть | Есть |
| Автодополнение процедур и функций глобального контекста | Есть | Есть | Есть |
| Автодополнение процедур и функций, уникальных для OneScript | Нет | Нет | Есть |
| Сниппеты (шаблоны текста) | [Есть](https://github.com/xDrivenDevelopment/1c-syntax/issues/110) | Есть | Есть |
| Использование автоматических отступов по ключевым словам | Есть | Есть | Есть |
| Автоматическое выравнивание блока кода или файла целиком | Есть | Есть | Есть |
| Разворачивание конструкций вида `++`/`+=` и подобных по нажатию `Tab` | Есть | Есть | Есть |
| Автоматическое добавление символа &#124; при добавлении новой строки во время редактирования строкового литерала | Есть | Есть | Есть |
| Запуск скриптов `.os`/`.bsl` с помощью OneScript | Есть | Есть | Есть |
| Линтер на базе `oscript -check` | Есть | Есть | Есть |
| Использование отступов в виде 4х-символьных табов | Есть | Есть | Есть |
| Поиск мест использования процедур | Нет | Нет | Есть |
| Информация о процедуре | Нет | Нет | Есть |
| Предварительный просмотр определения процедуры | Нет | Нет | Есть |
| Автодополнение через точку | Нет | Нет | Есть |
| Подсказка по параметрам процедур | Нет | Нет | Есть |
| Поиск определения | Нет | Нет | Есть |
| Поддержка английского языка конфигурации | Нет | Нет | Есть |
| Создание описания метода | Нет | Нет | Есть |
| Синтакс-помощник по функциям глобального контекста | Нет | Нет | Есть |
| Синтакс-помощник по методам oscript | Нет | Нет | Есть |
| Автоматическая вставка скобок | Нет | Нет | Есть |
| Динамические шаблоны | Нет | Нет | Есть |

Информацию об использовании каждой из возможностей вы найдете в README
соответствующего редактора.

## Сотрудничество

Если вы разработчик и хотите помочь с разработкой пакетов и/или грамматикой, пожалуйста, ознакомьтесь с [гайдом для разработчиков](https://github.com/xDrivenDevelopment/1c-syntax/blob/master/CONTRIBUTING.md).  
Уже поставленные задачи по разработке можно найти на странице [Issues](https://github.com/xDrivenDevelopment/1c-syntax/issues) данного репозитория.
