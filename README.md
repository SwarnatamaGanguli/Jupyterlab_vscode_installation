# 10thjune26_jupyterlab_installation
Create python jupyter lab/notebook 
# Python + Anaconda + JupyterLab Setup Guide (Best Practices)

## Goal

Set up a clean Python learning and teaching environment using:

* Anaconda
* Conda Environments
* JupyterLab
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* IPyKernel

Recommended for:

* Python Learning
* Teaching Python
* AI/ML Development
* Data Analytics
* Clean Environment Management

---

# Step 1 — Install Anaconda

Download Anaconda:

https://www.anaconda.com/download

Install with the following options:

☑ Create shortcuts
☐ Add installation to PATH
☐ Register Anaconda as default Python
☑ Clear package cache (optional)

Click:

Install

Wait until installation completes.

---

# Step 2 — Open Anaconda Prompt

Open:

Windows Search
↓

Anaconda Prompt

Expected:

```bash
(base) C:\Users\YourName>
```

---

# Step 3 — Check Existing Environments

Run:

```bash
conda env list
```

Example:

```text
base
myenv
```

---

# Step 4 — Create a Clean Environment

Example environment:

```text
learning_env
```

Run:

```bash
conda create -n learning_env python=3.12 -y
```

Wait until:

```text
Executing transaction: done
```

---

# Step 5 — Activate Environment

Run:

```bash
conda activate learning_env
```

Expected:

```bash
(learning_env) C:\Users\YourName>
```

Verify Python:

```bash
python --version
```

Expected:

```text
Python 3.12.x
```

---

# Step 6 — Install Required Packages

Run:

```bash
pip install jupyterlab notebook pandas numpy matplotlib ipykernel
```

Packages installed:

| Package    | Purpose                          |
| ---------- | -------------------------------- |
| jupyterlab | Modern notebook interface        |
| notebook   | Classic notebook                 |
| pandas     | Data analysis                    |
| numpy      | Numerical computing              |
| matplotlib | Visualization                    |
| ipykernel  | Connect environment with Jupyter |

Verify:

```bash
jupyter --version
```

---

# Step 7 — Register Environment into Jupyter

Run:

```bash
python -m ipykernel install --user --name=learning_env --display-name "Python (learning_env)"
```

Expected:

```text
Installed kernelspec learning_env
```

---

# Step 8 — Launch JupyterLab

Run:

```bash
jupyter lab
```

Browser opens:

```text
http://localhost:8888/lab
```

Alternative:

Open classic notebook:

```bash
jupyter notebook
```

---

# Step 9 — Create Notebook

Inside JupyterLab:

Notebook
↓

Python (learning_env)

Click and open.

---

# Step 10 — Verify Environment

Run:

```python
import sys

print(sys.version)
```

Expected:

```text
3.12.x
```

---

# Step 11 — Verify Libraries

Run:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

print("Environment Ready 🚀")
```

Expected:

```text
Environment Ready 🚀
```

---

# Step 12 — Optional: Open Terminal Inside JupyterLab

Inside Jupyter:

Other
↓

Terminal

Expected:

```bash
(learning_env)
```

---

# Daily Startup Workflow

Open:

Anaconda Prompt

Run:

```bash
conda activate learning_env

jupyter lab
```

That’s it.

No reinstall.
No recreate environment.
No duplicate Python installs.

---

# Common Commands

Deactivate environment:

```bash
conda deactivate
```

List environments:

```bash
conda env list
```

Remove environment:

```bash
conda remove --name learning_env --all
```

Install additional package:

```bash
pip install package_name
```

Update package:

```bash
pip install --upgrade package_name
```

---

# Recommended Folder Structure

```text
Python_Learning/
│
├── notebooks/
├── practice/
├── projects/
├── datasets/
├── notes/
└── README.md
```

Happy Learning 🚀
