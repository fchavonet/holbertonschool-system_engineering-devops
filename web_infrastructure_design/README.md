<img  height="50px" align="right" src="https://apply.holbertonschool.com/holberton-logo.png">

# Web infrastructure design

## 🎓 Objective

At the end of this project, I had to be able to explain to anyone, without the help of Google :

- You must be able to draw a diagram covering the web stack you built with the sysadmin/devops track projects.
- You must be able to explain what each component is doing.
- You must be able to explain system redundancy.
- Know all the mentioned acronyms: LAMP, SPOF, QPS.

## 🔨 Tech stack

<p align="left">
    <img src="https://img.shields.io/badge/DRAW.IO-F08705?logo=diagramsdotnet&logoColor=white&style=for-the-badge" alt="Photoshop badge">
    <img src="https://img.shields.io/badge/PHOTOSHOP-31A8FF?logo=adobephotoshop&logoColor=white&style=for-the-badge" alt="Photoshop badge">
    <img src="https://img.shields.io/badge/UBUNTU-e95420?logo=ubuntu&logoColor=white&style=for-the-badge" alt="Ubuntu badge">
    <img src="https://img.shields.io/badge/VIM-019733?logo=vim&logoColor=white&style=for-the-badge" alt="VIM badge">
<p>

## 📋 Requirements

- For each task, once you are done whiteboarding (on a whiteboard, piece of paper or software or your choice), take a picture/screenshot of your diagram.
- Upload a screenshot, showing that you completed the required levels, to any image hosting service.
- For the following tasks, insert the link from of your screenshot into the answer file.
- After pushing your answer file to GitHub, insert the GitHub file link into the URL box.

## 📝 Instruction

### <span id="mandatory-tasks">Mandatory tasks</span>

<details>
	<summary>
		<b>Task. 0. Simple web stack</b>
	</summary>
	<br>

A lot of websites are powered by simple web infrastructure, a lot of time it is composed of a single server with a <a href="https://en.wikipedia.org/wiki/LAMP_%28software_bundle%29">LAMP stack</a>.

On a whiteboard, design a one server web infrastructure that hosts the website that is reachable via `www.foobar.com`. Start your explanation by having a user wanting to access your website.

Requirements:

- You must use:
    - 1 server.
    - 1 web server (NGINX).
    - 1 application server.
    - 1 application files (your code base).
    - 1 database (MySQL).
    - 1 domain name `foobar.com` configured with a `www` record that points to your server IP `8.8.8.8`.

- You must be able to explain some specifics about this infrastructure:
    - What is a server?
    - What is the role of the domain name?
    - What type of DNS record `www` is in `www.foobar.com`?
    - What is the role of the web server?
    - What is the role of the application server?
    - What is the role of the database?
    - What is the server using to communicate with the computer of the user requesting the website?

- You must be able to explain what the issues are with this infrastructure:
    - SPOF.
    - Downtime when maintenance needed (like deploying new code web server needs to be restarted).
    - Cannot scale if too much incoming traffic.

Please, remember that everything must be written in English to further your technical ability in a variety of settings.
#
**Repo:**
- GitHub repository: `holbertonschool-system_engineering-devops`.
- Directory: `web_infrastructure_design`.
- File: `0-simple_web_stack`.
<hr>
</details>

<details>
	<summary>
		<b>Task. 1. Distributed web infrastructure</b>
	</summary>
	<br>

On a whiteboard, design a three server web infrastructure that hosts the website `www.foobar.com`.

Requirements:

- You must add:
    - 2 servers.
    - 1 web server (NGINX).
    - 1 application server.
    - 1 load-balancer (HAproxy).
    - 1 set of application files (your code base).
    - 1 database (MySQL).

