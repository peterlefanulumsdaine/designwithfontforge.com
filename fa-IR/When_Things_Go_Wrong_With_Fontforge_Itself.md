---
published: true
layout: bookpage_fa-IR
weight: 69
category: Appendices
title: مواجهه با مشکلات در فونت‌فورج
---

توسعهٔ فونت‌فورج روی گیت‌هاب انجام می‌شود.
تیم فونت‌فورج از بخش Issues برای گفتگو بر سر مشکلات، خطاها، و ایده‌های بهبود نرم‌افزار استفاده کرده
و سپس شخصی راه‌حلی را آماده و به صورت یک *Pull Request* درخواست ادغامش را با دیگران هم‌رسانی می‌کند.

NOTE: Users looking for general advice on how to use FontForge and other tools, or how to make fonts, should use the [FontForge mailing list](https://sourceforge.net/p/fontforge/mailman/fontforge-users/)

برای آن که بیشتر دربارهٔ گیت‌هاب فرابگیرید، صفحهٔ
[Good Resources for Learning Git and GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)
را ببینید.

## پرداخت برای پشتیبانی

This might be a surprise, but it is both possible and encouraged to pay for FontForge [support](https://www.reddit.com/r/opensource/comments/g5ip5f/is_it_ethical_to_pay_someone_to_develop_a_feature/) when things go wrong.

زمانی که سایر ویرایش‌گرهای فونت با امکانات تقریبا مشابه، صدها دلار امریکا هزینه در بر دارند، اگر هر کدام از کاربران مبلغ مشابهی را در ازای رفع برخی مشکلات آزاردهنده، به توسعه‌دهندگان فونت‌فورج پرداخت کنند، فونت‌فورج بهتر و بهتر خواهد شد.

There are a number of websites that provide resources for users and supporters who
are willing and interested in providing [bounties](https://en.wikipedia.org/wiki/Bug_bounty_program), [rewards](https://www.google.com/search?q=bug+bounty+reward), and work [for hire](https://www.google.com/search?q=open+source+feature+for+hire).

So, how would you go about doing this?

Find a reputable website as per the suggested lists above which is able to provide the sort of service you are looking for. Then, follow steps similar to this (now defunct website - FreedomSponsors = circa~2012?):

1. Create a FontForge issue describing what you want to be changed (see below). Copy the URL of the issue to the clipboard.
2. Visit FreedomSponsors and sponsor a new issue, using the URL you copied earlier.
3. Revisit the issue and add a comment with the link to the FreedomSponsors issue page, with a personal note that you're offering a paid bounty for this issue to be closed.

NOTE: Rather than delete and replace the Freedomsponsor website listed above, it made more sense to leave it listed above as an acknowledgement to you/us/everyone, that some websites will appear and eventually fadeout with time, so it's worth your time to choose a reputable site that is expected to stay-around a while.

## گزارش یک مشکل

1. به [بخش گزارش مشکلات روی گیت‌هاب فونت‌فورج](https://github.com/fontforge/fontforge/issues) رفته و وارد حساب گیت‌هاب‌تان شوید. اگر حساب ندارید، حسابی بسازید.
2. در بخش جستجو، برای بررسی این که آیا مشکل مشابهی پیش‌تر گزارش شده است یا خیر تلاش کنید. غیر از گزارش‌های باز، گزارش‌های بسته‌شده را نیز بررسی کنید.
اگر مشکل مشابهی قبلا گزارش شده اما کاملا با مشکل شما تطابق ندارد، زیر همان گزارش نظر جدیدی بگذارید.
3. اگر مشکل شما پیش‌تر گزارش نشده، گزارش جدیدی بسازید.
روی دکمهٔ New Issue کلیک کنید.
عنوانی کوتاه و توصیفی بنویسید و سپس در بخش اصلی، درباره مشکل‌تان و این که چه چیز باعث بروز آن شد بنویسید و یا اگر ایده‌ای برای بهبود دارید، درج کنید.

جزئیات مرتبط مانند موارد زیر را نیز در گزارش خود شامل کنید:

* نوع و نسخهٔ سیستم‌عامل
* نسخهٔ فونت‌فورج و این که از کجا آن را تهیه کرده‌اید
* **گام به گام توضیح دهید که برای بازتولید مشکل چه کارهایی باید انجام شود**
* **چه پیام خطایی دریافت می‌کنید**
* **انتظار دارید چه اتفاقی رخ دهد**

می‌توانید تصویری از محیط نرم‌افزار در زمان بروز مشکل تهیه کرده و به گزارش‌تان ضمیمه کنید.

راه سادهٔ دیگری که می‌توانید برای گزارش مشکل انجام دهید، ضبط فیلم از صفحهٔ نمایش است که در آن درباره مشکل توضیح بدهد. ویدئو را در جایی روی اینترنت بارگذاری کرده و پیوندش را در گزارش قرار دهید.

برای این که امکان بازتولید مشکل توسط توسعه‌دهندگان وجود داشته باشد، بارگذاری پروندهٔ فونتی که روی آن کار می‌کنید نیز می‌تواند مفید باشد.
اگر بتوانید پرونده را با حذف کردن بخش‌هایی که به مشکل‌تان مربوط نیست کوچک‌تر کنید، انتشعابی (fork) از مخزن فونت‌فورج گرفته و پرونده‌تان را در پوشهٔ
[/tests/fonts](https://github.com/fontforge/fontforge/tree/master/tests/fonts)
بارگزاری کنید و به صورت یک Pull Request برای توسعه‌دهندگان بفرستید.
در نهایت، اگر تمایل ندارید که پرونده‌تان به صورت عمومی در دسترس باشد، می‌توانید رایانامه‌ای را در اختیار توسعه‌دهندگان فونت‌فورج قرار دهید تا بتوانند برای دریافت خصوصی پرونده با شما ارتباط بگیرند.

Please don't close other people's issues &mdash; ask them to close the issue if it is closed to their satisfaction.

## شیوهٔ گزارش یک فروپاشی (Crash)

فرایند گزارش یک فروپاشی یا انواع دیگر مشکلات (bugs) همانند گزارش ویژگی‌های جدید یا طرح سوال است.
ارسال گزارش فروپاشی خوب می‌تواند به توسعه‌دهندگان فونت‌فورج برای بهبود پایداری برنامه برای همگان کمک کند!
از گزارش چنین مسائلی خجالت نکشید، زیرا فروپاشی‌ای که گزارش نشده است، فروپاشی‌ای است که احتمال رفع آن بسیار کم است.

اگر فونت‌فورج حین استفاده دچار فروپاشی شد، یک گزارش (issue) به روشی که بالاتر گفته شد ایجاد کنید.
اگر یک پروندهٔ فونت خاص (مثلا ttf یا sfd یا غیره) دارید که موجب تحریف فروپاشی می‌شود، می‌توانید آن را جایی روی اینترنت بارگذاری کرده و نشانی‌اش را در گزارش درج کنید.
همچنین با روشی که بالاتر گفته شد می‌توانید رایانامه‌تان را در اختیار توسعه‌دهندگان قرار دهید تا برای دریافت خصوصی پرونده با شما تماس بگیرند.

با توضیحاتی که منتشر می‌کنید، توسعه‌دهندگان فونت‌فورج تلاش خواهند کرد تا فروپاشی را بازتولید کنند.
انجام این کار، آن‌ها را قادر می‌سازد تا روی مشکل کار کرده و عامل فروپاشی را شناسایی و آن را رفع کنند.

پس از ادغام شدن Pull Request حاوی راه‌حل، نیاز به دریافت نسخهٔ جدید فونت‌فورج دارید.
برای این منظور یکی از کارهای زیر را انجام دهید:

* بر اساس آخرین تغییرات کد منبع روی گیت‌ها، کامپایل جدید بگیرید (
[نصب فونت‌فورج](Installing_Fontforge.html)
را ببینید)
* وجود ساخت‌های روزانه را بررسی کنید ( معمولا ساخت‌های روزانه برای
[مکینتاش](http://fontforge.github.io/en-US/downloads/mac/)
وجود دارد)
* wait until the next [release](https://github.com/fontforge/fontforge/releases) (average of yearly).

### بهترین گزارش‌های فروپاشی

برای کمک به توسعه‌دهندگان تلاش کنید تا مشکل را پیدا کرده و **واقعا** تلاش کنید بفهمید چگونه می‌شود آن را درست کرد.
می‌توانید این کار را با تهیهٔ گزارش عملکرد برنامه (backtrace) انجام دهید.
گزارش backtrace حاوی فهرستی از توابعی از برنامه است که در طول اجرای برنامه، توسط تابع دیگری فراخوانی شده‌اند.
در این گزارش می‌تواند دید که در کدام فراخوانی، برنامه دچار فروپاشی شده است.
یک گزارش backtrace، به خصوص اگر شمارهٔ خط توابع را نیز شامل شود بسیار می‌تواند سودمند باشد.

برای ایجاد یک backtrace ممکن است نیاز به نصب فونت‌فورج از روی کد منبع و با با شامل کردن _debugging information_ داشته باشید.
از فرامین `type` و `nm` برای پیدا کردن مسیر و وضعیت پروندهٔ دودویی فونت‌فورج استفاده کنید.
مثلا:

```sh
$ type -all fontforge;
fontforge is /usr/bin/fontforge
$ nm /usr/bin/fontforge;
nm: /usr/bin/fontforge: no symbols
```

در این مثال `no symbols` را می‌بینیم که یعنی باید نصب‌مان را با شامل کردن debug information به‌روز کنیم.

#### نصب Debugging Information روی فدورا

فدورا در مخزن استاندارد، فرمانی را برای تسهیل نصب debugging information برای فونت‌فورج ارائه می‌دهد.
(توجه کنید که اگر بسیاری از وابستگی‌ها را نداشته باشید، این کار ممکن است نیاز به صرف چند صد مگابایت برای دریافت پرونده‌ها داشته باشد)
برای نصب، دستور زیر را اجرا کنید:

```sh
debuginfo-install fontforge;
```

## Using the GNU Debugger to Report Crashes

گزارش backtrace توسط اشکال‌یاب پروژه گنو (GNU Project Debugger) و با فرمان `gdb` قابل تولید است.
شما هم می‌توانید gdb را به نمونهٔ در حال اجرای فونت‌فورج متصل کرده و هم می‌توانید فونت‌فورج را داخل یک نشست gdb اجرا کنید.
اینجا، مثلی از دومی را می‌توایند ببینید:

```
$ gdb fontforge;
GNU gdb (GDB) Fedora (7.3.50.20110722-16.fc16)
Copyright (C) 2011 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.  Type "show copying"
and "show warranty" for details.
This GDB was configured as "x86_64-redhat-linux-gnu".
For bug reporting instructions, please see:
<http://www.gnu.org/software/gdb/bugs/>...
Reading symbols from /usr/local/bin/fontforge...done.
```

اکنون اگر با فرمان run اشکال‌یاب را فعال کنید، فونت‌فورج روی صفحه باز می‌شود:

```
(gdb) run
Starting program: /usr/local/bin/fontforge
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib64/libthread_db.so.1".
Copyright (c) 2000-2012 by George Williams.
 Executable based on sources from 14:57 GMT 31-Jul-2012-ML-TtfDb-D.
 Library based on sources from 14:57 GMT 31-Jul-2012.
```

از اینجا به بعد می‌توانید فونت‌فورج را به همان شیوهٔ معمول استفاده کنید اما اکنون این مزیت را دارید که می‌توانید به شکل مؤثری مشکلاتی که فونت‌فورج احتمالا پیدا کند را ثبت و گزارش کنید.

یک تفاوت عمده که اجرای فونت‌فورج داخل نشست gdb ایجاد می‌کند، شیوه‌ای است که فروپاشی بروز می‌کند.
بدون gdb، وقتی فونت‌فورج دچار فروپاشی شود، از صفحهٔ نمایش ناپدید می‌شود.
اما وقتی آن را داخل gdb اجرا می‌کنید، فونت‌فورج فروپاشی‌کرده همچنان با همان واسط کاربری‌اش باز باقی می‌ماند.

اگر واسط کاربری، واکشی نشان نمی‌دهد، به همان پایانه یا ترمینالی که gdb را در آن اجرا کرده بودید برگردید. ممکن است چیزی مثل `SIGSEGV` را در متنی که ببنید که بعد از آن یک اعلان `(gdb)` وجود دارد.
اگر اعلان `(gdb)` را می‌بینید، فونت‌فورج دیگر در حال اجرا نیست.

اکنون (بالاخره!) می‌توانید از فرمان `bt`برای دریافت گزارش backtrace استفاده کنید.
پس از این می‌توانید با فرمان `quit` از نشست gdb خارج شود تا فونت‌فورج دچار فروپاشی، بسته شود.
این، مثال از گزارش backtrace است:

```
Program received signal SIGSEGV, Segmentation fault.
0x00007ffff74a7c01 in ?? () from /lib/x86_64-linux-gnu/libc.so.

(gdb) bt
#0  0x00007ffff74a7c01 in ?? () from /lib/x86_64-linux-gnu/libc.so.6
#1  0x00007ffff6389a80 in copy (str=0x900000008) at memory.c:82
#2  0x00007ffff7a4aeb5 in KCD_AutoKernAClass (kcd=kcd@entry=0xe80c40, index=2, is_first=is_first@entry=1)
    at kernclass.c:236
#3  0x00007ffff7a51405 in KCD_FinishEdit (g=0xeb0fe0, r=1, c=, wasnew=1) at kernclass.c:2020
#4  0x00007ffff5effe2d in GME_SetValue (gme=gme@entry=0xeb0fe0, g=0xe94760) at gmatrixedit.c:988
#5  0x00007ffff5f00554 in GME_FinishEdit (gme=0xeb0fe0) at gmatrixedit.c:997
#6  0x00007ffff5f01c1a in GMatrixEditGet (g=g@entry=0xeb0fe0, rows=rows@entry=0x7fffffffcf78)
    at gmatrixedit.c:2214
#7  0x00007ffff7a4ea3c in KCD_Expose (event=0x7fffffffd1e0, pixmap=0x83ae00, kcd=0xe80c40)
    at kernclass.c:1446
#8  kcd_e_h (gw=0x83ae00, event=0x7fffffffd1e0) at kernclass.c:1762
#9  0x00007ffff5eabe8f in _GWidget_Container_eh (gw=gw@entry=0xe7f040, event=event@entry=0x7fffffffd1e0)
    at gcontainer.c:269
#10 0x00007ffff5eac385 in _GWidget_TopLevel_eh (event=0x7fffffffd1e0, gw=0xe7f040) at gcontainer.c:734
#11 _GWidget_TopLevel_eh (gw=0xe7f040, event=0x7fffffffd1e0) at gcontainer.c:606
#12 0x00007ffff5ef86ce in GXDrawRequestExpose (gw=0xe7f040, rect=0xef72b0, doclear=)
    at gxdraw.c:2687
#13 0x00007ffff5eea075 in gtextfield_focus (g=0xef72a0, event=0x7fffffffd2e0) at gtextfield.c:1888
#14 0x00007ffff5eaa857 in _GWidget_IndicateFocusGadget (g=0xe94760, mf=mf@entry=mf_normal)
    at gcontainer.c:143
#15 0x00007ffff5eaac97 in GWidgetIndicateFocusGadget (g=) at gcontainer.c:155
#16 0x00007ffff5f02b1e in GME_StrSmallEdit (event=0x7fffffffd670, str=0xe10e60 "A", gme=0xeb0fe0)
    at gmatrixedit.c:890
#17 GMatrixEdit_StartSubGadgets (gme=gme@entry=0xeb0fe0, r=1, c=c@entry=0, event=event@entry=0x7fffffffd670)
    at gmatrixedit.c:1472
#18 0x00007ffff5f03d69 in GMatrixEdit_MouseEvent (event=0x7fffffffd670, gme=0xeb0fe0) at gmatrixedit.c:1499
#19 matrixeditsub_e_h (gw=, event=0x7fffffffd670) at gmatrixedit.c:1735
#20 0x00007ffff5eabd98 in _GWidget_Container_eh (gw=0xeeb2e0, event=0x7fffffffd670) at gcontainer.c:393
#21 0x00007ffff5ef6555 in dispatchEvent (gdisp=gdisp@entry=0x769a50, event=event@entry=0x7fffffffd9b0)
    at gxdraw.c:3475
#22 0x00007ffff5ef7d1e in GXDrawEventLoop (gd=0x769a50) at gxdraw.c:3574
#23 0x00007ffff7ad353a in fontforge_main (argc=, argv=) at startui.c:1196
#24 0x00007ffff736676d in __libc_start_main () from /lib/x86_64-linux-gnu/libc.so.6
#25 0x00000000004006e1 in _start ()
(gdb) quit
A debugging session is active.

       Inferior 1 [process 19196] will be killed.

Quit anyway? (y or n) y
```

یک توسعه‌دهنده می‌تواند در چنین گزارشی ببیند که فونت‌فورج داخل تابع `‬copy` دچار فروپاشی شده است.
تابع `‬copy` توسط تابع دیگری به نام `KCD_AutoKernAClass` فراخوانی شده است.
گزارش backtrace به یک توسعه‌دهندهٔ نرم‌افزار، خطوط دقیقی که در آن‌ها این فراخوانی‌ها صورت پذیرفته و همچنین راهنمایی در خصوص نامعتبر بودن پارامترهایی که به تابع `copy` داده شده بودند را می‌گوید.
این اطلاعات کمک بزرگی برای اصلاح برنامه می‌کنند.

Use gdb's quit command in gdb to exit gdb and close the crashed FontForge.

