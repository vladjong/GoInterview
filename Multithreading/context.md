# Context

## Определение

Context - объект, который служит для хранения значения и сообщать о завершение.

## Создание Context

```
ctx := context.Background() // создает корневой контекст

ctx := context.TODO() // пригоден для тестов
```

## Виды дочерних контекстов

### With value

```
withValue := context.WithValue(ctx, key, value)
```

Антипатерн использование данного контекста, лучше передовать переменные в функции!

### With cancel

```
withValue, cancel := context.WithCancel(ctx) // cancel - функция которая завершает контекст
cancel() // завершаем context
```

Надо закрывать context на том уровне где его создаем!

### With deadline

```
withDeadliine, cancel := context.WithDeadline(ctx, time.Now().Add(time.Second * 3)) // через 3 секунды он должен завершиться
defer cancel()
```

### With timeout

```
withDeadliine, cancel := context.WithDeadline(ctx, time.Second * 3) // через 3 секунды он должен завершиться
defer cancel()
```

## Методы контекста

1. Deadline() - 
2. Error() - вывод ошибку
3. Done() - ждет завершения контекста и печатает значение из канала