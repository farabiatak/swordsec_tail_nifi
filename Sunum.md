# Kuyruklama Projesi -- ApacheNifi & PostgreSQL

## Projenin Amacı 
Bize verilen json dosyalarındaki user bilgilerini Http ile Json kullanarak, sunucuya taşınması gerekli. Sunucuda kuyruklama ( redis queue ) kullanılarak, postgresql veritabanına kaydetmemiz isteniyor.
Flask , postgresql, redis ve kuyruktaki işleri postgresql e kaydedecek kod için ayrı ayrı docker container ile çalışılması gerekli. Toplam 4 docker ayakta olmalı.

# Benim Projeye Yaklaşımım ve Yapabildiklerim
Öncelikle elimdeki user bilgilerini postgresql'e kuyruklama ile aktarmam gerektiğini biliyordum fakat docker ve postgreye aşina olmakla birlikte flask ve redis hiç kullanmadım .Bu sebeple bana teslim için ayrılan
süre zarfında öğrenip proje tamamlayamadım.Lakin amaçta belirtildiği gibi benden istenenin tam karşılayamasamda benzer bir proje hazırladım.

# Proje Detayları 
User bilgilerine nifi ile http ile almak istesekte başaramadık.Nifi'de bunun için prosessor olmakla birlikte kurulumunu yapamadık.Bu sebeple user bilgilerini locale indirip DB'ye nifi üzerinden kuyruklama ile docker compose ile aktardık.
Verileri once bilgisayara,ardından nifinin konteynırına sonra postgreye aktardık.Nifi prosesörleride fazla ayarlama olduğu için README dosyasında tüm detaylar aktarılacaktır. 
