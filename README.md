1. **vagrant up**
2. **vagrant ssh app**
3. **cd /home/ubuntu/app**
4. **sudo npm install ejs mongoose express**
5. **node seeds/seed.js**
6. **node app.js**


- Web servers:
  - Apache
  - Microsoft IIS
  - Nginx
    - Lightweight
    - Small server
    - Fast
    - Embeddable
- A web server is a computer that stores web server software and a website's component files
  - It is connected to the internet and supports physical data interchange with other devices connected to the web
- Reverse proxy
  - Type of proxy server that retrieves resources on behalf of a client from one or more servers
  - These resources are then returned to the client, appearing as if they originated from the proxy server itself
  - It sits in front of webservers and forwards client requests to those web servers


1. **cd /etc**
2. **cd nginx**
3. **cd sites-enabled**
4. **cat default**
5. **sudo vi default**
6. Scroll to the location to insert
    ````
    location / {
            proxy_pass http://localhost:3000;
    ````
7. System needs to restart, run following commands:
  - **sudo systemctl stop nginx**
  - **sudo systemctl start nginx**
  - To check -> **sudo nginx -t**
8. **cd ~**
9. **cd /home/ubuntu/app**
10. **node app.js**
