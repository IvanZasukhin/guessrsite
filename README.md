# SiteGuessr
Цель создания сайта — разработка развлекательной платформы, которая даст возможность пользователям угадывать названия случайно выбранных веб-сайтов. Основная функция сайта — генерация скриншота случайного сайта, по которому игроку нужно угадать, какой это сайт. Сайт регулярно обновляется новым контентом и функциями, чтобы поддерживать интерес пользователей, будет добавлена возможность пользоваетлям предлагать новые сайты для игры, а админам принимать поступающие заявки.

# ТЗ
## БД
3 таблицы: websites(id, name, url), users(id, login, description, role, banned, created_date, modified_date, hashed_password), games(id, user_id, websites_id, scores, finish_date), statistic(id, user_id, total_games, correct_answers, wrong_answers, average_score, best_score)
## 1. Общие требования:
1.1. Разработать развлекательную платформу под названием SiteGuessr, предоставляющую возможность пользователям угадывать названия случайно выбранных веб-сайтов.  
1.2. Реализовать функцию перекидывания пользователя на случайный сайт из собственного API.  
1.3. Обеспечить возможность пользователям предлагать новые сайты для игры и администраторам принимать поступающие заявки.  
1.4. Реализовать авторизацию пользователей и сохранение информации по логину в базе данных.  

## 2. Функциональные требования:
2.1. Разработать механизм случайного выбора веб-сайта из собственного API и перекидывания пользователя на этот сайт.  
2.2. Реализовать возможность пользовательской подачи заявок на добавление новых сайтов для игры.  
2.3. Обеспечить администраторам возможность принимать, отклонять и управлять поступающими заявками.  
2.4. Добавить функцию скрытия названия сайта в тексте.  
2.5. Разработать систему авторизации пользователей с возможностью сохранения информации по логину в базе данных.  

## 3. Требования к безопасности:
3.1. Гарантировать безопасность хранения логинов и другой пользовательской информации в базе данных.  
3.2. Обеспечить защиту от несанкционированного доступа к административной функциональности сайта.

# Пояснительная записка
Авторы проекта: Савин Даниил, Засухин Иван
## Описание идеи
SiteGuessr – это развлекательная платформа, которая позволяет пользователям угадывать названия случайно выбранных веб-сайтов. Основной функционал включает в себя генерацию изменёной копии случайного сайта, по которому игроку необходимо угадать, какой это сайт.

## Описание реализации
В основе нашего сайта лежит библиотека Flask, обеспечивающая функциональность сайта, и sqlalchemy для работ за базами данных. Так же мы используем несколько основных классов для работ с базами данных:
- User(id, login, description, role, banned, created_date, modified_date, hashed_password)
- Statistic(id, user_id, total_games, correct_answers, wrong_answers, average_score, best_score)
- Game(id, user_id, websites_id, scores, finish_date)
- Website(id, name, url)
  
Cтруктура БД      
![image](https://github.com/IvanZasukhin/SiteGuessr/assets/120732767/a5b4ef3e-5c75-4e4e-bef4-a5feb05f651a)  
Также реализована система авторизации пользователей с сохранением информации по логину в базе данных.

## Описание технологий + необходимые для запуска библиотеки
- Для запуска проекта необходима библиотека Flask.
- Также необходима datatime для работы со временем.
- Также необходима SQLAlchemy для работы с БД.
- Библиотека Requests также для выполнения HTTP-запросов.
- Библиотека urllib, bs4 и re для парсинга сайтов.
- Библиотека random для рандомизации некоторых элементвов игры.
- Библиотека os, itertools - вспомогательные функции.

# Презентайия  
https://docs.google.com/presentation/d/1NuwgMM5xJufJ6nR9azFz7iXkYbLDaGbriPL8QF-x_-I/edit#slide=id.g2cef894cb7c_0_16
