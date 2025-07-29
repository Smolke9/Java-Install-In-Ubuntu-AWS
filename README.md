
# Java 21 Installation on Ubuntu (AWS EC2)

This guide provides step-by-step instructions to install **Java 21 (OpenJDK 21)** on an Ubuntu server (such as an AWS EC2 instance).

---

## 📌 Prerequisites

- Ubuntu 20.04 / 22.04 system (e.g., AWS EC2)
- Sudo privileges

---

## 🚀 Installation Steps

### 1. Update System Packages

```bash
sudo apt update
```

---

### 2. Install OpenJDK 21

```bash
sudo apt install openjdk-21-jdk -y
```

---

### 3. Verify Java Version

```bash
java -version
```

✅ Example output:

```
openjdk version "21" 2023-09-19
OpenJDK Runtime Environment (build 21+35)
OpenJDK 64-Bit Server VM (build 21+35, mixed mode)
```

---

## ⚙️ Set JAVA_HOME (Optional)

### 4. Find Java Path

```bash
readlink -f $(which java)
```

Example output:

```
/usr/lib/jvm/java-21-openjdk-amd64/bin/java
```

### 5. Export JAVA_HOME

```bash
echo 'export JAVA_HOME="/usr/lib/jvm/java-21-openjdk-amd64"' >> ~/.bashrc
echo 'export PATH="$JAVA_HOME/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

---

## 🔄 Manage Multiple Java Versions (Optional)

If you have more than one Java version:

```bash
sudo update-alternatives --config java
```

Select the version of Java you want as default.

---

## ✅ Java 21 is Now Installed!

You can now compile and run Java 21 applications on your Ubuntu system.

---

## 🔗 Resources

- [OpenJDK Documentation](https://openjdk.org/)
- [Ubuntu Package Search](https://packages.ubuntu.com/)
