# Problem
The error `E: Unable to locate package aircrack-ng` occurs when trying to install **aircrack-ng** in Termux using the command:
```
pkg install aircrack-ng
```
![Error Screenshot](https://user-images.githubusercontent.com/95903270/218306989-1c45813f-6f59-44c7-843e-d95160018101.jpg)

---

# Reason Behind the Problem
The Termux team has removed the **aircrack-ng** package from its root repository.

---

# Solution
To resolve this issue, we need to manually install **aircrack-ng** in Termux.

---

# Installation
1. **Install Termux** from [F-Droid](https://f-droid.org/).  
2. Update and upgrade packages:  
   ```
   apt update && apt upgrade -y
   ```
3. Install `wget`:  
   ```
   pkg install wget -y
   ```
4. Install necessary dependencies:  
   ```
   apt install libc++ libnl libpcap libsqlite openssl pcre zlib -y
   ```
5. Determine your device architecture:  
   ```
   uname -m
   ```  
   Example: My device architecture is `aarch64`.  
   ![Architecture Screenshot](https://user-images.githubusercontent.com/95903270/218307987-bf49478d-b54f-439e-b33a-04526119c5a4.jpg)

6. Download the appropriate `.deb` file based on your architecture:  
   - For `aarch64`:  
     ```
     wget https://raw.githubusercontent.com/pitube08642/aircrack-ng-for-termux/main/dists/termux/aircrack-ng/binary-aarch64/aircrack-ng_3_1.7_aarch64.deb
     ```  
   - For `arm`:  
     ```
     wget https://raw.githubusercontent.com/pitube08642/aircrack-ng-for-termux/main/dists/termux/aircrack-ng/binary-arm/aircrack-ng_3_1.7_arm.deb
     ```  
   - For `i686`:  
     ```
     wget https://raw.githubusercontent.com/pitube08642/aircrack-ng-for-termux/main/dists/termux/aircrack-ng/binary-i686/aircrack-ng_3_1.7_i686.deb
     ```  
   - For `x86_64`:  
     ```
     wget https://raw.githubusercontent.com/pitube08642/aircrack-ng-for-termux/main/dists/termux/aircrack-ng/binary-x86_64/aircrack-ng_3_1.7_x86_64.deb
     ```  

7. Install the `.deb` file for your architecture:  
   - For `aarch64`:  
     ```
     dpkg -i aircrack-ng_3_1.7_aarch64.deb
     ```  
   - For `arm`:  
     ```
     dpkg -i aircrack-ng_3_1.7_arm.deb
     ```  
   - For `i686`:  
     ```
     dpkg -i aircrack-ng_3_1.7_i686.deb
     ```  
   - For `x86_64`:  
     ```
     dpkg -i aircrack-ng_3_1.7_x86_64.deb
     ```  

8. Congratulations! You have successfully installed **aircrack-ng** on your non-rooted phone using Termux.

---

# Testing
To test **aircrack-ng** and check your device's password-cracking speed, run:  
```
aircrack-ng -S
```  