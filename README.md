#A simple Node.JS, Express, and Mongo template for OpenShift
This is the completed application to go with this blog post:
????????????

##How to use

?????????????These need to be changed as well
Assuming you already have an OpenShift account
1) Create a Node.JS application and add a mongo cartridge

	rhc app create -t nodejs-0.6 -a <your app name>
	rhc app cartridge add -a <your app name> -c mongo-2.0

2) cd into the directory that matches your application name
	
	cd <your app name>
	
3) add this git repository to your application
	
	git remote add upstream -m master git://github.com/thesteve0/simple_node_express_mongo.git

4) merge this repository into your application

	git pull -s recursive -X theirs upstream master
	
5) Modify the code and push back up to your OpenShift gear

	git push
	

The MongoDB code you want to modify can be found in this line

	self.db.collection('names').find().toArray(function(err, names) {}
	



