# 🎨 Color GPL Contrast Analyzer

A lightweight, browser-based tool designed for designers and developers to analyze **GIMP Palette (.gpl)** files for WCAG accessibility. It automatically calculates contrast ratios between all color pairs in your palette and filters them based on your custom accessibility needs.

🚀 **[Live Demo](https://bained.github.io/color-contrast-analyzer/)** *(Note: Replace YOUR-USERNAME with your actual GitHub username after publishing)*

---

## ✨ Features

* **Drag & Drop Support:** Simply upload your `.gpl` file to start analyzing.
* **Smart Contrast Calculation:** Uses the W3C WCAG 2.1 formula to calculate relative luminance and contrast ratios.
* **Custom Threshold Slider:** Set your own contrast requirements (default is **5.3:1**).
* **Advanced Filtering:**
    * Filter by a specific color to see its compatible pairs.
    * **"Use as Background only"** mode: Focus on how other colors look as text on your selected brand color.
* **Dual Visualization:** Displays both "Dark on Light" and "Light on Dark" variations for every accessible pair.
* **Hex Code Integration:** Automatically converts RGB values to Hex for easy copying to Figma, Adobe XD, or CSS.

---

## 🛠 How It Works

The tool parses the plain-text structure of a GIMP Palette file, extracting the RGB values and color names. It then runs a combinatorial analysis:

1.  **Luminance Calculation:**
    $$L = 0.2126 \times R + 0.7152 \times G + 0.0722 \times B$$
    *(where R, G, and B are linearized coefficients)*.
2.  **Contrast Ratio:**
    $$Ratio = \frac{L1 + 0.05}{L2 + 0.05}$$
3.  **Filtering:** Only pairs meeting the user-defined threshold (e.g., 5.3) are rendered as visual cards.

---

## 🚀 Quick Start

1.  Clone this repository or download the `index.html` file.
2.  Open `index.html` in any modern web browser.
3.  Upload your `.gpl` file.
4.  Adjust the contrast slider and find your perfect accessible color combinations!

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/YOUR-USERNAME/gpl-contrast-analyzer/issues).

---
*Created with ❤️ for accessible design.*
