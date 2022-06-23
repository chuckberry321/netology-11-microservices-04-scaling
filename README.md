# Домашнее задание к занятию "11.04 Микросервисы: масштабирование"

## Задача 1: Кластеризация

Предложите решение для обеспечения развертывания, запуска и управления приложениями.
Решение может состоять из одного или нескольких программных продуктов и должно описывать способы и принципы их взаимодействия.

Решение должно соответствовать следующим требованиям:
- Поддержка контейнеров;
- Обеспечивать обнаружение сервисов и маршрутизацию запросов;
- Обеспечивать возможность горизонтального масштабирования;
- Обеспечивать возможность автоматического масштабирования;
- Обеспечивать явное разделение ресурсов доступных извне и внутри системы;
- Обеспечивать возможность конфигурировать приложения с помощью переменных среды, в том числе с возможностью безопасного хранения чувствительных данных таких как пароли, ключи доступа, ключи шифрования и т.п.

  **Ответ:**   
   Предложил бы решение *Yandex Managed Service for Kubernetes* 
  
   Как мне кажется, это решение удовлетворяет необходимым требованиям:
- поддерживает контейнеризацию ( интегрирован с Yandex Container Registry, что дает возможность использовать этот репозиторий и хранить Docker-образы рядом с инфраструктурой)
- можно управлять кластерами с помощью командной строки kubectl или с использованием Helm, Draft или Brigade для автоматизации доставки приложений
- поддерживается автоматическое масштабирование
- безопасная инфраструктура ( все взаимодействия между мастером и узлами кластера шифруются при помощи протокола TLS, есть возможность создать приватный кластер, недоступный из интернета, и управлять доступами с помощью сервиса IAM)
- легок в обслуживании (часть работ по обслуживанию кластера контролируются облачным провайдером)
- высокая доступность
