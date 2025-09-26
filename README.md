# intel-image-classification
intel image classification

Giriş
Bu proje, intel image classification kullanılarak görüntü sınıflandırma problemi üzerinde çalışılmıştır.  
Proje, Kaggle Notebook ortamında geliştirilmiş ve public olarak paylaşılmıştır. Burada toplamda 6 sınıfla çalışılarak bir CNN tabanlı model oluşturulmuştur. Veri ön işleme adımları gerçekleştirildi. Train, val, test verileri sırasıyla yüzde 70, 14, 16 olarak belirlenmiştir. Veri seti dağılım grafikleri oluşturulmuş ve detaylı sınıf bazlı istatistikler belirlenmiştir. Her sınıf için görselleştirme yapılmıştır.

Convolutional Neural Network (CNN) mimarisi oluşturuldu.  
bu proje kapsamında öncelikle CNN tabanlı model oluşturulup aşırı öğrenme kontrol edidi. değerler sonucunda aşırı öğrenmenin önüne geçebilecek teknikler kullanılıp Geliştirilmiş CNN modeli oluşturulup karşılaştırma işlemi yapılmıştır. bu projede keras tuner  otomatik optimizasyon yöntemi kullanılmıştır.

Model

Optimizasyon için rmsprop optimizer kullanıldı.  
İki model içinde Kayıp fonksiyonu: categorical_crossentropy  
Model, belirli sayıda epoch boyunca eğitildi.

Metrikler

Temel bir CNN mimarisi tasarlanmış 
ve modelin performansı incelenmiştir. Eğitim süreci sonunda model, eğitim verisinde %83.39 doğruluk, doğrulama verisinde ise %86.97 doğruluk elde etmiştir. Loss değerleri incelendiğinde eğitim kaybı 0.8574, doğrulama kaybı ise 0.7671 olarak ölçülmüştür. Ardından, geliştirilmiş CNN mimarisi uygulanmıştır. Bu geliştirilmiş modelde dropout, batch normalization ve veri artırma (data augmentation) gibi yöntemler kullanılarak aşırı öğrenmenin önüne geçilmeye çalışılmıştır. Sonuçlar incelendiğinde eğitim doğruluğu %81.59, doğrulama doğruluğu %81.36 olarak kaydedilmiş; eğitim kaybı 0.5498, doğrulama kaybı ise 0.6103 değerinde gerçekleşmiştir. 

linkler

https://www.kaggle.com/code/gurbetbudak/intel-image-classification

https://github.com/Gurbetbdk36/intel-image-classification/blob/main/intel-image-classification.ipynb
