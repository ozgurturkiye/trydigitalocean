# Digital Ocean ilk ubuntu kurulumu sonrası yapılanlar
### root parola değiştirme, yeni kullanıcı ekleme, kullanıcı yetkilerini düzenleme


1.İlk olarak ssh ile suncumuza bağlanıyor ve root parolasını değiştiriyoruz.
```
ssh root@ipadresi
```
2.Şimdi sistemde yeni kullanıcılar oluşturalım
```
 # adduser newuser
```
3.(root) ```sudo```  yetkilerini kullanabilecek kullanıcıları belirleyelim
```
usermod -aG sudo newuser
```
Burada -aG seçeneği ```usermod``` komutuna kullanıcıyı sudo grubuna eklemesini sağlar
