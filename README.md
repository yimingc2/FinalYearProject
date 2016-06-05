# FinalYearProject

Author
Yiming Chen (656180)

CouchDB URL database: http://115.146.89.12:5984/_utils/ backup database1: http://115.146.89.210:5984/_utils/ backup database2: http://115.146.89.218:5984/_utils/ 

Web URL http://115.146.89.219/ - the visualization of the result of data analysis 

Youtube Link https://youtu.be/MbNBaod0ggI 

Procedure to run the code

This project is to assessing the impact of B Corp on public sentiment of companies through a cloud-based big data infrastructure. To analyse impact, I retrieve relevant tweets from Twitter and do the sentiment analysis for tweets that posted before and after companies joining B Corp. 

CouchDB has to be established and the database name in the code has to be changed to the corresponding database name.

In the backend folder, there are 6 folders for 6 virtual machines to retrieve relevant tweets based on different lists of companies. There are 87 companies averagely separated into 6 machines running simultaneously to improve the efficiency. The code contains different lists of companies based on different machines.

smallData.csv contains all companies that a virtual machine is responsible for and they are separated into list1.csv and list2.csv to implement multiple threads in the main.py. 

testTweepy.py provides a set of functions to retrieve tweets from Twitter server, process returned data and save the tweets in database. Class clientKeys is used to make authorization in order to have access to Twitter server. Class getUserTimeline and search are used to collect tweets from different aspects. 

To run the code, you should run main.py which is used to retrieve tweets from companies themselves, followers and common users through functions defined in testTweepy.py. In main.py, some threads are created for each type of collecting like searching and getting user timeline.

In the frontend folder, opening index.html can open the website. main.html is the homepage including a list of companies, comparison between before and after being certified from a big view. company.html contains details information and the comparison chart involve each company. services.js contains code for drawing the charts while controller.js controlls the methods to interact with database. companyList.json lists all the companies and their specific information.

