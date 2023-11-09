# Detaylar
>docker cp ile localdeki user bilgilerini nifi bash'te oluşturuduğunuz klasöre aktarın.(not:bash'açılan dosya dizininin arkasında klasör veya dosya aktarmayın.Getfile prosesörü çalışmaz.)
>postgrede verilierimizin tipine göre bir tablo yaratıyoruz.

>Flowu bu şekilde tasarladık.
<img src="https://github.com/farabiatak/swordsec_tail_nifi/blob/main/nifi-ayarlar-1/Screenshot%20(222).png" width="auto">
## GETFILE

Getfile ayarları Sheduling Kısmında -Run shedule kısmını dosyalarımızın hedef dizininden ne sıklıkla çekilmesini ayarlıyoruz.Burada database'ye eğer elimizde olan 10 user dosyasındaki 10000 kişilik bilgiyi istersek 10 dakikada veya
10 saniyede aktarabiliriz.Ben 10 saniyeyi tercih ettim bu da verilerimizin 100 saniyede database'e aktarılacağı anlamına gelir.Güvenlik protokolüne göre geliştirici istediği zaman istediği gibi ayarlayabilir.Dosyaları kendi aralarında
kuyruklayabilmekle beraber tek dosyayı içindeki 1000 kişilik veriyi kuyruklayamadım.Kafka veya TailFile bu sorunuda aşmaya çalışacağım.

<img src="https://github.com/farabiatak/swordsec_tail_nifi/blob/main/nifi-ayarlar-1/Screenshot%20(224).png" width="auto">

##ConvertToJson
Burada resimlerdeki ayarlamalar yapıldıktan sonra table_name kısmına potgrede oluşturdugumuz tablonun ismini veriyoruz.Ardından Connection Poolda olan oka tıklayıp ,karşımıza çıkan panelde sağdaki ayarlar paneline tıklıyoruz.
Çıkan panele yapılacak ayarlamalar resimde var.Onun dışında bilmeniz gerekenler ; postgre driveri indirmelisiniz.42.5.1 versiyonu gayet stabil sorun çıkarmıyor.ardından bunu nifi bashte bir dosyaya koyup olduğu yerin konumunu ayarlarda belirtilen location kısmına kopyalamalısınız.user ve password bilgileri .yaml dosyasında var oradan bakabilirsiniz.düzenleme bittikten sonra enable yapmayı unutmayınız.

<img src="https://github.com/farabiatak/swordsec_tail_nifi/blob/main/nifi-ayarlar-1/Screenshot%20(215).png" width="auto">
<img src="https://github.com/farabiatak/swordsec_tail_nifi/blob/main/nifi-ayarlar-1/Screenshot%20(216).png" width="auto">
<img src="https://github.com/farabiatak/swordsec_tail_nifi/blob/main/nifi-ayarlar-1/Screenshot%20(217).png" width="auto">

##PUTSQL
<img src="https://github.com/farabiatak/swordsec_tail_nifi/blob/main/nifi-ayarlar-1/Screenshot%20(218).png" width="auto">
<img src="https://github.com/farabiatak/swordsec_tail_nifi/blob/main/nifi-ayarlar-1/Screenshot%20(219).png" width="auto">







