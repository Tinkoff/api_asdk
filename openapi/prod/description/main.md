# История изменений
| Версия | Описание |  Дата |
| ------ | -------- | ----- |
| 1.42 | Изменили обязательность параметра rebill_id в методе GetCardList | 30.08.2022 |

# Термины и сокращения
| **Термин** | Определение |
| ------ | -------- |
| **Продавец** | Участник, принимающий и осуществляющий переводы по банковским картам на своем сайте |
| **Покупатель** | Стандарт безопасности данных индустрии платёжных карт. Стандарт представляет собой совокупность 12 детализированных требований  по обеспечению безопасности данных о держателях платёжных карт. Данные передаются, хранятся и обрабатываются в информационных инфраструктурах организаций. Принятие соответствующих мер пообеспечению соответствия требованиям стандарта подразумевает комплексный подход к обеспечению информационной безопасности данных платёжных карт |
| **PCI DSS** | Протокол, который используется как дополнительный уровень безопасности для онлайн-кредитных и дебетовых карт. 3-D Secure добавляет ещё один шаг аутентификации для онлайн-платежей |
| **3-DSecure** | Протокол, который используется как дополнительный уровень безопасности для онлайн-кредитных и дебетовых карт. 3-D Secure добавляет ещё один шаг аутентификации для онлайн-платежей |
| **Терминал** | Точка приема платежей продавца (в общем случае привязывается к сайту, на котором осуществляется прием платежей) Далее в этой документации описан протокол для терминала мерчанта |
| **ККМ** | Контрольно-кассовая машина|

