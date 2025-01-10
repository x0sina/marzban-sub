English l [Persian](/persianREADME.md)
<p align="center">
  <a href="https://github.com/x0sina/marzban-sub" target="_blank" rel="noopener noreferrer">
    <img src="https://raw.githubusercontent.com/x0sina/marzban-sub/main/PreviewTemplate.png" title="Marzban-Sub"/>
  </a>
</p>
<h1 align="center">Subscription Template for <a href="https://github.com/Gozargah/Marzban">Marzban Panel</a></h1>

## Table of Contents
- [Features](#features)
- [Installation Steps](#installation-steps)
- [Default Language](#default-language)
- [Personalization](#personalization)
- [Host Version](#host-version)

# Introduction
A simple HTML template for better display of user information.

# Features
- Quick addition of subscription links to apps.
- Links for downloading required applications.
- Supports three languages: Russian, English, Persian.
- Fancy subscription page with an appealing design.
- Ability to copy configurations with a copy icon at the bottom of the page.

# Installation Steps
1. Download the template file:
```sh
sudo wget -N -P /var/lib/marzban/templates/subscription/ https://raw.githubusercontent.com/x0sina/marzban-sub/main/index.html
```

2.	Run the following commands in your server terminal:

```sh
echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"' | sudo tee -a /opt/marzban/.env
echo 'SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"' | sudo tee -a /opt/marzban/.env
```

Alternatively, uncomment the following values in the `.env` file located in /opt/marzban by removing the # symbol:

```sh
CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"
SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"
```

3. Restart marzban
```
sudo marzban restart
```

## Update
To update the template, repeat step 1.

## Default Language
To change the default language, go to the end of the HTML file and adjust the select tag for your preferred language. Example:

```sh
<select id="countries" class="border text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 bg-gray-700 border-gray-600 placeholder-gray-400 text-white">
  <option value="fa">فارسی</option>
  <option value="en">English</option>
  <option value="ru">Русский</option>
</select>
```

In this example, the default language is Persian.

# Personalization
To personalize the Telegram ID, background image and user logo, changes must be included in the html file, which is possible by searching for some values.
To search using nano, first open the file with nano with the following command:
```
nano /var/lib/marzban/templates/subscription/index.html
```
Then open the search bar with Ctrl + W combination buttons and search for the following phrase to change Telegram support ID:
```
https://t.me/yourID
```
Search for the user's logo:
```
images/marzban.svg
```
Search for the background image:
```
background: url('https://4kwallpapers.com
```
After making changes, save the file and restart Marzban.

## Host Version
To use the host version, upload the sub folder to the host and change the value of BASE_URL to your panel address in the index.php file just like the following example. Remember to write http if you don't have an SSL for your panel domain.
```
const BASE_URL = "https://BaseUrl:PORT";
```
If you dont have an SSL certificate for your panel domain, use http.

## Copyright
This template is based on <a href="https://github.com/Gozargah/Marzban">Marzban Templates<a> design.
