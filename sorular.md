## Araştırma Soruları

Şimdi görevi gerçekleştirmek için hazırsınız. Şimdi biraz daha kullandığımız araçları anlama zamanı. Bu dokümanı güncelleyerek, aşağıdaki soruları cevaplayınız. Git'e biraz daha aşina olmaya başladığınızı göreceksiniz. 

Soruları cevaplamak için [GitHub docs](https://docs.github.com/en)'u kullanabilirsiniz. Docs, (ingilizce documentation'ın kısaltılmış halidir) bir programı veya dilin nasıl kullanılacağını anlatan dokümandır. Yazılım dünyasında sıkça kullanılır. Bir yazılımcı olarak zamanınızın büyük çoğunluğu da bu tarz dokümanları okumakla ve üzerinde çalışmakla geçer.

Eğer aradığınız soruların cevapları GitHub docs'ta yok ise Google'lama becerileriniz size yardımcı olacaktır :)

1. Git nedir?

Git , yazdığımız projeleri ve uygulamaları, bilgisayarımızda ya da harici disklerde değilde internet üzerinde tutmamızı ve yönetmemizi sağlayan bir versiyon kontrol sistemidir.

2. Git ile GitHub arasında ne fark var?

Git, bir sürüm kontrol sistemidir, Github ise, Git kullanan projeler için bir depolama servisidir.

3. Neden bir branch oluşturuyoruz? 

Projemizin o anki halini bozmamak ve herhangi bir sorun çıkması halinde geri dönüp önceki versiyona ulaşmayı sağlar . Ayrıca projenizdeki her değişiklik,versiyon için repo açmanıza gerek kalmadan her bir versiyon için branch acarak versiyonları bir arada kolayca takip edebilir ve erişebilirsiniz

4. Pull Request'in amacı nedir?

Pull request talebi, temelde branch’dan sorumlu kişiden kodunuzu eklemesini istemektir. Ayrıca o kişinin kodda tam olarak neyi değiştirdiğinizi görmesine de yardımcı olur.

5. Bir Branchten diğerine geçmek için kullanıdığımız KOMUT nedir? Örneğin ADINIZ-SOYADINIZ branch'inde çalıştığınızı hayal edin ve main branch'ine geçmek istiyorsunuz.

Git’te branch değiştirmek için checkout komutunu kullanıyoruz. git checkout dedikten sonra branch adımızı yazmamız yeterli. Eğer branch adımızı hatırlamıyorsak git branch yazarak bütün branchleri listeleyebilirsiniz.

6. `git fetch`, `git merge` ve `git pull` arasındaki farklıarı açıklayınız. Bu konutlar ne yapar açıklayınız.

Git Fetch = Bu komut remote’daki tüm commitleri local’e çeker. Fakat çekilen commitler remote branch’lar olarak depolanır, local olarak değil. Bu sayede local’deki kodla merge etmeden önce gözden geçirme şansı verir.

Git merge = Başka bir branch'deki değişiklikleri üzerinde çalıştığınız kendi branch'inize entegre etme işlemidir. Git merge işlemi sırasında değişikliklerin çoğunu sizin için otomatik olarak entegre eder.
Fakat 

Git pull = git fetch + git merge

7. Merge conflict nedir?
Bu durum genellikle aynı dosya üzerinde değişiklikler yapıldığında ortaya çıkar, bu durumda bile Git dosyadaki değişiklikleri nasıl entegre edileceğine çoğu zaman otomatik karar verebilir. Fakat aynı satırda yapılan değişiklikler veya takımdaki bir kişinin bir satırı silmesi durumunda sizin bu değişikliği kendi branch'inize nasıl entegre edileceğine karar vermeniz gerekir. Bu durumda Git dosyanızı conflicted (çakışmalı) olarak işaretler ve sizin çalışmanıza devam edebilmeniz için bu çakışmayı çözmeniz gerekir.

8. Merge conflict'i nasıl çözeriz?

Öncelikle çakışmanın neden olduğunu anlamak gerekir 
Bunun için git status komutu çalıştırılır ve çakışma olan dosyayı öğreniriz. Dosyamızı açıcaz ve <<<<<<<<< HEAD ile başlayan ve ============ kadar devam eden kısım dosyanın bizim branch'imizde olan versiyonuna ait olan bölümü görmüş olucaz
================ belirtecinden sonraki kısım da değişiklikleri entegre etmek istediğimiz branch'de yer alan dosyanın içeriğini gösterir.
Dosyamızın içeriğinin ne olacağına karar verip kaydettikten sonra normal bir commit işlemi ile çakışmayı çözme işlemini tamamlıyoruz.
git add dosya adı ve git commit ederek tamamlıyoruz 
