# Quizify

# 1. Google Cloud & Environment Setup

<details>
  <summary>Step 1: Create a Google Cloud Project</summary>

1. **Start a New Project**:
   - Go to the [Google Cloud Console](https://console.cloud.google.com/).
   - Click on the project drop-down menu at the top of the page and select “New Project.”
   - Name your project something like "Quizify" and create it.

2. **Enable Vertex AI APIs**:
   - Navigate to the [Vertex AI section](https://console.cloud.google.com/vertex-ai/).
   - Enable all the recommended APIs to ensure you have the necessary functionalities for your project.

3. **Set Up Service Accounts**:
   - In the Google Cloud Console, search for **Service Accounts** in the top search bar.
   - Create a new service account and assign the role **Owner** to it for broad permissions.
   - Generate an authentication key in JSON format for this service account and download it.

4. **Configure Authentication**:
   - Place the downloaded JSON file into your project directory.
   - Open your terminal and set an environment variable to point to your JSON key file:
     ```bash
     export GOOGLE_APPLICATION_CREDENTIALS="/path/to/your/authentication.json"
     ```
   - To ensure your security, add the JSON key file to your `.gitignore` to prevent it from being uploaded to version control.

</details>

<details>
  <summary>Step 2: Setting Up a Python Virtual Environment</summary>

1. **Create a Virtual Environment** (recommended for managing dependencies):
   - In your terminal, navigate to your project directory.
   - Run the following command to create a virtual environment named `env`:
     ```bash
     python3 -m venv env
     ```
   - Activate the environment:
     ```bash
     source env/bin/activate
     ```

2. **Update `.gitignore`**:
   - To keep your repository clean, add the virtual environment folder (`env/`) to your `.gitignore` file. This prevents it from being tracked by version control.

</details>

<details>
  <summary>Step 3: Install Required Packages</summary>

1. **Dependencies Installation**:
   - Ensure you have a `requirements.txt` file listing all the necessary Python packages for your project.
   - With your virtual environment activated, install the required packages:
     ```bash
     pip install -r requirements.txt
     ```

</details>

<details>
  <summary>Step 4: Install the gcloud CLI</summary>

  - Follow the instruction on [Install the gcloud CLI](https://cloud.google.com/sdk/docs/install)
</details>

# 2. Document Processor

As part of our Data Ingestion Pipeline, we will build a Data Processor class in the task_3.py file. 


<img width="750" alt="2_FileUploader" src="https://github.com/NegarTajziyehchi/Quizify/assets/6012786/5c91627a-c838-4a4c-8345-ae4aace02d03">

Run the following command in the command line to start the Streamlit app.

```bash
streamlit run task_3/task_3.py
```

<img width="750" alt="2_FileUploader" src="https://github.com/NegarTajziyehchi/Quizify/assets/6012786/8623c48f-c788-40cf-a142-53a98ed82678">

# 3. Embedding with VertexAI & Langchain

We are taking our documents from Task 3 and pushing them into the embeddings client in the task_4.py file.

<img width="750" alt="3_Embedding" src="https://github.com/NegarTajziyehchi/Quizify/assets/6012786/45bb6dcc-403f-40b1-88ac-4ef183b86735">
