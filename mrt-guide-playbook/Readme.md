<div align="center">

# 🛡️ Microsoft MRT (Malicious Software Removal Tool) — Complete Guide

![Made with Love](https://img.shields.io/badge/Made%20with❤️-Cyra-blueviolet?style=for-the-badge)
![Windows Tool](https://img.shields.io/badge/Windows-Utility-blue?style=for-the-badge&logo=windows)
![Security](https://img.shields.io/badge/Security-Malware%20Removal-red?style=for-the-badge&logo=microsoftdefender)
![Documentation](https://img.shields.io/badge/Docs-Complete-brightgreen?style=for-the-badge)

### **👨‍💻 Developer: Arun VK**

</div>

---

## 🌙 Dark-Theme Optimized Overview

This guide explains everything about the **Microsoft Malicious Software Removal Tool (MRT)** — how to open it, run scans, interpret results, and view logs.  
All images and layouts are optimized to look clean and vibrant on **GitHub’s dark mode**.

---

## 📌 What is MRT?

**MRT (Malicious Software Removal Tool)** is a built-in Windows tool that:

- Detects and removes **common high-risk malware**
- Runs automatically every month
- Can be launched manually using the **mrt** command

> ⚠️ NOTE: MRT is *not* a full antivirus. Use it with Windows Defender.

---

## 🚀 How to Open MRT

### **Method 1 — Run Dialog**
Press:

Win + R → type mrt → Enter


---

### **Method 2 — Windows Search**

<p align="center">
  <img src="https://github.com/user-attachments/assets/05cefde2-1bd2-490c-8f9b-b86c73b748a5" width="550">
</p>

---

## 🧭 Step-by-Step Guide to Using MRT

### **Step 1 — Launch MRT**

---

### **Step 2 — Welcome Screen**

<p align="center">
  <img src="https://github.com/user-attachments/assets/a9fa6f8a-5140-44ab-ac5e-e8da3e6602db" width="550">
</p>

Click **Next** to continue.

---

### **Step 3 — Select Scan Type**

<p align="center">
  <img src="https://github.com/user-attachments/assets/978e8395-134a-4fbc-bf69-fe418d97e16f" width="550">
</p>

Fast, checks common malware zones.

#### **2️⃣ Full Scan**
Deep scan of entire system (can take hours).

#### **3️⃣ Customized Scan**
Choose drives/folders manually.

Click **Next** after selecting.

---

### **Step 4 — Scan Running**

MRT scans and removes threats automatically.

---

### **Step 5 — Viewing Scan Results**
<p align="center">
  <img src="https://github.com/user-attachments/assets/e1f60890-504a-4258-8b4d-d837fdafa6e3" width="550">
</p>

Results include:

- Infections found  
- Files cleaned  
- Malware removed  

---

## 🗂️ Viewing MRT Log Files

Every scan generates a log.

**Log location:**

C:\Windows\debug\mrt.log


Open it with:

notepad C:\Windows\debug\mrt.log


---

## ⚠️ Limitations of MRT

MRT **does not** provide:

- Real-time protection  
- Full malware coverage  
- Ransomware protection  

This is why you still need **Windows Defender** ⬇️

<p align="center">
  <img src="https://github.com/user-attachments/assets/43e58c5f-324a-49bd-a4e7-bec6247888c7" width="550">
</p>

---

## 📊 Feature Comparison Table

| Feature                    | MRT Benefit                  | Limitation                       |
|---------------------------|------------------------------|----------------------------------|
| **Quick Scan**            | Fast health check            | Limited depth                    |
| **Full Scan**             | Deep system scan             | Slow                             |
| **Custom Scan**           | Targeted inspection          | User-selected only               |
| **Malware Removal**       | Yes                          | Only known threats               |
| **Real-time Protection**  | ❌ No                         | Requires Defender / Antivirus    |

---

## ✅ Summary

MRT is a useful malware cleanup utility for Windows that provides quick, reliable scanning.  
Use it alongside **Windows Defender** to maintain full system protection.

---

<div align="center">

### ⭐ If this helped you, consider starring the repo!

</div>
