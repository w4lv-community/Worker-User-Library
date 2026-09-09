# Worker User Library

Welcome to the **Worker User Library** — a growing collection of reusable Workers, Worker libraries, and project templates for **Workers for LabVIEW**.

The library is maintained by the Workers Community and is designed to make it easy to reuse existing functionality, share useful Workers with other developers, and provide complete project templates that can be adapted for new applications.

Workers 5.1 can download the contents of this repository directly through the **Worker User Library** tool.

---

## 📦 What This Library Contains

Items in the Worker User Library can include:

- **Workers** — reusable Workers with Public APIs that can be added to your existing projects.
- **Worker Libraries** — collections of related Workers and supporting code.
- **Project Templates** — complete LabVIEW projects designed to be copied and adapted for your own applications.

Items are organized by the LabVIEW version in which they were created, for example:

- **LabVIEW_2017**
- **LabVIEW_2019**

Each item should include documentation describing its purpose, usage, requirements, and any external dependencies.

---

## 🚀 Using the Worker User Library with Workers 5.1

Workers 5.1 can download the latest library items directly from this GitHub repository.

### Download the Community Library

1. Open LabVIEW and select **Tools > Workers tools menu**.
2. Open the **Worker User Library** tool.
3. Press **Pull from GitHub**.
4. In the dialog that appears, press **W4LV-Community Repo** to populate the repository address.
5. Press **Download items from GitHub**.

The tool will download the Workers Community repository and make the available items appear in the **Items in User Library** list.

You can repeat this process whenever you want to pull the latest versions of the community library items from GitHub.

---

## ➕ Adding Workers and Libraries to a Project

For reusable Workers and Worker libraries:

1. Select the item in the **Items in User Library** list.
2. Review its description, requirements, and dependencies.
3. Press **Add selected Item to Project**.
4. Select where the item should be copied.

A copy of the selected Worker or library will be added to your project, allowing you to modify or use it without changing the original library source.

---

## 🧩 Creating a Project from a Project Template

Some Worker User Library items are supplied as complete **project templates**.

For these items:

1. Select the project template in the **Items in User Library** list.
2. Review its description and dependencies.
3. Press **Create copy of Project Template**.
4. Select where the new project should be created.
5. Press **Create Project**.

A complete copy of the project template will be created at the selected location.

Project templates are useful when the functionality requires more than a single Worker or library, or when a complete working example provides the best starting point.

---

## 🌐 gRPC Worker Templates

Workers 5.1 adds two project templates for integrating Workers applications with gRPC:

- **gRPC Server Worker Template**
- **gRPC Client Worker Template**

These templates provide Workers that map their Public Requests and Responses onto a bidirectional gRPC stream. They can be used together or with applications written in other languages such as Python or C++ that implement the same **.proto** contract.

The templates are supplied as complete projects with Tester Workers so they can be run and studied before being adapted for your own applications.

**Note:** The gRPC templates require LabVIEW 2019 or later and additional NI gRPC packages. Review the item description and README before creating a project from either template.

---

## 🧪 Example Worker: Check All Worker Queues

The **Check All Worker Queues** Worker allows you to monitor the number of messages waiting in each Worker's message queue within a running application.

This can be useful for detecting message-processing bottlenecks or Workers that are unable to process incoming messages quickly enough.

The Worker can be dynamically loaded into an application and communicated with through its Public API.

---

## 📌 Contributing

Have a useful Worker, Worker library, or project template that you think other developers could benefit from? Contributions are welcome.

Before submitting an item, please make sure that it:

- Is designed for use with Workers for LabVIEW.
- Is modular, reusable, and reasonably self-contained.
- Includes a **README.md** describing its purpose, usage, requirements, and any external dependencies.
- Clearly documents any packages or third-party software required to use it.
- Uses a Workers Public API where appropriate.
- Includes a Worker User Library **.ini** configuration file.
- Is organized under a folder containing your name, company, or organization.
- Identifies the LabVIEW version in which the item was created.
- Includes appropriate license information.

External dependencies are allowed, but they must be clearly documented so users know what must be installed before opening or running the item.

### Repository Structure

Items are organized by LabVIEW version. The source code should exist inside a contributor or company folder, while the corresponding Worker User Library **.ini** configuration file exists at the LabVIEW-version folder level.

For example:

    LabVIEW_2019/
        My Company/
            My Worker/
                ...
                README.md

        My Worker.ini

The **.ini** file provides the information displayed by the Worker User Library tool, including the item name, source path, description, version, license, LabVIEW version, dependencies, and other configuration information.

Use the **Worker User Library Config File Editor** in Workers for LabVIEW to create or edit this configuration.

To contribute, fork this repository, add your item to the appropriate LabVIEW-version folder, and submit a pull request.

---

## 📚 Resources

- [Workers for LabVIEW Homepage](https://workersforlabview.io/)  
- [Workers for LabVIEW Community](https://community.workersforlabview.io/)  
- [Workers for LabVIEW Documentation](https://docs.workersforlabview.io/)  

---

## 🙌 Acknowledgements

Thank you to everyone who has contributed Workers, libraries, templates, ideas, testing, and feedback to the Workers for LabVIEW community.

The goal of this repository is to make useful components easy to share and reuse so that developers do not have to solve the same problems repeatedly.

---

## 📄 License

Content in this repository is distributed under the license specified for each item.

The repository itself is provided under the BSD-3-Clause license unless otherwise stated.
