# LogStash Boilerplate

[https://www.elastic.co/products/logstash](Logstash) is great tool to process and analyze gigantic log files. This project lets you start a new project with a clean slate and some common settings to help you carry out your analysis.


# Requirements

* Java 7 or higher
* LogStash
* Ubuntu 14 or Debian-based box (use vagrant for local development)

# Installation

First, you need to have Java installed:

```
sudo add-apt-repository -y ppa:webupd8team/java
sudo apt-get update
sudo apt-get -y install oracle-java8-installer
```

Then, install Logstash:

```
wget -qO - https://packages.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -
echo "deb http://packages.elastic.co/logstash/2.1/debian stable main" | sudo tee -a /etc/apt/sources.list
sudo apt-get update
sudo apt-get install logstash
```


# Usage

sample configuration files can be found in config folder. You can copy the blank.conf file and rename it to something else and start adding your configurations.
You should store the raw log files in the input folder and output stuffs in output folder. That is how you can everything neat and organized.

Processing a file is as simple as:
```
logstash -f config/your.conf
``` 

replace the your.conf with whatever config file you had written.
