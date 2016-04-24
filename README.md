# TurnkeyLinux-FFA-IMS
Docker Container Template of FFA's IMS

#Clears the root directory and puts admin files in the webmin folder
RUN mkdir webmin
RUN mv *.* webmin
RUN mv cgi-bin css images js webmin

#Clones the IMS Repo
RUN git clone origin https://github.com/ano/TurnkeyLinux-FFA-IMS.git
