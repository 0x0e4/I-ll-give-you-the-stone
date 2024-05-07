## Тема: 
AS-1: Разделить базу данных на несколько отдельных частей

## Статус:
Принято

## Контекст: 
В системе существует несколько видов пользователей, каждый из которых влияет на базу данных. Так, аналитик может просматривать как каталог товаров, так и данные клиентов. А менеджер по управлению каталогом может менять каталог и просматривать его. Менеджеру каталога не нужно иметь доступ к данным клиентов.

## Решение:
База данных будет разделена на несколько отдельных частей, к каждой из которых будет доступ у разных видов пользователей

## Последствия:

Плюсы:
- Безопасность. Из-за разделения прав доступа, снижается риск получения доступа к важным данным, наличие доступа к которым не нужно тем или иным видам пользователей БД.
- Целостность. Доступные только для просмотра данные невозможно специально или случайно отредактировать или удалить. Также, если чужие данные нельзя просмотреть, то их невозможно изменить в целях нанесения вреда.
- Снижение путаницы. Для работника проще видеть только необходимые таблицы и работать с ними, чем иметь доступ ко всем таблицам, из которых нужны только несколько.

Минусы:
- Усложнение администрирования. Настройка разных ролей доступа усложнит управление базой данных.
- Уменьшение гибкости. При изменении условий ведения бизнеса, из-за разделения базы на уровни доступа, уменьшается гибкость системы в целом.

---
## Тема: 
AS-2: Использовать сервисную (Service-based architecture) архитектуру как базовую в разработке и представлении

## Статус:
Принято

## Контекст: 
В ходе разработки архитектуры мы поняли, что делать её монолитной для достаточно типичной информационной системы дорого с точки зрения разработки и нелогично. В ходе рассмотрения вариантов архитектуры, мы пришли к выводу, что нам больше подходит service-based, модульная архитектура. Наше приложение завязано на использовании множества сервисов. Тем не менее, внедрение микросервисной архитектуры для нас проблематично - информационная система завязана на работу с определёнными модулями. Их замена возможна, но осуществляется нелегко. Поскольку SBA имеет меньшую степень декомпозиции, она нам подходит больше, чем иные варианты

## Решение:
В ходе обсуждений мы начали прорабатывать домены, на которые будет разделена система, в том числе и разделение базы данных на части, и то, у каких ролей будет доступ к какой из частей.

## Последствия:
Плюсы:
- Модульность. Такая архитектура позволяет создавать приложение на основе относительно независимых модулей, что упрощает разработку, тестирование и обслуживание
- Гибкость и масштабируемость. Модульная архитектура гибка в разработке и дальнейших стадиях создания и обслуживания. Добавление новых сервисов проще, чем изменение всего монолитного кода.
- Относительно крупные сервисы. Большие сервисы проще разрабатывать для нашей архитектуры и их взаимодействие проще организовать, в отличие от микросервисной архитектуры.

Минусы:
- Плохая тестируемость. Из-за большого количества сервисов, значительная часть которых не принадлежит нам, её сложнее тестировать.
- Не лучшая разворачиваемость. Создать и развернуть модульную систему сложнее, чем монолитную.
- Отказоустойчивость. Система на основе SBA-архитектуры менее отказоустойчива, чем микросервисная.

---

## Тема: 
AS-3: Зафиксировать, какие части нашей системы будут внешними модулями, а какие нет

## Статус:
Принято

## Контекст: 
Для продолжения разработки архитектуры необходимо уточнить, какие её части будут разрабатываться нами, а какие будут являться внешними модулями

## Решение:
Мы приняли, что наша система не занимается информационным обслуживанием доставки и хранения - эти занимается служба логистики. Задача нашей системы лишь получать информацию о доставке, которая подробнее расписана в диаграммах. Также наша система будет использовать внешнюю аналитику - сервис Яндекс Метрика

## Последствия:
Плюсы:
- Простота в подключении. Сторонний сервис достаточно интегрировать, его не нужно разрабатывать.
- Надёжность. Мы берём готовые решения у надёжных поставщиков ПО, таких как Яндекс.

Минусы:
- Невозможно изменять. Мы никак не можем изменить код сторонних сервисов.
- Сложность в тестировании. Мы видим лишь входы и выходы системы, и не видим её внутреннюю часть. Это усложняет тестирование.

---

## Тема: 
AS-4: Использовать WhatsApp Buisness или аналоги в качестве средства общения с клиентами для службы поддержки

## Статус:
Принято

## Контекст: 
При разработке архитектуры мы опираемся на идею о том, что нет необходимости создавать программные решения с нуля, когда они уже созданы. В бизнесе широко используются приложения для месседжеров, такие как WhatsApp Buisness, позволяющие общаться с клиентом с корпоративного аккаунта.

## Решение:
Мы приняли, что общение с клиентами должно происходить через корпоративные аккаунты в месседжерах типа WhatsApp или Telegram. Это удобно и понятно для клиентов.

## Последствия:
Плюсы:
- Простота в коммуникации. Клиентам проще коммуницировать через знакомые средства обмена информацией.
- Упрощение обучения операторов. Работников магазина проще обучить использованию усложнённой, но знакомой системы, чем полностью новой.

Минусы:
- Невозможность изменения кода. Выбор готовых решений накладывает все выше перечисленные издержки, в том числе и невозможность изменить код.

---

## Тема: 
AS-5: Уточнить методы разделения базы данных

## Статус:
Принято

## Контекст: 
В AS-1 недостаточно подробно описано, каким образом будет разделена база данных. Это архитектурное решение уточнит, каким образом это будет реализовано.

## Решение:
База данных будет фактически разделена лишь на две части - актуальную, и архивную, в которую будут заноситься данные о транзакциях, которые не будут нужны в работе магазина, но могут понадобиться для аналитики или налоговой отчётности в будущем. В актуальной и архивной базах будут применены разные технологии. Однако база данных будет разделена логически по уровням доступа различных пользователей. 

## Последствия:
Плюсы:
- Скорость создания. Создание двух баз быстрее, чем пяти и более, что предполагалось изначально.

Минусы:
- Меньшая безопасность. Защита данных у одной базы со множеством уровней доступа сложнее, чем множества разных баз с небольшим количеством уровней доступа.