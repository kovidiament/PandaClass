# Open Telemetry and Istio Introduction
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

Istio was set up with help from this tutorial : https://www.youtube.com/watch?v=voAyroDb6xk .

The default namespace received the label, or key-value pair, to enable istio.
 ![image](https://user-images.githubusercontent.com/31549975/220732916-5ddafb82-eefd-4f3b-9e69-4992b4d3935d.png)


The deployment was then deleted and restarted, so that the istio injection would take place afterward. 
When “get pod” is run after restart, there are now two containers per pod because of istio.
 
![image](https://user-images.githubusercontent.com/31549975/220732975-b9675b5b-2c57-43c0-a253-f5001d9ddade.png)


The jaeger addon was applied. This added the tracing and jaeger-collector services to the istio-system namespace.
 ![image](https://user-images.githubusercontent.com/31549975/220733087-2d9fa423-6d41-4687-9e5b-9b108238da5d.png)

The jaeger dashboard was started. 
 ![image](https://user-images.githubusercontent.com/31549975/220733140-47d131c2-16e6-4a96-a9c1-75b7555a1072.png)

The rolldice webpage was loaded a few times, giving traces in the dashboard.
 
 
![image](https://user-images.githubusercontent.com/31549975/220733169-ffab1df2-5388-471b-8011-796e0a6a4660.png)

![image](https://user-images.githubusercontent.com/31549975/220733198-41c9d099-9147-4d68-a2e6-4ef6370756bd.png)

