# MetroSimulation
Metro istasyonları arasında en kısa ve en hızlı rotaları bulan simülasyon projesi
# Metro Simülasyonu Projesi

Bu proje, bir metro ağındaki istasyonlar arasında en az aktarmalı ve en hızlı rotaları bulmak için geliştirilmiş bir simülasyondur. Proje, BFS (Breadth-First Search) ve A* algoritmalarını kullanarak rotaları hesaplar.

## Kullanılan Teknolojiler ve Kütüphaneler

- **`collections`**: `deque` yapısı için kullanıldı.
- **`heapq`**: A* algoritmasında öncelik kuyruğu oluşturmak için kullanıldı.
- **`typing`**: Tür ipuçları (type hints) eklemek için kullanıldı.

## Algoritmaların Çalışma Mantığı

### 1. BFS (Breadth-First Search) Algoritması
- En az aktarmalı rotayı bulmak için kullanılır.
- Başlangıç istasyonundan başlar ve tüm komşu istasyonları keşfeder.
- Hedef istasyona ulaşana kadar bu işlemi tekrarlar.

### 2. A* Algoritması
- En hızlı rotayı bulmak için kullanılır.
- Her adımda, mevcut maliyet ve tahmini maliyet toplamını hesaplar.
- En düşük maliyetli rotayı seçer.

## Örnek Kullanım ve Test Sonuçları

### Senaryo 1: AŞTİ'den OSB'ye
- **En Az Aktarmalı Rota**: AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB
- **En Hızlı Rota (23 dakika)**: AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB

### Senaryo 2: Batıkent'ten Keçiören'e
- **En Az Aktarmalı Rota**: Batıkent -> Demetevler -> Gar -> Keçiören
- **En Hızlı Rota (21 dakika)**: Batıkent -> Demetevler -> Gar -> Keçiören

### Senaryo 3: Keçiören'den AŞTİ'ye
- **En Az Aktarmalı Rota**: Keçiören -> Gar -> Sıhhiye -> Kızılay -> AŞTİ
- **En Hızlı Rota (14 dakika)**: Keçiören -> Gar -> Sıhhiye -> Kızılay -> AŞTİ

### Senaryo 4: Kızılay'dan Keçiören'e
- **En Az Aktarmalı Rota**: Kızılay -> Ulus -> Demetevler -> Gar -> Keçiören
- **En Hızlı Rota (20 dakika)**: Kızılay -> Ulus -> Demetevler -> Gar -> Keçiören

## Projeyi Geliştirme Fikirleri

1. **Grafiksel Arayüz Eklemek**: Kullanıcılar, başlangıç ve hedef istasyonları seçebilir ve rotaları görsel olarak görebilir.
2. **Fiyatlandırma Eklemek**: Kullanıcılar, seçtikleri rotanın güncel tutarını görebilir.
3. **Çoklu Dil Desteği**: İngilizce, Türkçe gibi çoklu dil desteği eklenebilir.
