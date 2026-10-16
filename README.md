# Блок 1: Фоновые службы, медиа и геотрекинг (Services)

1. ### Фоновый шагомер (Step Tracker):** Разработайте сервис переднего плана, слушающий аппаратный датчик `TYPE_STEP_COUNTER` и обновляющий число шагов в уведомлении раз в 10 секунд.   <img width="1920" height="1020" alt="photo_1_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/2549848b-0dc6-4e77-aed4-2b9ada086239" />

2. ### Аудиоплеер с управлением из шторки:** Реализуйте привязанный сервис с кнопками «Play», «Pause», «Next» в интерактивном уведомлении (`NotificationCompat.Action`).<img width="1920" height="1020" alt="photo_2_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/b8113cc2-7c47-49bc-879c-b9d51d6bdb49" />

3. ### Сервис пакетной выгрузки фотографий:** Напишите службу скачивания архива из 100 файлов с флагом `START_REDELIVER_INTENT` и отображением прогресс-бара в процентах.<img width="1920" height="1020" alt="photo_3_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/edc79aaa-822c-4ba2-b191-8470a2755eeb" />

4. ### Фоновый веб-сокет клиент:** Создайте сервис с непрерывным WebSocket-соединением для получения биржевых котировок, автоматически восстанавливающий связь при падении.<img width="1920" height="1020" alt="photo_4_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/4fb4c7e2-c914-45a9-ba33-61a52c1e1e1d" />

5. ### Сервис геозоны (Geofencing Monitor):** Разработайте сервис, непрерывно запрашивающий GPS-координаты и подающий звуковой сигнал при выходе из радиуса 500 метров от склада.<img width="1920" height="1020" alt="photo_5_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/1bb6dc18-6e9d-4188-8364-34b9fde7a138" />

6. ### Служба сжатия видеофайлов:** Напишите сервис с очередью задач на перекодирование видеороликов с использованием фонового пула `Executors.newSingleThreadExecutor()`.<img width="1920" height="1020" alt="photo_6_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/bec3fb1c-9d7c-48c2-977a-4ecfb946ce96" />

7. ### IPC через Messenger:** Создайте службу, взаимодействующую с клиентами из другого процесса с помощью объектов `Messenger` и сообщений `Message`.<img width="1920" height="1020" alt="photo_7_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/aec3d724-37b4-492e-a9ed-9f3cdbe17b4d" />

8. ### Служба очистки кэша по расписанию:** Реализуйте сервис, подсчитывающий размер каталога кэша и удаляющий файлы старше 7 дней при старте.<img width="1920" height="1020" alt="photo_8_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/f364221b-81bf-4c1f-8fd6-1f4c642d27d0" />

9. ### Служба мониторинга буфера обмена:** Разработайте сервис, отслеживающий появление в буфере обмена телефонных номеров и предлагающий быстрый звонок.<img width="1920" height="1020" alt="photo_9_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/b402e185-28af-427d-9813-1a008371ef64" />

10. ### Ограничитель времени работы сервиса:** Реализуйте авто-остановку Foreground-службы через 30 минут работы с помощью таймера и метода `stopForeground(true)`.<img width="1920" height="1020" alt="photo_10_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/a5a7ffb5-e43d-4184-b2fd-b954d051169b" />


# Блок 2: Системные события и широковещательные приемники (Broadcasts)

11. ### Детектор подключения зарядного устройства:** Зарегистрируйте приемник событий `ACTION_POWER_CONNECTED` и `ACTION_POWER_DISCONNECTED` с выводом текущего типа зарядки (быстрая, беспроводная, USB).<img width="1920" height="1020" alt="photo_11_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/261f1a1e-b708-4411-8f4c-708b33977624" />

12. ### Монитор изменения часового пояса:** Напишите приемник `ACTION_TIMEZONE_CHANGED`, пересчитывающий время локальных будильников при перелете пользователя.<img width="1920" height="1020" alt="photo_12_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/7125e99c-bd37-42de-8630-fdbfb520bf3b" />

