# RuREBus

Приглашаем принять участие в **RuREBus** (Russian Relation Extraction for Business) – соревновании по извлечению отношений(фактов) в постановке, приближенной к индустриальным задачам.

## Мотивация:
Извлечение отношений – одна из самых востребованных бизнесом задач. Существует несколько стандартных корпусов для задачи извлечения отношений на английском языке. Однако, все они достаточно далеки от типичной бизнес-постановки задачи по следующим причинам. 

Во-первых, отношения выделены в тексте достаточно плотно (напротив, в бизнес-задачах часто есть 1-2 вхождения отношений на достаточно объемные тексты). Во-вторых, в стандартных корпусах определены отношения бытового и повседневного характера (отношение работы персоны в компании, купли/продажи, владения, родственные отношения, факты рождения и смерти и т. п.), тогда, как в бизнес-задачах обычно требуется выделять отношения, имеющие специфическую природу, связанную с тематикой предметной области.

Целью дорожки является сравнение методов извлечения отношений на русском языке в постановке, приближенной к практике. Для этого предлагается использовать корпус Минэкономразвития (МЭР) (около 280 млн. токенов). 

Корпус представляет собой различные отчеты региональных органов о проделанной работе и запланированных мероприятиях, а также прогнозы и планы на будущее. Некоторое подмножество корпуса будет размечено специальными именованными сущностями (8 классов) и семантическими отношениями на них (11 классов). Всего хотелось бы получить как минимум несколько сотен размеченных текстов.


Эскиз инструкции для разметчиков можно прочесть [здесь](https://github.com/dialogue-evaluation/RuREBus/blob/master/markup_instruction.docx)
 (мелкие детали могут уточняться). 

## Задачи:
Соревнование будет проводиться по трем задачам: 

1. Выделение именованных сущностей (named entity recognition, NER). Метрика оценивания - микро F-мера с точным совпадением спана сущности.

2. Извлечение семантических отношений между сущностями (relation extraction, RE). В данной задаче заранее сущности заданы в тексте и требуется установить отношения между ними. Метрика оценивания -- микро F-мера.

3. End-to-end извлечение семантических отношений. В данной задаче заранее сущности не заданы, требуется выделить сущности и отношения между ними. Метрика совпадает с п. 2.

## Данные:

Участникам будут выданы следующие файлы: 

(i) обучающая выборка, размеченная вручную сущностями и отношениями; 

(ii) большая неразмеченная коллекция текстов МЭР (что, опять же, приближает нас к бизнес-постановке, когда неразмеченные тексты зачастую есть в изобилии), 

(iii) тестовая выборка. Оценка качества автоматических моделей будет происходить на тестовой выборке.

 
Важно отметить, что оргкомитет принципиально не будет запрещать участникам самим размечать дополнительные тексты. Дорожка позиционируется как симуляция реальной рабочей задачи, и, если для улучшения решения задачи эффективнее потратить время на разметку текстов, а не на улучшение модели, размечать тексты – валидная стратегия. Если участники прибегнут к дополнительной разметке, они будут должны предупредить оргкомитет и прислать размеченные ими тексты.


Дополнительный смысл выдачи участникам большого корпуса неразмеченных текстов из одной и той же предметной области основан на следующем предположении: мы хотим позволить участникам дорожки самостоятельно предобучить языковые модели на неразмеченных данных. 
Мы хотим проверить гипотезу: верно ли, что такие языковые модели будут показывать лучшие результаты, по сравнению с моделями, предобученными на текстах из других предметных областей.

## Важные даты:
* 31 декабря 2019 - выдача примера размеченных данных
* 1 февраля 2020 - выдача обучающей выборки и всего неразмеченного корпуса
* 20 февраля 2020 - начало тестирования
* 29 февраля 2020 - финальная подача систем
* 5 марта 2020 - объявление официальных результатов
* 16 марта 2020 - дедлайн по статьям в сборник конференции Dialogue-2020

## Состав оргкомитета и контакты

Иван Смуров, Виталий Иванин, ABBYY: ivan.smurov@abbyy.com, vitalii.ivanin@abbyy.com

Елена Тутубалина, Казанский федеральный университет: tlenusik@gmail.com

Владимир Иванов, Иннополис: nomemm@gmail.com

Вероника Саркисян, Екатерина Артемова  / НУЛ ММВП, НИУ ВШЭ: impecopeco@gmail.com, Echernyak@hse.ru

Антон Емельянов, ПАО Сбербанк: login-const@mail.ru

Татьяна Батура, Новосибирский Государственный Университет: tatiana.v.batura@gmail.com


