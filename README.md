# How it works
1. Install `ipsherlock` client on your device
2. That's it

When you want to know the IP address of your device visit https://ip.jena.at and see the IP of your local devices.

# How it works internally
`ipsherlock` client is sending the information about each network adapter. The client is sending a JSON dictionary
containing the following items:

* `address` (string, required): Address of the device (usuall IPv4 or IPv6 address)
* `label` (string, optional): Label to be shown
* `interface` (string, optional): Used interface to send this request (like `"wlan0"` or `"eth0"`)
* `links` (list, optional): A list of dictionaries describing links that can be followed
  * `scheme` (string, required): Used scheme (e.g. `http`)
  * `userinfo` (string, optional): Optional user info (e.g. ftp://**user**@server.org)
  * `port` (integer, optional): Port number to be used
  * `path` (string, optional): Path section of the URI
  * `query` (string, optional): Query part (the part behind the query operator `?`)
  * `framgent` (string, optional): Fragment part (begind the fragment operator `#`)
  * `label` (string, optional): Label to show
  * `description` (string, optional): Additional description of this links
* `data` (object, optional): Additional data for individual purpose
