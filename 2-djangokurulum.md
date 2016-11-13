# Django web framework kurulumu (Ubuntu 16.04)

##Bu kısımda ```pip``` kullanılarak ```virtualenv``` içerisine kurulum anlatılacak.

> Bu yöntem bize sanal bir Python çervresi sağlayacak ve sistemin genelini etkilemeden ayrı ayrı Python projeleri yapmamıza olanak tanıyracaktır.

1.```sudo apt-get update```

2.```sudo apt-get install python3-pip```

3.```sudo pip3 install virtualenv```

4.Şimdi proje dizininde adı ```newenv``` olan sanal ortamı oluşturalım

```mkdir ~/newproject```

```cd ~/newproject```

5.Bu kodu çalıştırınca yalnız bir şekilde çalışan Python kurmuş olduk.

```virtualenv newenv```

6.Sanal çevreyi aktif edelim

```source newenv/bin/activate```
> Eğer ```(newenv)username@hostname:~/newproject$``` şeklinde gözüküyorsa sanal çevredesin :)

7.Djangoyu kuralım (artık pip ve pip3 yazmanız artık fark etmeyecektir)

```(newenv) pip install django```

8.Kurulumu kontrol edelim

```(newenv) django-admin --version

9.Sanal çevreden ayrılmak için herhangi biryerde ```deactivate``` komutunu çalıştırmalıyız.

```(newenv) deactivate```

10.Projede terar çalışmak istediğinde, proje dizinine girip tekrar aktif etmen gerekir.

```cd ~/newproject```

```source newenv/bin/activate```




