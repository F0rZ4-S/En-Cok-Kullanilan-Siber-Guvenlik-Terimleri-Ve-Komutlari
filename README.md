# En-Cok-Kullanilan-Siber-Guvenlik-Terimleri-Ve-Komutları
En çok kullanılan komutlar ve ne işe yaradığını paylaşıyoruz. Pyhton Komutları

# Burada bulunan bütün açıklamalar ve bilgiler "Etik Hacker" olmayı amaçlayan kişiler için yapılmıştır. Kesinlikle amacı dışında kullanmayınız. Ek olarak bu yöntemlerde kullanacağınız bütün bilgiler sizlere zarar verebilir bu yüzden tam anlamıyla öğrenmenizi ve güvenlik için kullanmanızı tavsiye ediyorum.


Tcp: Bağlantı tabanlı (connection oriented) bir protokoldür. TCP'de akış kontrolü vardır. TCP başlığı (header) 20 bayttır.
Udp: UDP bağlantı tabanlı değildir (connectionless). UDP'de akış kontrolü yoktur. UDP başlığı 8 bayttır.

## Portlar
1. SSH - TCP,UDP - Port 22 - Kullanıcılara sunucularını internet üzerinden kontrol etmesini ve düzenlemesini sağlayan uzak yönetim protokolüdür.
2. FTP - 21/TCP,UDP - Port 21
   File Transfer Protocol, Türkçesi ile Dosya aktarma protokolüdür. Bilgisayar ağından sunucuya dosya aktarımı sağlamaktır. Örnek Filezilla programı ftp programı bir aracı işlevi görür fakat ftp protokolü ile bilgisayarınızdan sitenize veyahut hostinge dosya aktarımı sağlar.
3. Telnet - 23/TCP,UDP - Port 23 - Telnet güvenli bağlantıya yönelik transfere dayanan bir istemci-sunucu protokolüdür. Genellikle bu protokol bir parola eşitleme programının dinlediği TCP port 23 te bağlantıyı tasdik etmek için kullanılır.
4. SMTP - 25/TCP,UDP - Simple Mail Transfer Protocol, E-Posta göndermekte kullanılan bir protokoldür.
   


## Python - Kali - Linux Komutları - En çok kullanılanlar
1. nmap (IP ADRESS) - Ağ tarafama ve zafiyetlerini bulmak için kullanılan bir açık kaynaklı linux programıdır.
2. netdiscover - Yerel ağlarda ip taraması yapan bir komuttur ve bu router içerisinde iseniz bir wifi olabilir bunların taramasını size listeler.
3. Gobuster - bir dizin keşfi yapabilen brute force saldırı programıdır.
4. ftp - Eğer "21/tcp open ftp" taramadan sonra önünüze geldi ise ftp komutu ile bu açıktan yararlanarak ftp üzerinde "Anonymous" olarak sızmanızı sağlar.
5. Telnet - Telecommunication Network, bir bilgisayarın, internet üzerinden uzaktaki bir bilgisayarla iletişim kurmasını sağlayan metin tabanlı bir TCP/IP ağ protokollerinden biridir. Telnet hizmetlerinin de Web siteleri gibi  bir adresi vardır.



## Nmap Ek Komutları
1. nmap 255.255.0.255 255.255.255.255 şeklinde 2 adet ip üzerinde arama yapabilirsiniz.
2. nmap 0.0.1.1-10 ise 1 ila 10 arasındaki bütün ip adresini taramak örnek vermek gerekirse ip adresinin aralığını biliyorsunuz fakat hangisi olduğunu bilmiyorsanız bu aralığı taratabilirsiniz.
3. nmap -A Agresif taramadır. Bu tarama stili genelde tavsiye edilmez eğer bir sunucu test etmiyorsanız genelde sessiz olması saldırının gizli ilerlemesi gerekmektedir.
4. nmap taraması direkt taramadır fakat genelde bu çok uzun sürer ve bütün ip ve portları tarar.
5. nmap -p * bütün portları taratan bir komuttur.
6. nmap -sn Port taraması yapma anlamına gelir.
7. nmap -F Daha hızlı tarama yapar ama sonuçlar daha az olur.
8. nmap -sC Varsayılan komut dizisini kullanarak bir komut dosyası taraması gerçekleştirir. --script=default ile eşdeğerdir . Bazı
    Bu kategorideki betiklerin %40'ı izinsiz olarak kabul edilir ve bir hedefe karşı çalıştırılmamalıdır. İzinsiz çalıştırılmamalıdır. Eğer bir sızma senaryosu içerisinde iseniz izinli bir şekilde kullanılabilir.
