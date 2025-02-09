# 🧹 Refiner - Unused Code & Asset Cleaner

🚀 **A powerful tool to detect and remove unused PHP files, functions, variables, images, CSS, JavaScript, and dependencies in large projects.**  

---

## 📖 Overview  
Refiner helps developers maintain a clean codebase by identifying and removing:  
- **Unused PHP code** (files, functions, variables, classes).  
- **Unused front-end assets** (images, CSS, JavaScript).  
- **Unused dependencies** in `composer.json` and `package.json`.  

### 🔍 Why use Refiner?  
✅ Improve **code maintainability** by removing dead code.  
✅ Reduce **project size** by eliminating unused assets.  
✅ Increase **performance** by optimizing front-end files.  
✅ Prevent security risks from old, unmaintained dependencies.  

---

## ✨ Features  
✔️ **PHP Code Analysis** – Detects and removes unused PHP files, functions, and variables using PHPStan/Psalm.  
✔️ **Asset Cleanup** – Finds and removes unused images, CSS, and JavaScript files.  
✔️ **Dependency Cleanup** – Detects unused Composer and npm dependencies.  
✔️ **Custom Scans** – Choose which parts of the project to scan.  
✔️ **Comprehensive Reports** – Outputs detailed logs of unused files.  
✔️ **CLI & Web Dashboard Support** – Flexible usage for developers.  

---

## 🛠 Installation  

### **Prerequisites**  
Ensure you have the following installed:  
- PHP `>=8.0`  
- Composer  
- Node.js & npm  
- Git  

### **Clone the Repository**  
```bash
git clone https://github.com/geremi101/refiner.git
cd refiner
```

### **Install Dependencies**  
```bash
# Install PHP dependencies
composer install

# Install Node.js dependencies
npm install
```

---

## 🚀 Usage  

### **Command-Line Interface (CLI) Usage**  
Run Refiner via CLI to scan for unused files:  
```bash
php refiner.php --scan php,assets,dependencies --exclude logs/,tests/
```

#### **Available CLI Options:**  
| Option               | Description |
|----------------------|-------------|
| `--scan php`        | Scan for unused PHP code |
| `--scan assets`     | Scan for unused images, CSS, and JavaScript |
| `--scan dependencies` | Scan for unused Composer/npm dependencies |
| `--exclude path`    | Exclude specific directories from the scan |
| `--output json`     | Output results in JSON format |

---

### **Web Dashboard Usage (Optional)**
If you're using the web interface, start the local server:  
```bash
php -S localhost:8000 -t web
```
Then open [http://localhost:8000](http://localhost:8000) in your browser.

---

## 📋 Example Output  

```plaintext
🔍 Scanning for unused files...

✅ PHP Files:
- controllers/oldController.php (Not referenced anywhere)
- models/unusedModel.php (No active usage found)

✅ Unused Assets:
- assets/images/oldImage.png (Not found in HTML/CSS)
- assets/css/unusedStyles.css (Not referenced in any files)

✅ Unused Dependencies:
- monolog/monolog (Not used in PHP files)
- lodash (Not used in JS files)

💡 Suggested Cleanup: Use the --delete flag to remove unused files.
```

To delete all detected unused files:  
```bash
php refiner.php --delete
```

---

## 🛠 Configuration  
You can configure Refiner via `config.json`:  

```json
{
  "exclude": ["logs/", "tests/"],
  "outputFormat": "json",
  "enableAutoDelete": false
}
```

---

## 🤝 Contributing  

🔥 We welcome contributions! To get started:  
1. **Fork the repository**  
2. **Create a feature branch**:  
   ```bash
   git checkout -b feature-new-scanner
   ```
3. **Commit changes**:  
   ```bash
   git commit -m "Added new feature"
   ```
4. **Push to GitHub**:  
   ```bash
   git push origin feature-new-scanner
   ```
5. **Create a Pull Request**  

---

## 🛡 Security Considerations  
- Refiner does not delete files unless explicitly specified (`--delete`).  
- Always **review reports** before running destructive actions.  
- Keep your dependencies up-to-date to avoid vulnerabilities.  

---

## 📜 License  
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.  

---

## 📞 Need Help?  
If you have any questions or feature requests, feel free to:  
- Open an [Issue](https://github.com/geremi101/refiner/issues).  
- Join our **developer Discord community** (Link here).  

---

### 🎯 Future Roadmap
🔹 Improve accuracy of PHP function and variable detection.  
🔹 Add support for Laravel and Symfony-specific cleanup.  
🔹 Web-based UI improvements.  

💡 **Got an idea?** Open an issue and let’s discuss it!  
