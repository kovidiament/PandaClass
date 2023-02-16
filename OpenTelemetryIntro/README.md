# Open Telemetry Getting Started
This directory contains the work done to follow the open telemetry tutorial, starting in week one.
The Python tutorial at https://opentelemetry.io/docs/instrumentation/python/getting-started/ was followed.

Built and ran the docker container as follows:
docker build -t tag-goes-here:latest
docker run -p 5000:5000 tag-goes-here:latest

To access the dice roll webpage on the host, go to the second IP address listed in the console flask output,
under the /rolldice endpoint. 
For example, http://172.17.0.2:5000/rolldice