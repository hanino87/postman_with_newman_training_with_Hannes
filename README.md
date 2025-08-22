# ✦ Installation and Introduction to Newman with Postman collections✦

Newman is a modern, high-performance command tool that run your Postman collections with their requests outside Postmans GUI. 

---

## 🔹 1. Prerequisites & Installation 

•  Node JS+

    Install from 🔗 https://nodejs.org/

• 📦 Pip (Python package installer)
  Usually comes with Python. Check with:

  ```Shell

  pip --version

  
  ```

💡 On macOS or Linux, if you have multiple Python versions installed, you may need to use pip3 instead:

 ```Shell

pip3 --version 
  
```

• 🧪Virtual Environment (optional but recommended)
  To isolate project dependencies:

```Shell

python -m venv .venv

```

💡 On macOS and Linux, you may need to use python3 instead:

```Shell

python3 -m venv .venv

```

💡 For more information about script commands in detail when working with virtual enviorment visit this REPO i have created about it. 

🔗 https://github.com/hanino87/Training_Virtual_Environments_With_Hannes

• ✅ FastAPI & 🚀 Uvicorn 

Install with Pip 

```Shell

pip install fastapi uvicorn

```
💡 On macOS or Linux, if you have multiple Python versions installed, you may need to use pip3 instead:

 ```Shell

pip3 install fastapi uvicorn
  
```

## 🔹 2. Export your Collection in Postman 

To export a collection in Postman, follow these steps:

1. Open Postman and go to the Collections tab on the left sidebar.

2. Find the collection you want to export.

3. Click the three-dot menu (⋮) next to the collection name.

4. Select "Export" from the dropdown menu.

5. In the export window:

Choose the export format (typically Collection v2.1 (recommended)).
Click the "Export" button.

Choose a location on your computer to save the .json file.
Your collection is now exported and can be shared or imported elsewhere as needed


## 🔹 3. Setup and Run Newman in VS Code Terminal with HTML Reporter

🔸 Step 1: Install Node.js (if not already installed) see instructions above 


🔸 Step 2: Install Newman Globally

 ```Shell

npm install -g newman

```

## 🔹 4. Starting Uvicorn-servern before running Newman

 ```Shell

uvicorn your_app_module:app --reload

```

Replace your_app_module:app with your actual module and app instance.

The --reload flag enables auto-reloading when code changes (optional).

The server will now be running, typically on http://127.0.0.1:8000.



## 🔹  Step 5: Run Your Postman Collection with Newman


 ```Shell

newman run your-collection-name.json

```

🔸 Step 6: Run Your Postman Enviorment Collection with Newman

```Shell

newman run your-collection-name.json -e your-environment.json 

```

## 🔹 Step 7: Install Pretty HTML Report for Newman

```Shell

npm install -g newman-reporter-htmlextra

```
🔸 Step 8: Run Your Postman Enviorment Collection and create a Pretty HTML Report for Newman 

```Shell

newman run your-collection-name.json -r htmlextra

```

The HTML report will be saved in the newman directory by default.

🔸 Optional: Customize Output Location

```Shell

newman run your-collection-name.json -r htmlextra --reporter-htmlextra-export reports/report.html


```

This saves the report as report.html inside the reports folder.

