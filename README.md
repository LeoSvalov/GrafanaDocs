# Getting Started with Grafana
This short tutorial aims to take you step-by-step on how to :  

*  [Install Grafana locally from its latest Docker image](https://github.com/LeoSvalov/GrafanaDocs#installing-grafana-locally-from-its-latest-docker-image).
*  [Open Grafana on the localhost and create a test dashboard](https://github.com/LeoSvalov/GrafanaDocs#open-grafana-on-the-localhost-and-create-a-test-dashboard).

## Installing Grafana locally from its latest Docker image
* **Preliminary step**:  Make sure that you have Docker installed. You can download the latest version [here](https://www.docker.com).

After docker setting up, follow the procedure:   
1. Download Grafana image  - `docker pull grafana/grafana`
2. Run the image - `docker run -d grafana/grafana`  
   Grafana is configured by default to run on port `3000`. It is possible that the default port is already in use by something other, hence fail of command will occur - `failed: port is already allocated`  
   In this case, you need to specify external port manually and run the command:  
   `docker run -d -p <external port>:<internal port> grafana/grafana`  
    Internal port is usually specified the same as default port.  
3. Open `localhost:<external port>` in Browser.  
   if everything went correctly, it will display a login interface that looks like this:  
    <img alt="Login interface" src="https://github.com/LeoSvalov/GrafanaDocs/blob/master/screenshots/Снимок%20экрана%202020-03-27%20в%2023.07.49.png" width="700" height="400">
## Open Grafana on the localhost and create a test dashboard