13. ### Перехватчик исходящих SMS (Служебный режим):** Сконфигурируйте ресивер для обработки событий телеком-модуля при наличии соответствующих прав.<img width="1920" height="1020" alt="photo_13_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/615173f1-8bf5-42b7-9cf9-fe0a85def84b" />

14. ### Сигнализатор переполнения памяти накопителя:** Напишите приемник системного действия `ACTION_DEVICE_STORAGE_LOW`, автоматически инициирующий сброс временных картинок.<img width="1920" height="1020" alt="photo_14_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/090e519b-9314-4364-bf9e-d101fb03a1ce" />

15. ### Автоматический запуск службы после перезагрузки:** Настройте цепочку: прием события `BOOT_COMPLETED` -> валидация настроек -> вызов `startForegroundService()`.<img width="1920" height="1020" alt="photo_15_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/ece4282a-64e6-4578-b8c6-b0caaceb2b9f" />

16. ### Перехват подключения гарнитуры:** Напишите приемник события `ACTION_HEADSET_PLUG`, автоматически ставящий аудиоплеер на паузу при извлечении наушников.<img width="1920" height="1020" alt="photo_16_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/740bbe5c-efe8-4bfb-a91f-baa0853aedba" />

17. ### Локальный шифратор широковещательных сообщений:** Реализуйте отправку сообщений, подписанных цифровой подписью, с проверкой в ресивере через кастомное разрешение уровня `signature`.<img width="1920" height="1020" alt="photo_17_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/4d9229b2-b4a4-4272-9b0f-01c6fe1601bb" />

18. ### Индикатор изменения системного языка:** Сконфигурируйте ресивер действия `ACTION_LOCALE_CHANGED` для мгновенной переинициализации локализованных кэшей.<img width="1920" height="1020" alt="photo_18_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/02455720-caea-4e57-a40b-db0caad8591b" />

19. ### Динамический фильтр бродкастов с приоритетом:** Создайте 3 приемника в разных модулях и продемонстрируйте передачу модифицированных результатов через `setResultData()`.<img width="1920" height="1020" alt="photo_19_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/04d8b9d8-a3f1-499f-9e60-0a8305cbbe59" />

20. ### Антикраш-ресивер с таймаутом:** Оберните логику `onReceive()` в контролируемый асинхронный контекст `goAsync()` с принудительным завершением через 8 секунд.<img width="1920" height="1080" alt="photo_20_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/27358654-7148-401d-bcf0-a89fd014599b" />


# Блок 3: Обмен данными и файлами (Content Providers)

21. ### Провайдер безопасного доступа к логам:** Спроектируйте `ContentProvider` с правами только на чтение (`readPermission`), отдающий зашифрованные логи приложения аналитическому сервису.<img width="1920" height="1020" alt="photo_21_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/16744b7b-48cc-4c84-85a8-bbb1c6d951df" />
22. ### Интеграция с системным поиском (Quick Search Box):** Реализуйте провайдер, возвращающий курсор подсказок по схеме `SearchManager.SUGGEST_URI_PATH_QUERY`.<img width="1920" height="1020" alt="photo_22_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/44ae2beb-5cf3-4b3b-950a-b0cebee8687c" />

23. ### Экспорт визитных карточек (vCard):** Создайте провайдер, отдающий файлы контактов в формате `.vcf` через метод `openFile()`.<img width="1920" height="1020" alt="photo_23_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/82602162-6eaa-4c0b-9d81-13e42327c524" />

24. ### Синхронизация корзины между двумя приложениями:** Разработайте два разных приложения одной компании, где второе читает состав корзины первого через `ContentResolver`.<img width="1920" height="1020" alt="photo_24_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/ed93118e-a5c5-470a-86ff-aca2eeac54b4" />

25. ### Провайдер конфигураций приложения:** Реализуйте шифрованный поставщик настроек, хранящий пары «ключ-значение» в защищенном хранилище EncryptedSharedPreferences.<img width="1920" height="1020" alt="photo_25_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/c511b7bd-0978-4aff-b07a-a4a2d20d4d1c" />

