<div align="center">

# Standart Sapma Hesaplama

### Sayıların dağılımını birkaç adımda keşfet.

![C#](https://img.shields.io/badge/C%23-2563eb?style=for-the-badge)
![.NET Framework](https://img.shields.io/badge/.NET%20Framework-0891b2?style=for-the-badge)
[![MIT](https://img.shields.io/badge/MIT-16a34a?style=for-the-badge)](LICENSE)

Bir sayı dizisinin standart sapmasını döngülerle hesaplayan konsol uygulaması. Depo adına rağmen hesaplama iteratif yöntem kullanır.

**İteratif istatistiksel hesaplama**

[Projeyi keşfet](https://github.com/silanpehlivan/RecursiveY-ntemi/tree/master) · [Kurulum ve ayrıntılar](#projeyi-çalıştırmak-ve-incelemek)

</div>

---

## İçeride neler var?

- **01** · Ortalama, varyans ve standart sapma hesabı
- **02** · Konsol üzerinden veri girişi
- **03** · Döngü tabanlı matematiksel işlemler

## Projeyi çalıştırmak ve incelemek

<details>
<summary><strong>Kurulum, kod yapısı ve teknik notları aç</strong></summary>

## Öne Çıkanlar

- Ortalama, varyans ve standart sapma hesabı
- Konsol üzerinden veri girişi
- Döngü tabanlı matematiksel işlemler

## Teknolojiler

C# · .NET Framework

### Teknik yaklaşım

Ortalama hesaplandıktan sonra değerlerin ortalamadan farklarının kareleri biriktirilir; varyans üzerinden standart sapma elde edilir.

### Kodu incelemeye başlayın

- [Program.cs](Program.cs)

### Kapsam ve sınırlar

Depo adındaki recursive ifadesine rağmen mevcut örnek döngü tabanlıdır; özyineleme uygulaması olarak sunulmaz.



Bu proje, bir sayı dizisinin standart sapmasını iteratif (döngüsel) yöntemle hesaplayan bir C# konsol uygulamasıdır. Proje adı “Recursive Yöntemi” olsa da, uygulama özyineleme yerine döngüler kullanılarak geliştirilmiştir. Bu yaklaşım, istatistiksel hesaplamaların temel mantığını programlama ile göstermeyi amaçlamaktadır.

---

 Projenin Amacı
---

Bu projenin temel amacı, verilen bir sayı dizisi için standart sapma değerini adım adım iteratif bir yöntemle hesaplamaktır. Bu kapsamda:

- Standart sapma hesaplama süreci programatik olarak gösterilir  
- Döngü (iteration) yapılarının kullanımı pekiştirilir  
- Veri işleme ve matematiksel modelleme mantığı geliştirilir  
- C# konsol uygulaması geliştirme pratiği kazanılır  

---

 Standart Sapma Nedir?
---

Standart sapma, bir veri setindeki değerlerin ortalamadan ne kadar uzaklaştığını ölçen istatistiksel bir ölçüdür.

- Düşük standart sapma → Veriler ortalamaya yakındır  
- Yüksek standart sapma → Veriler daha geniş aralığa yayılmıştır  

### Hesaplama Adımları:

1. Veri setinin ortalaması hesaplanır  
2. Her değerin ortalamadan farkı alınır ve karesi hesaplanır  
3. Bu kareler toplanır  
4. Toplam değer veri sayısına bölünerek varyans bulunur  
5. Varyansın karekökü alınarak standart sapma elde edilir  

---

 Teknik Detaylar
---

| Özellik | Açıklama |
|----------|----------|
| Dil | C# |
| Platform | .NET Framework |
| Paradigma | İteratif Programlama |
| Uygulama Tipi | Konsol Uygulaması |
| IDE | Visual Studio |

---

 Implementasyon Detayları
---

Projenin ana mantığı `Program.cs` dosyasında bulunan `iterasyonlaStandartSapma(double[] x, int n)` metodunda yer almaktadır. Hesaplamalar döngüler kullanılarak gerçekleştirilmiştir.

### C# Kodu:

```csharp
static double iterasyonlaStandartSapma(double[] x, int n)
{
    // 1. Ortalama hesaplama
    double mean = 0;
    for (int i = 0; i < n; i++)
    {
        mean += x[i];
    }
    mean /= n;

    // 2. Varyans hesaplama
    double varyans = 0;
    for (int i = 0; i < n; i++)
    {
        varyans += Math.Pow(x[i] - mean, 2);
    }

    varyans /= n;

    // 3. Standart sapma
    return Math.Sqrt(varyans);
}
```

Main metodu içerisinde kullanıcıdan veri alınır ve fonksiyon çağrılarak sonuç ekrana yazdırılır.

---

 Kurulum ve Çalıştırma
---

1. Projeyi indirip klasöre çıkarın  
2. `VeriOdevi8.sln` dosyasını Visual Studio ile açın  
3. F5 tuşu ile projeyi çalıştırın  
4. Konsol ekranından veri girişi yaparak sonucu görüntüleyin  

---

 Proje Yapısı
---

```
RecursiveYontemi-master/
├── App.config
├── Program.cs
├── VeriOdevi8.csproj
├── VeriOdevi8.sln
├── Properties/
└── LICENSE
```

---




</details>

---

<div align="center">

**© 2023 Şilan PEHLİVAN**

Bu proje MIT lisansı kapsamında sunulmaktadır. Kullanım ve dağıtım koşulları: [LICENSE](LICENSE).

</div>
