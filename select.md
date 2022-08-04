# Select

## Определение

Select - это swich case для работы с каналами

## Приоритеты case

1. Блокирующая операция - прочитать данные из канала (2 приоритет)

2. Неблокирующая операция - записать данные в канал, когда буфер заполнен (1 приоритет)

3. Default (3 приоритет)

```
package main

import (
    "fmt"
    "time"
)

func main() {

    c1 := make(chan string)
    c2 := make(chan string)

    go func() {
        time.Sleep(1 * time.Second)
        c1 <- "one"
    }()
    go func() {
        time.Sleep(2 * time.Second)
        c2 <- "two"
    }()

    for i := 0; i < 2; i++ {
        select {
        case msg1 := <-c1:
            fmt.Println("received", msg1)
        case msg2 := <-c2:
            fmt.Println("received", msg2)
        }
    }
}
```