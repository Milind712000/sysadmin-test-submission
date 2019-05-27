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

## Question 2. 

### solution 
The domain students.iitmandi.ac.in has been bought from [ERNET India](http://www.ernet.in)

### approach 
Perform whois lookup on _"students.iitmandi.ac.in"_ to get domain related info

### resources 
1. [WhoIS](http://whois.domaintools.com/)
2. [WhoIS](https://www.whois.com/)