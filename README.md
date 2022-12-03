# 80-port-error-xampp

Persian language

یکی از رایج‌ترین خطاها در محیط لوکال هاست وردپرس که با زمپ ایجاد شده است اینه که وب سرور آپاچی (apache) که هنگام اجرای نرم افزار و کلیک بر روی دکمه Start جهت اجرا صورت میگیره با خطا مواجه شده و به رنگ قرمر در میاد و از اونجایی که لازمه تا سرور آپاچی و همچنین mysql در هنگام کار با زمپ فعال باشه با خطا مواجه شده و عملا سایت ما در محیط لوکال هاست بالا نمیاد. این مشکل به این دلیل رخ میده که چون وب سرور آپاچی از پورت 80 برای اجرا استفاده میکنه ممکنه تا توسط برنامه دیگه‌ای که در کامپیوتر شما نصب هست و توسط اون اشغال شده؛ به همین دلیل وب سرور آپاچی در این پورت اجرا نشده و به دلیل ایجاد تداخل با خطا مواجه خواهید شد.

برای رفع این مشکل به مسیری که برنامه Xampp نصب کردید مراجعه کنید و سپس در پوشه xampp همانطور که در تصویر زیر مشاهده میکنید پوشه apache را باز کرده و سپس با مراجعه به پوشه conf فایلی که با عنوان httpd.conf را در آن وجود داره با استفاده از یک برنامه ویرایشگر متن همچون notepad باز کنید. حالا سعی کنید تا با استفاده از قابلیت جستجو که با کلیدهای ترکیبی Ctrl + F در اختیار شما قرار داره به دنبال عبارت Listen بگردید تا خط زیر رو پیدا کنید.

1 Listen 0.0.00:80 #

2 Listen [::]: 80

3 Listen 80

کافیه تا عدد 80 در تمامی خطوط فوق به عدد دیگری همچون 81 تغییر بدین تا پورت سرور آپاچی به 81 تغییر داده بشه و از این به بعد آپاچی در پورت 81 اجرا بشه و بتونید ازش استفاده کنید. در نهایت فایل مورد نظر را ذخیره کرده و سپس با کلیک بر روی دکمه Quit از برنامه زمپ خارج بشین و مجددا برنامه را اجرا کرده و با کلیک روی دکمه start در مقابل apache، خواهید دید که مشکل رفع شده و به رنگ سبز در میاد، حالا روی دکمه Start که مقابل mysql قرار داره کلیک کنید تا پایگاه داده php هم روشن بشه و به سایتتون دسترسی داشته باشید.
