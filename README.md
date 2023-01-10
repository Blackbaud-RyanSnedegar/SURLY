# SURLY
OTG Short URL yippeee relinker


## Short base URL?
 - blkbd.org|.co domain
 - bbcloud.tech|.me
 - l.$domain/ for links.  Adds a bit of length but allows for other usage of the domain later.  
 - ladmin.$domain/ for admin.
 - for full implementation we should use geoip DNS.
 - for full implementation, SSL
 
## Which software to use?
 - POLR: https://github.com/Antelope-Valley-College/polr
 - BIY: https://realpython.com/build-a-python-url-shortener-with-fastapi/ and others
 - Some other third thing

## API?
 - yes.
 - admin-server hosted, not on every web server.
 - db backed? [depends on tooling]
 - add, delete, stats calls if possible?

## Admin page?
 - api functions but on a web page!
 - for full implementation, AD auth
 - add an edit url option here.  

## Which servers to use?
 - most likely, azure vm's.  
 - DB can be hosted on azure mysql, though may be cheaper to run a vm and host our own with the admin interface.
 - for full implementation, an admin server to handle api and db updates, and geo-located web servers as needed to handle redirection (US, EU, APAC?)
 - can start with one location and expand as needed.

## Security?
 - Admin interface should be restricted to VPN endpoints.
 - harden vm's to current standards for cloud hosts.

## Logs:
 - will have to plug into cloud splunk?
 - local storage for web servers for n timeframe.

## Monitoring:
 - depends on os team[s] supporting it.

## Billing:
 - Ooooh that'll be a fun one. Admin/DB hosts would be $30-40/mo on 3yr agreement, web servers may want to scale based on traffic, but probably similar.  2x web + 1 db per location, one main admin/db host, and geoip dns, divide by number of products using it, etc.

