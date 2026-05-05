# pip-demo
🚀 Python + pip Project Demo
This guide will help you create, manage dependencies, and run a simple Python application using pip.

🧰 Prerequisites
Make sure you have:

✅ Check installations
python3 --version
pip3 --version
If not installed:

Install Python from https://www.python.org
pip comes with Python
📁 Step 1: Create Project Folder
mkdir my-python-app
cd my-python-app
🧠 Step 2: Create Virtual Environment (VERY IMPORTANT)
👉 Why?

Keeps dependencies isolated
Avoids conflicts between projects
Used in real DevOps pipelines
python3 -m venv venv
Activate environment
Mac/Linux:
source venv/bin/activate
Windows:
venv\Scripts\activate
👉 You will see (venv) in terminal

📦 Step 3: Install Dependency
Example: install Flask

pip install flask
✍️ Step 4: Create Application
Create file:

touch app.py
Add code:

from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "Hello from Python + pip!"

if __name__ == "__main__":
    app.run(port=5000)
▶️ Step 5: Run Application
python app.py
👉 Open browser:

http://localhost:5000
👉 Output:

Hello from Python + pip!
📄 Step 6: Dependency Management
Save dependencies
pip freeze > requirements.txt
👉 Creates:

requirements.txt
Install dependencies later
pip install -r requirements.txt
👉 This is used in:

CI/CD pipelines
Production deployments
🔁 Step 10: Lifecycle (Simple)
install → develop → package → deploy
🧠 DevOps Connection (IMPORTANT)
👉 Real flow:

Developer writes code
↓
pip installs dependencies
↓
requirements.txt used in pipeline
↓
App deployed in server/container
Used in tools like:
Jenkins
Docker
🎯 What You Learned
What is pip
What is virtual environment
How to install dependencies
How to run Python app
What is requirements.txt
Python packaging basics
