# YOLOv5

- YOLO konvolüsyonel sinir ağları kullanarak nesne tespiti yapan bir algoritmadır. Açılımı ‘’You Only Look Once’’ demektir.
- Sebebi ise algoritmanın nesne tespitini oldukça hızlı bir şekilde ve tek seferde yapabiliyor olmasıdır.
- YOLO algoritmasının diğer algoritmalardan daha hızlı olmasının sebebi resmin tamamını tek seferde nöral bir ağdan geçiriyor olmasıdır.
- YOLO algoritması görüntüler üzerinde tespit ettiği nesnelerin çevresini bounding box ile çevreler.
- YOLO kendisine girdi olarak verilen görüntüyü NxN’lik ızgaralara böler.
- Her ızgara kendi içerisinde nesne olup olmadığını ve nesne var olduğunu düşünüyorsa merkez noktasının kendi alanında olup olmadığını düşünür.
- Nesnenin merkez noktasına sahip olduğuna karar veren ızgara o nesnenin sınıfını, yüksekliğini ve genişliğini bulup o nesnenin çevresine bounding box çizmelidir.

## Nasıl çalışır?
Her bir ızgara kendi içinde, alanda nesnenin olup olmadığını, varsa orta noktasının içinde olup olmadığını, orta noktası da içindeyse uzunluğunu, yüksekliğini ve hangi sınıftan olduğunu bulmakla sorumlu. Daha açık anlatmak gerekirse örneğin yukarıdaki resimde arabanın orta noktası 7. ızgaraya denk geldiği için arabanın tespit edilmesinden/etrafına kutucuk çizmesinden o ızgara sorumlu.

![1_07b0zWzUFT8nYOEW2P23wg](https://user-images.githubusercontent.com/59111328/137702607-bc092fd7-7a62-4a99-a826-c8c6b22d9590.png)

Buna göre YOLO her ızgara için ayrı bir tahmin vektörü oluşturur.

Bunların her birinin içinde:

**Güven skoru:** Bu skor modelin geçerli ızgara içinde nesne bulunup bulunmadığından ne kadar emin olduğunu gösterir. (0 ise kesinlikle yok 1 ise kesinlikle var) Eğer nesne olduğunu düşünürse de bu nesnenin gerçekten o nesne olup olmadığından ve etrafındaki kutunun koordinatlarından ne kadar emin olduğunu gösterir.
**Bx:** Nesnenin orta noktasının x koordinatı
**By:** Nesnenin orta noktasının y koordinatı
**Bw:** Nesnenin genişliği
**Bh:** Nesnenin yüksekliği
**Bağlı Sınıf Olasılığı:** Modelimizde kaç farklı sınıf varsa o kadar sayıda tahmin değeri. **Örn;**
Yukarıdaki resimde Grid 7’ ye baktığımızda eğer araba olduğundan kesin olarak eminse:
**Araba:** 1, Yaya: 0 olacaktır.

