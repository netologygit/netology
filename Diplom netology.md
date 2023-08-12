Для выполнения дипломной работы были развернуты 8 ВМ


![1](https://github.com/netologygit/netology/assets/123411071/dde312df-ce09-4efb-9190-a4eab9e0bbb2)

По условиям задания сервера web, Prometheus, Elasticsearch были размещены в приватные подсети. Сервера Grafana, Kibana, application load balancer определены в публичную подсеть.
Также сервера web1 и web2 размещены в разных зонах доступности.

На сервера web1 192.168.2.15 и web2 192.168.3.11 был установлен Nginx, для их работы настроен балансировщик

![1](https://github.com/netologygit/netology/assets/123411071/0c410e4c-cb84-45b1-8cc7-47971cb7a6d9)

![2](https://github.com/netologygit/netology/assets/123411071/8defd843-de3d-4993-aa0e-9ba6af967ed9)

![2](https://github.com/netologygit/netology/assets/123411071/a8c46924-12e9-4ed4-91b6-048972d1b50d)

![1](https://github.com/netologygit/netology/assets/123411071/4a6cdab0-10c1-458f-ab11-36117db3dedf)

Были созданы  Target Group и Backend Group

![1](https://github.com/netologygit/netology/assets/123411071/b2bcb1cf-5c4c-44c2-8108-180441e41013)

![2](https://github.com/netologygit/netology/assets/123411071/597c5b84-12b2-49ad-bb15-af2f9ee60f54)

Также был создан HTTP router

![1](https://github.com/netologygit/netology/assets/123411071/4e9e729a-1e08-4dde-bd5c-04cfb34312c0)

Создан Application load balancer

![балансировщик](https://github.com/netologygit/netology/assets/123411071/3eb37ebf-948f-44c0-9002-a5045c55ed73)

На сервере 192.168.2.25 установлена Grafana

![1](https://github.com/netologygit/netology/assets/123411071/2e649c42-4054-44de-ae6e-ac68673dd90b)

На web1 и web2 установлены Node Exporter и Nginx Log Exporter. Также настроен Prometheus на сбор метрик с этих exporter.

![1](https://github.com/netologygit/netology/assets/123411071/c5005f59-54c3-4ce0-b0e7-c96bedf97c0f)

![2](https://github.com/netologygit/netology/assets/123411071/95d5fd01-4246-4556-9486-7ba90d69a111)

![1](https://github.com/netologygit/netology/assets/123411071/1e0222fa-07e0-43db-a548-7da2b9945818)

![2](https://github.com/netologygit/netology/assets/123411071/ee740502-a19b-4cc5-b7bf-1ce02c787160)



![1](https://github.com/netologygit/netology/assets/123411071/73becee5-9c9a-414a-9157-c2efdb1cf3c8)

![2](https://github.com/netologygit/netology/assets/123411071/60a70785-66d8-486f-9c64-0eed7e2c6335)


Cоздана ВМ, на которой развернут Elasticsearch 192.168.2.4. Установлен filebeat в ВМ к web1 и web2, настроена отправка access.log, error.log nginx в Elasticsearch.

Создана ВМ, на которой развернута  Kibana  192.168.2.16, сконфигурировано соединение с Elasticsearch.

![1](https://github.com/netologygit/netology/assets/123411071/b7ebc6ff-131c-41da-a93d-833055836a71)

![2](https://github.com/netologygit/netology/assets/123411071/2a0fa659-77bb-4aa1-9dc5-11862a07a1ad)

![1](https://github.com/netologygit/netology/assets/123411071/2afc65a1-4feb-4e6b-9172-228b6f185da7)

![2](https://github.com/netologygit/netology/assets/123411071/9386ecdc-ab27-4007-b449-1cb7aa46787f)


![3](https://github.com/netologygit/netology/assets/123411071/4282bebd-ae4b-45e0-93b9-4fdbc27e023a)




![1](https://github.com/netologygit/netology/assets/123411071/1439195b-b024-436e-8f11-be6f9dfd0779)

![1](https://github.com/netologygit/netology/assets/123411071/8d5b4955-02c3-43fe-9e6e-1d7f35d0b9d6)


Настроены Security Groups на входящий трафик только к нужным портам 

![1](https://github.com/netologygit/netology/assets/123411071/79885033-767a-4c4f-adee-569a9d1bd4ac)

![1](https://github.com/netologygit/netology/assets/123411071/9094433f-749a-4be2-8cae-1cdf6890e787)

ВМ 192.168.2.29 реализует концепцию bastion host

![1](https://github.com/netologygit/netology/assets/123411071/89078f20-3b54-4ff7-9bad-baf24355e0ca)


Созданы снимки дисков всех ВМ

![1](https://github.com/netologygit/netology/assets/123411071/b802130c-630c-4521-9a76-ab817fa694a9)


![snapshots](https://github.com/netologygit/netology/assets/123411071/24d2bc53-6378-479d-b59b-d21928705448)











