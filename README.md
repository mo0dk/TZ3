# Food Delivery Application Design

## Описание системы

Приложение предназначено для доставки еды. Оно позволяет пользователям просматривать меню различных ресторанов, выбирать блюда, оформлять заказы и отслеживать их статус в реальном времени. Система включает несколько основных компонентов: пользовательский интерфейс, модуль управления заказами, модуль управления курьерами, модуль оплаты и интеграция с ресторанами. Основные роли в системе: пользователь, администратор и курьер.

### Основные сценарии

1. **Регистрация и вход пользователя в систему**: Пользователь может зарегистрироваться и войти в систему для получения персонализированного опыта.
2. **Просмотр меню ресторанов и выбор блюд**: Пользователь может просматривать меню доступных ресторанов и выбирать блюда для заказа.
3. **Оформление и оплата заказа**: Пользователь может оформить заказ, указав адрес доставки и выбрав способ оплаты (например, картой или наличными).
4. **Отслеживание статуса заказа**: Пользователь может отслеживать статус заказа от момента его оформления до доставки.
5. **Получение заказа курьером и доставка пользователю**: Курьер получает задание на доставку, забирает заказ из ресторана и доставляет его пользователю.

## UML Диаграммы

### 1. Диаграмма вариантов использования (Use Case Diagram)
![](use_case2.drawio.png)

**Акторы:**
- Пользователь
- Администратор
- Курьер

**Основные сценарии:**
1. Пользователь
- Регистрация и вход в систему
- Просмотр меню и выбор блюд
- Оформление и оплата заказа
- Отслеживание статуса заказа
- Просмотр истории заказов
- Оценка и отзыв о заказе
- Уведомления о статусе заказа
- Чат с поддержкой
2. Администратор
- Управление пользователями
- Управление ресторанами
- Управление меню ресторанов
- Управление заказами
- Просмотр отчетов и статистики
- Уведомления о статусе заказа
- Чат с поддержкой
3. Курьер
- Просмотр назначенных заказов
- Подтверждение получения заказа
- Обновление статуса доставки
- Подтверждение доставки заказа
- Уведомления о статусе заказа
### 2. Диаграмма последовательности (Sequence Diagram)
![](SequencDiagram.drawio(1).png)

Процесс заказа еды:
1. Пользователь выбирает ресторан и просматривает меню.
2. Пользователь добавляет выбранные блюда в корзину.
3. Пользователь оформляет заказ и выбирает способ оплаты.
4. Система проверяет наличие блюд и подтверждает заказ.
5. Пользователь получает подтверждение заказа и статус "В обработке".
6. Система передает информацию о заказе ресторану и курьеру.
7. Курьер получает задание на доставку.
8. Курьер доставляет заказ пользователю.

### 3. Диаграмма состояний (State Diagram)
![](StateDiagram.png)

Статусы заказа:
- Создан
- В обработке
- Подтвержден
- Готовится
- В пути
- Доставлен
- Отменен

### 4. Диаграмма деятельности (Activity Diagram)
![](ActivityDiagram.png)

Процесс обработки заказа:
1. Получение заказа от пользователя.
2. Проверка наличия блюд.
3. Подтверждение заказа и уведомление пользователя.
4. Передача информации о заказе ресторану.
5. Подготовка заказа рестораном.
6. Назначение курьера для доставки.
7. Доставка заказа курьером.
8. Завершение заказа.

### 5. Диаграмма классов (Class Diagram)
![](ClassDiagram.drawio(1).png)

Модули системы:
- Пользовательский интерфейс:
  - Классы: User, Authentication
- Модуль управления заказами:
  - Классы: Order, Item, Menu, Restaurant
- Модуль управления курьерами:
  - Классы: Courier, DeliveryAssignment
- Модуль оплаты:
  - Классы: Payment, Invoice
- Модуль интеграции с ресторанами:
  - Классы: RestaurantIntegration, MenuSync
