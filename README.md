
# Домашнее задание к занятию 1.  «Введение в виртуализацию»

   
## Задача 1

- Done 

## Задача 2

Выберите один из вариантов платформы в зависимости от задачи. Здесь нет однозначно верного ответа так как все зависит от конкретных условий: финансирование, компетенции специалистов, удобство использования, надежность, требования ИБ и законодательства, фазы луны.

Тип платформы:

- физические сервера;
- паравиртуализация;
- виртуализация уровня ОС;

Задачи:

- высоконагруженная база данных MySql, критичная к отказу; 
_я бы предложил виртуализацию уровня ОС в нескольких контейнерах разместил бы несколько одинаковых БД, чтоб надежно  или отдельные физические сервера, что дает возможность к дальнейшему масштабированию_
- различные web-приложения;  
*тут можно использовать к примеру LXC  на ProxMox, возможность гибкой настройки и можно легко мигрировать приложения*
- Windows-системы для использования бухгалтерским отделом; 
*любое решение из разряда паравиртуализации, виртуальную машину Windows c удаленным доступом. или физический сервер можно тоже*
- системы, выполняющие высокопроизводительные расчёты на GPU. 
*первостепенно физический сервер самые большие мощности и вычислительные возможности*

Объясните критерии выбора платформы в каждом случае.

## Задача 3

Выберите подходящую систему управления виртуализацией для предложенного сценария. Опишите ваш выбор.

Сценарии:

1. 100 виртуальных машин на базе Linux и Windows, общие задачи, нет особых требований. Преимущественно Windows based-инфраструктура, требуется реализация программных балансировщиков нагрузки, репликации данных и автоматизированного механизма создания резервных копий. 
*наиболее подходящим выбором системы управления предлагяю VMware vSphere - богатый функционал, поддержка различных операционных систем, включая Windows и Linux, интегрированные средства для реализации программных балансировщиков нагрузки, репликации данных и автоматизированного создания резервных копий*
2. Требуется наиболее производительное бесплатное open source-решение для виртуализации небольшой (20-30 серверов) инфраструктуры на базе Linux и Windows виртуальных машин. 
*Я за PROXMOX. Очень запросто с такими задачами справится*
3. Необходимо бесплатное, максимально совместимое и производительное решение для виртуализации Windows-инфраструктуры. 
*Ну тут Hyper-V. Предлагает все возможности для виртуализации  Windows-инфраструктуры.* 
4. Необходимо рабочее окружение для тестирования программного продукта на нескольких дистрибутивах Linux. 
*Предлагаю VirtualBox.  Поддерживает многие дистрибутивы и версии Linux. Достаточно гибок в настройках для тестирования программных продуктов.*

## Задача 4

Опишите возможные проблемы и недостатки гетерогенной среды виртуализации (использования нескольких систем управления виртуализацией одновременно) и что необходимо сделать для минимизации этих рисков и проблем. Если бы у вас был выбор, создавали бы вы гетерогенную среду или нет? 
*Если бы у меня был выбор, я бы не использовал гетерогенную среду виртуализации. Это сложность в управлении, овслуживании, усложнение безопасности, проблемы совместимости. Как решить? - централизованная система управления, стандартизировать процессы и настройки, обеспечить адекватный уровень безопасности*


