# Slice

##  Определение

Slice - динамически расширяемый массив

## Структура slice

```
type slice struct {
    array unsafe.Pointer // позволяет обойти систему типов и преобразование между произвольными типами
    len int // текущая длина среза
    cap int // длина внутреннего массива
}
```

## Иницилизация

```
s := make(
	[]int, 
	10, // len 
	10, // cap
)
```

При создании среза нужно выставлять большой cap, чтобы избежать новых аллокаций и копирований
