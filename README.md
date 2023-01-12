# SURLY
OTG Short URL yippeee relinker


## base URL
 - should be able to handle multiple domains
 - blkbd.org|.co, bbcloud.tech|.me, justgive.to, etc
 - for full implementation geoip DNS?
 - for full implementation, SSL

## Which software to use?
 - https://github.com/amitt001/pygmy is a good start, would require some work to make it complete

## Link shortening
 - fixed length hash?  Is this worth doing?
 - link expiration option? Off by default

## API?
 - admin-server hosted, not on every web server.
 - add, delete, stats calls if possible?
 - API user or key tied to single domain. 

## UI pages?
 - login page (tie into AD)
 - main link page (create a new link, edit a link)
 - admin page (default shows basic stats, click to api key mgmt, domains)
 - api management page (default shows list, click to add, edit, remove, blacklist, whitelist)
 - domain page (default shows list, click to add, edit, remove)
 - blacklist page (default shows blocked keywords/domains, click to add, edit, remove)
 - whitelist page (default shows list of ranges, click to add, edit, remove)

## where to run?
 - best bet, azure vm's.  
 - for full implementation, an admin server to handle api and db updates, and geo-located web servers as needed to handle redirection (US, EU, APAC?)
 - can start with one location and expand as needed.

## Security?
 - Admin interface should be restricted to VPN endpoint ip ranges for access.
 - API interface should be restricted to product ip ranges.
 - harden vm's to current standards for cloud hosts.

## Logs:
 - will have to plug into cloud splunk
 - local storage for web servers for n timeframe.

## Monitoring:
 - depends on os team[s] supporting it, but admin page test and at least one short url redirector should get tested.  DCM has various locations, so would help ID if a local instance was having issues.
 

