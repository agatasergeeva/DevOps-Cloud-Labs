# Лабораторная работа №1

## Настройка Nginx

### Сначала обновляем все с помощью `sudo apt update`, а затем установим *nginx* на виртуальной машине (Linux Ubuntu):

![первый скрин](https://github.com/agatasergeeva/DevOps-Cloud-Labs/blob/main/DevOps_1/folder/first.png)


![второй скрин](https://github.com/agatasergeeva/DevOps-Cloud-Labs/blob/main/DevOps_1/folder/second.png)

После этого проверяем статус работы с помощью `systemctl status nginx` 
### Затем создаем все папки/файлы, которые нам потребуются в дальнейшей работе

![третий скрин](https://github.com/agatasergeeva/DevOps-Cloud-Labs/blob/main/DevOps_1/folder/third.png)

### Также нам необходимо добавить домены сайтов в хосты с помощью `sudo nano /etc/hosts/`, где мы записываем IP сервера и домены:

![четвертый скрин](https://github.com/agatasergeeva/DevOps-Cloud-Labs/blob/main/DevOps_1/folder/fourth.png)

### Для начала попробуем не перенаправлять HTTP на HTTPS

![пятый скрин](https://github.com/agatasergeeva/DevOps-Cloud-Labs/blob/main/DevOps_1/folder/fifth.png)

Для lab2 прописываем все по аналогии, меняем цифру 1 на 2, где требуется. 

Эта конфигурация указывает Nginx на необходимость обслуживать файлы из каталога /var/www/lab1 с использованием index.html в качестве страницы по умолчанию. Директива try_files позволяет управлять тем, как сервер обрабатывает запросы на потенциально отсутствующие ресурсы.

*Все работает успешно, поэтому можно переходить к следующему этапу* 

### Подготовим все для того, чтобы сделать сертификаты:

![шестой скрин](https://github.com/agatasergeeva/DevOps-Cloud-Labs/blob/main/DevOps_1/folder/sixth.png)

### Теперь для каждого домена генерируем самоподписанный сертификат:

![седьмой скрин](https://github.com/agatasergeeva/DevOps-Cloud-Labs/blob/main/DevOps_1/folder/seventh.png)

![восьмой скрин](https://github.com/agatasergeeva/DevOps-Cloud-Labs/blob/main/DevOps_1/folder/eighth.png)

**Разберем команду, чтобы сгенерировать сертификат:**

`-req`: указывает, что будет выполняться запрос на создание сертификата

`-x509` указывает, что необходимо создать самоподписанный сертификат в формате X.509. Это стандартный формат для сертификатов SSL.

`-nodes`: означает, что ключ не будет зашифрован паролем. Это позволяет использовать сертификат без необходимости ввода пароля при каждом его применении.

`-days 365`: определяет срок действия сертификата

`-newkey rsa:2048`: указывает на создание нового приватного ключа с использованием алгоритма RSA длиной 2048 бит.

`-keyout`: определяет путь, по которому будет сохранен приватный ключ

`-out`: указывает на путь, где будет сохранен сертификат

`-subj “/CN=…”`: Определяет объектное имя сертификата, указывая, для какого доменного имени сертификат предназначен. 

### Также необходимо активировать файлы, поэтому создадим символические символы на них: 

![девятый скрин](https://github.com/agatasergeeva/DevOps-Cloud-Labs/blob/main/DevOps_1/folder/ninth.png)

### Далее отредактируем наши файлы конфигурации для того, чтобы у нас происходило перенаправление HTTP-запросов на HTTPS (для lab1 аналогично):

![десятый скрин](https://github.com/agatasergeeva/DevOps-Cloud-Labs/blob/main/DevOps_1/folder/tenth.png)

.....

### И вот, что у нас получилось в итоге:

![одиннадцатый скрин](https://github.com/agatasergeeva/DevOps-Cloud-Labs/blob/main/DevOps_1/folder/eleventh.png)

![двенадцатый скрин](https://github.com/agatasergeeva/DevOps-Cloud-Labs/blob/main/DevOps_1/folder/twelfth.png)

.....

![тринадцатый скрин](https://github.com/agatasergeeva/DevOps-Cloud-Labs/blob/main/DevOps_1/folder/thirteenth.png)

![четырнадцатый скрин](https://github.com/agatasergeeva/DevOps-Cloud-Labs/blob/main/DevOps_1/folder/fourteenth.png)

Отлично, у нас все заработало

*Нам снова надо создать много интересных вещей:* 

![пятнадцатый скрин](https://github.com/agatasergeeva/DevOps-Cloud-Labs/blob/main/DevOps_1/folder/fifteenth.png)

### После создания нам необходимо снова изменить файлы конфигураций: 

![шестнадцатый скрин](https://github.com/agatasergeeva/DevOps-Cloud-Labs/blob/main/DevOps_1/folder/sixteenth.png)

![семнадцатыый скрин]()

......
