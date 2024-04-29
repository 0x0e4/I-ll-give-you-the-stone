# Камень я дам

- [О проекте](#о-проекте)
    - [Цели создания](#цели-создания-продукта)
    - [Наша команда](#наша-команда)
- [Требования](#требования)
    - [Функциональные требования](#функциональные-требования)
    - [Метрики качества](#метрики-качества)
- [Архитектура](#архитектура)
    - [Архитектурные решения→](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/tree/master/Reports/architecturalSolutions.md)
    - [Заинтересованные стороны](#заинтересованные-стороны)
    - [Модели и диаграммы](#ссылка-на-модели-и-диаграммы)
    - [Бизнес-процессы](#бизнес-процессы)
    - [Контекстная диаграмма](#контекстная-диаграмма)
    - [Диаграмма классов](#диаграмма-классов)
    - [Диаграмма данных](#диаграмма-данных)
    - [Обеспечение безопасности→](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/blob/master/Reports/SoftwareSolutions/information_security.md)
- [Имплементация архитектуры](#имплементация-архитектуры)
    - [Макет сайта](#ссылка-на-макет-сайта)
    - [Фронтенд→](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/tree/master/Code/Frontend)
    - [Бэкенд→](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/tree/master/Code/Backend)
- [Дополнительно](#дополнительно)
    - [Собранная информация→](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/tree/master/Reports/InformationCollected)
    - [Презентации→](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/tree/master/Reports/Presentations)
    - [Программные решения→](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/tree/master/Reports/SoftwareSolutions)
    - [Стадии создания→](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/tree/master/Reports/CreationStages)

# О проекте

## Цели создания продукта

Цель создания нашего продукта - это создание эффективного рентабельного магазина по продаже камней.

## Наша команда

| Участник            | Роль               |
|---------------------|---------------------|
| [Алёна Данилова](https://github.com/AlyonaUi) | Системный архитектор 
| [Анастасия Аксёнова](https://github.com/lisl1ll) | Системный архитектор |
| [Валерия Чухлова](https://github.com/VHarndy) | Frontend-разработчик |
| [Елизавета Бакнина](https://github.com/fuyom) | Системный архитектор |
| [Елизавета Смирнова](https://github.com/Smrll) | Дизайнер |
| [Игорь Самойлов](https://github.com/7YearsOldTalent) | Frontend-разработчик |
| [Кирилл Боков](https://github.com/Kirill-Bokov) | Менеджер продукта |
| [Максим Румянцев](https://github.com/Roleng37) | Специалист по сбору информации |
| [Мария Иванова](https://github.com/Mary2811) | Системный архитектор |
| [Михаил Ермолаев](https://github.com/0x0e4) | Backend-разработчик |

# Системные требования

## Заинтересованные стороны

* Клиенты
  - Клиенты хотят, чтобы система быстро реагировала и была доступна в любое время, а также, чтобы пользовательский интерфейс был понятным и удобным.
  - Клиенты хотят, чтобы их персональные данные были в безопасности.
  - Клиенты хотят иметь связь со службой поддержки.

* Отдел по работе с клиентами
  - В некоторых случаях службе поддержки необходим доступ к данным профиля пользователя.

* Менеджер (управление каталогом)
  - Менеджеру необходимо постоянно следить за изменениями в каталоге и базе данных товаров, чтобы предоставлять пользователям магазина актуальную информацию на сайте и оперативно отправлять запросы на закупку товаров.

* IT-отдел
  - IT-отделу нужно подерживать работу всей системы, внедрять изменения и расширять систему (при необходимости).

* Отдел аналитики
  - Занимается анализом поведения пользователей и анализом работы различных частей системы.
  - Создаёт отчёты на основе собранной информации и передаёт руководству.

* Служба логистики
  - Внешняя система, занимающаяся закупкой и доставкой товаров.
  - получает и предоставляет информацию о товарах, статусе и адресе доставки.
  - получает и предоставляет информацию о закупаемых товарах.

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
5. Поддержка пользователей и возврат товара: Отдел по работе с клиентами должен обеспечивать поддержку пользователей. При возникновении у пользователей каких-либо вопросов, связанных с функционалом сайта, ценами, каталогом или свойствами товаров, представитель службы поддержки должен ответить на подобные вопросы.Если пользователя не устроил товар, то система должна обрабатывать его возврат - делать соответствующие записи в базы данных, сопровождать возврат средств; согласно описанию соответствующего бизнес-процесса.  
6. Анализ статистики. Система должна предоставлять маркетологу доступ ко всей собранной информации о покупках для последующего анализа с целью внедрения эффективных стратегий для увеличения продаж. Система должна иметь в базе данных все данные о товарах - их количество, период продажи товаров, количество купленных товаров, их цены. Также в система должна иметь возможность анализировать поведение пользователей с помощью сервиса "Яндекс Метрика" или аналогов.  

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
    - Безопасность – система должна соответствовать стандарту ISO/IEC 27001. Система должна предоставлять информацию, сигнализирующую о том, насколько нормально в ней протекают информационные процессы.  
4. Ремонтопригодность:  
    - Система должна быть пригодна для обновления и изменения ПО по требованию заинтересованных сторон  
5. Переносимость:  
    - Система не должна быть привязана к специфичным технологиям хостинга, оплаты и разработки ПО, для того чтобы имелась возможность без особых усилий заменить как оборудование, на котором работает система, так и команду   поддержки ПО и оборудования.  

# Архитектура

![dx_eaL_1NT0](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/assets/113982481/4ab54ea5-610f-4f24-bd2d-b1c4afde5429)


## Ссылка на модели и диаграммы 

https://drive.google.com/file/d/1qti0p4eiksP_n_B6XOT3IIjgxSQeeDNo/view?usp=sharing_eip_se_dm&ts=65c63363

## Бизнес-процессы

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
![bpten](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/blob/master/Reports/BuisnessProcess/Анализ_статистики.png)


## Контекстная диаграмма

Под системой подразумевается совокупность взаимодействий между пользователями и элементами сайта. 
С кем взаимодействует система? 
1. Пользователи-покупатели
Взаимодействие происходит через web-сайт или его мобильную версию. Данное взаимодействие является двухсторонним. Покупатель предоставляет нашей системе личные данные (ФИО, дата рождения, номер телефона),  адреса для доставки товара, данные для оплаты товара. Система же предоставляет пользователю список товаров, условия доставки товара, состояние заказа (в обработке, собран на складе, упакован, передан в доставку, доставлен на пункт выдачи, получен).
2. Пользователи-читатели
Взаимодействие происходит через web-сайт или его мобильную версию. Данное взаимодействие является односторонним. Система предоставляет читателям статьи о камнях, ссылки на эзотерические материалы и прочее. 
3.  Службы доставки (СДЭК) 
Взаимодействие происходит при помощи API-интеграции. Данное взаимодействие является двусторонним. Система передает в службу доставки адреса для доставки, адреса для получения товара (склад), вес товара. Службы доставки предоставляют системе состояние заказа, сроки доставки 
4. Поставщики товаров 
Взаимодействие происходит при помощи специализированных платформ для электронной торговли (В2С). Поставщики предоставляют системе список товаров, стоимость и количество товаров, условия поставки, место получения товара. Система же предоставляет дату отгрузки товара (дату, когда мы хотим забрать товар). 
5. Службы логистики
Взаимодействие происходит при помощи API-интеграции. Данное взаимодействие является двусторонним. Службы логистики предоставляют стоимость перевозки и сроки. Система передает в службу логистики дату и время получения товара от поставщика, адрес получения и адрес доставки (склад).
6. Служба бухгалтерии 
Взаимодействие происходит при помощи специализированного ПО. Данное взаимодействие является двусторонним. Службы бухгалтерии предоставляют финансовые отчеты. Система предоставляет список проданных товаров, отчет о расходах и доходах.
7. Платежная система?
Взаимодействует ли платежная система с нашей системой? 


Автоматизированные процессы
1. Процесс создания заказа 
2. Процесс приема и обработки заказа
3. Процесс возврата товара 
4. Процесс оплаты товара
5. Процесс закупки товара 
6. Процесс доставки товара

![bpkd](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/blob/master/Reports/BuisnessProcess/Контекстнаядиаграмма.png)

## Диаграмма классов

В рамках нашей системы центральной сущностью является ЗАКАЗ, у которого есть следующие атрибуты: уникальный номер заказа, вес данного заказа, количество товаров в данном заказе, дата заказа, стоимость заказа и статус заказа. Каждый ЗАКАЗ может содержать один и более ТОВАРОВ, атрибуты ТОВАРА: название камня, все камня, цена камня, описание камня, место хранения . Каждый ЗАКАЗ имеет только одного ПОКУПАТЕЛЯ, но при этом один ПОКУПАТЕЛЬ может иметь несколько ЗАКАЗОВ. ПОКУПАТЕЛЬ имеет следующие атрибуты: ФИО, номер телефона, адреса для доставки, электронная почты и дата рождения (для статистики). Каждый ПОКУПАТЕЛЬ может совершать одну или больше ТРАНЗАКЦИЙ, которые имеют следующие атрибуты: номер транзакции, сумма оплаты и дата платежа. Кроме того существует сущность ПОСТАВЩИК с атрибутами: название компании, ИНН, номер расчетного счета для оплаты товаров. ПОСТАВЩИК выполняет ЗАКАЗЫ НА ПОСТАВКУ, которые включают в себя перечень товаров в заказе, стоимость заказа, дату заказа. ЗАКАЗ НА ПОСТАВКУ может иметь только одного ПОСТАВЩИКА и при этом имеет связь 1 ко многим с ТОВАРОМ. Также существует сущность СКЛАД, которая имеет связь с ТОВАРОМ. Атрибуты СКЛАДА: название, адрес, вместимость, загруженность. Кроме этого существует сущность СЛУЖБА ДОСТАВКИ с атрибутами …. СЛУЖБА ДОСТАВКИ имеет связь с ЗАКАЗОМ. Один ЗАКАЗ может выполнять только одна СЛУЖБА ДОСТАВКИ.  
![bpDK](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/blob/master/Reports/BuisnessProcess/ДК2.PNG)

##  Диаграмма данных

![bpDd](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/blob/master/Reports/BuisnessProcess/модель_данных.png)


## Диаграммы последовательности 
### Описание варианта использования "Онлайн заказ товара"
Данная диаграмма состоит из следующих элементов: 
1. Actor Покупатель, т.е. пользователь, который совершает покупку на нашем сайте
2. Control Lifeline Manager, который подразумевает нашу систему
3. Control Lifeline PayManager - платежная система
4. Boundary Lifeline StartPage - главная страница нашего сайта (стартовая) 
5. Boundary Lifeline CataloguePage - страница с каталогом товаров 
6. Boundary Lifeline GoodPage - страница с фотографией товара и его описанием (т.е. карточка товара)
7. Boundary Lifeline BasketPage - страница с корзиной (список товаров, которые покупатель хочет заказать)
8. Boundary Lifeline BookingPage - страница, на которой оформляется заказ (пустая форма для заполнения) 
9. Boundary Lifeline PayPage - страница для оплаты, предоставляемая платежной системой 
10. Boundary Lifeline TrackingPage - страница отслеживания оформленного заказа
11. Entity Lifeline Заказ - база данных с заказами

Покупатель заходит в нашу систему и попадает на стартовую страницу, с которой он может перейти на страницу, которая содержит каталог товаров. На этой странице покупатель может просматривать наши товары и перейти на страницу товара. На странице товара содержится фото товара и его описание, также на этой странице содержится кнопка “добавить в корзину”, покупатель может добавить понравившийся товар в корзину и затем перейти на страницу корзины. На этой странице содержится список товаров, которые покупатель ранее добавил, а также кнопка “оформить заказ”, при нажатии этой кнопки покупатель переходит на страницу оформления заказа, на которой содержится форма для заполнения, после того как Покупатель заполнит все поля, станет доступна кнопка “Оплатить”, при нажатии этой кнопки наша система запросит страницу для оплаты у платежной системы, а затем передаст Покупателю. После оплаты покупателю станет доступна страница с отслеживанием.

Ссылка на диаграмму: https://online.visual-paradigm.com/app/diagrams/#G1QVv8nUBHLZKPZcRdIOoKzrUDxmRWk5jy

https://drive.google.com/file/d/1QVv8nUBHLZKPZcRdIOoKzrUDxmRWk5jy/view?usp=drive_link



## Обеспечение безопасности

[Представлено в Reports/SoftwareSolutions](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/blob/master/Reports/SoftwareSolutions/information_security.md)

# Имплементация архитектуры

## Ссылка на макет сайта

https://www.figma.com/file/fNnfCoxTaYQVdUub9OFBx2/Untitled?type=design&node-id=0%3A1&mode=design&t=L9bdKk4Me7nEnzDA-1

### Критика макета

https://docs.google.com/document/d/12VWFEz1BASJv5BKvC6Taj1sMLB4cnxp7r6hYHnpmu9g/edit?usp=sharing

## Фронтенд

[Представлено в Code/Frontend](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/tree/master/Code/Frontend)

## Бэкенд

[Представлено в Code/Backend](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/tree/master/Code/Backend)

# Дополнительно

## Собранная информация

[Представлено в Reports/InformationCollected](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/tree/master/Reports/InformationCollected)

## Презентации

[Представлено в Reports/Presentations](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/tree/master/Reports/Presentations)

## Программные решения

[Представлено в Reports/Presentations](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/tree/master/Reports/SoftwareSolutions)

## Стадии создания

[Представлено в Reports/CreationStages](https://github.com/Kirill-Bokov/I-ll-give-you-the-stone/tree/master/Reports/SoftwareSolutions)
