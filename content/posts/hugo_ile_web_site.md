+++
title = 'Hugo_ile_web_site'
date = 2023-10-15T13:34:05+03:00
draft = false
+++
## Website yapımına Basit ve Hızlı Başlangıç

Hugo nedir: Hugo, Go dili ile yazılmış ve web sitesi oluşturmayı yeniden eğlenceli hale getirmek için tasarlanmış hızlı ve modern bir statik site oluşturucudur.

Gereklilikler: 
1. [Hugo](https://assemble.io)'nun indiirlmesi
2. [Git](https://assemble.io)'in indiirlmesi

### Windows için hugo indirme 
Chocolatey, Scoop veya Winget paket yöneticilerinden herhangi biri ile indiribeilirsiniz.
komutlar:
choco install hugo-extended
scoop install hugo-extended
winget install Hugo.Hugo.Extended

### Linux için hugo indirme
1. Snap ile indirme:
```Sudo snap install hugo```
2. Homebrew ile ndiirlmesi:
```Brew install hugo```
3. ArchLinux dağıtımları için indirme:
```Sudo pacman –S hugo```
4. Dabian dağıtımları için indirme:
```Sudo apt install hugo```
5. Fedore için indirme
```Sudo dnf install hugo```

## Başlangıç
Web sitesini oluşturmaya başlamadan çnce siteniz için bir tema seçmelisniz. Hugo web sitesinde seçebileceğiniz farklı tema tasarımları bulunur. Buradan temalara ulaşabilirsiniz. 
Yeni bir web sitesi oluşturma adımları
Terminalinizi açın ve site klasörünüzü oluşturmak istediğiniz dizine gidin. Bundan sonra yapılması gereken aşağıdaki komutları sırasıyla girmek.
hugo new site Site_ismi
Açıklaması Site_ismi adında bir klasör oluşturarak projenin gerekli altyapıyı kurar.
cd Site_ismi
Klasörün içeirisine girer
git init
Klasörü git ile ilişkilendirir.
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
Siteniz için seçtiğiniz temayı ekler. Burada örnek olarak ananke teması verilmiştir. Kırmızı ile belirtilen yere kendi temanızın github adresini ekeyin.
echo "theme = 'ananke'" >> hugo.toml
Hugo.toml dosyası sitenizin yapılandırma ayarlarının buunduğu dosyadır. Bu komutla temanızı bu dosyaya kaydetmiş olacaksınız. 
hugo server
Hugo server sitenizi görüntelemenize olanak sağlar. Görselde belirtilen linke tıklayarak sitenizin görünümünü inceleyebilirsiniz. 
## İçerik Eklenmesi
Content klasörünüz içeriklerinizin yer alacağı klasördür. Projenizin olduğu klasör içerisinde aşağıdaki komutla yeni bir post oluşturabilirsiniz. 
hugo new content posts/my-first-post.md
[New repository](https://raw.githubusercontent.com/Gulsum-Turk/pictures/main/post3/new%20repositories.png)
Draft bölümü true olması içeriğin taslak olaak kaydedildiği ve görünmeyeceği anlamına gelir. Içeriği yayınlamak için draft’ı false yapın.  İçerik kısmını markdown ile kolayca oluşturabilirsiniz. Markdown yazımı temmelleri için tıklayınız.
## Ayarlar ve Yayınlama
Projenizdeki hugo.toml dosyasının yapılandırma ayarlarını barındırdığını söylemiştik.  Buradaki ayarları inceliyerek siteniz için gerekli olanları yapılandırabilirsiniz. 
[New repository](https://raw.githubusercontent.com/Gulsum-Turk/pictures/main/post3/new%20repositories.png)
Base url: burada example.org kısmını silerek sitenizin url sini ekleyin. 
Dil kısmına Temanızdaki dil bölümünden dil kodunuzu yapıştırın. Türkçe için >>
Title= site başlığı
Yayınlama:
Hugo komutu : Bu komutu kök dizinde çalıştırdığınızda hugo public adında bir klasör oluşturur. Bu klasör mevcut sitenizin yayınlanmaya hazır html dosyalarıdır. Public Klasörünü yayınlayabilirsiniz. 
