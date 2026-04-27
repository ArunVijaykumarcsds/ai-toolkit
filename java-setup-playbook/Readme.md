# ☕ Java Installation Playbook (Windows + VS Code)

A clean step-by-step guide to install and set up Java (JDK 21) with VS Code.

---

# 📥 Step 1: Download JDK

## 🔗 Official Link

[https://www.oracle.com/java/technologies/downloads/#jdk21-windows](https://www.oracle.com/java/technologies/downloads/#jdk21-windows)

## ⚡ Direct One‑Click Download (Windows x64 .exe)

[https://download.oracle.com/java/21/latest/jdk-21_windows-x64_bin.exe](https://download.oracle.com/java/21/latest/jdk-21_windows-x64_bin.exe)

## 🪞 Backup Mirrors (if Oracle is slow)

* Adoptium (Temurin JDK 21): [https://adoptium.net/temurin/releases/?version=21](https://adoptium.net/temurin/releases/?version=21)
* Azul Zulu JDK 21: [https://www.azul.com/downloads/?version=java-21-lts&os=windows&package=jdk](https://www.azul.com/downloads/?version=java-21-lts&os=windows&package=jdk)

👉 Choose:

* Version: **JDK 21 (LTS)**
* OS: Windows
* File: **x64 Installer (.exe)** (~167 MB)

---

# ⚙️ Step 2: Install JDK

1. Open the downloaded `.exe` file
2. Click:

   * Next → Next → Install → Finish

Java will be installed in:

```
C:\Program Files\Java\jdk-21...
```

---

# ✅ Step 3: Verify Installation

Open Command Prompt and run:

```
java -version
javac -version
```

Expected output:

```
java version "21.x.x"
javac 21.x.x
```

---

# ❗ Step 4: Fix PATH (if needed)

If commands don’t work:

1. Search: **Environment Variables**
2. Open → Edit system environment variables
3. Click **Environment Variables**
4. Under System Variables → select **Path** → Edit
5. Add:

```
C:\Program Files\Java\jdk-21\bin
```

6. Click OK and restart PC

---

# 🧠 Step 5: Setup in VS Code

1. Open VS Code
2. Go to Extensions
3. Install:

   * Extension Pack for Java (Microsoft)

---

# ▶️ Step 6: Run First Java Program

## Create File

```
Hello.java
```

## Code

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello Java 🚀");
    }
}
```

## Run (Terminal)

```
javac Hello.java
java Hello
```

Expected Output:

```
Hello Java 🚀
```

---

# 🎥 Video Walkthrough (Quick)

* YouTube: [https://www.youtube.com/watch?v=Qgl81fPcLc8](https://www.youtube.com/watch?v=Qgl81fPcLc8)
  (Search: "Install Java JDK 21 Windows VS Code" if link changes)

---

# 🧹 Cleanup

* You can delete the installer `.exe` file after installation
* It does NOT affect Java

---

# ⚠️ Common Mistakes

* File name must match class name (Hello.java)
* Don’t run: `java Hello.java`
* Always compile first: `javac`
* Ensure PATH is set properly

---

# 🚀 Ready For

* Java Basics
* DSA (Data Structures & Algorithms)
* Placement Preparation

---

# 💯 Status Checklist

* [x] JDK Installed
* [x] PATH Configured
* [x] VS Code Setup
* [x] Java Program Ran Successfully

---

🔥 You are fully ready to start Java + DSA.
