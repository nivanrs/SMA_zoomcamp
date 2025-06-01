# Getting Started with Stock Market Analytics Zoomcamp

This guide provides essential information to help you get started with the "Stock Market Analytics Zoomcamp," including prerequisites, environment setup, and how to access course materials.

## Prerequisites

To get the most out of this course, it is recommended that you have:

- Basic understanding of Python programming.
- Familiarity with fundamental data concepts.
- A Google account for accessing Colab notebooks.

## Environment Setup

The course primarily utilizes Google Colab for hands-on exercises. For local development and automation in Module 5, specific setup instructions are provided.

### Google Colab

Most of the course's code examples are provided as Google Colab notebooks. You can access them directly via the links in the module documentation. Colab provides a cloud-based Jupyter environment, so no local setup is required for the notebooks.

### Local Environment Setup (for Module 5: Deployment and Automation)

For Module 5, you will transition to local Python files and may need to set up a local development environment.

1.  **Change Working Directory:**
    ```bash
    cd source/stock-markets-analytics-zoomcamp/05-deployment-and-automation/
    ```
2.  **Install Virtual Environment:**
    ```bash
    pip3 install virtualenv
    ```
3.  **Create a New Virtual Environment (venv):**
    ```bash
    virtualenv venv
    # OR
    python3 -m venv venv
    ```
4.  **Activate the New Virtual Environment:**
    - **Linux/macOS:**
      ```bash
      source venv/bin/activate
      ```
    - **Windows (Command Prompt):**
      ```bash
      venv\Scripts\activate
      ```
    - **Windows (PowerShell):**
      ```powershell
      .\venv\Scripts\Activate.ps1
      ```
5.  **Install Ta-lib (Technical Analysis Library):**

    - **On Mac:**
      - **Step 1: Install Homebrew** (if not already installed):
        ```bash
        /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
        ```
      - **Step 2: Install TA-Lib using Homebrew:**
        ```bash
        brew install ta-lib
        ```
      - **Step 3: Install the ta-lib Python package** (ensure your virtual environment is active):
        ```bash
        pip3 install ta-lib
        ```
      - **Step 4: Ensure Numpy version compatibility:** Make sure you have Numpy of a version earlier than 2 (e.g., "numpy==1.26.4" in `requirements.txt`) to ensure `ta-lib` can be successfully imported. Refer to [this link](https://stackoverflow.com/questions/78634235/numpy-dtype-size-changed-may-indicate-binary-incompatibility-expected-96-from) for more details.
    - **For other operating systems**, please refer to the official TA-Lib installation guides.

6.  **Install all requirements to the new environment (venv):**
    ```bash
    pip3 install -r requirements.txt
    ```

### Running the Project (Local)

After setting up your local environment and activating the virtual environment:

- **Start the local Jupyter Server:**
  ```bash
  jupyter notebook
  ```
  (You can check all running servers with `jupyter notebook list`)
- **Open `test.ipynb` to check the system's operation:**
  - From your web browser (navigate to `http://localhost:8888/tree` or similar).
  - Or via the VS Code UI (specify the server address kernel).
- **Run `main.py` from the Terminal (or Cron) to simulate one new day of data:**
  ```bash
  python main.py
  ```

## Accessing Course Materials

All course materials are freely available:

- **YouTube Recordings:** Each module has a corresponding YouTube livestream recording. Links are provided in the module-specific documentation.
- **Slides:** Presentation slides for each module are available via Google Slides links.
- **Code in Colab:** Interactive Jupyter notebooks hosted on Google Colab are provided for hands-on coding.
- **Homework Assignments:** Found in the `cohorts/` folder for the respective year. Submission links and deadlines are provided there.
