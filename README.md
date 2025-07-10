# Proje 1: Insertion Sort

### Dizi

[22, 27, 16, 2, 18, 6]

### Insertion Sort Aşamalara Göre Sıralama

> Insertion Sort, diziyi adım adım sıralı bir hale getirir. Her adımda, sıralı olmayan kısımdan bir eleman alınır ve sıralı kısmın doğru yerine yerleştirilir.

#### Başlangıç Durumu:

[22, 27, 16, 2, 18, 6]

#### Adım 1 (Eleman: 22)
İlk eleman zaten sıralı kabul edilir.  
[22 | 27, 16, 2, 18, 6]

#### Adım 2 (Eleman: 27)
27 > 22 olduğu için yer değiştirmez.  
[22, 27 | 16, 2, 18, 6]

#### Adım 3 (Eleman: 16)
16 < 27 → 27 sağa kayar  
16 < 22 → 22 sağa kayar  
16 kendi yerine yerleşir.  
[16, 22, 27 | 2, 18, 6]

#### Adım 4 (Eleman: 2)
2 < 27 → 27 sağa  
2 < 22 → 22 sağa  
2 < 16 → 16 sağa  
2 yerine yerleşir.  
[2, 16, 22, 27 | 18, 6]

#### Adım 5 (Eleman: 18)
18 < 27 → 27 sağa  
18 < 22 → 22 sağa  
18 > 16 → 18 kendi yerine yerleşir.  
[2, 16, 18, 22, 27 | 6]

#### Adım 6 (Eleman: 6)
6 < 27 → 27 sağa  
6 < 22 → 22 sağa  
6 < 18 → 18 sağa  
6 < 16 → 16 sağa  
6 > 2 → 6 kendi yerine yerleşir.  
[2, 6, 16, 18, 22, 27]

---

### Big-O Gösterimi

- **En İyi Durum (Best Case):** Dizi zaten sıralıysa, her eleman sadece bir karşılaştırma yapar → O(n)
- **Ortalama Durum (Average Case):** Genellikle O(n²)
- **En Kötü Durum (Worst Case):** Dizi ters sıralıysa, her eleman için en fazla karşılaştırma ve kaydırma yapılır → O(n²)

---

### Time Complexity: 18 Sayısı Hangi Duruma Girer?

Dizi sıralandıktan sonraki hali:  
[2, 6, 16, 18, 22, 27]

18 sayısını doğrusal arama (linear search) ile ararsak:

- 1. eleman → 2  
- 2. eleman → 6  
- 3. eleman → 16  
- 4. eleman → 18 → Bulundu

18 dizinin ne en başında ne de en sonunda olduğundan **Average Case** kapsamına girer.

---

## Selection Sort

### Dizi

[7, 3, 5, 8, 2, 9, 4, 15, 6]

### Selection Sort'a Göre İlk 4 Adım

> Selection Sort, her adımda sıralı olmayan kısımdaki en küçük elemanı bulur ve onu sıralı kısmın sonuna (yani doğru pozisyonuna) yerleştirir.

#### Başlangıç Durumu:

[7, 3, 5, 8, 2, 9, 4, 15, 6]

#### Adım 1
En küçük eleman: 2  
2 ile ilk eleman olan 7 yer değiştirir.  
[2, 3, 5, 8, 7, 9, 4, 15, 6] (Sıralı kısım: [2])

#### Adım 2
Sıralı olmayan kısım: [3, 5, 8, 7, 9, 4, 15, 6]  
En küçük eleman: 3  
3 ile 3 yer değiştirir.  
[2, 3, 5, 8, 7, 9, 4, 15, 6] (Sıralı kısım: [2, 3])

#### Adım 3
Sıralı olmayan kısım: [5, 8, 7, 9, 4, 15, 6]  
En küçük eleman: 4  
4 ile 5 yer değiştirir.  
[2, 3, 4, 8, 7, 9, 5, 15, 6] (Sıralı kısım: [2, 3, 4])

#### Adım 4
Sıralı olmayan kısım: [8, 7, 9, 5, 15, 6]  
En küçük eleman: 5  
5 ile 8 yer değiştirir.  
[2, 3, 4, 5, 7, 9, 8, 15, 6] (Sıralı kısım: [2, 3, 4, 5])


