# Getting Started with Grafana
This short tutorial aims to take you step-by-step on how to :  

*  [Install Grafana locally from its latest Docker image](https://github.com/LeoSvalov/GrafanaDocs#installing-grafana-locally-from-its-latest-docker-image)
*  [Open Grafana on the localhost and create a test dashboard](https://github.com/LeoSvalov/GrafanaDocs#open-grafana-on-the-localhost-and-create-a-test-dashboard)

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
You have installed Grafana and opened it in Browser.  
Now, it is time to make the first steps in Grafana:
1. When you firstly log in Grafana, type `admin` for the username and password.  
   After that, change your the username and password.
2. When you have logged in to Grafana, the main menu is displayed.  
   Click __*Add data source*__ 
   
   
   <img alt="Main interface" src="https://github.com/LeoSvalov/GrafanaDocs/blob/master/screenshots/Снимок%20экрана%202020-03-27%20в%2023.08.43.png" width="700" height="400">  
   
   
   Select the __TestData DB__ data source:
   
   
    <img alt="Add data source" src="https://github.com/LeoSvalov/GrafanaDocs/blob/master/screenshots/Снимок%20экрана%202020-03-28%20в%2017.02.05.png" width="700" >  
      
      
3. To create a test dashboard, click __*Build a dashboard*__  in the main menu.  
   After that, click __*Add query*__ on appeared panel:  
   
    <img alt="New query" src="https://github.com/LeoSvalov/GrafanaDocs/blob/master/screenshots/Снимок%20экрана%202020-03-28%20в%2017.15.34.png" width="700" >  
      
      
4. You can choose different scenarios and visualization modes for your new query.  
   As an example, you can have a look on the following query:  
   
   <img alt="Query edit mode" src="https://github.com/LeoSvalov/GrafanaDocs/blob/master/screenshots/Снимок%20экрана%202020-03-28%20в%2017.53.01.png" width="700" >    
      
   You can configure your query in the 4 subclasses: __Queries, Visualization, General and Allert__ settings.  
   
   _In this particular example, there are __Graph__ visualization mode and 2 scenarious for A-series - __Random Walk(with error)__ and for B-series - __CVS Metric Values__ are used._ 
   
