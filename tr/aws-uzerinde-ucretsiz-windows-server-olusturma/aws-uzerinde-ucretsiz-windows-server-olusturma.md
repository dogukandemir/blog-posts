# AWS Üzerinde Ücretsiz Windows Server Oluşturma

Eğer AWS hesabınız yoksa önce [AWS Hesabı Oluşturma](http://dogukandemir.com/tr/aws-hesabi-olusturma/) başlıklı yazımı okuyarak hesap oluşturabilirsiniz. Hesabınızı oluşturduysanız giriş yaptıktan sonra https://console.aws.amazon.com adresine girip Services altından EC2 seçin.

![Services EC2](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/aws-uzerinde-ucretsiz-windows-server-olusturma/images/console-services-compute-ec2.png)



Create Instance bölümündeki "Launch Instance" butonuna tıklayın.

![Launch Instance](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/aws-uzerinde-ucretsiz-windows-server-olusturma/images/console-create-instance.png)



Bu adımda sunucunuzun işletim sisteminiz seçin. Bu yazımızda Windows sunucu oluşturarak devam edeceğiz. Bunun için "Microsoft Windows Server 2016 Base" yanındaki "Select" butonuna tıklayın.

![Microsoft Windows Server 2016 Base](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/aws-uzerinde-ucretsiz-windows-server-olusturma/images/windows-server-2016-select-button.png)



Sunucumuzun türü olarak t2.micro seçtikten sonra "Next: Configure Instance Details" butonuna tıklayın.

![Instance Type](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/aws-uzerinde-ucretsiz-windows-server-olusturma/images/instance-type-configure-button.png)



"Configure Instance", "Add Storage" ve "Add Tags" adımlarında herhangi bir değişiklik yapmadan "Next" butonuna tıklayarak ilerleyebilirsiniz.

Not: Bu adımlarda bulunan ayarlarda değişiklik yapabilirsiniz fakat seçimlerinizi yaparken ihtiyaçlarınızı aşmamalısınız. Aksi taktirde kredi kartınızdan ücret kesintisi yapılabilir.



Configure Security Group adımına geldiğimizde burada bazı değişiklikler yapacağız. Sunucumuza RDP, HTTP ve HTTPS erişimi vermek için öncelikle bu kuralları eklememiz (RDP ekli olarak geliyor) gerekiyor. Ek olarak 8080 ve 3000 portlarını da ileride kullanmak üzere ekleyebilirsiniz. Sunucunuza her yerden erişmek istiyorsanız "Source" özelliğini "Anywhere" seçmeniz gerekiyor. Erişim kısıtlaması yapmak isterseniz "Custom" veya "My IP" seçtikten sonra CIDR ([Classless Inter-Domain Routing](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)) gösterimiyle IP adresi girebilirsiniz. Ayarlarınızı yaptıktan sonra "Review and Launch" butonuna tıklayın.

![Configure Security Group](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/aws-uzerinde-ucretsiz-windows-server-olusturma/images/security-group.png)



Son adımda, sunucu özelliklerinizi gözden geçirip "Launch" butonuna tıklayın.

![Launch Instance](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/aws-uzerinde-ucretsiz-windows-server-olusturma/images/review-instance-launch.png)



Oluşturduğumuz sunucuya bağlanmak için mutlaka elimizde gizli bir anahtar dosyası (key pair file) olması gerekiyor. Key pair dosyasını oluşturmak için "Create a new key pair" seçip "Key pair name" alanına istediğiniz bir isim verdikten sonra "Download Key Pair" butonuna tıklayarak dosyayı indirmeniz gerekiyor. Dosyanızı indirdikten sonra "Launch Instances" butonuna tıklayın.

Not: Key pair dosyanızı kaybetmeyeceğiniz ve erişebileceğiniz bir yere kaydetmeniz gerekiyor. Bu dosyayı sadece ilk oluşturduğunuzda indirebilirsiniz. Sonrasında indirebileceğiniz bir panel bulunmuyor.

![Create a new key pair](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/aws-uzerinde-ucretsiz-windows-server-olusturma/images/key-pair-launch-instances.png)



Tebrikler sunucunuz hazırlanma aşamasına geçti. Sunucunuzun son durumunu görmek için "View Instances" butonuna tıklayın.

[![View Instance](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/aws-uzerinde-ucretsiz-windows-server-olusturma/images/view-instances.png)](https://console.aws.amazon.com/ec2/v2/home?#Instances:sort=instanceId)



Sunucunuzun hazır olması bir kaç dakika sürüyor. Son durumunu "Instance State" alanında görebilirsiniz.

![Instance State](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/aws-uzerinde-ucretsiz-windows-server-olusturma/images/view-instances-instance-state.png)



Sunucunuzun diğer sunucularla karışmaması için bir isim verebilirsiniz. Name alanına geldiğinizde gözüken kalem simgesine tıkladığınızda sunucunuza istediğiniz adı verebilirsiniz.

![Edit Name](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/aws-uzerinde-ucretsiz-windows-server-olusturma/images/view-instances-edit-name-button.png) ![Name Edit](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/aws-uzerinde-ucretsiz-windows-server-olusturma/images/view-instances-edit-name-done-button.png)



Tebrikler. Windows sunucunuzu başarıyla oluşturdunuz. Sonraki yazımda oluşturduğumuz bu sunucuya nasıl bağlanabileceğimizi anlatacağım.