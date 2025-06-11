# 🛍️ Amazon Product Scraper

This Python script allows you to **scrape product details from Amazon.in** based on a search keyword and the number of pages you want to scrape. It collects:

- 📦 Product Titles  
- 💰 Product Prices  
- 🔗 Product URLs  

The scraped data is saved into a **cleanly formatted Excel file**.

---

## 📌 Features

- GUI input prompts using `Tkinter` – no need to use terminal.
- Scrapes multiple pages of Amazon search results.
- Automatically stores product data in an `.xlsx` file.
- Retrieves accurate prices and product links.
- Simple and customizable codebase for future modifications.

---

## ⚙️ Requirements

Make sure you have the following installed:

### 🐍 Python Packages

Install all required Python packages using pip:

```bash
pip install selenium openpyxl pyautogui
```

### 🌐 Browser & Driver

- **Google Chrome** (latest version recommended)
- **ChromeDriver** matching your Chrome version  
  [Download here](https://sites.google.com/a/chromium.org/chromedriver/downloads)

Ensure `chromedriver` is added to your **system PATH** or placed in the same folder as the script.

---

## 🚀 How to Use

1. Clone or download this repository.
2. Run the script:

```bash
python main.py
```

3. A GUI will pop up asking:
   - 📥 **Search term** (e.g., "headphones", "laptop")
   - 📄 **Number of pages to scrape** (e.g., 2, 5, 10)

4. Wait for the scraping to complete. A file will be generated in the same directory:

```
Details for <your_search_term>.xlsx
```

5. ✅ Done! Open the Excel file to see the product titles, prices, and links.

---

## 📁 Output Format (Excel)

| Title                  | Price in ₹ | URL of the product                         |
|------------------------|------------|--------------------------------------------|
| Example Product Name   | 2,499      | https://www.amazon.in/example-product-url  |

---

## 🧠 Notes

- 🛑 This script is for educational purposes only.  
- Amazon's website structure may change over time, which could break the XPaths.
- You might need to **update Selenium** and **ChromeDriver** if things stop working.

To update Selenium:

```bash
pip install --upgrade selenium
```

---

## 🛠️ Customization

### Run in Headless Mode

Uncomment the following line in the code to run without opening the browser:

```python
# options.add_argument("--headless")
```

### Change Marketplace

By default, the script scrapes from `https://www.amazon.in`. To scrape from other marketplaces (e.g., `.com`, `.co.uk`), update the base URL in this line:

```python
driver.get(f"https://www.amazon.in/s?k={word}&page={page}")
```

---

## 🧾 License

This project is open-source and available under the MIT License.

---

## 🙋‍♂️ Author

**Wolfie Crypto**  
Built with ❤️ using Python, Selenium & OpenPyXL
