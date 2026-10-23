##Farklı sistemlerde depolama sistemleri:
-
**NTFS**: Açılımı "New Technology File System". Windows için standart dosya sistemidir. 
**ext4**: Linux dağıtımlarında varsayılan dosya sistemidir.
**APFS**: "Apple File System". Apple'ın SSD'ler içim tasarladığı sistemdir.

Bu üç sistemin özellik karşılaştırmasını bir tablo üzerinde göstereceğim.


| **Özellik** | **NTFS** | **ext4** | **APFS** |
| :---: | :---: | :---: | :---: |
| Journaling | Var | Var | Yok |
| Copy-on-write | Yok | Yok | Var |
| Snapshot | Var | Yok | Yerleşik |
| Yerleşik Şifreleme | Var | Sınırlı | Güçlü, yerleşik |
| En İyi Olduğu Ortam | Windows | Linux | Apple |

Peki bu özellikler nedir?
*Journaling* : Yazma işleminden önce yapılacak değişikliğin bir “günlüğe” yazılması. Elektrik kesilirse sistem günlüğe bakıp bozulmayı onarabilir.
*Copy-on-write* : Veriyi yerinde değiştirmek yerine yeni bir yere yazıp sonra işaretçiyi güncelleme yöntemi. Bozulma riskini azaltır ve anlık görüntü (snapshot) almayı kolaylaştırır.
*Snapshot* : Dosya sisteminin belirli bir andaki durumunun hızlı kopyası.
*Yerleşik Şifreleme* : Şifreleme özelliğinin dosya sisteminin ya da işletim sisteminin kendi içinde hazır gelmesi, ayrı bir program kurmanıza gerek kalmaması.


##Blok Yapısı Nedir?
-
Blok, veriyi diske yazarken kullandığı en küçük ayrılabilir depolama birimdir. Dosya sistemi depolamayı bayt bayt işlemek yerine sabit boyutlu bloklarla işler. Bu bloklar genelde 4KB alan kaplar. Küçük blok boyutu(1-4KB) kullanımı küçük dosyalar için avantaj sağlarken büyük dosyalarda çok fazla blok tutulmasına sebep olur. Büyük blok boyutu(32-64KB) kullanımıysa küçük dosyaların gereksiz yer kaplamasına sebep olur ama büyük dosyalar için avantajlıdır.

*ext4 sisteminde* bloklar için bir 'extent' yapısı kullanılır. Eski sistemlerde dosyanın blokları tek tek kaydedilirken extent ile x bloğundan n bloğuna kadar olan blokların bir dosyaya ait olduğu blok aralığı kaydedilir. Büyük dosyalarda kayıt sayısını azaltır.


##HDD ve SSD Çalışma Prensipleri
-
Öncelikle bu iki depolama sisteminin de kalıcı veri tuttuğunu söylemeliyim.
**HDD**
Mekanik ve manyetik bir sistemi vardır. Dönen diskler, okuma/yazma kafası, kol ve motordan oluşan bir fiziki yapıdır. Plakalar manyetik alanlara ayrılmıştır, veri yazılırken alanın manyetik yönü değiştirilir, okunurken de kafa buna göre hareket eder. Plakalar çok yüksek devirlerde döner. Bu fiziksel hareket HDD yavaşlığının temel sebebidir.

**SSD**
Elektronik ve hareketsiz bir sisteme sahip. Veri, NAND flash belleği adı verilen yarı iletken hücrelerde elektrik yükü olarak depolanır. Rastgele erişim hızı daha yüksektir. 



