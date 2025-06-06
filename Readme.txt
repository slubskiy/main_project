Перед нами стояла задача разработать решение, которое позволит персонализировать предложения постоянным клиентам, чтобы увеличить их покупательскую активность.

Исходные данные у нас были в виде четырех датасэтов. В результате предобработки мы избавились от пропусков и дубликатов, привели строчные значения к одному регистру и исправили неверные форматы в данных.

Провели исследовательский анализ данных. Избавились от вылетов и аномалий, а так же исключили 3х клиентов, которые не подходили под условие совершения покупок последние 3 месяца.

Объединили таблицы и провели корреляционный анализ признаков, по результатом которого избавились от мультиколленеарности

Выполнили подготовку пайплайнов и выполнили поиск лучшей модели с перебором гиперпараметров и без. Лучшей моделью оказалась SVC - "метод опорных векторов" c параметром 'kernel = rbf' и значением метрики roc_auc=0.91.

Выполнили анализ важности признаков. Наименее важными оказались популярные категории товаров у пользователей, а так же разрешение на отправку сообщений с акциями. Наиболее важным признаком оказалось duration (время прошедшее с момента регистрации), time_previous_month (время проведенное на сайте в предыдущем месяце), mean_view_cat_per_visit (средний просмотр категория за визит).

Выполнили сегментацию покупателей и выяснили, что покупатели, у которых категория "товары_для_детей" и у которых снизилась покупательская активность, в основном покупают по акции, практически не рассматривают другие категории за визит, просматривают мало страниц и проводят меньше времени на сайте, чем покупатели, у которых активность осталась на прежнем уровне. Одним из предложений для данного сегмента - это устроить акцию.