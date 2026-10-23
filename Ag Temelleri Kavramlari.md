*IP-Port-DNS-TCP-UDP Nedir?*
-
**IP(Internet Protocol)** : İnternet veya bilgisayar ağındaki cihazların birbirini tanımasını, veri aktarımı yapmasını sağlayan kurallardır. Buradan başka bir kavrama daha geçiyoruz.
**IP Adresi** : Bu protokole bağlı olarak cihazlara verilen kimlik numarasıdır. Verinin doğru alıcıya ulaşmasını sağlar ; posta koduna benzetilebilir.

**Port** : Bilgisayar ağlarında ve internette veri paketlerinin bilgisayara veya sunucuya girip çıkarken kullandığı kapılardır. 

**DNS(Domain Name System)** : "google.com" gibi basit alan adreslerini bilgisayarın anlayabileceği IP adreslerine dönüştürür.

**TCP(Transmission Control Protocol)** : İnternet üzerinde veri paketlerinin bir bilgisayardan diğerine hatasız, eksiksiz ve doğru sırayla gönderilmesini sağlayan en temel kurallar bütünüdür. Verilerin güvenli şekilde paylaşılmasını garanti altına alır.Yavaş ama güvenilirdir. TCP'nin en büyük alternatifi UDP'dir.

**UDP(User Datagram Protocol)** : TCP'nin aksine hız odaklıdır. Küçük veri kayıplarının önemsenmediği hızın ön planda olduğu yerlerde tercih edilir. DNS de UDP protokolünü kullanır. Rekabetçi oyunlarda, platform canlı yayınlarında da tercih edilir.

*Paket Yapısı Nasıl Çalışır?*
-
 Gönderilen veriler tek parça yerine paketlere bölünerek taşınır. Bir ağ paketinin yapısı üç ana yapıdan oluşur. Üstbilgi kısmında; kaynak ve hedef IP, port numalaraları, paket numarası. Veri kısmında; taşınan verinin bir parçası. Altbilgi kısmında; hata kontrolü yer alır. 
 Paketlerin yolculuğundan bahsedecek olursak: Kapsülleme, yolculuk, kapsülü açma aşamalarından geçer. *Kapsülleme* aşamasında veri küçük parçalara bölünür. TCP veya UDP protokolüyle üstbilgi eklenir. Ardından IP protokolü kendi üstbilgisini ekler. *Yolculuk* aşamasında paketler internete salınır, tüm paketler aynı yolu izlemek zorunda değildir. Yoğunluğa göre belirlenir. *Kapsül açma* aşamasında tüm paketler hedef cihaza ulaştığında altbilgiler kontrol edilir, üstbilgiler (IP ve Port etiketleri) sökülüp atılır. Paketler sıra numaralarına göre dizilerek orijinal büyük veri eksiksiz şekilde ekranda gösterilir.

 *Ping, traceroute, nslookup ne işe yarar?*
 -
  Bilgisayar ağlarında ve internette yaşanan sorunları test etmek, bağlantıları test etmek ve bilgi toplamak için kullanılan temel ağ tanılama komutlarıdır. 
*ping* : Hedef cihazın açık olup olmadığını ve hızını test ölçer.
*traceroute* : Verinin hedefe ulaşırken hangi yollardan geçtiğini gösterir.
*nslookup* : Bir alan adının arkasındaki IP adresini sorgular.


 
 
