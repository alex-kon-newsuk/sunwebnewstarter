#New starter SUNWEB getting started notes
To continue after step 2, you will need admin access rights. If you don't have this, submit an Enhanced Desktop Access Form first.
You will also need a github account, (https://github.com). 

1. Check if you have git installed. If not install XCode Command Line tools. This can be installed without admin rights. 
	-	Open terminal and run : git --version

2. Request access to the following repos from service desk. Use the following form :
	-	https://spreadsheets.google.com/a/news.co.uk/spreadsheet/viewform?formkey=dHFNXzkwOTJtcGE1UGpORXFjYnp1bUE6MQ
	-	Ask to be added to : 
		https://github.com/orgs/newsinternational/teams/sun-web-dev
		https://github.com/newsinternational
		https://github.com/orgs/newsinternational/teams/cps
		https://github.com/orgs/newsinternational/teams/sunweb ( legacy, probably you don't need it)
	-	make sure you eplcitely ask for access to the following : 
		cps-content-ingest
		cps-content-api
		nu-sunweb-content-renderer-tablet-feed

3. Install nodejs 0.10.38
	Download and install the latest version of node.js (this will install npm as well)
	Isntall a node version managment tool (https://github.com/tj/n)
	Install version 0.10.38

4. Install Java 7. Required by Elastic Search to run and for our functional tests

5. Install Elasticsearch (https://www.elastic.co/)
	- also install the http://mobz.github.io/elasticsearch-head/ plugin. 

6. Ruby should be by default installed in MAC machines. Try ruby --version

7. Install your IDE of choise  (intellJ, sublime etc etc)

8. Populate the local elastic search instance with test data
	-	Copy everything from here : https://files.slack.com/files-pri/T029S066X-F04PADA0D/data.json
	-	Paste everything in the a file called data.json
	-	Create js file with the code from the following gist, in the same folder with the data.json file ( https://gist.github.com/alex-kon-newsuk/a2f94739f246d94f95e4 )
	-	Run the script with the command : node <file> 

9. Request AWS credentials for Times and SUN s3 buckets
	
10. Add aws config to the app : 
	
		npm install aws-sdk

		Configure - Create a credentials file at ~/.aws/credentials on Mac/Linux or C:\Users\USERNAME\.aws\credentials on Windows
		[default]

		aws_access_key_id = your_access_key

		aws_secret_access_key = your_secret_key

11. Open terminal :
	-	go to cps-content-ingest/sun
		run : NODE_ENV=development NODE_PUB=sol node app
	-	go to nu-sunweb-content-renderer-tablet-feed/src
  		run : node app
  	-	go to yout ekastic search folder
  		run : bin/elasticsearch		
  	-	go to cps-content-api
  		run : node app


