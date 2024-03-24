# Камень я дам

## Функциональные требования 
Функциональные требования к системе:
Система – магазин по продаже камней, название «Камень я дам». Требования составлены на основе анализа заинтересованных сторон и бизнес-процессов. Общее требование – быть коммерчески выгодным магазином по продаже камней.  
Задача системы – автоматизировать следующие процессы:  
1. Покупка товара. С помощью онлайн-заказа, пользователь может совершать покупку товара. Технические требования к пользовательскому интерфейсу:  
Просмотр каталога товара  
Возможность просмотра всех свойств товара  
Возможность онлайн-оплаты покупок  
Просмотр корзины покупок  
Просмотр истории покупок  
Персонализированные рекомендации на основе предыдущих покупок и покупок пользователей с похожим поведением  
2. Приём и обработка заказов. Система должна взаимодействовать с логистической службой и отправлять ей всю необходимую для осуществления доставки информацию, такую как:  
Название товара  
Количество товара 
Точный адрес доставки – город и пункт выдачи  
Дополнительную информацию об условиях доставки товара  
3. Закупка товара. Система должна взаимодействовать с логистической службой, чтобы определять количество недостающего товара и автоматически закупать его. Логистическая служба должна отправлять информацию о количестве каждого вида товара на складе, на основе чего система в полуавтоматическом режиме с помощью интерфейса закупок и ответственного за закупки должна осуществлять запрос в логистическую службу на закупку товара.  
4. Доставка товара. Система должна взаимодействовать с ресурсами логистической службы: получать информацию о статусе доставки товара для того, чтобы сообщать её покупателю.  
5. Возврат товара: Если пользователя не устроил товар, то система должна обрабатывать его возврат - делать соответствующие записи в базы данных, сопровождать возврат средств; согласно описанию соответствующего бизнес-процесса.
6. Анализ статистики. Система должна предоставлять маркетологу доступ ко всей собранной информации о покупках для последующего анализа с целью внедрения эффективных стратегий для увеличения продаж.
## Метрики качества
За основу взят стандарт ISO/IEC 9126  
1. Эффективность:  
    - Загрузка каждой страницы сайта не должна превышать 3 секунды при 150 тысяч пользователях ежемесячно и около 500 заказах при нормальной конверсии в 0.3-0.4% от общего количества посетителей. В пиковые часы сайт должен обслуживать до 800 посетителей в рамках одного часа. В праздничные дни до 1600.    
2. Удобство:  
    - Интерфейс сайта не должен отталкивать покупателей – процент отказов не должен превышать 50%, а **среднее** время, проведённое на сайте, должно соответствовать таковому у конкурентов – 00:03:55.    
    - Время обучения пользованием внутреннего интерфейса системы для работников не должно превышать 2 часов.   
3. Функциональность:  
    - Система должна соответствовать выше изложенным функциональным требованиям и выполнять все эти операции. Все автоматизированные процессы представлены в пояснениях к диаграмме бизнес-процессов.    
    - Система должна быть интероперабельной для всех внешних систем, к которым она должна быть подключена. Внешние системы представлены в контекстной диаграмме.    
    - Безопасность – система должна соответствовать стандарту ISO/IEC 27001  
4. Ремонтопригодность:  
    - Система должна быть пригодна для обновления и изменения ПО по требованию заинтересованных сторон  
5. Переносимость:  
    - Система не должна быть привязана к специфичным технологиям хостинга, оплаты и разработки ПО, для того чтобы имелась возможность без особых усилий заменить как оборудование, на котором работает система, так и команду   поддержки ПО и оборудования.  


## Ссылка на макет
https://www.figma.com/file/fNnfCoxTaYQVdUub9OFBx2/Untitled?type=design&node-id=0%3A1&mode=design&t=L9bdKk4Me7nEnzDA-1

## Критика макета
https://docs.google.com/document/d/12VWFEz1BASJv5BKvC6Taj1sMLB4cnxp7r6hYHnpmu9g/edit?usp=sharing

## Ссылка на модели и диаграммы 
https://drive.google.com/file/d/1qti0p4eiksP_n_B6XOT3IIjgxSQeeDNo/view?usp=sharing_eip_se_dm&ts=65c63363 


## Бизнес процессы:
### Список обозначений: 
![symbols](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/blob/master/Reports/BuisnessProcess/Условные_обозначения.PNG)

### Процессы:
![bpsecond](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/blob/master/Reports/BuisnessProcess/Возврат_товара.PNG)
![bpthird](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/blob/master/Reports/BuisnessProcess/Доставка_товара.PNG)
![bpfourth](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/blob/master/Reports/BuisnessProcess/Закупка_товара.PNG)
![bpfifth](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/blob/master/Reports/BuisnessProcess/Инвентаризация.PNG)
![bpsixth](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/blob/master/Reports/BuisnessProcess/Онлайн_заказ_товара.PNG)
![bpseventh](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/blob/master/Reports/BuisnessProcess/Оплата_товара.PNG)
![bpeightth](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/blob/master/Reports/BuisnessProcess/Получение_и_хранения_товара.PNG)
![bpninth](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/blob/master/Reports/BuisnessProcess/Прием_и_обработка_заказа.PNG)


