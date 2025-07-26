### 🌐 Web Scraping in Python

**Web scraping** is the process of **extracting data from websites**. Python offers powerful libraries like `requests` and `BeautifulSoup` to help you scrape web content efficiently.

---

## ✅ Required Libraries

Install them with:

```bash
pip install requests beautifulsoup4
```

---

## 🔹 Step-by-Step Example

```python
import requests
from bs4 import BeautifulSoup

# Step 1: Send a request to the webpage
url = 'https://example.com'
response = requests.get(url)

# Step 2: Parse the HTML content
soup = BeautifulSoup(response.text, 'html.parser')

# Step 3: Extract specific elements
title = soup.title.text
print("Page Title:", title)

# Example: Find all paragraph tags
paragraphs = soup.find_all('p')
for p in paragraphs:
    print(p.text)
```

---

## 🔍 Useful `BeautifulSoup` Methods

| Method                      | Description                                |
| --------------------------- | ------------------------------------------ |
| `soup.title`                | Gets the `<title>` tag                     |
| `soup.find(tag)`            | Finds first occurrence of a tag            |
| `soup.find_all(tag)`        | Finds all occurrences of a tag             |
| `soup.find(id='value')`     | Finds element by ID                        |
| `soup.find(class_='value')` | Finds element by class name                |
| `.text`                     | Gets the text inside a tag                 |
| `.get('href')`              | Gets the value of an attribute (e.g. link) |

---

## 🔗 Example: Get All Links

```python
links = soup.find_all('a')

for link in links:
    href = link.get('href')
    print(href)
```

---

## 🛡️ Responsible Scraping Tips

* Always check the website's `robots.txt`: `https://example.com/robots.txt`
* Avoid overloading servers — use delays between requests:

```python
import time
time.sleep(1)
```

* Use a custom user-agent to identify your bot politely:

```python
headers = {'User-Agent': 'MyScraperBot/1.0'}
response = requests.get(url, headers=headers)
```

---

## 🧠 Summary

| Tool            | Purpose                          |
| --------------- | -------------------------------- |
| `requests`      | Download HTML content            |
| `BeautifulSoup` | Parse and extract data from HTML |

