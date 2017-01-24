# AWS Üzerinde Bulunan Windows Servera Bağlanma

Eğer AWS üzerinde bir Windows Server oluşturmadıysanız [AWS Üzerinde Windows Server Oluşturma](http://dogukandemir.com/tr/aws-uzerinde-ucretsiz-windows-server-olusturma/) başlıklı yazımı okuyarak yeni bir sunucu oluşturabilirsiniz. Sunucunuzu oluşturduysanız "Instances" ekranında bulunan "Windows Server 2016" adlı sunucumuzu seçtikten sonra "Connect" butonuna tıklayın.

![Connect](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/aws-uzerinde-bulunan-windows-servera-baglanma/images/connect-button.png)



"Connect To Your Instance" ekranında "Download Remote Desktop File" butonuna tıklayarak .rdp dosyasını indirdikten sonra "Administrator" kullanıcınızın şifresini çözmek için "Get Password" butonuna tıklayın.

![Connect To Your Instance](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/aws-uzerinde-bulunan-windows-servera-baglanma/images/connect-to-your-instance.png)



Önceki yazıda oluşturduğumuz key-pair dosyasına bu adımda ihtiyacımız olacak. Benim oluşturduğum dosyanın adı Windows2016Server.pem olduğu için ekranda bu dosya adını belirterek bu dosyayı seçmemizi istiyor. Dosyayı seçtikten sonra "Decrypt Password" butonuna tıklayın.

![Decrypt Password](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/aws-uzerinde-bulunan-windows-servera-baglanma/images/connect-to-your-instance-get-password.png)



"Administrator" kullanıcınızın şifresini ekranda görebilirsiniz.

![Username Password](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/aws-uzerinde-bulunan-windows-servera-baglanma/images/username-password.png)



İndirdiğimiz .rdp dosyasını açtığınızda çıkan uyarıyı "Connect" butonuna tıklayarak geçebilirsiniz. "Password" alanında gördüğünüz şifreyi kopyalayıp "Administrator" kullanıcınızın şifresi olarak yapıştırın ve "OK" butonuna tıklayın. Sertifika ile ilgili çıkan uyarıyı "Yes" butonuna tıklayarak devam edebilirsiniz.

![Enter Your Credentials](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/aws-uzerinde-bulunan-windows-servera-baglanma/images/enter-your-credentials.png)



Bağlandığınızda sunucunuzun özelliklerini ekranın sağ üst köşesinde görebilirsiniz.

![Server Details](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/aws-uzerinde-bulunan-windows-servera-baglanma/images/server-details.png)



Tebrikler. Windows sunucunuza başarıyla bağlandınız. Sonraki yazımda sunucuya node.js kurulumunu ve bir hello world uygulaması yapıp bu uygulamaya nasıl erişeceğimizi anlatacağım.