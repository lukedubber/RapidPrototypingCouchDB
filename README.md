Rapid Prototyping with CouchDB
=======================

Document a work in progress!
==========================

This repository contains the examples I used during my presentation on using CouchDB as a backend for rapid prototyping.
If you have not seen the video or looked at he presentation it can be found here.

[Presentation (place holder)](http://example.com)

[Presentation Video (place holder)](http://example.com)

Goal
--------
The purpose of the Presentation and example code is to demo the idea of using a NoSQL backend for quick and loose 
data storage to use in prototype apps. This can be for a yourself, client or a for a startup weekend to show off 
concept to interested investors.


Apache2 config notes
-----------
These are the changes I had to make in order to proxy the service through a directory. If you want to get around the [same-origin policy](http://www.w3.org/Security/wiki/Same_Origin_Policy). This is what I have found to get it to work. But this is for a basic unsecure setup. 
<pre>
	AllowEncodedSlashes On
	ProxyRequests Off
	ProxyPass /db http://localhost:5984 nocanon
	ProxyPassReverse /db http://localhost:5984
	RequestHeader unset Authorization
</pre>
