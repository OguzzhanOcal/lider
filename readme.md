# LİDER AHENK UYGULAMASI NASIL KURULUR

## Bağımlılıkların Kurulması

Uçbirimde aşağıdaki komutları sırasıyla yazılır.

````
sudo apt-get install python3-yaml python3-paramiko python3-pyqt5
````

````
sudo apt-get install python3-pip
````

````
pip3 install ruamel.yaml
````

## Uygulamanın İndirilmesi

Lider Ahenk Kurulum Uygulamasını indirmek için,

````
sudo apt-get install git
````

komutu ile git paketi yüklenir.

````
git clone https://github.com/Pardus-LiderAhenk/lider-ahenk-installer.git
````

komutu ile Lider Ahenk Kurulum Uygulaması indirilir.

## Uygulamanın Çalıştırılması

Kurulum ugulamasını çalıştırmak için;

````
cd /lider-ahenk-instaler/src/
````

komutu ile src dizinine gidilir ve

````
python3 app.py
````

komutu ile kurulum uygulaması çalıştırılır.

##### Not : Uygulamayı çalıştırmadan önce lider ahenk kurulum uygulamasının çalıştırıldığı makinede ve  kurulum yapılacak makinelerde ssh paketinin kurulu olmalıdır.

## Menüler

Uygulamamız solda görüldüğü gibi 4 menüden oluşur.

### 1. Ayarlar Menüsü

Ayarlar menüsü, Lider Ahenk Sunucu Bağlantı Ayarları ve Lider Ahenk Paket Deposu Ayarlarının yapıldığı menüdür.

Lider Ahenk Sunucu Bağlantı Ayarları,
Standart Kurulum ve Gelişmiş Kurulum olmak üzere iki şekilde gerçekleşir.

**Standart Kurulum :** Lider Ahenk Bileşenlerini tek bir makineye kurmamızı sağlar. Sırasıyla; <br>
* Standart Kurulum, <br>
* Lider Ahenk Paket Deposu Ayarları,<br>
* Lider Menüsü,<br>
* Log Menüsü<br>

adımları izlenmelidir.<br>
Standart Kurulum adımları için <a href = "#standart" >**tıklayınız.**</a>

**Gelişmiş Kurulum :** Lider Ahenk Bileşenlerini ayrı makinelere kurmamızı sağlar. Sırasıyla; <br>
* Gelişmiş Kurulum, <br>
* Lider Ahenk Paket Deposu Ayarları,<br>
* Lider Menüsü,<br>
* Log Menüsü<br>

adımları izlenmelidir.<br>
Gelişmiş Kurulum adımları için <a href = "#gelismis" >**tıklayınız.**</a>

##### Not : Standart Kurulum ve Gelişmiş Kurulum 2 ayrı kurulum çeşididir. Kurulum sırasında sadece biri seçilmelidir.


##### Ana Paket Deposu : Geliştirilmelerin tamamlandığı kararlı paket deposudur.

##### Test Paket Deposu : Yeni geliştirmelerin yayınlandığı test paket deposudur.

<p id = "standart"></p>

#### 1.1. Standart Kurulum

Standart Kurulum, Lider Ahenk Sunucu bileşenlerinin (Veritabanı, OpenLDAP, XMPP, Lider) tek bir makineye kurulmasını sağlar.

Standart Kurulum için, Lider Ahenk Sunucu Bağlantı Ayarlarındaki Standart kutucuğuna tıklanır.

![1](1.png)


Lider Ahenk Sunucu Erişim Bilgileri alanında Lider Ahenk Uygulamasının kurulum yapılacağı makinenin bilgileri girilir. Sunucu adresi kurulum yapılacak makinenin ip bilgisini, kullanıcı adı ve kullanıcı parolası ise kurulum yapılacak makinede bulunan **sudo** yetkili kullanıcıyı ifade etmektedir.


![3](3.png)