26. ### Передача снимка с камеры через FileProvider:** Настройте генерацию безопасного `content://` URI для сохранения полноразмерного фото стандартным приложением камеры.<img width="1920" height="1020" alt="photo_26_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/9e445fb4-6b9f-4b4c-b6f2-1ab85d169a6b" />

27. ### Пакетная вставка 10 000 строк:** Оптимизируйте метод `bulkInsert()` в кастомном провайдере для быстрой загрузки каталога товаров в базу данных.<img width="1920" height="1020" alt="photo_27_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/c462ae2e-3d63-41f6-bfca-c0e1f1848882" />

28. ###  Провайдер с поддержкой MIME-типов PDF и CSV:** Реализуйте метод `getStreamTypes()` для отдачи отчетов в нескольких форматах по выбору клиента.<img width="1920" height="1020" alt="photo_28_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/659fa85a-c219-4d7f-ade8-03eae8047ad1" />

29. ### Мониторинг базы данных через ContentObserver:** Напишите сервис, слушающий изменения в системном журнале звонков и ведущий статистику вызовов.<img width="1920" height="1020" alt="photo_29_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/b3efa8e9-74aa-4c7b-9033-f81b5a643e4a" />

30. ### Полнотекстовый поиск по заметкам:** Спроектируйте ContentProvider над таблицей виртуальной полнотекстовой базы SQLite FTS4.<img width="1920" height="1020" alt="photo_30_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/b02ad57b-3423-4ce4-a9bf-bacf14b6c0ce" />


# Блок 4: Архитектурные комбинации и межкомпонентная интеграция

31. ### Комплекс «Фоновый загрузчик»:** Activity запускает Service скачивания -> Service по окончании рассылает Broadcast -> Receiver обновляет UI или показывает пуш.<img width="1920" height="1020" alt="photo_31_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/d1694337-9d03-4745-af48-c2691b504036" />


32. ### Комплекс «Аварийный сброс»:** Ресивер низкого заряда батареи останавливает тяжелые фоновые службы синхронизации и переводит провайдер данных в режим энергосбережения.<img width="1920" height="1020" alt="photo_32_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/21e29216-eb19-4645-9dab-aa5bef0a7305" />

33. ### Комплекс «Кэширующий прокси»:** ContentProvider при отсутствии данных в локальной БД обращается к Service для фонового запроса в сеть и уведомляет UI через `notifyChange()`.<img width="1920" height="1020" alt="photo_33_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/f40c8600-4231-43b2-8820-6ceba4c54e75" />


34. ### Удаленное управление сервисом через Broadcast:** Реализуйте управление плеером (Play/Stop/Mute) путем отправки внешних интентов из тестового консольного скрипта `adb shell am broadcast`.<img width="1920" height="1020" alt="photo_34_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/c29db30d-031e-423e-b913-268bef6af1f2" />


35. ### Двусторонняя связь Activity и Bound Service:** Настройте паттерн Callback/Listener, чтобы служба сама уведомляла экран о появлении новых данных датчиков.<img width="1920" height="1020" alt="photo_35_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/84761ec1-c5a1-4ea3-bc0f-4b7dd3accbe1" />


36. ### Автоматический бэкап базы в файл:** По сигналу системного времени (`ACTION_TIME_TICK`) сервис считывает данные из ContentProvider и сохраняет их в JSON-архив.<img width="1920" height="1020" alt="photo_36_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/63c2535d-6e1d-450e-a26a-f73bbdc4a05a" />

37. ### Контроль доступа к компонентам по белому списку пакетов:** Проверяйте имя вызывающего пакета через `Binder.getCallingUid()` и `PackageManager.getNameForUid()`.<img width="1920" height="1020" alt="photo_37_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/8204b59e-95ad-4629-ab51-b8f14be8d9d2" />


38. ### Передача дескрипторов файлов (PipeDataWriter):** Реализуйте передачу потоковых данных из сервиса в провайдер без сохранения промежуточного файла на диск через канал `ParcelFileDescriptor.createPipe()`.<img width="1920" height="1020" alt="photo_38_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/10a90a02-f55e-4784-8b81-7cfe1d88cd0d" />