## Контекстная диаграмма
Под системой подразумевается совокупность взаимодействий между пользователями и элементами сайта. 
С кем взаимодействует система? 
1.1. Пользователи-покупатели
Взаимодействие происходит через web-сайт или его мобильную версию. Данное взаимодействие является двухсторонним. Покупатель предоставляет нашей системе личные данные (ФИО, дата рождения, номер телефона),  адреса для доставки товара, данные для оплаты товара. Система же предоставляет пользователю список товаров, условия доставки товара, состояние заказа (в обработке, собран на складе, упакован, передан в доставку, доставлен на пункт выдачи, получен).
1.2. Пользователи-читатели
Взаимодействие происходит через web-сайт или его мобильную версию. Данное взаимодействие является односторонним. Система предоставляет читателям статьи о камнях, ссылки на эзотерические материалы и прочее. 
1.3. Службы доставки (СДЭК) 
Взаимодействие происходит при помощи API-интеграции. Данное взаимодействие является двусторонним. Система передает в службу доставки адреса для доставки, адреса для получения товара (склад), вес товара. Службы доставки предоставляют системе состояние заказа, сроки доставки 
1.4. Поставщики товаров 
Взаимодействие происходит при помощи специализированных платформ для электронной торговли (В2С). Поставщики предоставляют системе список товаров, стоимость и количество товаров, условия поставки, место получения товара. Система же предоставляет дату отгрузки товара (дату, когда мы хотим забрать товар). 
1.5. Службы логистики
Взаимодействие происходит при помощи API-интеграции. Данное взаимодействие является двусторонним. Службы логистики предоставляют стоимость перевозки и сроки. Система передает в службу логистики дату и время получения товара от поставщика, адрес получения и адрес доставки (склад).
1.6. Служба бухгалтерии 
Взаимодействие происходит при помощи специализированного ПО. Данное взаимодействие является двусторонним. Службы бухгалтерии предоставляют финансовые отчеты. Система предоставляет список проданных товаров, отчет о расходах и доходах.
1.7. Платежная система?
Взаимодействует ли платежная система с нашей системой? 


Автоматизированные процессы
2.1. Процесс создания заказа 
2.2. Процесс приема и обработки заказа
2.3. Процесс возврата товара 
2.4. Процесс оплаты товара
2.5. Процесс закупки товара 
2.6. Процесс доставки товара

![bpkd](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/blob/master/Reports/BuisnessProcess/Контекстная_диаграмма.PNG)


## Диаграмма классов 
В рамках нашей системы центральной сущностью является ЗАКАЗ, у которого есть следующие атрибуты: уникальный номер заказа, вес данного заказа, количество товаров в данном заказе, дата заказа, стоимость заказа и статус заказа. Каждый ЗАКАЗ может содержать один и более ТОВАРОВ, атрибуты ТОВАРА: название камня, все камня, цена камня, описание камня, место хранения . Каждый ЗАКАЗ имеет только одного ПОКУПАТЕЛЯ, но при этом один ПОКУПАТЕЛЬ может иметь несколько ЗАКАЗОВ. ПОКУПАТЕЛЬ имеет следующие атрибуты: ФИО, номер телефона, адреса для доставки, электронная почты и дата рождения (для статистики). Каждый ПОКУПАТЕЛЬ может совершать одну или больше ТРАНЗАКЦИЙ, которые имеют следующие атрибуты: номер транзакции, сумма оплаты и дата платежа. Кроме того существует сущность ПОСТАВЩИК с атрибутами: название компании, ИНН, номер расчетного счета для оплаты товаров. ПОСТАВЩИК выполняет ЗАКАЗЫ НА ПОСТАВКУ, которые включают в себя перечень товаров в заказе, стоимость заказа, дату заказа. ЗАКАЗ НА ПОСТАВКУ может иметь только одного ПОСТАВЩИКА и при этом имеет связь 1 ко многим с ТОВАРОМ. Также существует сущность СКЛАД, которая имеет связь с ТОВАРОМ. Атрибуты СКЛАДА: название, адрес, вместимость, загруженность. Кроме этого существует сущность СЛУЖБА ДОСТАВКИ с атрибутами …. СЛУЖБА ДОСТАВКИ имеет связь с ЗАКАЗОМ. Один ЗАКАЗ может выполнять только одна СЛУЖБА ДОСТАВКИ.
![bpDK](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/blob/master/Reports/BuisnessProcess/ДК.PNG)


## Заинтересованные лица

![Screenshot_65](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/assets/155570357/7cdc6d48-57cd-477a-8847-788ddde42700)


![O_r8VkRCJss](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/assets/113982481/791287d8-2a9c-4351-bd49-0c1608482a40)
![1-z0V5HT1I8](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/assets/113982481/aefc298f-b4b7-49e2-bdbe-4bb54896087c)
![9ONZY9KavR0](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/assets/113982481/5e09692b-a87b-4e37-bae5-f9bce663d91c)
![qhf5fl0IJgk](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/assets/113982481/1bf5386a-d6c0-4613-8d05-eda5b008ca54)

## Обеспечение безопасности
![InfoBez](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/assets/117998993/ea378251-a219-4542-9afe-fc095c38072e)

