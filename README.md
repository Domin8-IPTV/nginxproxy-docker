# nginxproxy-docker
Nginx Reverse Proxy 


How to use:
----


```
git clone https://github.com/random-robbie/nginxproxy-docker.git
cd nginxproxy-docker
nano nginx.vh.default.conf
```

Change USERAGENT to the user agent you need.
Change NEWURL to your domain i.e proxy.domain.com
Change IP to the IP address you wish to use for the x-forwarded-for
Change OLDURLWITHHTTP to the origin address i.e http://something.akamaihd.net/
Change OLDURL to the origin with no http or https i.e something.akamaihd.net

Build
----
```
docker build -t oldurl .
docker run oldurl:latest -p 80
```

now when you vist the new url it should reverse proxy the origin url.

