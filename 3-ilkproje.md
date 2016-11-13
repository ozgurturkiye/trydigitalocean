#Bu kısımda basit bir proje oluşturma anlatılacak.

###Sistemde virtualenv üzerinde django kurulu olduğunu varsayıyoruz :)

1.```(newenv) username@host:~/newproject$``` proje dizini içinde sanal ortamı aktif ettikten sonra aşağıdaki komutu veriyoruz.
Burada ```mysite```tan sonra bir boşluk ve ```.``` ya dikkat

```django-admin startproject mysite .```

2.Setting dosyasında birkaç ekleme yapalım(daha sonra tam olarak ne işe yaradığı anlatılacak)

```nano mysite/settings.py```

Dosyanın en altına aşağıdaki satırı ekleyelim

```STATIC_ROOT = os.path.join(BASE_DIR, 'static')```

request.py dosyasını açıp 100 numaralı satırada bulunan allowed_host = ['localhost', 'IP adresimiz'] listesine sitemizi ip adersini ekleyelim ki siteye ulaşabilsinler

```nano /home/USERNAME/newproject/newenv/lib/python3.5/site-packages/django/http/request.py```

3.Veritabanını oluşturmak için aşağıdaki komutu verelim()

```python3 manage.py migrate```

4.Firewall da 8000 nolu portu açalım(UFW)

```sudo ufw allow 8000```

5.Web sunucuyu çalıştıralım

```python3 manage.py runserver 0.0.0.0:8000```

6.Sayfamızı ziyaret edebiliriz. IP adresimizden sonra port :8000 numarasınız yazıyoruz.

``` server_ip_address:8000 ```

7.Admin paneline ulaşmak için server_ip_address:/admin yazmanız yeterli

``` server_ip_address:8000/admin ```

