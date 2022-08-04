# Mutex

## Определение

Mutex - специальная структура из пакета sync.

Основная цель - обеспечивать безопасный доступ к ресурсам.

## Методы

```
mu.Lock() // блокировка доступа к общим ресурсам

mu.Unlock() // разблокировка доступа к общим ресурсам
```

## RWMutex

Позволяет параллейно читать данные у объекта, но блокируется на запись. 

Обеспечивается параллейное чтение между горутинами, что увеличивает производительность.

# Советы

1. В структуре мьютекс помещается выше тех полей, которых он будет защищать

```
var sum struct {
    sync.Mutex     // <-- этот мьютекс защищает
    i int          // <-- это поле под ним
}
```

2. Держать блокировку min количество времени, чтобы не терять преимущество в конкурентном алгоритме

3. Использовать `defer`, там где у функции есть много return. Чтобы избежать дедлоков.