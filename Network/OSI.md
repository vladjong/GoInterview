## OSI

# Определение

Модель OSI - описывает, как работают сетевые устройства. Это процесс передачи данных, котроые разделили на 7 уровней.

В процессе передачи данных всегда участвуют устройство-отправитель, устройство-получатель, а также сами данные, которые должны быть переданы и получены. С точки зрения рядового пользователя задача элементарна — нужно взять и отправить эти данные. Все, что происходит при отправке и приеме данных, детально описывает семиуровневая модель OSI.

## Физичечский

Отвечает за обмен физическими сигналами между физическими устройствами

## Канальный

Уровень получает биты и кодирует их в Frame

Frame - полезные данные, которым добавлены адресс отправителя и получателя

Задача уровня - сформулировать кадры с адрессом отправителя и получателя, после чего отправить их по сети

## Сетевой

Происходит маршрутизация трафика. Маршрутизатор получают MAC - адрес от коммутаторов и занимаются построениме маршрутов от одного устройства к другому.

Применяется протокол ARP - который преобразует MAC-адрес в IP адрес

## Транспортный

Обеспечивает передачу пакетов по сети.

TCP - обеспечивает, контроль за передачей данных.

UDP - используется для передачи мультимедийных файлов, где потери не важны, критичнее будет задержка.

## Сеансовый

Отвечает за управлением сеансами, управляет взаимодействием между приложениями, открывает возможности синхронизации задач, завершением сеанса, обменв информацией

## Представление

Происходит процесс десериализация - биты преобразуются в нужный тип данных

## Прикладной

Это то, с чем взаимодействует пользователь, своего рода графический интерфейс.

Задача уровня использовать свои протоколы, чтобы пользователь увидел данные в понятном ему виде.

Протоколы - DHCP, TCP, HTTP, HTTTPS, DNS.