# PyTorch Kurulumu

- Bu kurulumu Cuda ve CuDNN kurulumlarının başarılı olup olmadığını kontrol etmek amacıyla yapıyoruz. Öncelikle [buradaki](https://pytorch.org/get-started/locally/) adrese gidiyoruz ve bize uygun olan seçenekleri seçerek ilerliyoruz.

![1](https://user-images.githubusercontent.com/59111328/137587205-dc1b60d1-8919-4559-9f96-d1eda447ffb2.PNG)

- Yukarıda çıkan komutu **Anaconda prompt(miniconda3)** ekranına giriyoruz ve inmesini bekliyoruz. Karşımıza çıkan ekrana **y** yazıp devam ediyoruz.

![2](https://user-images.githubusercontent.com/59111328/137587367-0b7edc9f-1e1d-41aa-aaaf-d465d81764f0.PNG)

- İndikten sonra komut ekranına ```python``` yazarak devam ediyoruz. Sırasıyla aşağıdaki komutları girdikten sonra resimde görünen çıktıları inceliyoruz. Kurulumun düzgün olduğunu çıktılardan anlayabiliriz.

```
import torch

torch.cuda.current_device()

torch.cuda.device(0)

torch.cuda.device_count()

torch.cuda.get_device_name(0)

torch.cuda.is_available()
```

![3](https://user-images.githubusercontent.com/59111328/137587572-37d2cfc6-7048-4706-af0d-db104a9623c7.PNG)



