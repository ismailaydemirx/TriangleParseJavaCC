# TriangleParseJavaCC
 KTÜ Derleyici Tasarımı Dersi Üçgen Açılarının Java CC ile çözüm yöntemleri projesi

# Derleyici Tasarımı: Üçgen Problemleri Çözümleri

Bu proje, üçgen problemlerin belirli durumlarını (SSS, SAS, ASA, AAS) analiz edip çözebilen bir derleyici örneği geliştirmeyi amaçlamaktadır. Projede, üçgenin kenar ve açı bilgilerine göre kesin çözümler üretmek için matematiksel yöntemler (kosinüs teoremi, sinüs teoremi, açı toplamı kuralı ve temel trigonometrik oranlar) kullanılmaktadır. Derleyici, JavaCC kullanılarak oluşturulmuştur.

## Özellikler

- **SSS (Üç Kenar Verilmiş):** Üç kenar bilgisi girildiğinde, kosinüs teoremi ile üçgenin açıları hesaplanır.
- **SAS (İki Kenar ve Aradaki Açı):** İki kenar ve aralarındaki açı verildiğinde, üçüncü kenar ve diğer açılar kosinüs ve sinüs teoremleriyle hesaplanır.
- **ASA (İki Açı ve Aradaki Kenar):** İki açı ve bu açıların arasında bulunan kenar bilgisi kullanılarak, üçüncü açı ve diğer kenarlar bulunur.
- **AAS (İki Açı ve Bir Kenar):** Verilen iki açı ve bir kenar üzerinden, eksik açı ve kenarlar sinüs teoremi yardımıyla hesaplanır.
- Kullanıcı girişi, `Triangle <Tip> (param1, param2, param3)` şeklinde tanımlanmıştır.  
  Örneğin:
  - `Triangle SSS (5,6,7)`
  - `Triangle SAS (5,60,7)`
  - `Triangle ASA (60,5,70)`
  - `Triangle AAS (60,70,5)`

## Proje Yapısı

- **TriangleParser.jj:** JavaCC tanım dosyası. Lexical ve syntactic analiz kuralları, ayrıca ilgili matematiksel hesaplamaları içeren semantic işlemler burada tanımlanmıştır.
- **README.md:** Proje hakkında genel bilgiler, kullanım ve derleme yönergeleri.
- **(Opsiyonel) Diğer dokümantasyon dosyaları:** Kullanım örnekleri, test senaryoları vs.

## Kullanım

### Gereksinimler

- Java Development Kit (JDK) 8 veya üstü
- [JavaCC](https://javacc.org/) (Java Compiler Compiler)

### Derleme ve Çalıştırma

1. **JavaCC Kurulumu:**
   - JavaCC'yi [resmi sitesinden](https://javacc.org/) indirin ve kurulum talimatlarını izleyin.
  
2. **Parser Dosyasını Derleyin:**
   ```bash
   javacc TriangleParser.jj
   javac TriangleParser.java
