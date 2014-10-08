dk2-blender-java-web-sockets
============================

Preliminary Oculus dk2 support for Blender via OculusWS http://laht.info/dk2-sensor-data-websocket-server/
we presuppose that you have the latest firmware for the Oculus dk2
Using OS Mavericks the following instructions will differ slightly for windows

So far we have a basic .blend file which requires websocket-client 0.18.0 https://pypi.python.org/pypi/websocket-client/
which depended on six.
Both modules were installed by installing python 3.4 from https://www.python.org/downloads/ and then installing set-up tools:

curl https://bootstrap.pypa.io/ez_setup.py -o - | python3  
Both modules were installed by installing python 3.4 from https://www.python.org/downloads/ and then installing set-up tools:   
curl https://bootstrap.pypa.io/ez_setup.py -o - | python3  
If you are using windows follow the instructions here:  
https://pypi.python.org/pypi/setuptools
After installing setuptools run
easy_install-3.4 websocket-client 
There doesn't (seem) to be an easy way to install Python modules within the Python version that comes with Blender. So we had to copy the files from 
/Library/Frameworks/Python.framework/Versions/3.4/lib/python3.4/site-packages/ 
to 
/Applications/Blender/blender.app/Contents/MacOS/2.71/python/lib/python3.4/site-packages (assuming Blender is in Applications)
(OS X Paths, Windows Path will differ)
We've included the jar file and required libraries as a file OculusWS.zip
First off the java SE must be installed onto your machine, you can follow the link http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
From here you will download and install the version based on your specific machine.
unzip the file and grab the jar file for the program which will be found in the dist folder of the zip file.
Then in order to run the file, you will use the terminal to call this command java -jar nameOfJarFile
Original Blender Python code was adapted from Lubosz's Blog from http://lubosz.wordpress.com/2013/06/26/oculus-rift-support-in-blender-game-engine/ 

