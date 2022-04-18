# mipt-databases-2022-sbt_HW_3
#*Домашняя работа №3. Redis*


0.  Для начала мы установили Redis и Redisinsight, последний понадобится для визуализации нашей работы. 


  ![image](https://user-images.githubusercontent.com/58188954/163783945-640c62ea-511c-4536-a3b5-0518f7f4fd7c.png)
  
  Как хорошо видно, redis мы смогли установить. Также можем установить redisinsight( хотя все команды можно делать в терминале, но более удобно их смотреть в Redisinsight)


![image](https://user-images.githubusercontent.com/58188954/163784210-9a0ca602-597a-4bf6-98a5-3309f80aa118.png)


**Приступаем к самому заданию**
1. Сохранить большой JSON (~20МБ) в виде разных структур - строка, hset, zset, list;
Вот тут мы можем скачать уже готовый JSON или же быстро сгенерировать на Python. Выбиру второй вариант, но вернусь к этому пункту немного попозже, буду его делать перед каждым замером, так как генерация происходит очень быстро. 

Также вспомним, что 20 мб это 20971520 байт

2. Изначально я хотел использовать ![image](https://user-images.githubusercontent.com/58188954/163844629-9d821dff-2893-473c-b5e2-39a94c559bba.png)
, но из-за проблем с установкой нужных пакетов я решил сделать дз с помощью Python в Jupyter

![image](https://user-images.githubusercontent.com/58188954/163847354-45307bc7-cb2c-4804-9ca2-0c8dac3ec902.png)

![image](https://user-images.githubusercontent.com/58188954/163847426-d7f51255-368c-47b7-a3b0-c0ee4b0feb6a.png)


1)Сначала разберемся со строками. Сначала мы ее генерим, а затем 500 раз записываем в нашу базу данных, а потом 500 раз считываем, в итоге получаем вот такие результаты


![изображение](https://user-images.githubusercontent.com/58188954/163860870-004d8606-e64e-4fb2-b6f8-ead05fa22e63.png)


2) Вот со списком уже более сложно, мы можем делать вставку lpush, rpush.

Сгенерировали данные нужного размера![изображение](https://user-images.githubusercontent.com/58188954/163862174-352c37f4-cd63-41a1-b158-0c018441dd63.png)


**lpush**
![изображение](https://user-images.githubusercontent.com/58188954/163862501-63200152-41cf-42e5-b892-9a6d2a1fd09d.png)


**rpush**
![изображение](https://user-images.githubusercontent.com/58188954/163862739-625ca424-c0e3-4289-ba3f-1a88d44d7143.png)



**get**
![изображение](https://user-images.githubusercontent.com/58188954/163862832-431f9af2-6323-4ea6-849e-8fef0dbdcd1f.png)



3) hset

Создали dict, который будем вставлять в нашу структуру в базе данных уже

Протестируем запись нашего словаря


![изображение](https://user-images.githubusercontent.com/58188954/163865638-9c77af41-c280-40c0-8c7e-e9d5d953f327.png)


Чтение:


![изображение](https://user-images.githubusercontent.com/58188954/163865700-0bdc50f2-dd5a-4f1a-a040-c618a87b29d1.png)





