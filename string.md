# Строки Go

String - это байтовый срез, предназначенный только для чтения.

```
message := "shalom"
```

Строки нельзя редактировать, можно получить доступ к отдельному символу.

```
c := message[5]
message[5] = 'd' // Нельзя присвоить message[5]
```

Эффективный способ конкатенации строк

```
func concat2builder(x, y string) string {
    var builder strings.Builder
    builder.Grow(len(x) + len(y)) // Только эта строка выделяет память
    builder.WriteString(x)
    builder.WriteString(y)
    return builder.String()
}
```
