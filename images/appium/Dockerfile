
	#############################################################
	# dockerfile to run appium for testing iOS apps             #
	#############################################################

	FROM ubuntu:14.04
	MAINTAINER jruffing@gmail.com

	# install appium dependencies
	RUN apt-get update
	RUN apt-get -y install nodejs npm git
	RUN ln -s /usr/bin/nodejs /usr/bin/node

	# get appium src in /opt/appium/src folder
	RUN mkdir -p /opt/appium/src && cd /opt/appium/src
	RUN git clone https://github.com/appium/appium.git

	# open appium port 
	#EXPOSE 4723
	
	# install appium server to /opt/source/.appium-npm/ via npm
	#RUN mkdir -p /opt/source/.appium-npm/
	#RUN cd /opt/source/.appium-npm/ && npm install appium
	
	# run appium's latest server
	#RUN mkdir -p /opt/source/appium/ && cd /opt/source/appium
	#CMD ./reset.sh --ios
	#CMD /opt/source/.appium-npm/node_modules/appium/bin/appium.js