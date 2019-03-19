# LİDER AHENK UYGULAMASI NASIL KURULUR

## Bağımlılıkların Kurulması

Terminali açarak aşağıdaki komutları sırasıyla yazıyoruz.

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

önce github kütüphanesini indirip yüklüyoruz.

````
git clone https://github.com/Pardus-LiderAhenk/lider-ahenk-installer.git
````

Githubdan Lider Ahenk Kurulum Uygulamasını kuruyoruz.

## Uygulamanın Çalıştırılması

Üstteki komutları yazdıktan sonra,

````
cd /lider-ahenk-instaler/src/
````

kurulum uygulmasını çalıştırmak için önce dosya dizinine gidilir.

````
python3 app.py
````
<a href = "#menü" > 
ile kurulum dosyası çalıştırılır.

##### Not : Uygulamayı çalıştırmadan önce kurulum yapılacak makinelerde ssh paketinin kurulu olduğundundan emin olunuz.

<id = "menü">
### Sekmeler

Uygulamamız solda görüldüğü gibi 4 sekmeden oluşur.

#### Ayarlar Sekmesi

Ayarlar sekmesi Standart ve Gelişmiş kurulumlardan hangisini seçiceğimizi belirlediğimiz kurulum yapılacak makinelerin bağlanmasını ve kontrolünü sağladığımız sekmedir. Ayrıca Lider Ahenk Paket Deposunu seçitiğimiz bölümdür.

##### Ana Paket Deposu : Geliştirilmelerin tamamlandığı stabil çalışan depordur.

##### Test Paket Deposu : Yeni geliştirmelerin yüklendiği depodur.

#### Lider Sekmesi

Bu sekme sunucu konfigürasyonlarının ve kurulumun başlatıldığı bölümdür.
##### Not : Burda dikkat etmemiz gereken LDAP seçeneğini eğer kurulucak sunucuda  OpenLDAP kuruluysa OpenLDAP Güncelle seçeneğini seçmeniz gerekir.

#### Ahenk Sekmesi

Ahenk sekmesinde ahenk kullanıcıların eklendiği bölümdür.

#### Log Sekmesi

Log sekmesi ise hangi dosyların kurulduğunu ve hangi komutların kullanıldığını gösteren kurulumda herhangi bir hata olursa gösteren bölümdür.

### Kurulum

Kurulum standart ve gelişmiş olarak iki şekilde gerçekleşiyor.

### Standart Kurlum

Standar kurulum Veritabanı, OpenLDAP, Xmpp ve Lideri aynı makineye kurmamızı sağlar.

![1](1.png)

Ayarlar sekmesinde ki standart seçeneğini seçiyoruz.
Sunucu ip adresi
Kullanıcı adı,
Kullanıcı parolası yazan yerlere kurulum yapılacak makinenin ip adresi kullanıcı adı ve parololarını yazmalıyız. Burda yüklenicek makinedeki sudo da yetkili kullanıcı olmasına dikkat ediyoruz.

### Gelişmiş Kurulum

Lider ahenk uygulamasının tüm bileşenlerinin farklı makinelere kurmamızı sağlar.

![2](2.png)

Ayarlar sekmesindeki gelimiş seçeneğini seçiyoruz.
Ekle butonu ile tek tek Veritabanı, OpenLDAP, XMPP, Liderin kurulacağı makinelerin ip adreslerini, sudo yetkili kullanıcı adlarını ve şifrelerini giriyoruz.


![3](3.png)

Bağlantıyı kontrol et butonuna tıkladıktan sonra bilgilendirme kutusunda onay alıyoruz eğer bir hata verirse ip adresine ve iki makinede de ssh paketitinin kurulu olduğundan emin olunuz.

![4](4.png)

Ana paket Deposunu seçiyoruz, (Yeni gelişmeleri takip etmek istiyorsanız test paket deposunu da seçebilirsiniz).
Ayarları kaydet butonuna basıp seçtiğimiz paketi onaylıyoruz.

![5](5.png)

Ayarlar sekmesinden sonra lider sekmesindeki alanları dolduruyoruz. LDAP seçeneğini makinede kuruluysa Güncelle seçeneğini seçiyoruz kurulu değilse kur seçeğini seçerek devam ediyoruz.

![6](6.png)

Anlatılan işlemleri yaptıktan sonra kuruluma başlamak için kuruluma başla butonuna tıklıyoruz.

![7](7.png)

Kurulum devam ediyor.

![8](8.png)

Kurulum bittiğinde bu bildirimi alırsınız.

![9](9.png)

Log sekmesine gelerek uygulamanın hangi kurulumları yaptığını bir hata olup olmadığını hangi komutları kullandığını kurulum sonrasında görebilirsiniz.
