# Подключение онлайн-платежей

## Провайдеры онлайн-платежей
1. [Яндекс.Касса](yandeks.kassa-yandex.kassa.md) (с поддержкой онлайн-касс)
2. [Ассист](assist-assist.md)

## Алгоритм работы с интернет-кассой по ФЗ-54
1. Интернет-магазин Zeta Web принимает оплату на сайте с помощью платежного шлюза Яндекс.Кассы.

2. Платежный шлюз передает данные об оплате в онлайн-кассу (фискальный регистратор), привязанную к нему. 
Перечень онлайн-касс, поддерживаемый шлюзом: https://kassa.yandex.ru/54fz.html

3. Онлайн-касса высылает данные об оплате в ОФД.

4. ОФД высылает чек пользователю (если необходимо).

## Последовательность действий для подключения
1. Купить или взять в аренду онлайн-кассу,совместимую с Яндекс.Кассы.
2. Зарегистрировать и настроить кассу.
3. Интегрировать кассу с Яндекс-кассой.
4. Подключить Zeta Web к Яндекс-кассе (необходим сертификат SSL и подключение по протоколу https)

