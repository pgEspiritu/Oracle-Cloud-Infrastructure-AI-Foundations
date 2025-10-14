# 🧠 OCI Vision – Console Demonstration

## 🏠 Navigating the OCI Console

Let’s explore how **OCI Vision** works directly from the **Oracle Cloud Console**.

1. From the **Console Homepage**, go to **☰ Menu → Analytics & AI → Vision**.  
2. On the **Vision Homepage**, you’ll find:
   - 📘 **Documentation links**  
   - 🔗 **API Reference and SDK Guides**  
   - 🧠 **Feature options** such as:
     - Image Classification  
     - Object Detection  
     - Document AI  
     - Custom Model Creation  

For this walkthrough, we’ll focus on **Image Classification** and **Object Detection**.

---

## 🏷️ Image Classification

### 🖼️ Using Default Images
- The Vision service includes **sample images** to help you explore classification right away.  
- When analyzed, the model assigns **tags** (classification labels) that describe what’s visible in the image.  
- Example output:
  ```
  overhead power line, transmission tower, plant, sky, line
  ```
  ✅ These are accurate tags for the provided scene.

---

### 📤 Uploading a Custom Image
You can also upload your own image for classification:
- Drag and drop an image into the **Image Classification** interface.
- Example: an image of **Iconic London**.
- The Vision service tags it as:
  ```
  skyscraper, water, building, bridge, boat
  ```
  ✅ These results correctly describe the London cityscape.

---

## 🎯 Object Detection

### 🔍 Detecting Objects in Images
Next, let’s switch to **Object Detection**.  
This feature identifies **individual objects** within an image and draws **bounding boxes** around each one.

- The sample image shows:
  - 🚗 Car (front and right side)
  - 🚌 Bus (background)
  - 🚶 People on the sidewalk
  - 🚘 Another car partially visible

Each object includes:
- A **bounding box**
- A **label**
- A **confidence score**

---

### 📝 Text Detection
OCI Vision also detects and extracts **text** found in images.  
In this case, it correctly recognized:
- License plate numbers  
- The **Oracle** logo  
- Bus route signs  
- Advertisements on vehicles  

Even faint or distant text, like a route on a far-away bus, is accurately captured.

---

## 🧍 Advanced Detection Example

### 🏙️ Scene with Hidden Objects
In a **low-resolution rooftop image**, Vision successfully detects:
- A **person** standing on the roof 🧍‍♂️  
However:
- It does **not** detect circular **microwave transmission antennas**, since the **pretrained model** is not designed for those objects.

➡️ You could create a **custom model** to detect antennas or any domain-specific object.

---

### 🚴 Multi-Object Detection
In another example with **cyclists**:
- Vision detects **people**, **bicycles**, and even **bicycle wheels**.
- It recognizes individuals **facing away** or in **nonstandard poses**.
- Bounding boxes show **nested relationships** (person on a bicycle).
- It also marks a small **dash on clothing** as text (demonstrating text sensitivity).

---

## ✅ Summary

| Feature | Description |
|----------|-------------|
| 🏷️ **Image Classification** | Tags entire images with relevant categories |
| 🎯 **Object Detection** | Identifies and labels multiple objects within an image |
| 🔤 **Text Detection** | Reads visible text in photos or signage |
| 🧩 **Custom Models** | Build your own for domain-specific recognition |

OCI Vision’s **console interface** makes it simple to analyze images and documents — whether for AI learning, automation, or business insights.
