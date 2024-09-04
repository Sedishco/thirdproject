1:

CONFİG.----------------

# git --version   > git yüklümü değilmi versiyon kontrolu 
# git config -- global user.name "kullanicı adı"
enter
# git config --list      > kullanıcıları listeleriz

# git config --global user.email "mail adresi"      > kullanıcı mail adresi ekledik
# git config --list      > kullanıcıları listeleriz




2:

GİT İNİT----------------------------

uygulama:
# mkdir firstproject
# cd app
# touch index.html
# touch test.txt
# ls

-------------
içinde bulunduğumuz klasöre gir #pwd ile kontrol et 

# git init >  klasör git özellikli proje dosyası haline geldi initialize oldu ---------klasöre master ünvanı geldi mi? kontrol et   master sana ait bir branch !!
# ls -a    >  . ile başlayan git gizli klasörünü gördün mü?




3:


GİT STATUS ---------------------------------
# git status    >   initlenmiş ama staging areaya aktarılmamış dosyaları gösterir / branch gösterir    kırmızı ile olanlar stage areaya girmemiş yeşiller hazır ??




4:


GİT ADD-------------------------

local repolardaki yapılan değişiklikleri push öncesi staging areya gönderme sürecidir (git add .)
# git add .     >  directorydeki tüm doyaları "." koyarak aktarabiliriz
veya
# git add "filename"    > commit etmek istediğin file veya değişiklikleri push etmeden önce add ile stagin areaya yani localdeki hazır haldeki kuyruğa alma işlemi


enter sonrası son durumu sana gösterecektir yeşi,l klasörlere dikkat edelim ....



uygulama 2 :
# touch deneme.txt 
# git status 
>>>dikkat edelim yeni oluşan klasör kırmızı yani, add edilmedi ve stagin area da yok .

# git add .
# git status    >> kontrol et tüm dosyalar stagin Area da 





5:


GİT COMMİT----------------------
# git commit -m "commit mesajımızı yazalım neden ne için olay ne"
# git status     >>   herhangibir commit bekleyen olay olmadığı yazar.


uygulama 3 :
# touch deneme2.txt
# git status
# git add deneme2.txt veya git add .
# git status 
# git commit -m "deneme2.txt dosyaını klasöre eklendi"
# git status 


6:

GİT LOG------------------------------------------

# git log      > yapılan commitlerin sıralı listeleri ve id ve branchleri gelir 



7:


GİT VERSİON----------------------- VERSİYON DEĞİŞİKLİĞİ

uygulama4:
# touch deneme3.txt
# git status
# git add .
# git commit -m "deneme4.txt eklendi"
# git status
# git log 
q ile çık 


örnek olay manuel olarak masaüstünden yanlışlıkla bir personel yeni açılan deneme 3 . txt sildi diyelim ve bizde silelim .????

# git status  >>>>>> kayıp dosya uyarısını alacağız  

# git add .
# git status >>>>> dediğimizde doya silindi şeklinde gözükür
# git commit -m "deneme4.txt silindi"
# git status 

 # git log


 sonuç olarak biz bu klasören yanlışlıkla silinen deneme4.txt dosyasını geri getirmek için önceki versiyona yani deneme4.txt silinmeden önceki versiyon commit işlemine geri dönelim .!!!


 # git log 
 >>>>> deneme 4 ü eklediğimiz açıklaması mevcuttur commit id sini kopyalayalım 

 # git checkout <versiyon commit id yapıştır> -- .
 enter sonrası eski hale geri döndük  ama bu dosyayı staging areaya tekrar aldı commit repostorysine değil .

 # git commit -m "deneme4.txt tekrar eklendi versiyon dönüldü"
 # git status 
 # git log 
 ls -la 



 8:
 
 
  GİT DİFF----------------

UYGULAMA 5 :
deneme 4.txt dosyasını masaüstünden ıu olarak açalım ve içine herhangi notlar yazalım kaydedelim ve terminale geri dönelim.


# git diff >>>>>   içinde değişiklik yapılan dosyayı gösterir .

# git add .

# git status 

# git commit -m " deneme4.txt içinde değişiklik yapıldı "

# git status
# git log



 9:

 GİT RESTORE--------------------- değişiklikleri geri alma    staging area ve working directoryde kilere değişiklik

uygulama:
deneme3.txt dosyasındaki bir bilgiyi silelim windows üzerinden ve kaydedelim
# git diff
# git checkout -- filename.txt 
# git add .
# git commit -m "lkjlksdjfsd"

# git reset HEAD dosyaadı.txt   > dersek stage area ya git add ile aldığımız dosyaları worging directorye geri alırız boşaltırız



 10:

 GİT REMOVE---------------------------
 dosya silme 
# git rm filename.txt
# git status
# git commit -m "filedeleted"
# git status

klasör silme 
# mkdir testklasör
# cd test
# touch test.xml deneme5.txt 
# git status
# git add .
# git commit -m " test klasörü eklendi "
silelim 
# cd ..
# git rm -r dosyaadı
#  git status
# git add .
# git commit -m "klasör silindi"
# git status




11:

 GİT MOVE-------------------- dosya ismi değiştirme ve taşıma 
isim değişikliği
# git mv filename.txt verilecekisim.txt
# git status
# git add .
# git commit -m " dosya ismi değiştirildi"

dosya taşıma 
# git mv test.txt dosya/yolu/belirle
# git status
# git add .
# git commit -m "dosya tasındı"
# git status





 12:

 GİT ALİAS----------------------------- bazı özellikleri kısaltır

 önemli bir konu değil işin şovu:)





 13:

 GİT PUSH-----------------------------pull

# git remote add origin <url>
# git remote
# git status 
# git push -u origin master
kullanıcı adı ve şifre gelecek 
autrohize git credentials manager seç.
push işlemi başlar 
git e gir repostory sekmesine tıkla ve kontrol et 

# add file tıkla githubdan    denemhithub.html dosyası aç ıu githubdn  <<commit new file tıkla >>

vs code a geri gir :
# git pull



14:

  GİT İGNORE---------------------------


  16.


  GİT BRANCH-------------------------------------------


https://www.youtube.com/watch?v=zcOZJGHEEw8&list=PLld6WWpFK1nEhFvvYi5ts-_JoUL3wF3zz&index=10
