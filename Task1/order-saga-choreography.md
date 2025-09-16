## Saga-хореография Заказа

Описание событий оформления Заказа

| Этап                                 | Тип события  | Название                      |
|:-------------------------------------|:------------:|:------------------------------|
| Успешная оплата                      |    domain    | PaymentSucceeded              |
| Возврат средств                      | compensation | RefundSucceeded               |
| Ошибка оплаты                        |   failure    | PaymentFailed                 |
| Время оплаты вышло                   |   timeout    | PaymentTimeout                |
| Заказ создан                         |    domain    | OrderCreated                  |
| Заказ отменен                        | compensation | OrderCancelled                |
| Товар добавлен в корзину             |    domain    | ShoppingCartAdded             |
| Товар удален из корзины              | compensation | ShoppingCartDeleted           |
| Доставка начата                      |    domain    | DeliveryStarted               |
| Изменен статус доставки              |    domain    | DeliveryStatusChanged         |
| Доставка отменена                    | compensation | DeliveryCancelled             |
| Товар добавлен на склад              |    domain    | WarehouseGoodAdded            |
| Товар закончился на складе           |    domain    | WarehouseGoodOutOfStock       |
| Товар зарезервирован на складе       |    domain    | WarehouseGoodReserved         |
| Товар снято резервирование на складе |    domain    | WarehouseGoodReserveCancelled |
| Товар ошибка резервирования          |   failure    | WarehouseGoodReserveFailed    |
| Товар таймаут резервирования         |   timeout    | WarehouseGoodReserveTimeout   |