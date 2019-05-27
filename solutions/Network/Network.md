# Network

## Question 1.

### solution
Use a webhook to make github send a post request to our local server so that our program is notified of any push event, verify that the request has indeed been sent by github by checking sha1 hash calculated with the help of signature  
*progam is in the github update folder*

### approach
1. make a local server to listen for post requests
2. make localhost publicly available by a public domain
3. register the public domain as webhook url in github
4. whenever we recieve a post request in our local server check the sha1 to make sure that it is indeed from github and then execute git pull

### resources
1. [sha1-compare-function](https://gist.github.com/stigok/57d075c1cf2a609cb758898c0b202428)
2. [public-ssh-server](https://serveo.net/)
3. [github-webhooks](https://medium.com/chingu/how-to-verify-the-authenticity-of-a-github-apps-webhook-payload-8d63ccc81a24)

### working video
[github auto pull](https://www.youtube.com/watch?v=f88w0HjFxkQ)

### How to use
1. run `npm install` to install all node modules
2. run `ssh -R 80:localhost:3000 serveo.net` to start a reverse ssh tunnel. This will make your localhost public. You will get a public url (lets call it URL1) note it.
3. paste the absolute path to git repository folder and a random string to serve as a secret in config.js
4. run `node app.js` to start the local webserver
5. visit URL1/github in browser, if you see a message saying server in running then its all set up
6. go to github repository page > settings > webhooks > add new webhook
7. enter URL1/github as payload url
8. select application/json as payload format
9. put the secret that you saved in config.js
10. It should now listen for push events and update your local repository ! (see the video if any step is not clear)

## Question 2. 

### solution 
The domain students.iitmandi.ac.in has been bought from [ERNET India](http://www.ernet.in)

### approach 
Perform whois lookup on _"students.iitmandi.ac.in"_ to get domain related info

### resources 
1. [WhoIS](http://whois.domaintools.com/)
2. [WhoIS](https://www.whois.com/)