- You must be able to explain some specifics about this infrastructure:
    - For every additional element, why you are adding it.
    - What distribution algorithm your load balancer is configured with and how it works?
    - Is your load-balancer enabling an Active-Active or Active-Passive setup, explain the difference between both.
    - How a database Primary-Replica (Master-Slave) cluster works.
    - What is the difference between the Primary node and the Replica node in regard to the application?

- You must be able to explain what the issues are with this infrastructure:
    - Where are SPOF.
    - Security issues (no firewall, no HTTPS).
    - No monitoring.

Please, remember that everything must be written in English to further your technical ability in a variety of settings.
#
**Repo:**
- GitHub repository: `holbertonschool-system_engineering-devops`.
- Directory: `web_infrastructure_design`.
- File: `1-distributed_web_infrastructure`.
<hr>
</details>

<details>
	<summary>
		<b>Task. 2. Secured and monitored web infrastructure</b>
	</summary>
	<br>

On a whiteboard, design a three server web infrastructure that hosts the website `www.foobar.com`, it must be secured, serve encrypted traffic, and be monitored.

Requirements:

- You must add:
    - 3 firewalls.
    - 1 SSL certificate to serve `www.foobar.com` over HTTPS.
    - 3 monitoring clients (data collector for Sumologic or other monitoring services).

- You must be able to explain some specifics about this infrastructure:
    - For every additional element, why you are adding it.
    - What are firewalls for?
    - Why is the traffic served over HTTPS?
    - What monitoring is used for?
    - How the monitoring tool is collecting data.
    - Explain what to do if you want to monitor your web server QPS.

- You must be able to explain what the issues are with this infrastructure:
    - Why terminating SSL at the load balancer level is an issue?
    - Why having only one MySQL server capable of accepting writes is an issue?
    - Why having servers with all the same components (database, web server and application server) might be a problem?

Please, remember that everything must be written in English to further your technical ability in a variety of settings.
#
**Repo:**
- GitHub repository: `holbertonschool-system_engineering-devops`.
- Directory: `web_infrastructure_design`.
- File: `2-secured_and_monitored_web_infrastructure`.
<hr>
</details>

<details>
	<summary>
		<b>Task. 3. Scale up</b>
	</summary>
	<br>

Readme:

<a href="https://intranet.hbtn.io/rltoken/QHWrcB0kVYwbgWCsL57mkQ">Application server vs web server</a>

Requirements:

- You must add:
    - 1 server.
    - 1 load-balancer (HAproxy) configured as cluster with the other one.
    - Split components (web server, application server, database) with their own server.

- You must be able to explain some specifics about this infrastructure:
    - For every additional element, why you are adding it.

Please, remember that everything must be written in English to further your technical ability in a variety of settings.
#
**Repo:**
- GitHub repository: `holbertonschool-system_engineering-devops`.
- Directory: `web_infrastructure_design`.
- File: `https://intranet.hbtn.io/rltoken/QHWrcB0kVYwbgWCsL57mkQ`.
<hr>
</details>

## 📂 Files description

| **FILE** | **DESCRIPTION** |
| :-----: | ----- |
| all_for_one.md | A file with all the diagram screenshots to get a good overview and compare them easily. |
| 0-simple_web_stack | Task 0 response with screenshot links. |
| 0-simple_web_stack.md | Detailed explanation for Task 0 diagram. |
| 1-distributed_web_infrastructure | Task 1 response with screenshot links. |
| 1-distributed_web_infrastructure.md | Detailed explanation for Task 1 diagram. |
| 2-secured_and_monitored_web_infrastructure | Task 2 response with screenshot links. |
| 2-secured_and_monitored_web_infrastructure.md | Detailed explanation for Task 2 diagram. |
| 3-scale_up | Task 3 response with screenshot links. |
| 3-scale_up.md | Detailed explanation for Task 3 diagram. |
| README.md | The readme file you are currently reading 😉. |
| assets | Directory with diagram screenshots. |

## ♥️ Thanks

A big thank you to all my Holberton School peers for their help and support throughout these projects.
