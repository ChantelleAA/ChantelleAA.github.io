---
layout: post
title: "3 Ways I’ve Learned to Scrape the Web (and When to Use Each One)"
date: 2025-04-12
categories: [intro, tutorials]
excerpt: "Scraping the web doesn’t have to be hard here are some of the tools that make it easy and efficient"
---

### 3 Ways I’ve Learned to Scrape the Web (and When to Use Each One)

I’ve been diving deep into web scraping lately as a machine learning engineer. It’s become an essential tool in my work, but I realized that there are **different levels** of complexity depending on what you’re scraping. Whether it’s static pages, dynamic content, or just basic bot-blocking websites, I’ve come across three main methods for scraping the web.

Let me walk you through them, share some of the lessons I’ve learned along the way, and show you the **tools I use** when things get tricky.

---

### 1. **Plain Scraping with `requests`: The Quick & Easy Way**

When you're scraping **simple websites** where the content is static (meaning everything you need is in the HTML), you don’t need anything fancy. **`requests`** is your go-to tool for this.

#### Example:

Here’s how I typically start scraping a static page:

```python
import requests
from bs4 import BeautifulSoup

url = "http://quotes.toscrape.com/"  # Simple static website
response = requests.get(url)
soup = BeautifulSoup(response.content, "html.parser")

# Let's extract the page title as a simple example
title = soup.title.string
print(title)
```

This is **pretty straightforward**. You send a request to the server, get the page’s HTML, and then parse it. It works well when the content you need is right there in the static HTML.

---

#### **When to Use:**

This method is perfect when the website doesn’t block bots, doesn’t require JavaScript, and the structure is simple enough to parse. Websites like [quotes.toscrape.com](http://quotes.toscrape.com/) are great examples.

---

### 2. **Handling Headers: Adding a Header to Bypass Blocked Requests**

Now, let’s step up our game. Some websites will block **basic requests** because they suspect bots are trying to scrape their data. **Headers** help us bypass this.

Websites sometimes block requests that don't look like they're coming from a real browser. So by adding headers, we make our request look legitimate.

#### Example:

```python
import requests

url = "https://httpbin.org/anything"  # A site that allows testing of headers
headers = {
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.124 Safari/537.36"
}

response = requests.get(url, headers=headers)
print(response.status_code)  # Should return a 200 if successful
```

#### **What Headers Do:**

Headers act like a disguise. They make our request look like it’s coming from a **real browser**, not a bot. This trick works with many websites that block simple bots or crawlers. **But** not all websites fall for this, so sometimes headers won’t be enough.

---

#### **When to Use:**

- Use this when you're dealing with websites that have **basic anti-bot measures** like blocking non-browser requests (think `403 Forbidden` errors).  
- Websites like [httpbin](https://httpbin.org/anything) are helpful for testing headers.

---

### 3. **When Headers Don’t Work: Enter Selenium**

When headers don’t work, or if the content is loaded **dynamically** (via JavaScript), it’s time to reach for **Selenium**.

Selenium is a tool that automates browsers. It allows you to **simulate user actions** like clicks, scrolling, and waiting for content to load.

#### Getting Started with Selenium:

To use Selenium, you’ll need two main things:
1. **Selenium Python library** (to interact with browsers)
2. **WebDriver** (a browser automation tool)

##### Step-by-Step Setup:

1. **Install Selenium:**

You’ll first need to install the Selenium library using pip. Open your terminal and run this command:

```bash
pip install selenium
```

2. **Install ChromeDriver:**

Since Selenium interacts with a real browser (Google Chrome, in this case), you need the **ChromeDriver**. ChromeDriver is a separate tool that allows Selenium to control the Chrome browser.

- Download ChromeDriver:  
  Go to the [ChromeDriver download page](https://sites.google.com/a/chromium.org/chromedriver/) and select the version that matches your Chrome version. You can check your Chrome version by going to **chrome://settings/help**.
  
- Once downloaded, extract the file and keep the `chromedriver` file in a known directory (e.g., `/path/to/chromedriver`).

3. **Use Selenium with ChromeDriver:**

Now, let’s write some code to launch the Chrome browser, load a page, and extract some content.

#### Example:

```python
from selenium import webdriver
from selenium.webdriver.common.by import By

# Set up the path to the ChromeDriver you downloaded
driver = webdriver.Chrome(executable_path='/path/to/chromedriver')

# Go to a page that loads content dynamically (example)
driver.get("https://quotes.toscrape.com/js/")  # A page with JavaScript-rendered content

# Wait for the page to load fully (you may want to use WebDriverWait here)
content = driver.find_element(By.CLASS_NAME, "quote")

print(content.text)

# Close the browser when done
driver.quit()
```

#### **What Selenium Does:**

With Selenium, you’re opening a real browser (like **Chrome** or **Firefox**) and interacting with the page just like a human would. This means it can handle **dynamic content** (JavaScript), **clicking buttons**, **scrolling**, and more.

---

#### **When to Use:**

- When a website has **dynamic content** that can’t be accessed just by scraping the HTML (e.g., the content loads after a button is clicked or a page is scrolled).
- Websites like [quotes.toscrape.com/js](https://quotes.toscrape.com/js/) or any JavaScript-heavy sites are perfect examples.
  
---

- **Got questions?** Feel free to **email me** if you're diving into web scraping or if you want to discuss which method you should use for your specific case.
- If you're starting to scrape the web, **let me know what methods have worked for you!** What’s been easy? What’s tripped you up?
