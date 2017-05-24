# NeubotTests

Collection of *download/upload HTTP speedtests* obtenined through the [Neubot project](http://www.neubot.org). See [Analyzing Large Data Collections with Apache Pig](http://espinosa-oviedo.com/big-data-visualization/hands-on/analyzing-large-data-collections-with-apache-pig/) for an example of how to work with this data collection. 

### Schema

Collection's records have the following structure:

Name | Description
---- | ------------
client_address |	User IP address (IPv4 or IPv6)
client_country |	Country where the test was conducted
lon | Longitud derived from client_address
lat | Latitud derived from client_address
client_provider |	Name of user’ internet provider
mlabservername  | Name of the server used for conducting the experiment
connect_time |	Number of seconds elapsed between the reception of the first and last package (Round-Trip Time)
download_speed |	Download speed (bytes/secs)
neubot_version |	Neubot version used for this test
platform |	User operative system
remote_address |	IP address (IPv4 or IPv6) of the server used for this test
test_name	| Test type (ex., speedtest, bittorrent, dash)
timestamp	| Time at which the test was realized. Measured as the number of seconds elapsed after 1/01/1970 (cf. UNIX timestamp)
upload_speed	| Upload speed (bytes/secs)
latency	| Delay between the sent and reception of a control package
uuid	| User ID (generated automatically by Neubot during installation)
asnum	| Internet provider’ ID
region	| Country region in which the test was realized (if known)
city	| Name of the city
hour	| derived from timestamp
month | derived from timestamp
year | derived from timestamp
weekday | derived from timestamp
day | derived from timestamp
filedate | derived from timestamp


### Installation 

```sh     
unzip "speedtests/*.zip" -d speedtests/
sudo rm -r .git speedtests/*.zip speedtests/__MACOSX  
```

### References 

- [Challenges and Issues on Collecting and Analyzing Large Volumes of Network Data Measurements](https://www.measurementlab.net/publications/analyzing-network-data-measurements.pdf)
- [Measuring DASH Streaming Performance from the End Users Perspective using Neubot](https://nexa.polito.it/nexacenterfiles/basso2014measuring.pdf)
- [Polito Internet Media Group](http://media.polito.it/wordpress/measuring-dash-streaming-performance-from-the-end-users-perspective-using-neubot/)
