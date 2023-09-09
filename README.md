<p align="center">
  <a href="https://github.com/x0sina/marzban-sub" target="_blank" rel="noopener noreferrer" >
    <img src="https://github.com/MuhammadAshouri/marzban-templates/blob/dca23a0ecbee84839686a1b928a2dc7e8aba4089/template-01/screenshot.jpg" alt="SubPage screenshots" width="800" height="auto">
  </a>
</p>

# Usage

First you need to copy [html file](https://github.com/x0sina/marzban-sub/blob/main/index.html) to your sever. You can do it by this:

```bash
cd /opt/marzban
apt install wget
wget https://raw.githubusercontent.com/x0sina/marzban-sub/main/index.html
```

Then you have to map it to your docker container. Add this line to volume section of `docker-compose.yml`:

(DO NOT REPLACE WHOLE FILE, Just the last line)
```docker
services:
    marzban:
        ...
        volumes:
            ...
            - /opt/marzban/index.html:/code/app/templates/subscription/index.html # this line
```

Now you can restart your marzban's docker:
```
marzban restart
```

# استفاده

ابتدا فایل [html file](https://github.com/x0sina/marzban-sub/blob/main/index.html) رو به سرور بفرستید. با دستور زیر میتونید این کارو بکنید:

```bash
cd /opt/marzban
apt install wget
wget https://raw.githubusercontent.com/x0sina/marzban-sub/main/index.html
```

حالا باید این فایل به به داکر مپ کنید. خط آخر رو به بخش volumes فایل `docker-compose.yml` اضافه کنید:

(کل فایل رو جایگزین نکنید!!! فقط خط آخر)
```docker
services:
    marzban:
        ...
        volumes:
            ...
            - /opt/marzban/index.html:/code/app/templates/subscription/index.html # this line
```

حالا مرزبان رو ری‌استارت کنید:
```
marzban restart
```
