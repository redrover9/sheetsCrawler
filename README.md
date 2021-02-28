Author: David Anderson

File: main.py

Purpose: This program is for WGU students. It uses Google Sheets API and Selenium Driver to
pull all LinkedIn addresses from the WGU LinkedIn Network Google sheet and controls a remote browser to
send requests to everyone on the list. This program may encounter problems if you are not at least a third connection
from the people in the list. So you may want to manually add one or two users before running it.

SETUP INSTRUCTIONS:
------------------------------------------------------------------------------------------------------------------------
Step 1: Make a copy of the WGU LinkedIn Network Google Sheet by clicking File -> Make a Copy. Store it in your 
own Google Drive and name it: Copy of WGU LinkedIn Network

Ensure you are logged into your Google account and have access to your Drive.

Step 2: You must first create your own client_secret.json file and enable the Google Drive AND Google Sheets APIs.
Follow these instructions:
    
    1.) Go to the Google APIs Console: https://console.developers.google.com/
    2.) Create a new project.
    3.) Click Enable API. Search for and enable the Google Drive API.
    4.) Create credentials for a Web Server to access Application Data.
    5.) Name the service account and grant it a Project Role of Editor.
    6.) Download the JSON file.
    7.) Copy the JSON file to your code directory and rename it to client_secret.json


NOTE: Make sure your client_secret.json file is in your working directory.

Step 3: Install gspread: Open terminal, navigate to directory.

    pip3 install gspread
    
    NOTE: You may have to use this instead: pip install gspread

Step 4: Install Selenium for Python.
 
    pip3 install -U selenium
    
    NOTE: You may have to use this instead: pip install -U selenium

Step 5: Get the Google Chrome chromedriver and install it.  Select the correct driver for your version
of chrome. If you are up-to-date it's likely either 88 or 89. Download page: https://chromedriver.chromium.org/downloads

Add it to your PATH. Make sure you have Google Chrome installed. 

How to add chromedriver to PATH (Ubuntu/Linux):

    1.) Open terminal and download it with the following command: wget https://github.com/mozilla/geckodriver/releases/download/v0.24.0/geckodriver-v0.24.0-linux64.tar.gz

    2.) Extract the file with: tar -xvzf geckodriver*

    3.) Find the file names 'chromedriver' and make it executable: chmod +x chromedriver

    4.) Add the driver to your PATH: sudo mv chromedriver /usr/local/bin/


Step 6: Go into the main.py code and enter your LinkedIn username and password where needed.
This will allow Selenium to login and add people to your network.

------------------------------------------------------------------------------------------------------------------------
USAGE INSTRUCTIONS:

Options:

A) Run from your IDE

B) Run from command line with ./main.py
