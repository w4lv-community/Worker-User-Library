# Worker-User-Library

Welcome to the **Worker User Library**—a growing collection of reusable Workers designed to support and accelerate development with the **Workers for LabVIEW** framework.

Each Worker in this repository provides useful functionality that can be dynamically loaded into your Workers applications and communicated with via their standardized Public APIs.

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

1. Download or checkout the **Workers5.0 branch** of this repository to your PC.
   - Recommended path: `C:\Users\<YourName>\Documents\Worker-User-Library`
   - The folders are organized by the version of LabVIEW that the Workers were created in. Eg. **LabVIEW 2017**. These can therefore be used in later versions of LabVIEW as well.
   - You only need the `LabVIEW_20XX` folder containing the Workers and/or Worker libraries.

2. Assuming that **Workers 5.0** is installed into LabVIEW, **Open LabVIEW** and go to the **Workers Tools Menu**.

3. Launch the **Worker User Library** tool.

4. Click the ➕ button to add a new source folder.

5. In the dialog that opens, **browse to the folder** where you downloaded this repository. E.g. `C:\Users\<YourName>\Documents\Worker-User-Library\LabVIEW_2017`

6. Once added, the Workers in this folder will appear in the tool's **Items in User Library** list.

7. From there, you can use the **Worker User Library** tool to easily **add a copy of any of these Workers or libraries into your project**.

---

## 🧪 Example Worker: Check All Worker Queues

One of the Workers included is `Check All Worker Queues`, which allows you to monitor the size of each Worker’s message queue within an application—helpful for detecting bottlenecks and improving performance.

 
1. 𝗟𝗼𝗮𝗱 𝗶𝘁 𝗱𝘆𝗻𝗮𝗺𝗶𝗰𝗮𝗹𝗹𝘆 from another Worker using its 𝗣𝘂𝗯𝗹𝗶𝗰 𝗔𝗣𝗜.  
2. Use its 𝗣𝘂𝗯𝗹𝗶𝗰 𝗔𝗣𝗜 to return a list of Workers and the number of elements in their queues.  
3. 𝗩𝗶𝗲𝘄 𝗶𝘁𝘀 𝗳𝗿𝗼𝗻𝘁 𝗽𝗮𝗻𝗲𝗹 (as shown in the image) via the 𝗗𝗲𝗯𝘂𝗴 𝗦𝗲𝗿𝘃𝗲𝗿’𝘀 𝗔𝗽𝗽𝗹𝗶𝗰𝗮𝘁𝗶𝗼𝗻 𝗠𝗮𝗻𝗮𝗴𝗲𝗿 while running.


---

## 📌 Contributing

Have a useful Worker you think others could benefit from? We welcome contributions!

- Please ensure your Worker is **self-contained** and includes:
  - No external dependencies. 
  - A standardized **Workers 5.0** Public API containing either:
	  - Public Requests
	  - Public Request with Replies
	  - Public Responses
  - A *.ini* file in the root directly that contains the configuration data for your Worker or library. See Worker User Library [Config File Editor](https://docs.workersforlabview.io/workers-tools/workers-tools-menu/worker-user-library/config-file-editor) tool for how to create a Worker User Library *.ini* file.

 To contribute, simply fork the repo and submit a pull request.

---

## 📚 Resources

- 💬 [Workers Homepage](https://community.workersforlabview.io/)  
- 🛠️ [Workers for LabVIEW Community GitHub Repo](https://github.com/w4lv-community)

---

## 🙌 Acknowledgements

Thanks to everyone who has contributed to this library and shared their solutions with the Workers for LabVIEW community!

---

## 📄 License

All content in this repository is shared under the **BSD-3 License**, unless otherwise stated.

---

*Let’s build better, faster LabVIEW applications—together.* 💛
