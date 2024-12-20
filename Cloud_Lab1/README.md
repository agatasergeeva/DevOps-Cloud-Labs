# Лабораторная работа 1. Знакомство с IaaS, PaaS, SaaS сервисами в облаке на примере Amazon Web Services (AWS). Создание сервисной модели.

(Вариант 2)

## Условие:

**Цель работы:**
Знакомство с облачными сервисами. Понимание уровней абстракции над инфраструктурой в облаке. Формирование понимания типов потребления сервисов в сервисной-модели. 

**Дано:**

   Слепок данных биллинга от провайдера после небольшой обработки в виде SQL-параметров. Символ % в начале/конце означает, что перед/после него может стоять любой набор символов.
Образец итогового соответствия, что желательно получить в конце. В этом же документе  

**Необходимо:**

- Импортировать файл .csv в Excel или любую другую программу работы с таблицами. Для Excel делается на вкладке Данные – Из текстового / csv файла – выбрать файл, разделитель – точка с запятой.
- Распределить потребление сервисов по иерархии, чтобы можно было провести анализ от большего к меньшему (напр. От всех вычислительных ресурсов Compute дойти до конкретного типа использования - Выделенной стойка в датацентре Dedicated host usage).
- Сохранить файл и залить в соответствующую папку на Google Drive.

**Алгоритм работы:** 

- Сопоставить входящие данные от провайдера с его же документацией.
- Написать в соответствие колонкам справа значения 5 колонок слева, которые бы однозначно классифицировали тип сервиса. Для столбцов IT Tower и Service Family значения можно выбрать из образца.


## Ход работы 

### Описание сервисов

1. **Cloud Services**

Облачные сервисы включают широкий спектр инструментов и услуг для тестирования, управления безопасностью и помощи разработчикам. Эти сервисы обеспечивают высокую степень автоматизации и масштабируемости.

*Использованные сервисы:*

- AWS Device Farm – предоставляет возможности тестирования устройств на различных платформах.
- Amazon CloudHSM – модуль аппаратной безопасности для обеспечения защиты данных в облаке.
- Amazon CodeBuild – сервис для сборки и тестирования приложений в облаке.


2. **Compute**
   
Категория Compute включает в себя сервис Amazon Elastic Compute Cloud (EC2), а также метрики, как BoxUsage для экземпляров EC2, Dedicated Usage, Host Usage и Elastic IP, предоставляющие вычислительные ресурсы для выполнения задач различного уровня сложности, от обработки данных до хостинга приложений.

3. **Database**

Сервисы для работы с базами данных предоставляют пользователям инструменты для хранения, управления и потоковой обработки данных.

*Использованные сервисы:*

- Amazon DynamoDB - управление базой данных, емкостью и использованием ресурсов.
- Amazon DynamoDB Accelerator - оптимизированная производительность для DynamoDB.


4. **Machine Learning (ML)**

Сервисы машинного обучения включают инструменты для анализа текста, обработки аудио и перевода, что помогает автоматизировать сложные задачи.

*Использованные сервисы:*

- Amazon Transcribe – транскрипция аудио.
- Amazon Comprehend – анализ текста.


5. **Migration & Transfer**
 
Эта категория охватывает сервисы для безопасного перемещения данных между разными системами и средами.

*Использованные сервисы:*

- AWS Database Migration Service - перемещение баз данных в AWS.
- AWS Database Migration Service Storage - хранение данных во время перемещения.


6. **Networking**
   
Сервисы для организации и управления сетями, включая управление трафиком и плату за партнерские соединения.

*Использованные сервисы:*

- Partner Network – сообщество партнёров, помогающее работать с продуктами AWS.

7. **Storage**
    
Категория включает услуги для хранения данных, резервного копирования и управления большими объемами информации.

*Использованные сервисы:*

- Amazon Backup: Сервис для автоматического управления резервными копиями.

*Биллинг и Метрики*

- Cold/Warm Storage Support – поддержка "холодного"/"теплого" хранения данных.

### Результат нашей работы:

![photo](https://github.com/agatasergeeva/DevOps-Cloud-Labs/blob/main/Cloud_Lab1/photo_2024-12-11_15-49-00.jpg)




