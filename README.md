# wpdev
A shellscript to create and manage an ubiqitous wordpress development environment.

**Once you execute this script it's create three container:**
* Frist container for database of mysql based on Orboan/dcsss-mariadb image.
* Second container for wordpress based on orboan/dcsss-httpd-wpdev image.
* And the third one of Cloud9 for php coding based on kdelfour/cloud9-docker image.

### Usage of this script

**wpdev run -d domain_name**

Creates and start the three containers and with **-d** option set the domain name used to asscess your wordpress development environment.

**_Note:_**  -d  option is totally optional to use.

**wpdev start -d domain_name**

Start the three containers if they are stopped.

**wpdev stop -d domain_name**

Stop the three containers if they are running.

**wpdev rm -d domain_name**

Remove all three container whether they are running or stopped.


### Prerequisites for using this script

* docker installed in your system
* Save this script with execution permissions in a directory included in the path (so you can easy execute the script fro anywhere)
* Create a subdirectory under your home directory /home/username/ 
* Now enter the directory that you created and execute the script: $wpdev run -d domain_name 

Once the all three container are running you can access your wordpress typing your domain_name in the browser and with domain_name:81 you can access the Cloud9 IDE to start developing.

### Examples:

**wpdev run -d manager.swarm.asix**

Creates and starts the three containers and with -d  option we are setting the manager.swarm.asix used to access the development environment but the default one is localhost.

**wpdev start**

Starts all three container if they are stopped.