39. ### Имитация системного будильника:** Соберите связку из `AlarmManager`, BroadcastReceiver и высокоприоритетного Foreground Service для пробуждения экрана.<img width="1920" height="1020" alt="photo_39_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/6e762ffc-63ce-4b61-9304-180554d4b136" />


40. ### Динамическое отключение компонентов:** Реализуйте включение и выключение BroadcastReceiver во время работы через метод `PackageManager.setComponentEnabledSetting()`.    <img width="1920" height="1020" alt="photo_40_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/32b63a4c-c77c-4084-a33c-0cf2647adf33" />



# Блок 5: Безопасность, оптимизация и отказоустойчивость

41. ### Защита от атак повторного воспроизведения (Broadcast Replay Attack):** Добавьте проверку таймстемпа и случайной одноразовой соли (Nonce) в широковещательные интенты.<img width="1920" height="1020" alt="photo_41_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/465333e0-283b-4191-a019-bd2a363b6529" />

42. ### Изоляция провайдера от обхода путей (Path Traversal):** Напишите валидатор путей в методе `openFile()`, блокирующий попытки извлечения файлов через последовательности `../`.<img width="1920" height="1020" alt="photo_42_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/c32ece86-47f2-4194-987a-889ee022fa31" />

43. ### Ограничение прав на чтение и запись:** Настройте в манифесте для провайдера раздельные атрибуты `android:readPermission` и `android:writePermission`.<img width="1920" height="1020" alt="photo_43_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/3e6fdee8-e05d-40ed-a308-2ec6f492f89b" />

44. ### Профилирование утечек памяти в сервисах:** Проанализируйте длительно работающий сервис на предмет удержания ссылок на уничтоженные Activity через статические поля.<img width="1920" height="1020" alt="photo_44_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/652cd342-d677-4afe-a5d2-e779c51fedbd" />

45. ### Адаптация сервисов под режим глубокого сна (Doze Mode):** Реализуйте корректную обработку перехода устройства в спящий режим и использование `PowerManager.WakeLock` с обязательным таймаутом.<img width="1920" height="1020" alt="photo_45_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/1fcfc12d-2344-437e-ba6b-fe90f31a6b63" />

46. ### Защита от неконтролируемого запуска службы:** Сделайте сервис недоступным для внешних приложений (`android:exported="false"`), защитив его от Intent Injection.<img width="1920" height="1020" alt="photo_46_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/a8f6e346-329b-44ab-af89-9ab7a6b8173a" />

47. ### Отказоустойчивость при падении SQLite:** Оберните все операции провайдера контента в обработку `SQLiteDatabaseCorruptException` с аварийным пересозданием файла базы данных.<img width="1920" height="1020" alt="photo_47_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/77e42a82-171f-48f6-ba2b-ef28e24b82c6" />

48. ### Контроль энергопотребления датчиков в сервисе:** Реализуйте снижение частоты опроса акселерометра в 10 раз при выключенном дисплее (`ACTION_SCREEN_OFF`).<img width="1920" height="1020" alt="photo_48_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/729b3554-5761-484e-9f00-9a09ca0a6775" />

49. ### Безопасная выдача временных разрешений на URI:** Реализуйте генерацию интента с флагами `FLAG_GRANT_READ_URI_PERMISSION` для передачи фотографии стороннему редактору.<img width="1920" height="1020" alt="photo_49_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/59c706dc-8e5f-4640-9467-19ccddd1f2ff" />

50. ### Комплексная архитектура Enterprise-модуля:**<img width="1920" height="1020" alt="photo_50_2026-10-17_00-12-00" src="https://github.com/user-attachments/assets/7808d800-9a11-4b48-91c6-49d169e99800" />

    - Разработайте защищенный Foreground Service с типом `dataSync`.
    - Подключите локальный ContentProvider с постраничной пагинацией.
    - Настройте динамический BroadcastReceiver для контроля сетевого статуса.
    - Обеспечьте нулевую вероятность возникновения ANR и полную очистку системных ресурсов в методах `onDestroy()`.

---
