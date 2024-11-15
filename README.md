---

# Appium Setup Guide

This guide provides step-by-step instructions to set up Appium and connect it to a real device for mobile testing. Follow the instructions carefully to ensure a smooth setup process.

---

## **Setup**

### **Step 1: Install Node.js**
1. Ensure **Node.js** is installed on your machine.  
   - Check the Node.js version:  
     ```bash
     node -v
     npm -v
     ```
2. Download and install Node.js from the [official website](https://nodejs.org/), if not already installed.

---

### **Step 2: Install Appium**
1. Install Appium globally using npm:  
   ```bash
   npm install -g appium
   ```
2. Verify the installation by checking the Appium version:  
   ```bash
   appium --version
   ```

---

### **Step 3: Start Appium**
1. Start Appium from the command line:  
   ```bash
   appium
   ```
2. To stop Appium, press **Ctrl + C**, and confirm by typing `Y`.

---

### **Step 4: Install Appium Desktop Client**
1. Download the Appium Desktop Client from the [official Appium website](https://appium.io/).  
2. Install it on your machine.

---

### **Step 5: Install Appium Doctor**
1. Install Appium Doctor globally using npm:  
   ```bash
   npm install -g appium-doctor
   ```

---

### **Step 6: Uninstall Appium (if needed)**
1. Uninstall Appium using npm:  
   ```bash
   npm uninstall -g appium
   ```

---

## **How to Connect to a Real Device**

### **Step 1: Install Java**
1. Ensure **Java** is installed on your machine.  
   - Check the Java version:  
     ```bash
     java -version
     ```
2. If not installed, download and install Java from the [official website](https://www.oracle.com/java/technologies/javase-downloads.html).

---

### **Step 2: Prepare an Android Device**
1. Have an Android device, a USB cable, and at least **200MB to 1GB** of available storage.

---

### **Step 3: Download Command Line Tools**
1. Download the **Command Line Tools** (not Android Studio) from the [Android Studio official website](https://developer.android.com/studio).
2. Extract the downloaded file and ensure the `bin` folder is inside the `tools` folder.

---

### **Step 4: Install Platform Tools**
1. Navigate to the `bin` folder inside the Command Line Tools directory.
2. Run the following command to install platform tools and the required Android version:  
   ```bash
   sdkmanager "platform-tools" "platforms;android-33"
   ```
   - Replace `android-33` with the API level corresponding to your Android version.  
     Refer to this [Android Version History](https://en.wikipedia.org/wiki/Android_version_history) to find the correct API level.

---

### **Step 5: Set Up Environment Variables**
1. Set the `ANDROID_HOME` environment variable to the Command Line Tools folder:  
   ```
   ANDROID_HOME=C:\cmdline-tools
   ```
2. Add the `platform-tools` folder path to the `PATH` environment variable.

---

### **Step 6: Enable USB Debugging**
1. On your Android device, enable **Developer Mode**:  
   - Go to **Settings** > **About Phone** > Tap **Build Number** seven times.  
   - Developer Mode will be enabled.
2. Enable **USB Debugging** in the **Developer Options** menu.

---

### **Step 7: Verify Device Connection**
1. Connect your device to the PC using a USB cable.
2. Run the following command to check connected devices:  
   ```bash
   adb devices
   ```
   - If no devices appear, ensure the device is connected, and USB Debugging is enabled.

---

### **Step 8: Mirror Your Device (Optional)**
1. Download and install **Vysor** on both your laptop and Android device to mirror your device on your laptop.  
   - Download Vysor from [its official website](https://www.vysor.io/).

---

### **References**
- [Command Line Tools User Guide](https://developer.android.com/tools)
- [SDK Manager Documentation](https://developer.android.com/tools/sdkmanager)
- [Android Version History](https://en.wikipedia.org/wiki/Android_version_history)

---
