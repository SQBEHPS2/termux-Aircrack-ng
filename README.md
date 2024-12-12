
# 🎉 **How to Install Aircrack-ng on Termux** 🎉

### **Are you encountering the following error?**
```
E: Unable to locate package aircrack-ng
```
Don’t worry! This is due to the removal of the **aircrack-ng** package from the official Termux repository. Let’s fix it together with a simple manual installation!

---

## 🚀 **Why Does This Happen?**
The **aircrack-ng** package was removed from Termux’s root repository, which leads to the installation error. But no worries, we'll guide you through installing it manually!

---

## 🛠️ **Solution: Manual Installation of Aircrack-ng**

Let’s manually install **aircrack-ng** in Termux, step by step. 🌟

---

### 1️⃣ **Install Termux**
First, make sure you have Termux installed on your device. You can download it from [F-Droid](https://f-droid.org/).

---

### 2️⃣ **Update & Upgrade Your Packages**
To ensure you have the latest packages and dependencies, run the following commands:

```bash
apt update && apt upgrade -y && pkg install wget -y && apt install libc++ libnl libpcap libsqlite openssl pcre zlib -y
```
This will ensure your Termux environment is up-to-date.

---

### 3️⃣ **Check Your Device Architecture**
Next, we need to determine your device architecture to download the correct version of **aircrack-ng**.  
Run the following command:

```bash
uname -m
```

For example, if your architecture is `aarch64`, that's the version you'll need to download.  
🧐 **Architecture Example:**  
![Architecture Screenshot](https://user-images.githubusercontent.com/95903270/218307987-bf49478d-b54f-439e-b33a-04526119c5a4.jpg)

---

### 4️⃣ **Download & Install the Correct Version of Aircrack-ng**

Here are the commands for each architecture. Choose the one that matches your device:

- **For `aarch64` (64-bit ARM):**
   ```bash
   wget https://raw.githubusercontent.com/pitube08642/aircrack-ng-for-termux/main/dists/termux/aircrack-ng/binary-aarch64/aircrack-ng_3_1.7_aarch64.deb && dpkg -i aircrack-ng_3_1.7_aarch64.deb && rm aircrack-ng_3_1.7_aarch64.deb
   ```

- **For `arm` (32-bit ARM):**
   ```bash
   wget https://raw.githubusercontent.com/pitube08642/aircrack-ng-for-termux/main/dists/termux/aircrack-ng/binary-arm/aircrack-ng_3_1.7_arm.deb && dpkg -i aircrack-ng_3_1.7_arm.deb && rm aircrack-ng_3_1.7_arm.deb
   ```

- **For `i686` (32-bit x86):**
   ```bash
   wget https://raw.githubusercontent.com/pitube08642/aircrack-ng-for-termux/main/dists/termux/aircrack-ng/binary-i686/aircrack-ng_3_1.7_i686.deb && dpkg -i aircrack-ng_3_1.7_i686.deb && rm aircrack-ng_3_1.7_i686.deb
   ```

- **For `x86_64` (64-bit x86):**
   ```bash
   wget https://raw.githubusercontent.com/pitube08642/aircrack-ng-for-termux/main/dists/termux/aircrack-ng/binary-x86_64/aircrack-ng_3_1.7_x86_64.deb && dpkg -i aircrack-ng_3_1.7_x86_64.deb && rm aircrack-ng_3_1.7_x86_64.deb
   ```

---

## ✅ **Installation Complete!**

You have successfully installed **aircrack-ng** on Termux. 🎉

---

## 🧪 **Test Aircrack-ng**

To verify the installation, simply run:

```bash
aircrack-ng -S
```

This will display the current version of **aircrack-ng** and ensure everything is working correctly.

---

## 📌 **Quick Tips:**
- **Keep Termux updated**: Regularly run `apt update && apt upgrade` to ensure your environment is up-to-date.
- **Check dependencies**: If you encounter issues, double-check that all dependencies are installed using the command:
  ```bash
  apt install libc++ libnl libpcap libsqlite openssl pcre zlib
  ```

---

## 📝 **License**

This project is licensed under the **MIT License**.  
For more details, visit the [MIT License page](https://opensource.org/licenses/MIT).

---

## 💬 **Feedback & Contributions**

We’d love to hear your feedback or contributions! If you run into any issues or need help, feel free to reach out. Happy cracking! 🔐

---

### **Thank You!** 🙏
