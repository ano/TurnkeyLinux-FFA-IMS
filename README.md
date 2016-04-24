# TurnkeyLinux-FFA-IMS
Docker Container Template of FFA's IMS
```Dockerfile
#Update and install required packages for PHPMaker applications
RUN apt-get update
RUN apt-get -y install php5-curl php5-cli git php5-mysql apt-get install php5-adodb
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer 

#Clears the root directory and puts admin files in the webmin folder
RUN mkdir webmin
RUN mv *.* webmin
RUN mv cgi-bin css images js webmin


#Clones the IMS Repo
RUN git clone origin https://github.com/ano/TurnkeyLinux-FFA-IMS.git
```
