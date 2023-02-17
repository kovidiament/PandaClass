# Open Telemetry Getting Started
This directory contains the work done to follow the open telemetry tutorial, starting in week one.
The Python tutorial at https://opentelemetry.io/docs/instrumentation/python/getting-started/ was followed.


Built and ran the docker container as follows:
docker build -t tag-goes-here:latest .
docker run -p 5000:5000 tag-goes-here:latest

To access the dice roll webpage on the host, go to the second IP address listed in the console flask output,
under the /rolldice endpoint. 
For example, http://172.17.0.2:5000/rolldice
Screenshot example of running the docker container and getting a trace :
![image](https://user-images.githubusercontent.com/31549975/219453633-393edbba-09af-4934-94f3-48254ee0631d.png)
![image](https://user-images.githubusercontent.com/31549975/219453797-3f6a23a6-610a-41cc-8b1c-43d54967a3f0.png)
![image](https://user-images.githubusercontent.com/31549975/219453979-ad36c732-f7ef-4382-bdee-71a13b064e7f.png)

![image](https://user-images.githubusercontent.com/31549975/219454070-ff166486-75da-451f-a1c1-cc352c925648.png)



Deployed to microk8s based on this tutorial : https://medium.com/manikkothu/build-and-deploy-apps-on-microk8s-1df26d1ddd3c