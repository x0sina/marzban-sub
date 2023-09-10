<p align="center">
  <a href="https://github.com/x0sina/marzban-sub" target="_blank" rel="noopener noreferrer">
    <img src="https://raw.githubusercontent.com/x0sina/marzban-sub/main/preview.png" title="Marzba-Sub"/>
  </a>
</p>
<h1 align="center"/>قالب سابسکریپشن برای پنل  <a href="https://github.com/Gozargah/Marzban">مرزبان</a></h1>

## فهرست مطالب
- [ویژگی‌ ها](#ویژگی-ها)
- [مراحل نصب](#مراحل-نصب)
- [زبان پیش فرض](#زبان-پیش-فرض)

# مقدمه
یک قالب html ساده برای نمایش بهتر اطلاعات کاربر

# ویژگی ها
- افزودن سریع لینک سابسکریپشن به برنامه ها
- لینک دانلود اپلیکیشن های مورد نیاز
- سه زبانه (روسی,انگلیسی,فارسی)
- پیج ساب فانتزی با رنگ و لعاب زیبا
- دریافت کانفیگ ها با آیکون کپی در آخر صفحه

# مراحل نصب
1. دانلود فایل template
```sh
sudo wget -N -P /var/lib/marzban/templates/subscription/  https://raw.githubusercontent.com/x0sina/marzban-sub/main/index.html
```

2. دستورات زیر رو تو ترمینال سرورتون بزنید:
```sh
echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"' | sudo tee -a /opt/marzban/.env
echo 'CLASH_SUBSCRIPTION_TEMPLATE="subscription/index.html"' | sudo tee -a /opt/marzban/.env
```
یا مقادیر زیر رو در فایل `.env` در پوشه `/opt/marzban` قرار بدین
```sh
CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"
CLASH_SUBSCRIPTION_TEMPLATE="subscription/index.html"
```

3. ری استارت مرزبان
```sh
marzban restart
```


# زبان پیش فرض
برای عوض کردن زبان پیش فرض کافیست در فایل html به آخر کد مراجعه کنید و زبان مورد نظرتونو توی تگ select بالا بیارین. مثال:
```
<select id="countries" class="border text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 bg-gray-700 border-gray-600 placeholder-gray-400 text-white :focus:ring-blue-500 :focus:border blue-500">
  <option value="fa">فارسی</option>
  <option value="en">English</option>
  <option value="ru">Русский</option>
</select>
```
در این مثال زبان اصلی فارسی است.

## بروزرسانی
برای بروزرسانی تمپلیت فقط کافیست مرحله 1 را تکرار کنید.

## کپی رایت
این قالب بر اساس طرح <a href="https://github.com/Gozargah/Marzban">Marzban Templates<a> ساخته شده.

# Table of Contents
- [Attributes](#Attributes)
- [Install Steps](#Install-Steps)
- [Default Language](#Default-Language)

# Introduction
A simple html template to better display user information

# Attributes
- Quickly add subscription links to programs
- The link to download the required applications
- Three languages (Russian, English, Persian)
- Sub fantasy page with beautiful color and glaze
- Receive the configs with the copy icon at the bottom of the page
# Install Steps
1. Download File Template
```sh
sudo wget -N -P /var/lib/marzban/templates/subscription/  https://raw.githubusercontent.com/x0sina/marzban-sub/main/index.html
```

2. Enter the following commands in your server's terminal:
```sh
echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"' | sudo tee -a /opt/marzban/.env
echo 'CLASH_SUBSCRIPTION_TEMPLATE="subscription/index.html"' | sudo tee -a /opt/marzban/.env
```
Or put the following values in `.env` file in `/opt/marzban` folder
```sh
CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"
CLASH_SUBSCRIPTION_TEMPLATE="subscription/index.html"
```

3. Restart Marzban
```sh
marzban restart
```

# Default Language
To change the default language, just refer to the end of the code in the html file and select the desired language in the select tag. Example:

```
<select id="countries" class="border text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 bg-gray-700 border-gray-600 placeholder-gray-400 text-white :focus:ring-blue-500 :focus:border blue-500">
  <option value="en">English</option>
  <option value="fa">فارسی</option>
  <option value="ru">Русский</option>
</select>
```
In this example, the main language is English.

## Update
To update the template, just repeat step 1.

## Copyright
This template is based on <a href="https://github.com/Gozargah/Marzban">Marzban Templates<a> design.
