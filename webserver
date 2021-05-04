#!/bin/bash
serverstart()
{
sudo service apache2 start
if [ $? == 0 ]
then
	echo "service started successfully"
	sudo mv index.html /var/www/html/
	echo "server started successfully"
	firefox 127.0.0.1
else
	echo "service not started"
	echo "trying to renstall apache2"
	sudo apt-get install --reinstall apache2
fi
}
which apache2 > /dev/null
if [ $? == 0 ]
then
 	echo "apache2 is already installed"
	service start
else
	ping -c 3 google.com
	if [ $? == 0 ]
	then
		sudo apt-get updae -y
		sudo apt-get install apache2 -y
		service start	
	else
		echo "check your internet connection"
fi
fi
