# Node.js Hello World Uygulaması

Windows sunucunuza bağlandıktan sonra Başlat menüsünde bulunan Node.js klasörü altındaki "Node.js command prompt"a tıklayın. Eğer Node.js kurulumunu yapmadıysanız önceki [Windows Servera Node.js Nasıl Kurulur?](http://dogukandemir.com/tr/windows-servera-node-js-nasil-kurulur/) başlıklı yazımı okuyarak kurulumu tamamladıktan sonra "Node.js command prompt"u çalıştırabilirsiniz.

"Node.js command prompt" ekranındayken aşağıdaki komutları girerek ilk uygulamanızı oluşturabilirsiniz. Peki ya bu komutlar ne anlama geliyor?

![Node.js Hello World](https://raw.githubusercontent.com/dogukandemir/blog-posts/master/tr/nodejs-hello-world-uygulamasi/images/npm-init.png)



Komut istemi kullanımını bilmeyenler için Node.js komut isteminden bağımsız olarak ekranda kullandığım 2 komuttan bahsetmek faydalı olacaktır.

cd: change directory (dizini değiştir)
mkdir: make directory (dizin oluştur)

"cd C:\" komutu C sürücüsünün ana dizinine geçmenizi sağlayacak.
"mkdir nodejs" komutu bulunduğunuz klasör içerisinde nodejs adında bir klasör oluşturmanızı sağlayacak.

C:\nodejs\helloworld dizinini oluşturup bu dizine girdiğinizde "npm init" komutunu kullanarak yeni bir Node.js uygulaması oluşturmak için npm paket oluşturucusunu çalıştırabilirsiniz. Size sırasıyla name (uygulamanızın adı), version (sürüm numarası), description (açıklaması), entry point (giriş noktası), test command (test komutu), git repository (git deposu), keywords (anahtar kelimeler), author (yazar) ve license (lisans) bilgileri soruluyor. Enter tuşuna basarak varsayılan değerler (parantez içinde yazan değerler) ile uygulamanızı oluşturabilirsiniz. Ben description ve yazar alanlarını değiştirerek oluşturdum. Bilgileri tamamladığınızda package.json dosyanızın önizlemesini kontrol edip enter tuşuna basarak uygulamanızı oluşturabilirsiniz.

"echo console.log("hello world"); > index.js" komutu ile bulunduğunuz dizinde index.js adında bir dosya oluşturup bu dosyanın içine "console.log("hello world");" yazdırıyorsunuz. Bu komut içerisindeki index.js değeri entry point olarak girdiğiniz değerle aynı olmak zorundadır. Son olarak "node index" komutuyla uygulamanızı çalıştırdığınızda hemen alt satırda "console.log" kodu ile ekrana yazdırdığınız "hello world" yazısını göreceksiniz.

Tebrikler AWS üzerinde bulunan Windows sunucunuzda Node.js kurulumu sonrası ilk uygulamanızı çalıştırdınız. Sonraki yazımda bu uygulamamıza sunucu dışındaki bir tarayıcıdan nasıl erişeceğinizi anlatacağım.