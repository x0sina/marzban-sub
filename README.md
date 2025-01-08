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

	2.	Run the following commands in your server terminal:

echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"' | sudo tee -a /opt/marzban/.env
echo 'SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"' | sudo tee -a /opt/marzban/.env

Alternatively, uncomment the following values in the .env file located in /opt/marzban by removing the # symbol:

CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"
SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"


	3.	Restart Marzban:

marzban restart



Update

To update the template, repeat step 1.

Default Language

To change the default language, go to the end of the HTML file and adjust the select tag for your preferred language. Example:

<select id="countries" class="border text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 bg-gray-700 border-gray-600 placeholder-gray-400 text-white">
  <option value="fa">فارسی</option>
  <option value="en">English</option>
  <option value="ru">Русский</option>
</select>

In this example, the default language is Persian.

Personalization

To customize the Telegram ID, background image, and user logo:
	1.	Open the HTML file using nano:

nano /var/lib/marzban/templates/subscription/index.html


	2.	Use Ctrl + W to search for and replace the following values:
	•	Telegram Support ID: Search for:

https://t.me/yourID


	•	User Logo: Search for:

images/marzban.svg


	•	Background Image: Search for:

background: url('https://4kwallpapers.com


	3.	Save the changes and restart Marzban.

Host Version

To use the host version, upload the sub folder to your host, then edit the BASE_URL value in the index.php file to match your panel address. Example:

const BASE_URL = "https://BaseUrl:PORT";

If you don’t have an SSL certificate for your panel domain, use http.

Copyright

This template is based on the design of Marzban Templates.

