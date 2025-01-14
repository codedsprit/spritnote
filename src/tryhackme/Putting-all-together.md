# Putting all together
- Load Balancers 
- CDN(Content Delivery Network)
- Databases
- WAF(Web application Firewalls)
- How a web server works.
<hr>

#### Load Balancers
Load balancers ensure websites can handle high traffic and provide failover if a server becomes unresponsive.
When you request a website, the load balancer forwards the request to one of the multiple servers behind it, using algorithms like round-robin (sequential) or weighted (least busy).
They also perform health checks on servers. If a server becomes unresponsive, the load balancer will stop sending traffic until it's functional again.


![img](https://tryhackme-images.s3.amazonaws.com/user-uploads/5c549500924ec576f953d9fc/room-content/829e340231cd8aa9f5ed2fa5c464ea80.svg)

#### Content Delivery Network
A CDN reduces traffic to busy websites by hosting static files (JavaScript, CSS, images, videos) across thousands of servers worldwide. When a user requests a file, the CDN sends it from the nearest server instead of a distant location.
##### Databases
Websites store user data by communicating with databases, ranging from simple text files to complex server clusters for speed and resilience. Common databases include MySQL, MSSQL, MongoDB, and PostgreSQL, each with unique features.


![img](https://www.tatvasoft.com/blog/wp-content/uploads/2023/01/Types-of-NoSQL-Databases-2-min-768x389.jpg)

#### Web Application Firewalls
A WAF sits between the user and the web server, protecting against hacking or denial of service attacks. It analyzes web requests for common attack techniques, checks if the request is from a real browser, and uses rate limiting to control excessive requests. Suspicious requests are dropped before reaching the web server.

![img](https://tryhackme-images.s3.amazonaws.com/user-uploads/5c549500924ec576f953d9fc/room-content/24cb6468b4e51e8d8bbe7872e96a22b3.svg)

### How a Web Server Works.
- Virtual Hosts 
- Static vs Dynamic content
- Scripting / Backend language 


###### Virtual Hosts on Web Servers

Web servers use **virtual hosts** to host multiple websites with different domain names. Here's how it works:

- The server checks the **hostname** in the HTTP headers.
- It matches the hostname to a virtual host configuration.
- If a match is found, the corresponding website is served.
- If no match is found, the default website is shown.

###### Directory Mapping
Each virtual host can have its root directory mapped to a specific location on the server, for example:

- `one.com` → `/var/www/website_one`
- `two.com` → `/var/www/website_two`

###### Unlimited Hosting
There’s no limit to the number of websites a web server can host using virtual hosts.

#### Static vs Dynamic Content
##### Static Content
- Content that never changes.
- Examples: Images, JavaScript, CSS, and unchanging HTML files.
- Served directly from the web server without modifications.
##### Dynamic Content
- Content that changes based on requests.
- Examples: Blog homepages showing the latest entries or search results.
- Generated by the **Backend** using programming and scripting languages
##### Frontend vs Backend
- **Backend**: Processes and generates dynamic content behind the scenes.
- **Frontend**: Displays the resulting content (HTML, CSS, etc.) in the browser.

#### Backend Languages and Interactivity

##### Backend Capabilities
- Make websites interactive by:
  - Interacting with databases.
  - Calling external services.
  - Processing user data.
- Examples of backend languages: PHP, Python, Ruby, NodeJS, Perl, etc.

##### Example: PHP Script
Requesting `http://example.com/index.php?name=adam` with the script:

```php
<html><body>Hello <?php echo $_GET["name"]; ?></body></html>
```
output:
```
<html><body>Hello adam</body></html>
```


&nbsp;
<p align="center">
	<img src="https://raw.githubusercontent.com/catppuccin/catppuccin/main/assets/footers/gray0_ctp_on_line.svg?sanitize=true" />
</p>
<p align="center">
	Copyright &copy; 2024-present <a href="https://github.com/codedsprit" target="_blank">codedsprit.xyz</a>
</p>
