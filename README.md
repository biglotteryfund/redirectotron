# redirectotron
A simple web server which sends traffic to the main website.

To use, create a new webserver and install Nginx. Use the provided `servers.conf` file here to handle redirecting our domains to the main website.

## SSL

We use [`certbot`](https://certbot.eff.org/instructions) to provision SSL certificates for the domains this server handles. It will automatically renew SSL certificates and update the above Nginx config to use the correct keys etc. 

## DNS
The current Redirectotron server has a fixed IP provided by AWS Elastic IP – `3.10.98.141`. It also has a CNAME – `redirectotron.blf.digital`. Any domain names can be redirected to our main website (https://www.tnlcommunityfund.org.uk/) by setting their `A` record to the above IP, or by creating a `www` `CNAME` to the above `CNAME` value.
