 ## 1) Настраиваем сервер NFS
**Установка nfs-utils**

![](https://github.com/dimkaspaun/NFS/blob/main/screen/1_1.png)
![](https://github.com/dimkaspaun/NFS/blob/main/screen/1_2.png)

**Включаем firewall и проверяем, что он работает**

![](https://github.com/dimkaspaun/NFS/blob/main/screen/1_3.png)

**разрешаем в firewall доступ к сервисам NFS**

![](https://github.com/dimkaspaun/NFS/blob/main/screen/1_4.png)

**включаем сервер NFS**

![](https://github.com/dimkaspaun/NFS/blob/main/screen/1_5.png)
![](https://github.com/dimkaspaun/NFS/blob/main/screen/1_6.png)

**создаём и настраиваем директорию, которая будет экспортирована
в будущем**

![](https://github.com/dimkaspaun/NFS/blob/main/screen/1_7.png)

**создаём в файле __/etc/exports__ структуру, которая позволит
экспортировать ранее созданную директорию**

**- экспортируем ранее созданную директорию**
**- проверяем экспортированную директорию следующейкомандой**
  
![](https://github.com/dimkaspaun/NFS/blob/main/screen/1_8.png)

## 2) Настраиваем клиент NFS

**Установка nfs-utils**

![](https://github.com/dimkaspaun/NFS/blob/main/screen/1_9.png)

**Включаем firewall и проверяем, что он работает**

![](https://github.com/dimkaspaun/NFS/blob/main/screen/1_10.png)

**добавляем в __/etc/fstab__ строку**
**и выполняем**
**заходим в директорию `/mnt/` и проверяем успешность монтирования**

**Обратите внимание на `vers=3` и `proto=udp`, что соответствует NFSv3
over UDP, как того требует задание.**

![](https://github.com/dimkaspaun/NFS/blob/main/screen/1_11.png)

## 3) Проверка работоспособности

**- заходим на сервер**

**- заходим в каталог `/srv/share/upload`**

**- создаём тестовыйфайл `touch check_file`**

**- заходим на клиент**

**- заходим в каталог `/mnt/upload`**

**- проверяем наличие ранее созданного фаила**

**- создаём тестовыйфайл `touch client_file`**

**- проверяем, что файл успешно создан**

![](https://github.com/dimkaspaun/NFS/blob/main/screen/1_12.png)
![](https://github.com/dimkaspaun/NFS/blob/main/screen/1_13.png)
![](https://github.com/dimkaspaun/NFS/blob/main/screen/1_14.png)

