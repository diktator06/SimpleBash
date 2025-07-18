  Учебные утилиты `s21_cat` и `s21_grep`

Репозиторий содержит 2 маленьких проекта на языке C (School 21): клоны утилит `cat` и `grep`.



  Быстрый старт

```bash
  Сборка
make cat      # создаёт ./s21_cat
make grep     # создаёт ./s21_grep

  Быстрые регрес‑тесты
chmod +x cat.sh grep.sh
./cat.sh      # сравнивает вывод с системным cat
./grep.sh     # сравнивает вывод с системным grep
```


  1. `s21_cat` — аналог GNU `cat`

| Что делает | Ключевые флаги |
|------------|----------------|
| Вывод файлов, объединение STDIN → STDOUT | `-b  -n  -s  -E  -T  -e  -t  -v` |

  Запуск примеров
```bash
  печать файла с нумерацией всех строк
./s21_cat -n file.txt
```


  2. `s21_grep` — аналог GNU `grep`

| Что делает | Ключевые флаги |
|------------|----------------|
| Поиск/regex по файлам и STDIN | `-e  -i  -v  -c  -l  -n  -h  -s  -f  -o` |

  Запуск примеров
```bash
  вывод строк и номеров, содержащих 'int'
./s21_grep -n "int" s21_grep.c
```


  
  Структура репозитория

```
s21_cat.c      исходник cat
s21_cat.h
cat.sh         bash‑тесты cat
s21_grep.c     исходник grep
s21_grep.h
grep.sh        bash‑тесты grep
pattern.txt    шаблоны для опции -f
Makefile       цели: cat  grep  clean
```

  Требования

  GCC (C11) или совместимый компилятор  
  Linux / macOS (проверено на Ubuntu 22.04)


