### ASCII язык, описывающий КС-грамматики

- Нетерминалы заключаются в @.
```text
@EXAMPLE@
```

- Терминалы заключаются в &.
```text
&example&
```

- Пустой символ.
```text
%%%%%
```

- Начало описания правила.
```text
<<><>>
```

- Разделение правил.
```text
~
```

- Конец описания правила.
```text
|||||
```

- Начальный нетерминал.
```text
-->@EXAMPLE@
```

> Использование `&` и `@` происходит с префиксом `\ `.

### Пример

```text
-->@S@
@S@ <<><>> &(& @S@ &)& ~ %%%%% |||||
```

[Другие примеры живут здесь. (ТЫК)](./tests)

### Запуск
Запуск лексера:
```shell
python3 lex.py `your_file.in`
```

Запуск парсера:
```shell
python3 pasrser.py `your_file.in`
```