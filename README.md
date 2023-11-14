# 03-customer-churn

**Задача:**
Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых.

Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. Мне предоставлены исторические данные о поведении клиентов и расторжении договоров с банком.

Необходимо построить модель с предельно большим значением F1-меры (не меньше 0,59). 

Источник данных: https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling

**Признаки:**
- RowNumber —индекс строки в данных
- CustomerId— уникальный идентификатор клиента
- Surname —фамилия
- CreditScore —кредитный рейтинг
- Geography —страна проживания
- Gender —пол
- Age —возраст
- Tenure —сколько лет человек является клиентом банка
- Balance —баланс на счёте
- NumOfProducts —количество продуктов банка, используемых клиентом
- HasCrCard —наличие кредитной карты
- IsActiveMember —активность клиента
- EstimatedSalary —предполагаемая зарплата

**Вывод:**
В работу поступила задача от "Бета-Банка", из которого ежемесячно стали уходить клиенты. 
Передо мной стояла задача спрогнозировать уйдет клиент из банка в ближайшее время или не уйдет.

Для решения данной задачи я протестировала три модели: модель решающего дерева, модель случайного леса и модель логистической регрессии. 
Наилучший результат, т.е. наибольшее значение F1-меры, удалось достичь модели случайного леса на увеличенной выборке. 
ROC кривая также подтвердила, что модель работает и отличается от случайной. 
Тестирование модели подтвердило ее работоспособность (F1=0.61 на тестовых данных).

Наибольшее количество клиентов банка - это люди в возрасте от 30 до 40 лет, которые пользуются одним или двумя продуктами банка.
Наибольшее влияние на решение клиентов уйти или остаться оказали такие факторы как "NumOfProducts"
("Количество продуктов, используемых клиентов") и "Age" ("Возраст") клиентов банка.
