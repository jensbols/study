# Internet

## How does the internet work?
The internet is a global network of computers connected to each other which communicate through a standardized set of protocols.

It is build up out of a large number of independently operated networks. This means there is no central control.

---
## What is HTTP?

**HyperText Transfer Protocol** 

In a browser you type a URL **(Uniform Resource Locator)** when pressing enter the computer starts talking to another computer called a server. Your computer then asks the server for a website and that server starts talking back to you in a language called HTTP 

**HTTP** is the language used to communicate between web browsers and servers. There are different types of HTTP requests and the most basic one is the **GET** request. When surfing to facebook.com/login you are requesting the login page of facebook.

---
## Browsers and how they work
**HTML HyperText Markup Lanaguage** 

is the language used to tell the web browser how to make the page look. This includes the actual text of the page.

Other parts like images, videos are seperate files with their own URLs that need to be requested.

If you are logging in on a website using a post request. You will mostlikely receive some sort of cookie to authorize you viewing/editing the received webpages. So everytime you request a new page you will send your cookie and the server will validate that you are who you say you are.

Now all the information is being sent in plain text. This makes it possible for hackers to intercept and read the data.

A solution to this is SSL **(Secure Sockets Layer)** or its succesor **(Transport Layer Security)** They are a layer of security wrapped around your communications. To protect them from snooping or tampering. You can see if a website is using SSL by the locket on the left side of the URL. The URL will also be https:// which stands for http-secure.

---
## DNS and how it works

### Domain Name Service

**DNS** is the system that translates human-readable domain names to IP adresses.

**IP adresses** are the numerical, uniquely assigned values that locate a particular server on the internet.

When you surf to a website you need to go through a process called DNS resolution. This is when the browser makes a request to a DNS Name Server. This server will respond with a unique IP adress of the website. The browser will cache this IP adress and make requests to the physical adress of the server to get the response which is a HTML page or any other resource.


### The Process of resolving URL to IP
1. Client Requests Domain
    - Computer will check Browser & Operating System Cache to short circuit the entire process.
1. DNS Resolver
    - Usually owned by your ISP
    - Check Resolver Cache if other people have made the same requests in the past, this again to short circuit the entire process.
1. Root Nameservers
    - Collective of 13 different servers distributed globally. 
    - Known as A -> M servers.
    - Managed by large corporate entities or academic institutions. (ex. Nasa, ICANN,...)
    - When the Root Nameserver doesn't have the requested IP it will check if it knows a server that knows the IP.
1. TLD Nameservers
    - TLD = Top Level Domain
    - These name servers end in (.com, .edu, .org,...)
1. Authorotative Name Server

We start at the top and end at the bottom, at each level we hope to receive the IP to the server we actually want to visit. If not we go down a level in hopes of finding the IP adress.

### The Process of resolving content from IP
1. Client Requests Domain (172.217.11.174)
    - Request to the server to view ex. google.com
      - Google server replies with files to fulfill this request.
      - Browser will interpret the files and load the page.
    - Browser will Cache the IP adress for a limited time for future reference.

---

## Domain Name

Is a string of text (ex. google.com) that maps to a numeric IP adress, used to access a website from client server (ex. browser)

## Hosting
Is the process of renting or buying space to house a website on the World Wide Web. Website content such as HTML, CSS and images have to housed on a server to be viewable online.
