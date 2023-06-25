•	Both backend and frontend base image is node:13.12.0-alpine since the application is running on node version: 13.12.0
•	The client image has been created using multistage to minimize on the size. This was done in two stages builder stage and package stage. nginx:stable-alpine was used as the package base minimizing image size to 43.1mb.
•	Networking achieved via subnet: 172.100.0.0/16 application connected via the database network.
•	Application connected to mongo db that is creating volumes.
•	Application https://github.com/Vinge1718/yolo forked and cloned.
•	Instructions given on the read me followed and node and npm version amended by adding >= for the  client to run.
•	Backed image tagged and pushed to docker hub as rwambui/yolo-backend:1.0.0 and client as rwambui/yolo-client:1.0.0.
•	Yolo client running successfully and products added successfully.
•	Added products are maintaintained and are visible both locally and mongo dB databases.
