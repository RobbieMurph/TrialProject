# TrialProject
The goal of the trial project is to write a python web service, which could display the top 10 most popular open source projects by Scrapinghub.
Below are the steps taken in order to complete the Trial Project. 
Intro:
1. Install Flask.
2. -> Use below link for steps needed to install Flask on a MAC OS. 
3. 'https://phoenixnap.com/kb/install-flask' 

  (a) Virtual Environment installed.

   - Use the MAC Terminal and follow the steps shown in the above link. 
  (b) Create an Environment
    
   - Use the MAC Terminal and follow the steps shows in the above link. 
  (c) Activate the Environment
   
   - Same as (a) & (b). 
   
  (d) Install Flask via MAC OS Terminal
  
  (e) Test the Environment
   
   - Create a test python file and edit it via TextEditor. 
   
Method:
1. Open a TextEditor and write out the code needed to display the top 10 projects. 
2. Googled how to create an API with python and attempted to create a website portraying the top 10 projects on Scrapinghub. 
3. Read through sites with info on Flask, Python Web Services, API's etc. 
  (a) https://realpython.com/beautiful-soup-web-scraper-python/#an-alternative-to-web-scraping-apis
  (b) https://phoenixnap.com/kb/install-flask
  (c) https://programminghistorian.org/en/lessons/creating-apis-with-python-and-flask#api-design-principles
  (d) etc etc. 
4. Went back to the PDF via emails.

  (a) Clicked on the link provided within the Trial Project PDF -> Was redirected to a GitHub site
  
  (b) Clicked on the 'Projects' tab but it was showing 0 projects, so I clicked on Repositories tab instead.
  
  (c) Sorted the Repositories by 'Stars' to show the best.
  
  (d) Tried to create files via TextEditor to scrape data from GitHub site using URL, but it gave an error advising 'Certificate not Found'.
  
   - Used the code below in order to print out the data of the page, just as a test run. The code failed - I wasnt able to get it working:
       
   import requests
   URL = "https://github.com/orgs/scrapinghub/repositories?q=&type=&language=&sort=stargazers
   page = requests.get(URL)
   print(page.text)
        
5. Created a file via TextEditor to print out the results via text rather than scrape the data and return then. 

  (a) See below Code:

Python Code:
------------

from flask import Flask
app = Flask(__name__)
@app.route('/')
def top10():
    return "<h1>Top 10 Repositories on Scrapinghub Today.</h1><p>Saturday 20th November: 17:30pm</p><p>1: portia</p><p> - Visual Scraping for Scrapy</p><p>2: splash</p><p> - Lightweight, scriptable browser as a service with an HTTP API</p>3: dateparser</p><p> - python parser for hunman readable dates</p><p>4: slackbot</p><p> - A chat bot for Slack</p><p>5: frontera</p><p> - A scalable frontier for web crawlers</p><p>6: python-crfsuite</p><p> - A python binding for crfsuite</p><p>7: scrapyrt</p><p> - HTTP API for Scrapy spiders</p><p>8: extruct</p><p> - Extract embedded metadata from HTML markup</p><p>9: spidermon</p><p> - Scrapy Extension for monitoring spiders execution</p><p>10: webstruct</p><p> - NER toolkit for HTML data</p>"

6. Ran the flask app via MAC Terminal to attach the file to the loopback IP

  (a) 'export FLASK_APP=API.py'
  
  (b) 'run flask'
  
  (c) IP Received: http://127.0.0.1:5000/
  
  (d) Once searched via browser, the above IP shows the output of the Python Code above. 

Conclusion:
1. Write out the work done via Readme.md on GitHub. 
