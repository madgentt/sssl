# Практическая работа №3 WAZUH

**Выполнил студент группы ББМО-01-23 Картунчиков А.М.**

## 1. Развернуть 2 ВМ и обеспечить между ними сетевой обмен

Развернем две ВМ и создадим пользователей kartunchikov_agent (192.168.44.133) & kartunchikov_serv (192.168.44.134)
![image](https://github.com/user-attachments/assets/2a91c5cb-d10e-4968-8c1e-bdff5ebefe9b)



Сетевая связность между ВМ
![image](https://github.com/user-attachments/assets/3328e78f-c1c8-4430-bd85-ae6a20942c2a)



## 2.Развернуть на одной из ВМ сервер WAZUH, а на другой клиент

Воспользуемся официальной документацией - https://documentation.wazuh.com/current/installation-guide/wazuh-server/installation-assistant.html

![image](https://github.com/user-attachments/assets/9523f24a-78e2-4f84-aac7-ab8b23321bd2)

![image](https://github.com/user-attachments/assets/ced5fcce-343f-48e7-84a5-7a41ad99d01e)

Логин - admin

Пароль - JQkH3nT911vzyBNpRQv..TZVZsyU9.dM

![image](https://github.com/user-attachments/assets/3e7a5649-54ec-4603-b888-84eb88a71792)

Установим агент 
![image](https://github.com/user-attachments/assets/16a2324b-1992-4c36-9899-04933ef76a93)
![image](https://github.com/user-attachments/assets/50019343-ccbd-48f1-8a24-fb5ddaa616e9)

Результаты сканирования на уязвимости 
![image](https://github.com/user-attachments/assets/49c3bca4-020d-4172-9a74-38298980d178)

## 3. Проверка целостности файлов
![image](https://github.com/user-attachments/assets/6f1ddaf5-95c1-4bd6-bd06-bb773b5fc603)
![image](https://github.com/user-attachments/assets/d41865bf-ed60-4da7-b0b4-0fde1943b997)


## 4. Настройте выявление уязвимостей
![image](https://github.com/user-attachments/assets/30da595c-bbcd-4413-bd27-c4f5c7e1c7ec)

## 5. Настройки выявления скрытых процессов
![image](https://github.com/user-attachments/assets/5b9ae691-b196-4989-8f1d-a60df7d8d0a4)
![image](https://github.com/user-attachments/assets/77f28aeb-2ff9-44db-bb15-dfd5910d64fb)
![image](https://github.com/user-attachments/assets/6e8e5028-a9d1-4045-a378-dade1f2e55cb)

## 6. Настройте выявление SQL-инъекций

![image](https://github.com/user-attachments/assets/49d12354-788c-4881-a46c-ce19a23ce83d)
![image](https://github.com/user-attachments/assets/f10b8e11-f7d5-4bd5-b3ed-4bd7e5097284)
![image](https://github.com/user-attachments/assets/5760b714-f770-4e7c-855d-92487150a94c)
