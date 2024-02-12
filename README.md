<img width="1376" alt="Screenshot 2024-02-12 at 17 48 30" src="https://github.com/melisacevik/AB-Testing/assets/113050206/8860a8cb-f920-4faf-a582-6c45ac985010">


# AB Testi ile Bidding Yöntemlerinin Dönüşümünün Karşılaştırılması

## İş Problemi
Facebook kısa süre önce mevcut "maximumbidding" adı verilen teklif verme türüne alternatif olarak yeni bir teklif türü olan "average bidding"’i tanıttı. blabla.com, bu yeni özelliği test etmeye karar verdi ve average bidding'in maximum bidding'den daha fazla dönüşüm getirip getirmediğini anlamak için bir A/B testi yapmak istiyor. A/B testi 1 aydır devam ediyor ve blabla.com şimdi bu A/B testinin sonuçlarını analiz etmenizi bekliyor. blabla.com için nihai başarı ölçütü Purchase'dır. Bu nedenle, istatistiksel testler için Purchase metriğine odaklanılmalıdır.

## Veri Seti Hikayesi
Bir firmanın web sitesi bilgilerini içeren bu veri setinde kullanıcıların gördükleri ve tıkladıkları reklam sayıları gibi bilgilerin yanı sıra buradan gelen kazanç bilgileri yer almaktadır. Kontrol ve Test grubu olmak üzere iki ayrı veri seti vardır. Bu veri setleri ab_testing.xlsx excel’inin ayrı sayfalarında yer almaktadır. Kontrol grubuna Maximum Bidding, test grubuna Average Bidding uygulanmıştır.

## Proje Görevleri
- **AB Testing (Bağımsız İki Örneklem T Testi)**
  1. Hipotezleri Kur
  2. Varsayım Kontrolü
     - 1. Normallik Varsayımı (Shapiro)
     - 2. Varyans Homojenliği (Levene)
  3. Hipotezin Uygulanması
     - 1. Varsayımlar sağlanıyorsa bağımsız iki örneklem t testi
     - 2. Varsayımlar sağlanmıyorsa Mann-Whitney U testi
  4. p-value değerine göre sonuçları yorumla

## Görev 1: Veriyi Hazırlama ve Analiz Etme
- Kontrol ve test grubu verilerinin okunması ve analiz edilmesi
- Veri setlerinin birleştirilmesi (Concat)

## Görev 2: A/B Testinin Hipotezinin Tanımlanması
- Hipotezin tanımlanması
- Kontrol ve test grubu için purchase (kazanç) ortalamalarının analizi

## Görev 3: Hipotez Testinin Gerçekleştirilmesi
- AB Testing (Bağımsız İki Örneklem T Testi)
- Normallik Varsayımı ve Varyans Homojenliği sonuçlarına göre uygun testin seçilmesi
- Test sonuçlarının yorumlanması

## Görev 4: Sonuçların Analizi
- Hangi testin kullanıldığının ve sebeplerinin belirtilmesi
- Elde edilen test sonuçlarına göre müşteriye tavsiyede bulunulması

## Sonuç
Maximum Bidding ve Average Bidding arasında bir fark olmadığı gözlemlenmiştir. Yani, iki teklif verme yöntemi arasında satın alma (Purchase) açısından istatistiksel olarak fark yoktur. Bu sonuçlar ile Avg. Bidding'e geçişin gerekli olmadığını düşünebilirsiniz.

## Kullanılan Teknolojiler
- Python
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scipy
  - statsmodels
