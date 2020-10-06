<div dir="rtl">

# روش نصب ویم بر روی تمامی سیستم عامل ها

![virgoolPost](https://user-images.githubusercontent.com/25862601/94466043-a9957580-01cd-11eb-95dd-4bf9dee56254.png)

این مطلب قسمت دوم سری صفر تا صد ویم هست که قراره در یک سری بلند تولید بشه و برای ادامه مطالب که گم نکنید یک مخزن در گیت هاب ساختیم که تمام لینک های مطالب مرتبط به ویم در اونجا قرار داره

این هم لینک تمام سری ویم ( یادتون باشه این ریپو همیشه در حال آپدیت شدن هست)

<div dir="ltr">

**[VIM FARSI LIBRARY](https://github.com/illustrayking/vimFarsiLibrary)**

</div>

در [قسمت اول](https://virgool.io/@illustrayking/whyichoosedvim-f5kbf8v3r275) با هم یک مروری رو داشتیم بر اینکه چرا ویم رو انتخاب کنیم و شایعاتی که در موردش میگفتند رو هم حرف زدیم

اما حالا بریم ببینیم اون مطلبی که گفتم که میشه ویم رو در همه جا به معنای واقعی کلمه تجربه کرد یعنی چی و چطور نصب کنیم

در کل ویم به دو صورت عرضه شده

<div dir="ltr">

1- Terminal Base (Recommended)

2- Graphical Vim or Gvim

</div>
ویم یا بر روی ترمینال قابل دسترس هست که بهترین و ساده ترین روش استفاده ویم از طریق خود ترمینال هست

و یا اینکه ویم از طریق یک نرم افزار مستقل در اختیار شما قرار میگیره که در بیشترین مواقع پیشنهاد نمیشه اما اگر راهی نداشتیم مجبور به استفاده میشیم

اینجا قرار هست که وارد تمام سیستم عامل های معروف بشیم و یواش یواش وارد مکان هایی بشیم که اصلا فکر نمیکردیم که بتونیم اونجا هم کدنویسی کنیم

## روش نصب در توزیعات لینوکسی

در 90 درصد توزیعات لینوکسی ویم به صورت پیشرفض نصب هست اما اگر تنها `vi` نصب بود بهتر هست که `vim` که مخفف `vi improved` هست رو نصب کنیم

من سعی میکنم دستورات تمام توزیعات معروف لینوکس ر وبنویسم اما در بیشترین مواقع نصب هست

ابتدا دستور زیر رو اجرا کنید که ببینید نصب هست یا نه

<div dir="ltr">

```
vim --version
```

</div>

اگر به شما ورژن ویم رو داد یعنی نصب هست

اما در بیشترین مخازن لینوکسی ویم موجود هست و شما به راحتی با دستور نصب میتونید اقدام به نصب ویم کنید

> نکته ای رو که خیلی خوب هست به دوستان لینوکسی بگم این هست که همیشه پکیج های خودتون رو قبل از نصب آپدیت کنید

<div dir="ltr">

```
sudo apt update
```

</div>

<div dir="ltr">

```
// debian

sudo apt install vim

//fedora

dnf install vim-enhanced (vim)

// arch linux

sudo pacman -S vim
```

</div>

اگر دقت کنید میبینید که در توزیعات لینوکسی بسیار راحت نصب میشه و نیازی به کش دادن مطلب نیست

### نصب ویم از طریق snap

در این حالت هم شما از طریق یک استور خاص خود محیط لینوکس میتونید به نصب ویم اقدام کنید

برای اینکار ابتدا باید به `snap` دسترسی داشته باشید

<div dir="ltr">

```
sudo apt update

sudo apt install snapd -y
```

</div>

و بعد از طریق دستور `sudo snap install vim-editor --beta` میتونیم ویم رو نصب کنیم

<div dir="ltr">

```
sudo snap install vim-editor --beta
```

</div>

## اما چطور یک ویم رو از ابتدا build کنیم

در لینوکس شما این قابلیت رو دارید که خودتون یک ابزار رو از ابتدا `make` کنید در اصطلاح

اما چرا ما نیاز داریم از ابتدا خودمون ویم رو بسازیم؟

بعضی اوقات ممکن هست که نتونیم از طریق `package manager` که ابزار مورد نظر رو برای توزیع ما بهینه کرده دسترسی داشته باشیم مثلا یکی از اون دلایل ها این هست که برنامه نویس مورد نظر برای توزیع ما اون رو نساخته به همین دلیل من خودم میتونم با در دسترس داشتن به فایل سورس شروع به بیلد کردن بکنم و برای توزیع خودم اون رو بالا بیارم

برای اینکار ابتدا وارد این وب سایت بشید

<div dir="ltr">

**[BUILDING VIM FROM SOURCE](https://github.com/ycm-core/YouCompleteMe/wiki/Building-Vim-from-source)**

</div>

ابتدا پکیج هایی که برای ساخت ویم نیاز هست رو باید نصب کنیم

نکته ای رو که باید بگم این هست که در پیج بالا سه پکیج رو در اختیار گذاشته که نیازی به نصب نیست چون در اوبونتو 20 به بعد اینها منتقضی شده اندا اما باز هم اگر قابل نصب بودند شما اون رو نصب کنید ولی اگر نبودند دستور پایینی که در احتیارتون گذاشتم رو نصب کنید

<div dir="ltr">

```
libgnome2-dev libgnomeui-dev libbonoboui2-dev
```

</div>

سه پکیج بالا منقضی شده اند و نیازی به نصب نیست

<div dir="ltr">

```
sudo apt install libncurses5-dev \
libgtk2.0-dev libatk1.0-dev \
libcairo2-dev libx11-dev libxpm-dev libxt-dev python-dev \
python3-dev ruby-dev lua5.2 liblua5.2-dev libperl-dev git
```

</div>

اما اگر در فدورا هستید به شیوه زیر پکیج های مورد نیاز رو نصب کنید

<div dir="ltr">

```
sudo yum install -y ruby ruby-devel lua lua-devel luajit \
luajit-devel ctags git python python-devel \
python3 python3-devel tcl-devel \
perl perl-devel perl-ExtUtils-ParseXS \
perl-ExtUtils-XSpp perl-ExtUtils-CBuilder \
perl-ExtUtils-Embed
```

</div>

حالا در فدورا باید یک `symlink` از `xsubpp` به دایرکتوری `perl` ایجاد کنیم

<div dir="ltr">

```
sudo ln -s /usr/bin/xsubpp /usr/share/perl5/ExtUtils/xsubpp
```

</div>

خب حالا اقدام به نصب میکنیم و بعد شروع به `build` کردن ویم میکنیم

ابتدا وارد دایرکتوری `HOME` میشید و بعد توسط دستور زیر ویم رو کلون میکنیم

<div dir="ltr">

```
cd ~/

git clone https://github.com/vim/vim.git
```

</div>

دستور زیر رو اجرا میکنیم

<div dir="ltr">

```
 ./configure --prefix=/usr/localonfigure --with-features=huge \
             --enable-multibyte \
	     --enable-rubyinterp=yes \
             --enable-python3interp=yes \
             --with-python3-config-dir=$(python3-config --configdir) \
             --enable-perlinterp=yes \
             --enable-luainterp=yes \
             --enable-gui=gtk2 \
             --enable-cscope \
             --prefix=/usr/local
```

</div>

و در قدم بعد

<div dir="ltr">

```
make VIMRUNTIMEDIR=/usr/local/share/vim/vim82
```

</div>

و در نهایت شروع به `make` کردن میکنیم

<div dir="ltr">

```
sudo make install
```

</div>

حالا اگر اخطاری نداده باشه ویم شما نصب هست کافی هست که یکبار دستور زیر رو اجرا کنید و ببینید نصب شده یا نه

<div dir="ltr">

```
vim --version
```

</div>

اگر میخواهید که ویم ادیتور دیفالت شما باشه از دستورات زیر استفاده کنید

<div dir="ltr">

```
sudo update-alternatives --install /usr/bin/editor editor /usr/local/bin/vim 1
sudo update-alternatives --set editor /usr/local/bin/vim
sudo update-alternatives --install /usr/bin/vi vi /usr/local/bin/vim 1
sudo update-alternatives --set vi /usr/local/bin/vim
```

</div>

الان تونستیم بفهمیم که چطور از ابتدا یک ویم رو بسازیم

اگر باز هم به مشکل خوردید به لینک بالایی برید و تمام دستورات رو یکبار مرور کنید من خودم اینطوری تونستم

## اما چطور gvim رو نصب کنیم

همونطور که گفتم ما میتونیم از طریق محیط گرافیکی هم دسترسی داشته باشیم به ویم

برای اینکار از دستور زیر استفاده میکنیم

<div dir="ltr">

```
sudo apt install vim-gtk3

for older versions

sudo apt install vim-gnome
```

</div>

## چگونه ویم رو در ویندوز تجربه کنیم

یکی از دیگر دغده هایی که برای تمام کسانی که با ویم کار میکنند این هست که چطور در ویندوز این ادیتور خوب رو تجربه کنیم

از ویندوز 10 خیلی از مشکلات حل شد و با اومدن `WSL` خیلی کم به مشکل بر میخوردیم

اما من در اینجا حتی به شکل کاملا مستقیم بر روی ویندوز هم آموزش میدم

در ویندوز ما به سه صورت میتونیم ویم رو تجربه کنیم

1- نصب WSL و تجربه اوبونتو که پیشنهاد من کاملا به این سمت هست چرا که اونجا دیگه یک اوبونتو کافی رو در اختیار دارید

برای اینکه بتونید `WSL` رو به راحتی نصب کنید به این مقاله ها برید

<div dir="ltr">

**[WSL INSTALLATION GUIDE](https://virgool.io/@illustrayking/howtosolvewslissue-ar4dqe2pgnec)**

**[WSL PORT-FORWARDING](https://virgool.io/@illustrayking/wslportforwarding-epzppnuwyb3i)**

</div>

از ویندوز 10 ما دیگه میتونیم یک کرنل واقعی لینوکس رو تجربه کنیم و ویم رو به راحتی هر چه تمام بارگذاری کنیم بدون ذره ای تفاوت بین اوبونتو و ویندوز و حتی میتونیم اینجا از دستوراتی که قبلا محروم بودیم در ویندوز هم استفاده کنیم به طور مثال من همیشه از دستور `sed` برای تغییرات کلمات استفاده میکنم پس الان دیگه خیالم راحت هست که این قابلیت رو از دست نمیدم

اگر شما در حال حاظر `WSL2` رو بر روی سیستم دارید که به مطلب بالا برید و مثل اوبونتو اون رو ران کنید اما اگر دلتون نمیخواد wsl رو داشته باشید و تنها میخواهید یک ادیتور ویم رو بدون ترمینال تجربه کنید بقیه مطلب رو بخونید

ابتدا به سایت زیر مراجعه کنید و فایل `gvim82.exe` رو دانلود کنید

<div dir="ltr">

**[GVIM DOWNLOAD](https://www.vim.org/download.php#pc)**

</div>

در هنگام نصب تنها شما تنظیمات رو از حالت `typical` به حالت `full` تغییر می دید

![Screenshot 2020-09-30 091614](https://user-images.githubusercontent.com/25862601/94776297-58a09f80-03ce-11eb-9bf2-01c7b77c558d.png)

![Screenshot 2020-09-30 091638](https://user-images.githubusercontent.com/25862601/94776331-6b1ad900-03ce-11eb-97e6-388eb7595d04.png)

حالا ما به یک ویم در حالت گرافیکی دسترسی داریم و این هم یک تصویر همراه با کانفیگ ها که دقیقا شبیه به ویم ترمینال کانفیگ میشه

![gvim](https://user-images.githubusercontent.com/25862601/95227227-bab43700-080a-11eb-8a69-fb068b6db9e5.png)

</div>
