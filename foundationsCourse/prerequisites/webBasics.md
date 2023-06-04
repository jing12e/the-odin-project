Overview
---
- Describe what the internet is.
- Describe what packets are and how they are used to transfer data
- Understand the differences between a web page, web server, web browser and search engine.
- Briefly explain what a client is.
- Briefly explain what a server is.
- Explain what IP addresses are.
- Explain what DNS servers are.

[How does the web work?](https://www.theodinproject.com/lessons/foundations-how-does-the-web-work)

How the Internet work?
---
**servers**
computers that store webpages, sites, or apps. When a client device wants to access a webpage, a copy of the webpage is downloaded from the server onto the client machine to be displayed in the user's web browser.

**clients**
typical web user's internet-connected devices (for example, your computer connected to your Wi-Fi, or your phone connected to your mobile network) and web-accessing software available on those devices (usually a web browser like Firefox or Chrome).

**ISP (Internet Service Provider)**
company that manages some special routers that are all linked together and can also access other ISPs' routers.
DSL
 
**Routers** 
shuttle packets of information across the internet, and transmit e-mail, pictures, and web pages.
like **signaler**

**modem**
turns the information from our network into information manageable by the telephone infrastructure and vice versa.
![picture](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work/internet-schema-7.png)

Finding computers
---
unique internet protocol address (IP address)

Internet and the web
---
the Internet is a technical infrastructure which allows billions of computers to be connected all together.
Among those computers, some computers (called Web servers) can send messages intelligible to web browsers.

Intranets and Extranets
---
Intranets are private networks that are restricted to members of a particular organization.
Extranets are very similar to Intranets, except they open all or part of a private network to allow sharing and collaboration with other organizations. 

How does web work?
---
[article](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works)
For now, let's imagine that the web is a road. On one end of the road is the client, which is like your house. On the other end of the road is the server, which is a shop you want to buy something from.

**Your internet connection**
Allows you to send and receive data on the web. It's basically like the street between your house and the shop.

**TCP/IP**
Transmission Control Protocol and Internet Protocol are communication protocols that define how data should travel across the internet. 

**DNS**
Domain Name System is like an address book for websites. When you type a web address in your browser, the browser looks at the DNS to find the website's IP address before it can retrieve the website. The browser needs to find out which server the website lives on, so it can send HTTP messages to the right place (see below). This is like looking up the address of the shop so you can access it.

**HTTP**
Hypertext Transfer Protocol is an application protocol that defines a language for clients and servers to speak to each other. This is like the language you use to order your goods.

**Component files** 
A website is made up of many different files, which are like the different parts of the goods you buy from the shop. These files come in two main types:
- Code files: Websites are built primarily from HTML, CSS, and JavaScript, though you'll meet other technologies a bit later.
- Assets: This is a collective name for all the other stuff that makes up a website, such as images, music, video, Word documents, and PDFs.    
  


When you type a web address into your browser (for our analogy that's like walking to the shop)
- The browser goes to the **DNS server**, and finds the real address of the server that the website lives on (you find the address of the shop).
- The browser sends an **HTTP request** message to the server, asking it to send a copy of the website to the client (you go to the shop and order your goods). This message, and all other data sent between the client and the server, is sent across your internet connection using **TCP/IP**.
- If the server approves the client's request, the server sends the client a "200 OK" message, which means "Of course you can look at that website! Here it is", and then starts sending the website's files to the browser as a series of small chunks called **data packets** (the shop gives you your goods, and you bring them back to your house).
- The browser assembles the small chunks into a complete web page and displays it to you (the goods arrive at your door — new shiny stuff, awesome!).

How does a DNS request work?
---
As we already saw, when you want to display a webpage in your browser it's easier to type a domain name than an IP address. Let's take a look at the process:

- Type mozilla.org in your browser's location bar.
- Your browser asks your computer if it already recognizes the IP address identified by this domain name (using a local DNS cache). If it does, the name is translated to the IP address and the browser negotiates contents with the web server. End of story.
- If your computer does not know which IP is behind the mozilla.org name, it goes on to ask a DNS server, whose job is precisely to tell your computer which IP address matches each registered domain name.
- Now that the computer knows the requested IP address, your browser can negotiate contents with the web server.
![picture](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/What_is_a_domain_name/2014-10-dns-request2.png)
Resolving name server
root name server
Com TLD name server
Authoratative name servers
cache
meemory

Webpage vs. Website vs. Web server vs. Search engine
---
**A web page** is a simple document displayable by a browser. Such documents are written in the HTML language. 
**A website** is a collection of linked web pages (plus their associated resources) that share a unique domain name.
**A web server** is a computer hosting one or more websites. "Hosting" means that all the web pages and their supporting files are available on that computer. 
**A search engine** is a special kind of website that helps users find web pages from other websites.
**A browser** is a piece of software that retrieves and displays web pages; **a search engine** is a website that helps people find web pages from other websites. (Chrome (broswer) uses Google as its default search engine)