**Bağlantıyı Kontrol Et** butonuna tıklanarak bağlantı durumu kontrol edilir. **Daha sonra Lider Ahenk Paket Deposu Ayarları yapılır. Bunun için <a href = "#ayarlar" >tıklayınız.** </a>

<p id = "gelismis"></p>

#### 1.2. Gelimis Kurulum

Gelişmiş kurulum Lider Ahenk Sunucu bileşenlerinin (Veritabanı, OpenLDAP, XMPP, Lider) ayrı makinelere kurulmasını sağlar.

Gelişmiş kurulum için, Lider Ahenk Sunucu Bağlantı Ayarlarındaki Gelişmiş kutucuğuna tıklanır.


![2](2.png)

Lider Ahenk Sunucu Erişim Bilgileri alanında bileşen (Veritabanı, OpenLDAP, XMPP, Lider) seçilip, ilgili bileşene ait erişim bilgileri girilir ve **Ekle** butonuna tıklanarak ilgili bileşen Lider Ahenk Sunucu Listesi alanına eklenir. Sunucu adresi kurulum yapılacak makinenin ip bilgisini, kullanıcı adı ve kullanıcı parolası ise kurulum yapılacak makinede bulunan **sudo** yetkili kullanıcıyı ifade etmektedir. **Bağlantıyı Kontrol Et** butonuna tıklanarak bağlantı durumu kontrol edilir. **Daha sonra Lider Ahenk Paket Deposu Ayarları yapılır. Bunun için <a href = "#ayarlar" >tıklayınız.** </a>

<p id = "ayarlar"></p>

#### 1.3. Lider Ahenk Paket Deposu Ayarları

Lider Ahenk Paket Deposu Ayarları, Ana Paket Deposu ve Test Paket Deposu olmak üzere 2 seçenekten oluşur.

Ana Paket Deposu geliştirmelerin tamamlandığı kararlı paket deposudur, Test Paket Deposu ise yeni geliştirmelerin yayınlandğı test paket deposudur.

![4](4.png)

Kullanılmak istenilen paket deposu seçildikten sonra **Ayarları Kaydet** butonuna tıklayarak bağlantı ayarları ve paket deposu ayarları kaydedilir. Lider Ahenk sunucu konfigürasyon ayarları için **Lider Menüsüne** geçilir.

### 2. Lider Menüsü

Lider menüsü Lider Ahenk sunucu konfigürasyonlarının yapıldığı ve kurulumun başlatıldığı bölümdür.

<br>

![6](6.png)

Sunucu konfigürasyonu için LDAP konfigürasyon bilgileri ve XMPP konfigürasyon bilgileri girilir.
LDAP İçin İşlem Seçiniz : Yeni kurulacak OpenLDAP için **OpenLDAP Kur**, kurulu OpenLDAP olması durumunda **OpenLDAP Güncelle** seçilmelidir.
LDAP Konfigürasyon Bilgilerinde yer alan;<br>
LDAP Base DN: LDAP temel düğümü,<br>
LDAP Admin Parolası: LDAP admin yönetici parolası,<br>
LDAP Config Kullanıcı Parolası: LDAP sunucu yapılandırmak için kullanılan şifre,<br>
Lider Arayüz Kullanıcı Adı: Lider arayüzü kullanacak kullanıcı adı (Lider Admini veya Sistem Yönetici), <br>
Lider Arayüz Kullanıcı Parolası: Lider arayüzü kullanacak kullanıcı parolası, <br>
XMPP Admin Kullanıcı Parolası: XMPP admin kullanıcı parolası, <br> girilir.

**Kuruluma Başla** butonuna tıklanarak kurulum başlatılır.

![7](7.png)

Kurulum devam ediyor. Kurulum Logları açılan XTerm ekranında da takip edilebilir.

![8](8.png)

Kurulum bittiğinde bu bildirim alınır.

### 2. Log Menüsü

Log Menüsüde ise kurulumda gerçekleşen komutları, bilgileri, hataların görüldüğü menüdür.

![9](9.png)

**Yenile** butonuna tıklanır kurulum hakkında bilgiler görülür.