# Коды ошибок
| CODE | MESSAGE | DETAILS (опционально) |
|---|---|---|
| 0 | None |  |
| 1 | Параметры не сопоставлены |  |
| 2 | Отсутствуют обязательные параметры. |  |
| 3 | Внутренняя ошибка системы интернет эквайринга. |  |
| 4 | Запрашиваемое состояние транзакции является неверным. |  |
| 5 | Неверный запрос. |  |
| 6 | Неверный статус карты. |  |
| 7 | Неверный статус покупателя. |  |
| 8 | Неверный статус транзакции. |  |
| 9 | Переадресовываемый url пуст. |  |
| 10 | Метод Charge заблокирован для данного терминала. |  |
| 11 | Невозможно выполнить платеж |  |
| 12 | Неверный параметр RedirectDueDate |  |
| 13 | Оплата с мобильного телефона недоступна |  |
| 13 | Оплата через WebMoney недоступна |  |
| 14 | Платеж неверный. |  |
| 15 | Не удалось осуществить платеж через EINV. |  |
| 16 | Счет был отклонен. |  |
| 17 | Неверные введенные данные. |  |
| 18 | Не удалось осуществить платеж через MC. |  |
| 19 | Не удалось осуществить платеж через WebMoney. |  |
| 20 | Ошибка повторного идентификатора заказа. |  |
| 21 | Внутренняя ошибка вызова сервиса ACQAPI. |  |
| 27 | Кассовая ссылка на текущий момент недоступна для повторной активации |  |
| 50 | Ошибка отправки нотификации. |  |
| 51 | Ошибка отправки Email. |  |
| 52 | Ошибка отправки Sms. |  |
| 54 | Повторное прохождение 3DS авторизации не допустимо. |  |
| 55 | Повторите попытку позже | Не найдено оплаченных назначений платежа |
| 60 | Запрещено получение документов по url для текущего терминала | Запрещено получение документов по url для текущего терминала |
| 61 | Должен быть заполнен один из параметров: emailList или Url | Должен быть заполнен один из параметров: emailList или Url |
| 62 | Запрещено получение документов по url для текущего systemId | Запрещено получение документов по url для текущего systemId |
| 63 | Не найдена операция | Не найдена операция |
| 64 | Невалидные данные в запросе | Невалидные данные в запросе |
| 65 | Не удалось сформировать документ. Обратитесь в службу поддержки | Не удалось сформировать документ. Повторите операцию позднее |
| 66 | Не удалось сформировать документ. Повторите операцию позднее | Запрещено получение документов по url для текущего терминала |
| 67 | Не удалось сформировать документ. Повторите операцию позднее | Не удалось сформировать документ. Повторите операцию позднее |
| 68 | Не удалось сформировать документ. Обратитесь в службу поддержки | Стороний сервис не доступен. |
| 76 | Операция по иностранной карте недоступна. | Операция по иностранной карте недоступна. Воспользуйтесь картой российского банка |
| 77 | Оплата иностранной картой недоступна. | Оплата по иностранной карте недоступна. Воспользуйтесь картой российского банка |
| 78 | Выплата на иностранную карту недоступна. | Выплата на иностранную карту недоступна. Воспользуйтесь картой российского банка |
| 79 | Возврат на иностранную карту недоступен. | Возврат на иностранную карту недоступен. Обратитесь в поддержку |
| 96 | Ошибка Iris. |  |
| 97 | Ошибка Jasper. |  |
| 98 | Ошибка SubExt. |  |
| 99 | Попробуйте повторить попытку позже | Банк, выпустивший карту, отклонил операцию |
| 100 | Повторите попытку позже | Ошибка в реквизитах карты |
| 101 | Не пройдена идентификация 3DS. | Ошибка прохождения 3-D Secure |
| 102 | Попробуйте повторить попытку позже | Заказ не может быть оплачен, обратитесь службу поддержки |
| 102 | Операция отклонена, пожалуйста обратитесь в интернет-магазин или воспользуйтесь другой картой. | Заказ не может быть оплачен, обратитесь службу поддержки |
| 102 | Превышен лимит на сумму выплат в месяц. |  |
| 102 | Отказ. Более двух успешных оплат с одного email в неделю по проекту dolyame.ru |  |
| 102 | Отказ. Более двух успешных оплат с одного phone в неделю по проекту dolyame.ru. |  |
| 102 | Отказ. Более двух успешных оплат с одной карты в неделю по проекту dolyame.ru. |  |
| 102 | Отказ. Более двух успешных оплат с одной карты в сутки по проекту dolyame.ru. |  |
| 102 | Отказ. Более двух успешных оплат с одного устройства в сутки по проекту dolyame.ru. |  |
| 102 | Отказ. Более двух успешных оплат с одного устройства в неделю по проекту dolyame.ru. |  |
| 102 | Отказ. Более двух успешных оплат с одного куки/идентификатора клиентского агента в сутки по проекту dolyame.ru. |  |
| 102 | Отказ. Более двух успешных оплат с одного куки/идентификатора клиентского агента в неделю по проекту dolyame.ru. |  |
| 102 | Отказ. Попытка оплаты с виртуальных или мошеннических бинов по проекту dolyame.ru. |  |
| 103 | Недостаточно средств на счете |  |
| 104 | Ошибка выполения рекуррента |  |
| 105 | По картам Maestro невозможно провести рекуррентный платёж. |  |
| 106 | Карта не поддерживает 3DS проверку. Попробуйте другую карту. |  |
| 107 | Неверно введен CardId. Проверьте, что такая карта была ранее привязана. |  |
| 108 | Оплата разрешена только по 3DS картам. Попробуйте другую карту. |  |
| 109 | Не найден dsTranId для сессии |  |
| 110 | Не передан cres |  |
| 111 | Передан некорректный cres |  |
| 116 | Недостаточно средств на карте. |  |
| 119 | Превышено допустимое количество запросов авторизации операции |  |
| 120 | Попробуйте повторить попытку позже |  |
| 123 | Попробуйте повторить попытку позже |  |
| 125 | Попробуйте повторить попытку позже |  |
| 191 | Некорректный статус договора, обратитесь к вашему менеджеру |  |
| 201 | Поле PaymentId не должно быть пустым. |  |
| 201 | Поле paymentMethod не должно быть пустым. |  |
| 201 | Поле paymentObject не должно быть пустым. |  |
| 201 | Поле measurementUnit не должно быть пустым. |  |
| 202 | Терминал заблокирован. |  |
| 203 | Параметры запроса не должны быть пустыми. |  |
| 204 | Неверный токен. Проверьте пару TerminalKey/SecretKey. |  |
| 205 | Неверный токен. Проверьте пару TerminalKey/SecretKey. | Указанный терминал не найден |
| 206 | Email не может быть пустым. |  |
| 207 | Параметр DATA превышает максимально допустимый размер. |  |
| 208 | Наименование ключа из параметра DATA превышает максимально допустимый размер. |  |
| 209 | Значение ключа из параметра DATA превышает максимально допустимый размер. |  |
| 210 | Размер поля TerminalKey должен быть от {min} до {max}. |  |
| 211 | Неверный формат IP. |  |
| 212 | Размер поля OrderId должен быть от {min} до {max}. |  |
| 213 | Размер поля Description должен быть от {min} до {max}. |  |
| 214 | Поле Currency должно быть меньше или равно {value}. |  |
| 215 | Размер поля PayForm должен быть от {min} до {max}. |  |
| 216 | Размер поля CustomerKey должен быть от {min} до {max}. |  |
| 217 | Поле PaymentId числовое значение должно укладываться в формат (<{integer} цифр>.<{fraction} цифр>). |  |
| 218 | Значение PAN не является числовым. |  |
| 219 | Неверный срок действия карты. |  |
| 220 | Размер поля CardHolder должен быть от {min} до {max}. |  |
| 221 | Значение CVV не является числовым. |  |
| 222 | Поле CardId числовое значение должно укладываться в формат (<{integer} цифр>.<{fraction} цифр>). |  |
| 223 | Поле RebillId числовое значение должно укладываться в формат (<{integer} цифр>.<{fraction} цифр>). |  |
| 224 | Неверный формат Email. |  |
| 225 | Неверный формат Email. |  |
| 226 | Размер поля Email должен быть от {min} до {max}. |  |
| 227 | Размер поля Phone должен быть от {min} до {max}. |  |
| 228 | Размер поля MD должен быть от {min} до {max}. |  |
| 229 | Размер поля PaRes должен быть от {min} до {max}. |  |
| 230 | Размер поля Code должен быть от {min} до {max}. |  |
| 231 | Не найден идентификатор карты. |  |
| 233 | Размер поля CardId должен быть от {min} до {max}. |  |
| 234 | Размер поля PAN должен быть от {min} до {max}. |  |
| 235 | Размер поля RebillId должен быть от {min} до {max}. |  |
| 236 | Размер поля Token должен быть от {min} до {max}. |  |
| 237 | Размер поля PaymentId должен быть от {min} до {max}. |  |
| 238 | Размер поля ExpDate должен быть от {min} до {max}. |  |
| 239 | Размер поля CVV должен быть от {min} до {max}. |  |
| 240 | Поле Amount числовое значение должно укладываться в формат (<{integer} цифр>.<{fraction} цифр>). |  |
| 241 | Поле Currency должно быть больше или равно {value}. |  |
| 242 | Размер поля InfoEmail должен быть от {min} до {max}. |  |
| 243 | Ошибка шифрования карточных данных. |  |
| 244 | Ошибка сопоставления карточных данных. |  |
| 245 | Параметр AddCard не сопоставлен. |  |
| 246 | Параметр SendEmail не сопоставлен. |  |
| 247 | Параметр Amount не сопоставлен. |  |
| 248 | Параметр CVV не сопоставлен. |  |
| 249 | Параметр Currency не сопоставлен. |  |
| 250 | Параметр DATA не сопоставлен. |  |
| 251 | Неверная сумма. Сумма должна быть больше или равна {value} копеек. |  |
| 252 | Срок действия карты истек. |  |
| 253 | Валюта {value} не разрешена для данного терминала |  |
| 254 | Дополнительные возможности отключены |  |
| 255 | Платеж не найден |  |
| 256 | Указан некорректный тип безопасной сделки | Указан некорректный тип безопасной сделки |
| 257 | Некорректное значение признака последней выплаты. Используйте значения true или false | Некорректное значение признака последней выплаты. Используйте значения true или false |
| 258 | Неверный параметр Ean13. |  |
| 259 | Параметр EncryptedPaymentData не сопоставлен |  |
| 260 | Максимальная длина номера телефона 30 символов |  |
| 261 | Параметр Source не сопоставлен |  |
| 262 | Истек срок действия родительского платежа |  |
| 300 | Ошибка регистрации чека в АТОЛ. |  |
| 301 | Ошибка получения статуса чека из АТОЛ. |  |
| 302 | Ошибка получения токена из АТОЛ. |  |
| 303 | Неверные логин или пароль. |  |
| 304 | Неверный код группы. |  |
| 305 | Ошибка проверки поля. |  |
| 306 | Ошибка связи АТОЛ. |  |
| 307 | Ошибка ответа АТОЛ. |  |
| 308 | Сумма всех позиций в чеке должна равняться сумме всех видов оплаты |  |
| 309 | Поле Receipt не должно быть пустым. |  |
| 310 | Дробная часть параметра Quantity не должна быть более {value} знаков |  |
| 310 | Целая часть параметра Quantity не должна быть более {value} знаков |  |
| 311 | Ошибка регистрации чека в Receipt Service. |  |
| 312 | Ошибка получения чека из Receipt Service. |  |
| 313 | Ошибка создания организации в Receipt Service. |  |
| 314 | Ошибка создания кассы в Receipt Service. |  |
| 315 | Касса не найдена. |  |
| 316 | Максимальная длина номера телефона 19 символов. |  |
| 317 | Неверное значение поля agentSign. |  |
| 318 | Поле AgentSign не должно быть пустым. |  |
| 319 | Поле SupplierInfo не должно быть пустым. |  |
| 320 | Поле Inn в объекте SupplierInfo не должно быть пустым. |  |
| 321 | Поле Receipts не должно быть пустым. |  |
| 322 | Передана некорректная подпись |  |
| 323 | Amount не совпадают |  |
| 324 | Указанный тип отмены не может быть выполнен по операции |  |
| 325 | Транзакция не найдена. |  |
| 326 | Неверный amount. |  |
| 327 | "Терминал не поддерживает C2C переводы или не передан Route=""C2C"" для C2C терминала" |  |
| 328 | Должны присутствовать данные для списания и данные для пополнения. |  |
| 329 | Email или Phone обязательны при передаче чека |  |
| 330 | Сумма в запросе больше чем в оригинальной транзакции |  |
| 331 | Неверный терминал |  |
| 332 | Поле Fee в объекте Shops должно быть больше или равно 0 |  |
| 333 | Поле Amount в объекте Shops должно быть больше или равно 1 |  |
| 334 | Суммы в чеке и в платеже не совпадают. |  |
| 335 | OrderId {value} не найден для TerminalKey {value} |  |
| 381 | Возможна привязка только резидентных карт |  |
| 382 | Возможна привязка только нерезидентных карт |  |
| 383 | Поле markProcessingMode должно быть заполнено для маркированных товаров |  |
| 383 | Поле markCode должно быть заполнено для маркированных товаров |  |
| 383 | Поле sectoralItemProps должно быть заполнено для маркированных товаров |  |
| 383 | Поле markQuantity должно быть заполнено для маркированных товаров |  |
| 383 | Поле {value} для маркированных товаров должно принимать значение: {value} |  |
| 383 | markCode.value имеет некорректное значение |  |
| 383 | numerator и denominator должны быть больше 0 |  |
| 383 | numerator должен быть строго меньше denominator |  |
| 383 | Для версии кассы ФФД 1.2 объекты AgentData и SupplierInfo должны быть переданы в Items |  |
| 384 | Для C2C запрещено проводить рекуррент по данной ПС | Для C2C запрещено проводить рекуррент по данной ПС |
| 385 | Поле markQuantity передается только для маркированных товаров |  |
| 385 | Поле markProcessingMode передается только для маркированных товаров |  |
| 401 | Внутренняя ошибка системы. |  |
| 402 | Повторите попытку позже. |  |
| 403 | Превышен лимит на количество пополнений в месяц. |  |
| 404 | Превышен лимит на сумму пополнения через бесконтактные сервисы. |  |
| 405 | Превышен лимит на сумму пополнения по виртуальной карте. |  |
| 406 | Превышен лимит на сумму пополнения в месяц через мобильное приложение. |  |
| 407 | Не найдено |  |
| 410 | Данный тип перевода для терминала не доступен |  |
| 411 | Сертификат не найден |  |
| 412 | Истек срок действия сертификата |  |
| 413 | Сертификат заблокирован |  |
| 414 | Сертификат уже сохранен для данного терминала |  |
| 415 | Дата начала срока действия сертификата еще не наступила |  |
| 416 | Некорректное значение параметра SetStatus |  |
| 417 | Ошибка обработки сертификата |  |
| 419 | Параметр account объекта DATA должен быть заполнен корректно для MCC: 6050/6051 |  |
| 500 | Добавление карты к данному терминалу запрещено. |  |
| 501 | Терминал не найден. |  |
| 502 | Карта по requestKey не найдена. |  |
| 503 | CustomerKey не найден. |  |
| 504 | Не удалось провести платеж при привязке карты. |  |
| 505 | Не удалось привязать карту. Внутренняя ошибка. |  |
| 506 | Карта добавлена в черный список. |  |
| 507 | Карта не поддерживает 3DS проверку. Попробуйте другую карту. |  |
| 508 | Неверный номер карты. |  |
| 509 | Не удалось выполнить отмену при привязке карты. |  |
| 510 | Карта уже привязана к переданному CustomerKey. |  |
| 511 | Проверка 3DS не пройдена. |  |
| 512 | Не удалось выполнить запрос на проверку 3DS. |  |
| 513 | Не удалось выполнить платеж после прохождения 3DS. |  |
| 514 | Введена неверная сумма холдирования. |  |
| 515 | Внутренняя ошибка. |  |
| 600 | Карта добавлена в черный список |  |
| 600 | Интернет-магазин отклонил операцию по данной карте. Обратитесь в интернет-магазин для выяснения причин отказа в платеже. |  |
| 601 | Разрешены операции только по MasterCard |  |
| 603 | Превышено количество попыток оплаты с данной карты |  |
| 604 | Не получилось совершить платеж. Свяжитесь с поддержкой | submerchant_id не привязан к terminal_Id |
| 619 | Отсутствуют обязательные данные отправителя | Не переданы персональные данные отправителя для операции emoney2card более 15000 руб. |
| 620 | Проверьте сумму — она не может быть равна 0 | Сумма операции не может быть равна 0 |
| 623 | Выплата по этому заказу уже прошла | Запрещено проводить платеж с OrderId для которого уже есть успешный платеж. |
| 632 | Превышен лимит на сумму операции | Лимит на сумму пополнения emoney2card. См. лимиты |
| 633 | Превышен лимит на количество переводов в день по иностранным картам | Лимит на кол-во пополнений emoney2card для карт эмитированных нерезидентами РФ за 1 отчетный день |
| 634 | Превышен лимит на сумму переводов по номеру карты в месяц | Лимит на сумму пополнения emoney2card по номеру карты одного получателя в отчетный месяц |
| 637 | Не хватает данных получателя или отправителя для выплаты на иностранную карту. Проверьте заполнение | Отсутствуют персональные данные получателя/отправителя при переводе на иностранную карту |
| 642 | Проверьте номер карты | Карта не прошла проверку по алгоритму Луна |
| 648 | Не получилось пополнить карту. Свяжитесь с поддержкой | submerchant_id заблокирован |
| 650 | Не получилось пополнить карту. Попробуйте позже | Внутренняя ошибка системы |
| 651 | Не получилось совершить платеж. Свяжитесь с поддержкой | Передаваемый Request_Id не найден. |
| 700 | Список карт Masterpass недоступен для данного магазина. |  |
| 701 | Сервис MasterPass недоступен. |  |
| 702 | Поле maid и saav должно быть задано в настройках терминала. |  |
| 703 | Не получилось пополнить карту. Попробуйте позже | Ошибка третьих систем |
| 800 | Комиссия не найдена |  |
| 903 | Повторите попытку позже |  |
| 914 | Платеж не найден |  |
| 926 | Сделка уже закрыта | Сделка уже закрыта |
| 927 | Сделка не найдена | Сделка не найдена |
| 991 | Для использования 3dsType необходимо установить 3ds терминал | Для использования TDS роутинга необходимо пользоваться ТДС терминалом |
| 999 | Попробуйте повторить попытку позже |  |
| 1001 | Свяжитесь с банком | Свяжитесь с банком, выпустившим карту, чтобы провести платеж |
| 1003 | Неверный магазин | Неверный номер магазина. Идентификатор магазина недействителен. |
| 1004 | Заберите карту | Карта украдена. Свяжитесь с банком, выпустившим карту |
| 1005 | Платеж отклонен банком, выпустившим карту | Платеж отклонен банком, выпустившим карту |
| 1006 | Платеж не прошел | Свяжитесь с банком, выпустившим карту, чтобы провести платеж |
| 1007 | Платеж не прошел | Карта украдена. Свяжитесь с банком, выпустившим карту |
| 1008 | Платеж отклонен, необходимо идентификация |  |
| 1012 | Платеж не прошел | Такие операции запрещены для этой карты |
| 1013 | Повторите попытку позже. | Сумма превышает лимит платежа вашего банка. Воспользуйтесь другой картой или обратитесь в банк |
| 1014 | Карта недействительна | Неправильные реквизиты — проверьте их или воспользуйтесь другой картой |
| 1015 | Неверный номер карты | Неверный номер карты |
| 1017 | Попробуйте снова или свяжитесь с банком, выпустившим карту | Попробуйте снова или свяжитесь с банком, выпустившим карту |
| 1018 | Неизвестный статус платежа |  |
| 1019 | Платеж отклонен — попробуйте снова |  |
| 1030 | Повторите попытку позже. | Не получилось оплатить. Попробуйте еще раз |
| 1033 | Истек срок действия карты | Неправильные реквизиты — проверьте их или воспользуйтесь другой картой |
| 1034 | Попробуйте повторить попытку позже | Не получилось оплатить. Воспользуйтесь другой картой или обратитесь в банк, выпустивший карту |
| 1038 | Превышено количество попыток ввода ПИН-кода |  |
| 1039 | Платеж отклонен — счет не найден |  |
| 1041 | Карта утеряна | Карта утеряна. Свяжитесь с банком, выпустившим карту |
| 1043 | Заберите карту | Карта украдена. Свяжитесь с банком, выпустившим карту |
| 1051 | Недостаточно средств на карте. | Не получилось оплатить. На карте недостаточно средств |
| 1053 | Платеж отклонен — счет не найден |  |
| 1054 | Истек срок действия карты | Неправильные реквизиты — проверьте их или воспользуйтесь другой картой |
| 1055 | Неверный ПИН |  |
| 1057 | Отказ | Такие операции запрещены для этой карты |
| 1058 | Такие операции запрещены для этой карты | Такие операции запрещены для этой карты |
| 1059 | Подозрение в мошенничестве | Подозрение в мошенничестве. Свяжитесь с банком, выпустившим карту |
| 1061 | Превышен лимит | Превышен дневной лимит платежей по карте |
| 1062 | Платежи по карте ограничены | Платежи по карте ограничены |
| 1063 | Подозрение в мошенничестве | Операции по карте ограничены |
| 1064 | Проверьте сумму |  |
| 1065 | Превышен лимит транзакций | Превышен дневной лимит транзакций |
| 1071 | Токен просрочен | Токен просрочен |
| 1075 | Неверный ПИН | Превышено число попыток ввода ПИН-кода |
| 1076 | Платеж отклонен — попробуйте снова |  |
| 1077 | Коды не совпадают — попробуйте снова |  |
| 1078 | Данный тип операции не поддерживается картой |  |
| 1080 | Неверный срок действия |  |
| 1082 | Неверный CVV | Неправильные реквизиты — проверьте их или воспользуйтесь другой картой |
| 1085 | Операция успешна | Успех |
| 1086 | Платеж отклонен — не получилось подтвердить ПИН-код |  |
| 1088 | Ошибка шифрования | Ошибка шифрования. Попробуйте снова |
| 1089 | Попробуйте повторить попытку позже | Не получилось оплатить. Попробуйте еще раз или обратитесь в банк, выпустивший карту |
| 1091 | Банк, выпустивший карту недоступен | Банк, выпустивший карту недоступен для проведения авторизации |
| 1092 | Платеж отклонен — попробуйте снова |  |
| 1093 | Подозрение в мошенничестве. Свяжитесь с банком выпустившим карту | Подозрение в мошенничестве. Свяжитесь с банком, выпустившим карту |
| 1094 | Системная ошибка | Повторная транзакция |
| 1096 | Системная ошибка | Системная ошибка |
| 1099 | Способ оплаты отключен |  |
| 1116 | Некорректная сумма выдачи | Сумма баланса меньше суммы переданной в операции выдачи |
| 1119 | Параметр account объекта DATA должен быть заполнен корректно для MCC: 6050/6051 | Передан некорректный номер кошелька |
| 1201 | Попробуйте повторить попытку позже |  |
| 1202 | Попробуйте повторить попытку позже | Превышена максимальная сумма операции |
| 1203 | Воспользуйтесь другой картой или обратитесь к продавцу | Превышена максимальная сумма или количество операций по карте в сутки |
| 1204 | Попробуйте повторить попытку позже | Превышена максимальная сумма операций в сутки |
| 1205 | Воспользуйтесь другой картой или обратитесь к продавцу | Платеж отклонен ввиду ограничений географии приема платежей |
| 1207 | Попробуйте повторить попытку позже | Заказ не может быть оплачен, обратитесь службу поддержки |
| 1217 | Воспользуйтесь другой картой или обратитесь к продавцу | Воспользуйтесь другой картой или обратитесь к продавцу |
| 1218 | Воспользуйтесь другой картой или обратитесь к продавцу | Воспользуйтесь другой картой или обратитесь к продавцу |
| 1316 | Запрещено проведение авторизации | Запрещено проведение авторизации с использованием 3DS |
| 1502 | Недостаточно средств на счете компании | Insufficient funds |
| 1503 | Некорректный статус счета, обратитесь в поддержку | Invalid account status |
| 2014 | Не пройдена идентификация 3DS |  |
| 2015 | Mерчант с таким именем и паролем не найден. |  |
| 2200 | Превышено допустимое количество запросов авторизации операции |  |
| 3001 | Оплата через QrPay недоступна |  |
| 3002 | Недостаточный баланс счёта для отмены. |  |
| 3003 | Отмена платежа в связи с мошенничеством. |  |
| 3004 | Способ СБП недоступен для магазина. |  |
| 3005 | Оплата через СБП не доступна |  |
| 3006 | Банк получателя не может принять возврат. Выберите другой банк. |  |
| 3007 | Отказ в проведении операции от СБП. |  |
| 3008 | У получателя нет расчетного счета в этом банке. Выберите другой банк. |  |
| 3009 | Отказ в проведении операции от СБП или банка получателя. |  |
| 3010 | У получателя нет расчетного счета в этом банке. ФИО некорректное. |  |
| 3011 | Оплата через E2C недоступна |  |
| 3012 | Привязка счета не найдена |  |
| 3013 | Рекуррентные платежи недоступны |  |
| 3014 | AccountToken не найден |  |
| 3015 | Неверный статус AccountToken |  |
| 3016 | Невозможно создать QR |  |
| 3017 | Переданное значение RedirectDueDate вне допустимого диапазона. |  |
| 3018 | Список банков не найден. |  |
| 3019 | Не включен СБП в личном кабинете |  |
| 8001 | Операция запрещена для рассрочки |  |
| 8002 | Tinkoff Credit Broker недоступен. Повторите попытку позже. |  |
| 8003 | Операция запрещена для покупки долями. |  |
| 8004 | BNPL недоступен. Повторите попытку позже. |  |
| 9001 | Попробуйте повторить попытку позже |  |
| 9999 | Внутренняя ошибка системы. |  |