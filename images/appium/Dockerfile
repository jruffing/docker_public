
	#############################################################
	# dockerfile to run appium for testing iOS apps             #
	#############################################################

	FROM ubuntu:14.04
	MAINTAINER jruffing

	RUN apt-get update
	RUN apt-get -y install nodejs git

	# create user
	RUN mkdir /opt/appium
	RUN useradd -m -s /bin/bash appium
	RUN chown -R appium:appium /opt/appium
	ENV HOME /home/appium

	# install appium
	RUN cd /opt && git clone https://github.com/appium/appium.git

	# open appium port 
	EXPOSE 4723
	
	# start appium server
	RUN cd /opt/appium
	CMD ./reset.sh
	CMD /opt/appium/node_modules/appium/bin/appium.js --device-ready-timeout 180