9. nmap -sV ile versiyon bilgileri alınır. Örneğin Apache versionunu buradan edinebilirsiniz.
10. nmap -v Ayrıntı düzeyini artırarak, Nmap'in sürmekte olan tarama hakkında daha fazla bilgi yazdırmasına neden olur. Ama bunu kullandığınızda sisteminize bağlı olarak süresi artacaktır.


## Terminal Komutları
    mkdir: Yeni bir dizinin oluşturulması amacıyla kullanılır. 
    rmdir: Zaten var olan bir dizini silmek için kullanılan komuttur.
    cd: Dizinler arasında belirlenen dizine geçiş yapmak için kullanılır.
    cd: Bir üst dizine geçişte kullanılır. Örnek "cd .." komutu ile kullanırsanız bir üst dizine geçersiniz.
    Rm: Dosyaları silen komuttur. Bulunduğunuz dizinde "rm *" komutu kullanırsanız bütün dosyaları silersiniz. Örnek rm * komutu en çok Logları silmek için kullanılır.
        rm dosyaismi - Sizden bu komutu kullandığınızda onay isteyecektir. Y/N şeklindedir.
        rm -f dosyaismi - izin almadan direkt dosyayı siler (Dikkatli olun)
        rm dosya_ismi1 dosya_ismi2 dosya_ismi3 - Birden fazla dosya silmenizi sağlar.
    cat: Herhangi bir metin tabanlı dosyayı önünüzdeki terminale dökmesi ve okumanıza yarayan bir komuttur.
    pwd: Print Working Directory, çalışmakta olduğunuz dizini gösteren komuttur.
    ls: Olduğunuz dizinde terminalle görmenizi sağlayan komuttur. Örnek masaüstündesiniz ve ls komutunu kullandınız gizli veya gizli olmayan bütün komutları görebilirsiniz.
    mv: Dosyaları taşımak veyahut yeniden adlandırmak için kullanılabilir. Örnek: mv dosya.txt /root/Desktop şeklinde gerçekleştirilebilir. Yeniden adlandırmak için ise mv dosya.txt yenidosya.txt şeklindedir.
    touch: Terminal üzerinden boş dosyalar açmanıza olanak sağlar. Örnek: /root/Desktop/index.html
    sudo: Kullanacağınız en önemli komuttur. Parolasız bir oturum açmamanızı tavsiye ederim. O yüzden sudo komutu ise SuperUser Do yani yönetici olarak çalıştırmanız gereken install etmeniz gereken dosyalar için önemlidir.
          Ve hata yaparsanız password alanında bunu iptal edebilirsiniz.
    df: Disklerinizin kilobayt bazında görebilirsiniz. Ek olarak df -m şeklinde kullanırsanız megabayt olarak görebilirsiniz.


## En Çok Bulunan Açıklar
SQL Injection: SQL enjeksiyonu, veri tabanına dayalı uygulamalara saldırmak için kullanılan bir atak tekniğidir; burada saldırgan SQL dili özelliklerinden faydalanarak standart uygulama ekranındaki ilgili alana yeni SQL ifadelerini ekler.


  ## Önemli Notlar - Bilinmeyenler veya Bilinmesi Gereken Komutlar
    Terminalde boşluk kullanmak: Eğer masa üstünüzde bir dosya var fakat terminalde "New Folder" olarak girerseniz o dosyaya ulaşamazsınız. O yüzden şu şekilde yazmalısınız: "cd New\ Folder" yani ters slash koyarsanız oranın boşluk olduğunu belirtmiş ve dosyaya girmiş olursunuz.
    Peki yaptığımız işletimi bitirmek için ctrl + c yani kopyalama komutuyla örnek ping atma işlemini bitirebilirsiniz.
    Ctrl + c işlemi bitirmek içinde kopyalamayı nasıl yapacağız? Shift Ctrl C veyahut yapıştırmak içinde aynı Shift Ctrl V şeklinde yapabilirsiniz.



# Hakkında tam bilgim olmadığı noktaları eklemedim eğer bilginiz varsa kesin bilgi şeklinde ekleyebiliriz.
# Lütfen birşey eklemekten çekinmeyin. Pull Request olarak gönderebilirsiniz.
# Hatalar var ise düzeltebilirsiniz. Hepimiz insanız hatalarımız olabilir bundan dolayı düzenleme yapabilirsiniz.
