# avl-uploader
A tool to pull videos from avloops.com and submit to youtube

## preparation
1. Have your csv file avl-clean-db.csv ready (comma delimited) in the same folder as script
2. Install Google, googleapiclient.http, apiclient.errors packages to Python
pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib
3. add credentials to client_secrets.json file (client_id and client_secret) from your Google Cloud Account (https://console.cloud.google.com/)

## how-to
1. Open the code in Notebook
2. when running the first script it will go through the csv file and download video files from the avloops.com according to the list
3. it will check if the file was already uploaded to Youtube (by checking if upload_time column is empty)
4. when finished or upon error - run the second part of the script from the notebook to save the log file for analysis and retry
