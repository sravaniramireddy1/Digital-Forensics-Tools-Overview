

## **Ex.No. 08 – Use Steg-Expose to Detect Hidden Data in Images**

### 🎯 **Objective**

To detect hidden data embedded in image files using the **StegExpose** tool and analyze them based on statistical properties.

---

### 🧰 **Requirements**

* ☕ **Java Runtime Environment (JRE)** – Required to run StegExpose (.jar file).
* 🧩 **StegExpose Tool** – Download from the [official GitHub repository](https://github.com/b3dk7/StegExpose).
* 🖼️ Supported image formats – `.png`, `.jpg`, `.bmp`, etc.

---

### ⚙️ **Steps to Perform the Experiment**

#### 🪄 **Step 1: Download and Set Up StegExpose**

1. Download the **StegExpose.jar** file from GitHub.
2. Ensure **Java** is installed on your system.
3. Place the `.jar` file in a working folder containing your images.

---

#### 🖼️ **Step 2: Select Images for Analysis**

Collect images that might contain hidden data (e.g., `image1.png`, `test.jpg`).

---

#### 💻 **Step 3: Open Command Prompt / Terminal**

Navigate to the folder containing **StegExpose.jar** and your image files.

---

#### 🧮 **Step 4: Run StegExpose on a Single Image**

```bash
java -jar StegExpose.jar <image_file_path>
```

**Example:**

```bash
java -jar StegExpose.jar test_image.png
```

---

#### 📊 **Step 5: Analyze the Output**

StegExpose gives a **suspect score** between **0 and 1**:

| Score Range | Meaning                         |
| ----------- | ------------------------------- |
| < 0.2       | ✅ Clean (No hidden data)        |
| 0.2 – 0.3   | ⚠️ Possibly hidden data         |
| > 0.3       | 🚨 Likely steganography present |

**Example Output:**

```
Analyzing suspect_image.png...
Result: 0.4
Steganography likely present
```

---

#### 🧰 **Step 6: Batch Analysis (Multiple Images)**

To scan an entire folder:

```bash
java -jar StegExpose.jar <folder_path>
```

---

#### ⚡ **Step 7: Advanced Options**

To view additional options:

```bash
java -jar StegExpose.jar --help
```

You can modify sensitivity and output details based on your needs.

---

### 📝 **Observation**

StegExpose successfully detects whether an image contains hidden data by comparing its statistical structure against normal images.

---

### 🧾 **Result**

The experiment demonstrates how **StegExpose** can efficiently identify images with hidden or embedded data using steganographic detection methods.

