# Практическая работа №4 - Network Threat Hunting

**Выполнил студент группы ББМО-01-23 Картунчиков А.М.**

# Развернем стенд
![image](https://github.com/user-attachments/assets/dd40391c-198b-4f30-90d6-9e479ae5368b)

# Добавление в safelist адреса скайп

![image](https://github.com/user-attachments/assets/df60be7b-c845-476a-b137-20d77af34128)

![image](https://github.com/user-attachments/assets/ae28624c-9d59-460c-8050-515850d2bea9)

# lab 1
## Импорт логов

![image](https://github.com/user-attachments/assets/4ce64c1c-621e-4e99-98a9-fdb296230044)

![image](https://github.com/user-attachments/assets/5bb41c4f-55fd-44d5-8d65-327937da35ab)

## Первый адрес

![image](https://github.com/user-attachments/assets/d6083802-ee73-4df9-915f-e8e5808639de)

Что можно понять о данном адресе:

- Очень высокий показатель beacon score.
- За последние 24 часа было сделано множество подключений (3 011).
- Гистограмма выглядит относительно ровной.
- Отсутствует строка хостинга. Необходимо указать полное доменное имя веб-сервера.

## Второй адрес

![image](https://github.com/user-attachments/assets/456ea314-6114-4c0b-9b59-0334ff019c03)

Легитимный домен майкрософт, можно исключить 

![image](https://github.com/user-attachments/assets/9814e97e-a7cc-45f3-a43a-7454dd506101)

После исключения отсются только два адреса

## Третий адрес

![image](https://github.com/user-attachments/assets/215f3e0b-4b7d-425c-8832-6b48cc39c68d)

Снова легитимный домен майкрософт, добваим в исключения

![image](https://github.com/user-attachments/assets/2347b8c9-f5ae-45a0-8c54-11a47a000c72)

## Первый адрес

Вернемся к первому подозрительному адресу и посмотрим к кому он подключался

![image](https://github.com/user-attachments/assets/0ac6ab3d-8eba-4a98-99ed-1333a265dd3f)

![image](https://github.com/user-attachments/assets/0051cc5e-06de-4853-bd39-600592d6df1c)

Первый адрес выглядит подозрительно

![image](https://github.com/user-attachments/assets/193c22d0-c67a-4305-a5a3-79d2c5d66519)


## Вывод: 

Соединения с IP-адресом 104.248.234.238 явно являются зловредными.

- Отсутствуют запросы с FQDN.
- URI имеет длинную и запутанную строку.
- 3 011 соединений с атрибутами beacon strong.
- Строка агента пользователя была изменена.
- Все остальные записи могут быть добавлены в safelist.
- Отсутствует поле "host" в HTTP-заголовке.
- По запросу "rmvk30g" в Google появляется "Fiesta EK".

# lab 2

## Импорт логов

![image](https://github.com/user-attachments/assets/a17479fc-7495-4567-bc3f-0f7bf8edf92e)

![image](https://github.com/user-attachments/assets/227a0a79-23c8-48d5-be1f-45a2bc57a146)

## DNS

Все влкдаки кроме днс пустые 

![image](https://github.com/user-attachments/assets/c00f37a7-4294-40e2-9913-ee2dc6209164)

Видим множество обращений на поддомены honesimnotevil.com

## Выводы

- Потенциальный C2 через DNS.
- Имя хоста состоит из шестнадцатеричных символов.
- Проверка в левом верхнем углу экрана указывает на необходимость проверки модуля DNS.

# lab 3

## Импорт логов

![image](https://github.com/user-attachments/assets/83cf1356-530f-4161-ae5a-99ffea7a032e)

![image](https://github.com/user-attachments/assets/72586f91-c095-4e1c-abb8-932de7be9b75)

## Первый адрес

![image](https://github.com/user-attachments/assets/44bb8533-6c06-4e48-b1aa-c611dd4089c7)

Что можно понять о данном адресе:

- Подозрительно выглядит доменное имя skypetm
- Очень высокий показатель beacon score.
- За последние 24 часа было сделано множество подключений (3 188).
- Гистограмма выглядит относительно ровной.

![image](https://github.com/user-attachments/assets/6a98c3f5-f113-460e-9446-4a8e4042359b)

Замаскировон под сервис Redmine, вероятно фишинг

![image](https://github.com/user-attachments/assets/b18f29a8-aedc-4b37-8f0a-19bd00070825)

К кому обращался данный адрес

![image](https://github.com/user-attachments/assets/3a0071ae-9ef5-4249-a602-e603c7334824)

Вредосноный адрес и тут, точно вредоносный адрес

## Второй адрес

![image](https://github.com/user-attachments/assets/21324255-6986-49fa-9d05-858f773d5984)

Легитимный домен майкрософт




