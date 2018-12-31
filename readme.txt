First configure the ribbon-time-service
main java file
app.properties

start discovery service first 
ribbon-time-service
create 2 instances using run configurations
ribbon-client-1(4444) and ribbon-client-2(5555)

Run both instance
http://localhost:4444/
The current time is Mon Dec 31 18:45:51 IST 2018 (answered by service running on 4444)
http://localhost:5555/
The current time is Mon Dec 31 18:45:40 IST 2018 (answered by service running on 5555)

http://localhost:8762/
TIME-SERVICE	n/a (2)	(2)	UP (2) - localhost:time-service:4444 , localhost:time-service:5555


now we'll write code to to use Ribbon to Load balance btw each of the instance of ribbon-time-service

ribbon-time-app
RibbonTimeAppApplication - after writing code, run it.
http://localhost:8080/

