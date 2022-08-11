# Паттерны

## Decorator - structural design pattern

Decorator - динамически наделяет объект новыми возможностями

Это структура с полем интерфейса, который реализует базовая структура, которую мы хотим изменить   

[Пример паттерна](https://github.com/vladjong/L2/blob/develop/pattern/09_decorator.go "Decorator")

## Adapter

Adapter - преобразует интерфейс класса к другому интерфейсу, на который расчитан клиент. Адаптер обеспечивает совместную работу классов невозможную в обычных условиях из-за несовместимости интерфейсов.

[Пример паттерна](https://github.com/vladjong/L1/blob/main/ex21/ex21.go "Adapter")

## Facade

Facade - это структура, которая маскирует более сложную систему и служит высокоуровневым интерфейсом для пользователя

[Пример паттерна](https://github.com/vladjong/L2/blob/develop/pattern/01_facade.go "Facade")

## Template method

Template method - задает скелет алгоритма в методе, оставляю определение реализации некоторых шагов субкласса. Субклассы могут переопрделять некоторые части алгоритма без изменения структуры

[Пример паттерна](https://github.com/vladjong/L2/blob/develop/pattern/10_template_method.go "Template method")

## Strategy

Strategy паттерн - это шаблон позволяет изменять поведение объекта во время выполнения программы

[Пример паттерна](https://github.com/vladjong/L2/blob/develop/pattern/07_strategy.go "Strategy")

## Factory

Factory - определяет общий интерфейс создания объектов в родительской структуре и позволяющий изменять дочерний объекты в дочернем классе

[Пример паттерна](https://github.com/vladjong/L2/blob/develop/pattern/06_factory.go "Factory")

## Builder

Builder - интерфейс, который реализует поэтапное конструирование объекта

## Visitor

Visitor - расширяет функциональность класса, не изменяя его первоначальную реализацию. Visitor - является интерфейсом, который является параметром метода базового класса.

## Command

Command позволяет представить запрос в виде объекта. Из этого следует, что команда - это объект. Такие запросы, например, можно ставить в очередь, отменять или возобновлять

## Chain of responsible

Chain of responsible - это поведенческий шаблон проектирования, позволяет создавать цепочку обработчиков запросов.
Для каждого входящего запроса он передается по цепочке и каждому из обработчиков
Когда использовать:
- шаблон применим, когда есть несколько кандидатов для обработки одного и того же запроса.
- когда клиент не знает получателя, ему не надо выбирать получателя

## State

State - основан на конечном автомате.
Использовать нужно, когда:
- объект может находиться в нескольких состояний. В зависимости от запроса он должен изменить свое состояние.
- объект когда объект имеет разные ответы на один и тот же запрос в зависимости от состояния
Предотвратит множественное if else