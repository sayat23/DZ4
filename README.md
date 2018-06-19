Домашнее задание №4
Задание #1. Практика с ООП
Представьте что вы создаете сайт для компании сдающих автомобили поминутно
(каршеринг). У компании есть ряд тарифов. Вам необходимо реализовать каждый
тариф в своем классе. У каждого тарифа две основные характеристики - цена за 1 км,
цена за 1 минуту. Каждый тариф обязан иметь метод для подсчета цены поездки. В
некоторых тарифах возможно использование дополнительных услуг, которые могут
быть объявлены с помощью механизма trait. Минимальный возраст водителя - 18 лет,
максимальный - 65 лет. В случае возраста от 18 до 21 года, тариф повышается на
10%. Ваша задача - посчитать цену, которую получит пользователь, если проедет Х км
и Y минут по тарифу Z.
Тариф базовый
● цена за 1 км = 10 рублей
● цена за 1 минуту = 3 рубля
Тариф почасовой
● Цена за 1 км = 0
● Цена за 60 минут = 200 рублей
● Округление до 60 минут в большую сторону
Тариф суточный
● цена за 1 км = 1 рубль
● цена за 24 часа = 1000 рублей
● округление до 24 часов в большую сторону, но не менее 30 минут. Например 24
часа 29 минут = 1 сутки. 23 часа 59 минут = 1 сутки. 24 часа 31 минута = 2 суток.
Тариф студенческий
● цена за 1 км = 4 рубля
● цена за 1 минуту = 1 рубль
● Возраст водителя не может быть более 25 лет
Дополнительные услуги (трейты):
- gps в салон - 15 рублей в час, минимум 1 час. Округление в большую сторону.
Доступно на всех тарифах
- Дополнительный водитель - 100 рублей единоразово, доступен на всех
тарифах кроме базового и студенческого
Ожидаемая реализация:
1. Создать интерфейс, который будет содержать описание метода подсчета цены
и другие необходимые функции
2. Реализовать абстрактный класс, который будет описывать основные методы и
заниматься определением возраста и имплементировать описанный в п. 1
интерфейс
3. Все тарифы должны наследоваться от абстрактного тарифа из п. 2
4. Дополнительные услуги реализовываются с помощью механизма трейтов. Они
доступны по умолчанию, но не активированы. Активация происходит путем
передачи аргументов в конструктор класса.
Пример вызова:
Тариф базовый(5 км, 1 час, 20 лет, без доп. услуг) = (5 * 10 + 60 * 3) * 1.1 = 253 руб; (5
км по 10 рублей плюс 60 минут по 3 рубля) * коэффициент молодежный 1.1 = 253
