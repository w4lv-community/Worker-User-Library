# Worker-User-Library

Welcome to the **Worker User Library**—a growing collection of reusable Workers designed to support and accelerate development with the **Workers for LabVIEW** framework.

Each Worker in this repository provides useful functionality that can be dynamically loaded into your Workers applications and communicated with via their standardized **Public APIs**.

---

## 📦 What This Library Contains

This repository includes a curated set of Workers contributed by the community or created in response to developer needs. Each Worker is:

- Self-contained and easy to add into a project.
- Compatible with **Workers 5.0**.
- Designed to be **modular** and **reusable**.
- Documented with a description of its purpose and usage.

---

## 🚀 How to Use These Workers

You can add these Workers to your project using the **Worker User Library** tool included in **Workers 5.0**.

### 🔧 Step-by-Step Instructions

1. **Download or clone the `Workers5.0` branch** of this repository to your PC.  
   - Recommended path: `C:\Users\<YourName>\Documents\Worker-User-Library`
   - The folders are organized by the version of LabVIEW the Workers were created in (e.g., `LabVIEW_2017`). These are forward-compatible with newer versions of LabVIEW.
   - You only need the `LabVIEW_20XX` folder containing the Workers and/or Worker libraries.

2. Assuming **Workers 5.0** is installed in LabVIEW, open LabVIEW and go to the **Workers Tools Menu**.

3. Launch the **Worker User Library** tool.

4. Click the ➕ button to add a new source folder.

5. In the dialog that opens, **browse to the folder** where you downloaded this repository.  
   Example: `C:\Users\<YourName>\Documents\Worker-User-Library\LabVIEW_2017`

6. Once added, the Workers in this folder will appear in the tool's **Items in User Library** list.

7. From there, use the **Worker User Library** tool to easily **add a copy of any Worker or library into your project**.

---

## 🧪 Example Worker: Check All Worker Queues

One of the Workers included is `Check All Worker Queues`, which allows you to monitor the size of each Worker’s message queue within an application—helpful for detecting bottlenecks and improving performance.

You can:

1. **Load it dynamically** from another Worker using its **Public API**.  
2. Use its **Public API** to return a list of Workers and the number of elements in their queues.  
3. **View its front panel** (as shown in the image) via the **Debug Server’s Application Manager** while running.

---

## 📌 Contributing

Have a useful Worker you think others could benefit from? We welcome contributions!

Please ensure your Worker is:

- **Self-contained**, with no external dependencies.
- Includes a standardized **Workers 5.0 Public API**, containing one or more of:
  - Public Requests
  - Public Requests with Replies
  - Public Responses
- Includes an `.ini` file in the root directory with configuration data for your Worker or library.

📘 See the [Worker User Library Config File Editor](https://docs.workersforlabview.io/workers-tools/workers-tools-menu/worker-user-library/config-file-editor) documentation for details on how to create the required `.ini` file.

To contribute, simply fork the repo and submit a pull request.

---

## 📚 Resources

- 💬 [Workers for LabVIEW Homepage](https://community.workersforlabview.io/)  
- 🛠️ [Workers for LabVIEW GitHub Organization](https://github.com/w4lv-community)

---

## 🙌 Acknowledgements

Thanks to everyone who has contributed to this library and shared their solutions with the **Workers for LabVIEW** community!

---

## 📄 License

All content in this repository is shared under the **BSD-3 License**, unless otherwise stated.

---

*Let’s build better, faster LabVIEW applications—together.* 💛
