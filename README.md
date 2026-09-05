# Optimization for Data Science — Homework 2

İTÜ YZV202E (Optimization for Data Science) dersi kapsamında hazırlanmış, üç bağımsız optimizasyon problemini kapsayan bir ödev. Her problemde standart kütüphane fonksiyonları (`scipy.optimize` vb.) yerine algoritmalar **sıfırdan** implemente edilmiş ve karşılaştırmalı olarak analiz edilmiştir.

## İçerik

### Soru 1 — Elips Uydurma (Nonlinear Least Squares)
200 veri noktasına (`data.txt`) 5 parametreli bir elips modeli (merkez, yarı-eksenler, dönüş açısı) uydurma problemi.
- Jacobian matrisi elle türetildi.
- **Gauss-Newton** ve **Levenberg-Marquardt** algoritmaları sıfırdan yazıldı.
- Yakınsama hızı ve koşul sayısı (condition number) üzerinden karşılaştırmalı analiz.

### Soru 2 — Dolphin Fonksiyonu (Global Optimizasyon)
Çok sayıda yerel minimuma sahip, öğrenci numarasına göre parametrelenmiş bir hedef fonksiyonun global minimumunu bulma problemi.
- **Particle Swarm Optimization (PSO)** ve **Genetik Algoritma** sıfırdan yazıldı.
- 25 bağımsız denemeyle istatistiksel karşılaştırma (başarı oranı, ortalama/std sapma).
- Gürültülü fonksiyon versiyonunda sağlamlık testi.
- Farklı değerlendirme bütçeleri (750/1000/1500) altında performans karşılaştırması.
- Rastgele alt-bölgelerde global minimumu bulma başarısı.

### Soru 3 — Beale Fonksiyonu (Gradyan Tabanlı Optimizasyon)
- **Fletcher-Reeves (Conjugate Gradient)** ve **Newton's Method** sıfırdan yazıldı, backtracking line search ile.
- 3 farklı başlangıç noktasından (minimuma yakın / uzak / tekil Hessian) yakınsama davranışı karşılaştırması.
- Hessian koşul sayısının optimizasyon yolu boyunca değişiminin analizi.

## Dosyalar

| Dosya | Açıklama |
|---|---|
| `hw2.ipynb` | Ana çalışma — tüm kod, görselleştirmeler ve yazılı analiz |
| `data.txt` | Soru 1 için elips veri noktaları (200 nokta) |
| `hw2.pdf` | Not defterinin PDF çıktısı (teslim kaydı) |
| `Optimization_2025_2026_HW2.pdf` | Ödevin orijinal soru kağıdı |

## Kullanılan Araçlar

Python — NumPy, Matplotlib. (Bilinçli olarak `scipy.optimize` gibi hazır optimizasyon kütüphaneleri kullanılmadı; amaç algoritmaların kendisini uygulamaktı.)
