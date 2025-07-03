Bu projenin temel amacı, görüntü tabanlı yaş grubu sınıflandırması yapan bir yapay zeka modelinin geliştirilmesi
ve bu modelin hem mobil cihazlarda çalışan uygulamalara hem de otomat sistemleri ve web tabanlı platformlara
dahil edilebilecek şekilde tasarlanarak yaş kısıtlaması gerektiren içeriklerin erişimini denetleyen işlevsel bir sistem
haline getirilmesidir. Böylece farklı yaş gruplarına uygun dijital deneyimlerin sağlanması ve etik dijital tüketim
alışkanlıklarının desteklenmesi hedeflenmektedir.
Projede ilk aşamada, etiketlenmiş görüntü veri setleri toplanarak bireyler yaş gruplarına göre sınıflandırılacaktır.
Bu kapsamda iki farklı yaş grubu sınıflandırma yapısının oluşturulması planlanmaktadır: biri üçlü (genç, yetişkin,
yaşlı), diğeri ise dörtlü (genç, yetişkin_1, yetişkin_2, yaşlı) yaş grubu ayrımı içerecektir. Toplanan veri seti
üzerinde toplamda 10 farklı derin öğrenme modelinin eğitilmesi hedeflenmektedir. Bu modellerin altısının sıfırdan
tasarlanmış özgün evrişimsel sinir ağı ( Convolutional Neural Network - CNN ) mimarilerine, dördünün ise transfer
öğrenme (transfer learning) yaklaşımına dayalı olması öngörülmektedir.
Model geliştirme sürecinde, önce özgün CNN mimarileri tasarlanacak; çeşitli katman sayısı, filtre boyutu,
aktivasyon fonksiyonu ve havuzlama stratejileri gibi hiper parametreler denenerek en uygun yapı belirlenecektir.
Aşırı öğrenme (overfitting) riskini azaltmak amacıyla dropout, toplu normalizasyon (batch normalization) ve erken
durdurma (early stopping) gibi düzenleme teknikleri uygulanacaktır.
Transfer öğrenme yaklaşımı kapsamında, ImageNet veri kümesi üzerinde önceden eğitilmiş olan MobileNetV2,
NASNetMobile ve ResNet gibi modern ve derin mimariler kullanılacaktır. Bu modellerin son katmanları çıkarılarak
yerine, yaş gruplarına uygun sınıflandırıcı katmanlar (dense layer) eklenecek ve modeller yalnızca bu yeni
katmanlar üzerinden yeniden eğitilecektir.
Tüm modeller eğitim sonrası test seti üzerinde karşılaştırılacak ve doğruluk + F1-score oranları temel alınarak en
iyi performanslı model belirlenecektir.
