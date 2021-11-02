# YOLOv5 Örnek

Bu örnekte [burada](https://github.com/ultralytics/yolov5) bulunan YOLO'nun hazır modellerden kullanacağız. Bunu için Jupyter-Lab'a giriyoruz ve bir .py dosyası açıyoruz. İçine aşağıdaki kodu yazıyoruz.

```
import torch

# Modeli seçiyoruz.
model = torch.hub.load('ultralytics/yolov5', 'yolov5s')  # or yolov5m, yolov5l, yolov5x, custom

# Resmi seçiyoruz.
img = 'https://ultralytics.com/images/zidane.jpg'  # or file, Path, PIL, OpenCV, numpy, list

results = model(img)

# Sonucu görüntülüyoruz.
results.print()
```

Dosyayı kaydediyoruz ve bu dosyayı çalıştırmak yeni bir terminal açıyoruz. 

![+](https://user-images.githubusercontent.com/59111328/139831253-7010c120-7631-4e17-88dc-78a54619d641.PNG)
<br>
![seç](https://user-images.githubusercontent.com/59111328/139831352-9c8be50f-72ef-469f-8742-8a7bf2cc7f66.PNG)
<br>

Açılan terminalde .py uzantılı dosyamızın konumuna gidiyoruz. 

![git](https://user-images.githubusercontent.com/59111328/139831679-c2f219f3-bb8c-415c-a312-1c92d428341c.PNG)

Dosyayı çalıştırıyoruz ve sonuç karşımıza çıkıyor. 2 adam ve bir kravat olarak çıktı alıyoruz.

![sonuc](https://user-images.githubusercontent.com/59111328/139831803-11c9ea50-c1ec-409a-8e62-3cdcb2ead4a9.PNG)






