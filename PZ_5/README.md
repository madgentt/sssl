# Практическая работа №5 - Threat Hunting

**Выполнил студент группы ББМО-01-23 Картунчиков А.М.**

Для выполнения работы воспользуемся лабораторным стендом из практической работы 3

Стенд состоит из 3 виртуальных машин
1) Убунту с агентом вазух
2) Убунту с сервером вазух
3) Кали

![image](https://github.com/user-attachments/assets/c7158bd7-9c1f-42cd-9d8b-d4cb34a01106)

# IDS Suricata

Развернем дополнительно на защищаемом хосте IDS Суриката

![image](https://github.com/user-attachments/assets/639811dd-0916-4f9f-ac45-43b199226efe)

Внесем сбор логов сурикаты в конфиг вахуха

![image](https://github.com/user-attachments/assets/76ce5dd1-b7d0-42f0-9a0c-054dd466489e)

На защищаемом сервере поднят пустой апач на ажресе 192.168.44.133Ж:80

![image](https://github.com/user-attachments/assets/25424f67-ca5a-442e-aeb8-d0c3d69c8f4d)

Запустим сканер уязвимостей Nikto

![image](https://github.com/user-attachments/assets/c8e24dab-ab7a-4256-ba7a-72fecb833d04)

События от сурикаты в SIEM

![image](https://github.com/user-attachments/assets/d3233340-5c9c-46db-a79b-e9c15e3e6e4f)

# YARA

Скачаем и установим нужные пакеты
![image](https://github.com/user-attachments/assets/f59036c9-46f7-405c-b9af-12ab8fcf8435)

![image](https://github.com/user-attachments/assets/53bf5a41-cfda-4688-bcf2-6250d7251402)

Скачаем пакет правил 
![image](https://github.com/user-attachments/assets/485b8277-8101-4adf-af50-092c359d164f)

Создадим конфиг активного реагирования
![image](https://github.com/user-attachments/assets/e16b71d8-a89f-4243-8913-9249484610f9)

Добавим мониторинг директории home в конфиг
![image](https://github.com/user-attachments/assets/79c66485-95d0-43a3-9bd0-5887867cfab2)

Конфигурация сервера
![image](https://github.com/user-attachments/assets/4d87d904-f6bd-4118-bb32-467ea9ae3f1d)

Конфигурация будующих событий
![image](https://github.com/user-attachments/assets/576e6ab9-4d47-499a-9c24-df226599307f)

Конфигурация действий регаирования 
![image](https://github.com/user-attachments/assets/5c26a954-ade4-4d4d-9069-8dadbf57e015)

Сработки ЯРА правил
![image](https://github.com/user-attachments/assets/7a15f3c2-4717-4405-ad27-d90321b5b9c9)

![image](https://github.com/user-attachments/assets/6fa86f90-ff77-4c56-aafc-7efe46bb4b30)

