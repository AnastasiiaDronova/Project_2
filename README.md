Представьте, что вы работаете в крупном дейтинговом приложении. 

Помимо базовых функций, в приложении также имеется премиум-подписка, которая дает доступ к ряду важных дополнительных возможностей. Был проведен A/B тест, в рамках которого для новых пользователей из нескольких стран была изменена стоимость премиум-подписки* при покупке через две новые платежные системы. При этом стоимость пробного периода оставалась прежней.

<hr>

### Проверьте:

Был ли эксперимент успешен в целом. Деньги за подписку списываются ежемесячно до тех пор, пока пользователь её не отменит.

<hr>

### Описание данных: 
* Всего есть три группы:
* тестовая (test)
* контрольная 1 (control_1)
* контрольная 2 (control_2)

Для каждой из них:

* **users_*.csv** – информация о пользователях:
    * **uid** - идентификатор пользователя
    * **age** – возраст
    * **attraction_coeff** – коэффициент привлекательности (от 0 до 1000, лайки/просмотры∗1000)
    * **coins** – число монеток (внутренняя валюта) 
    * **country** – страна
    * **visit_days** – в какие дни после регистрации пользователь посещал приложение (напр. в 1, затем в 7)
    * **gender** – пол
    * **age_filter_start** – фильтр поиска, мин. значение
    * **age_filter_end** – фильтр поиска, макс. значение
    * **views_count** – число полученных оценок
    * **was_premium** – был ли когда-либо премиум (либо пробный период премиум-статуса, либо купленный
      
* **transactions_*.csv** – информация о платежах пользователей:
    * **uid** – идентификатор пользователя
    * **country** – страна
    * **joined_at** – дата и время регистрации
    * **paid_at** – дата и время покупки
    * **revenue** – нормированная выручка
    * **payment_id** – идентификатор платежа
    * **from_page** – откуда пользователь перешел на страницу оплаты
    * **product_type** – тип продукта (trial_premium – пробная премиум-подписка, premium_no_trial - премиум-подписка без пробной, coins - подписка за внутреннюю валюту, other_type - другое)
 
### Файлы:
  
* **users_test** – информация о пользователях в тестовой группе
* **users_control_1** – информация о пользователях в первой контрольной группе
* **users_control_2** – информация о пользователях во второй контрольной группе
* **transactions_test** – информация о платежах пользователей в тестовой группе
* **transactions_control_1** – информация о платежах пользователей в первой контрольной группе
* **transactions_control_2** – информация о платежах пользователей в тестовой группе

<hr>

### Реализация проекта:
 * 1 Проведен EDA для пользователей.
 * 2 Проведен EDA для транзакций.
 * 3 Сделаны выводы по EDA анализам.
 * 4 Подготовка данных для A/B- тестирования. (Рандомизация).
   * 4.1 Возраст
   * 4.2 Коэффициент привлекательности
   * 4.3 Число монеток (внутренняя валюта)
   * 4.4 Страна
   * 4.5 Количество дней, проведенное пользователем в приложении
   * 4.6 Пол пользователей
   * 4.7 Фильтр поиска, мин. значение
   * 4.8 Фильтр поиска, макс. значение
   * 4.9 Число просмотров
 * 5 A/B тестирование
 * 6 Вывод

 

