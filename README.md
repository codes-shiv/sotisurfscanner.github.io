# 📷 SOTI Surf Scanner Web Interface

A lightweight and responsive barcode scanning web project designed to interact with Android native functionality via JavaScript interfaces. This web interface can be deployed to [GitHub Pages](https://pages.github.com/) and is ideal for integrating with enterprise Android applications using **WebView** and **Android-JS communication**.

---

## ✨ Features

- ✅ **Barcode scanning via camera**
- 🔁 **Focus management** for seamless scanning
- 📱 **Android integration** through JavaScriptInterface
- 🌐 **Responsive UI** for tablets and phones
- 🧠 **Error handling** and feedback pages
- 💡 **Modular screens** like `index.html`, `display.html`, `feedback.html`, `screens.html`, etc.

---

## 📁 Project Structure

| File/Folder        | Purpose                                 |
|--------------------|------------------------------------------|
| `index.html`       | Landing page with camera scanning       |
| `camerascanning.html` | Fullscreen camera scanner UI          |
| `screens.html`     | Screen manager with navigation          |
| `display.html`     | Result display logic                    |
| `feedback.html`    | Feedback form                           |
| `connection.html`  | Connection/disconnect logic             |
| `error.html`       | Error page for fallback                 |
| `NoMatch.html`     | Shown when no barcode match found       |
| `success.html`     | Shown on successful scan                |
| `styles.css`       | Custom styles for UI                    |
| `app_icon.png`     | App icon for branding                   |
| `proglove.jpg`     | Reference image                         |

---

## 📲 Android Integration

This project is meant to be loaded inside an Android WebView with a JS interface.  
Ensure the WebView is configured like this:

```java
webView.getSettings().setJavaScriptEnabled(true);
webView.addJavascriptInterface(new BarcodeJSInterface(), "AndroidFunction");
webView.loadUrl("file:///android_asset/index.html");
