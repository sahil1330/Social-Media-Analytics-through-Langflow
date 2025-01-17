# Social-Media-Analytics-through-Langflow

This project is a basic analytics module utilizing <a href="www.langflow.org">Langflow</a> and <a href="www.datastax.com">DataStax</a> to analyze engagement
 data from mock social media accounts.

It fetches the engagement data from the csv file of mock social media accounts, stores it in AstraDB and using Langflow it accepts post types (e.g., carousel, reels, static images) as input and queries the dataset in Astra DB to calculate average engagement metrics for each post type.

It then utilizes Google Generative Ai integration in Langflow to generate simple insights based on the data.

### To run this project you need to follow the below steps:

If you want to use langflow online, then go the below website <a href="www.langflow.org">Langflow</a> website and create an account if not already created or login to your langflow account and you will be redirected to your langflow dashboard.

In the left side of the dashboard, you will see an icon to upload a flow.

<img src="images/langflow online json upload.png"/>

Upload the flow "Social Media Engagement Flow.json" that is present in this repository.

The project flow will open after finished uploading.

<img src="images/Flow.png" />

Create a vectorized database in <a href="https://astra.datastax.com/">AstraDB</a> and a collection called engagement.
Create the application token by clicking on Generate New token in the overview tab of the database.

<img src="images/generate app token astra.png" />

Copy this token and replace it with Application token in AstraDB component present in the flow and all the fields according to the created database.

Replace the Gemini Api Key in the Google Generative Ai Model Component and Google Generative Ai Embedding Component from your own Gemini Api Key

<img src="images/Gemini api key image.png" />

You can use a different model according to your preference if not Gemini.

To run this flow, click on the Playground in the right side and enter your input mentioning any post type and hit enter.

<img src="images/output.png" />

The model will calculate the metrics and give the insights as outputs based on your input.

### If you want to use this project on local host, you need to create a virtual environment first.

```
python -m venv .venv
.venv\Scripts\activate
```

### Virtual environment with uv:

```
uv venv
.\.venv\Scripts\activate
```

### Install Langflow with pip:

```
python -m pip install langflow
```

### Install Langflow with uv:

```
uv pip install langflow
```

### Run Langflow:

To run Langflow with uv, enter the following command.

```
uv run langflow run
```

To run Langflow with pip, enter the following command.

```
python -m langflow run
```

Confirm that a local Langflow instance starts by visiting http://127.0.0.1:7860 in a Chromium-based browser.

<img src="images/langflow run url.png" />

Access the langflow locally through the local url mentioned in the terminal and follow the same steps that are mentioned for langflow's hosted version.

If you are having any issues in installation of langflow, visit <a href="https://docs.langflow.org/get-started-installation">Langflow's docs</a> website for installing langflow.

To contact me, mail me anytime at sahilmane025@gmail.com .