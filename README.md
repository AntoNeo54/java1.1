# Отчёт о тестировании установки OpenJDK11 и работы приложения KeyValidator

## Краткое описание

31/10/2020 - 31/10/2020 было проведено тестирование установки OpenJDK11 и функциональное тестирование приложения KeyValidator.

На тестирование затрачено: 1 час

В результате тестирования выявлены следующие дефекты:
* Валидные ключи определяются не валидным #1 [#issue-733709486](https://github.com/AntoNeo54/java1.1/issues/1#issue-733709486)
* Не валидные ключи определяются валидным #2 [#issue-733712999](https://github.com/AntoNeo54/java1.1/issues/2#issue-733712999)

## Описание процесса тестирования

В процессе тестирования использовались следующие артефакты:
* Инструкция по установке OpenJDK11 [Инструкция по установке OpenJDK 11](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/openjdk11-manual.md)
* Руководство использования KeyValidator [Руководство использования](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md)
* Приложение KeyValidator [KeyValidator](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/artifacts/KeyValidator.class)


В качестве тестовых данных использовались данные [Ключи для проверки](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/user-manual.md#%D0%BA%D0%BB%D1%8E%D1%87%D0%B8-%D0%B4%D0%BB%D1%8F-%D0%BF%D1%80%D0%BE%D0%B2%D0%B5%D1%80%D0%BA%D0%B8):

Валидные ключи:
* 8f05e6a7-70e9-33d7-bfe7-b19eae0d8998 
* 80b427f8-92cd-3aae-ba04-3927fbe17c6
* b295bc63-9f03-3b4b-af80-969b39f8c262
* 387eedc6-12e9-3b32-9881-63b6b5e85317
* c19a8cf9-5c3a-37c5-b7f3-d16d38a0c180

ожидаемый результат Result for `валидный ключ`: OK

Невалидные ключи:
* 18252235-78e0-44a5-8720-556f0c7da17a
* e66075b6-ddad-445e-baf6-161b3289522b
* b6d53250-f07e-4352-a293-6102ddf7f1ca
* c2bc778a-1cb9-46c6-b435-0489649d2a42
* 2fb98b44-93e7-3bdd-a2ad-79347bfe4ad1

ожидаемый результат Result for `невалидный ключ`: FAIL


Тестирование производилось в следующем окружении:
* Операционная система Windows 10 Pro версия 1909 x64
* Java
openjdk version "11.0.7" 2020-04-14
OpenJDK Runtime Environment AdoptOpenJDK (build 11.0.7+10)
OpenJDK 64-Bit Server VM AdoptOpenJDK (build 11.0.7+10, mixed mode)

* Терминал Git x64 version 2.28.0.windows.1
