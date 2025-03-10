# [Русский] Debian Almquist Shell (dash) grep Использование: поиск текста в файлах

## Обзор
Команда `grep` используется для поиска строк, соответствующих заданному шаблону, в текстовых файлах. Она полезна для фильтрации данных и анализа текстовой информации.

## Использование
Основной синтаксис команды выглядит следующим образом:

```bash
grep [опции] [аргументы]
```

## Общие опции
- `-i`: Игнорировать регистр при поиске.
- `-v`: Вывести строки, которые не соответствуют шаблону.
- `-r`: Рекурсивно искать в подкаталогах.
- `-n`: Показать номер строки, где найдено совпадение.
- `-l`: Показать только имена файлов, в которых найдено совпадение.

## Общие примеры
Вот несколько практических примеров использования команды `grep`:

1. Поиск строки "example" в файле `file.txt`:
   ```bash
   grep "example" file.txt
   ```

2. Поиск строки "example" без учета регистра:
   ```bash
   grep -i "example" file.txt
   ```

3. Поиск строки "example" во всех файлах в текущем каталоге:
   ```bash
   grep "example" *
   ```

4. Рекурсивный поиск строки "example" в каталоге `mydir`:
   ```bash
   grep -r "example" mydir/
   ```

5. Показать номера строк, где найдено совпадение:
   ```bash
   grep -n "example" file.txt
   ```

## Советы
- Используйте опцию `-i`, если не уверены в регистре текста.
- Комбинируйте опции для более точного поиска, например, `grep -rin "example" mydir/`.
- Для поиска по большому количеству файлов используйте `grep` вместе с `find` для более эффективного поиска.