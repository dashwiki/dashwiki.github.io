# [Русский] Debian Almquist Shell (dash) mkdir использование: создание каталогов

## Обзор
Команда `mkdir` используется для создания новых каталогов в файловой системе. Она позволяет пользователям организовывать файлы и директории, создавая структуру, которая упрощает навигацию и управление данными.

## Использование
Основной синтаксис команды выглядит следующим образом:

```bash
mkdir [опции] [аргументы]
```

## Общие опции
- `-p`: Создает промежуточные каталоги, если они не существуют.
- `-m`: Устанавливает права доступа для создаваемого каталога.
- `--help`: Показывает справочную информацию по команде.

## Общие примеры
Создание одного каталога:

```bash
mkdir новый_каталог
```

Создание нескольких каталогов одновременно:

```bash
mkdir каталог1 каталог2 каталог3
```

Создание каталога с промежуточными директориями:

```bash
mkdir -p /путь/к/каталогу/новый_каталог
```

Создание каталога с заданными правами доступа:

```bash
mkdir -m 755 новый_каталог
```

## Советы
- Используйте опцию `-p`, чтобы избежать ошибок при создании вложенных каталогов.
- Проверяйте права доступа после создания каталога, чтобы убедиться, что они соответствуют вашим требованиям.
- Регулярно организуйте свои файлы и каталоги для упрощения поиска и управления данными.