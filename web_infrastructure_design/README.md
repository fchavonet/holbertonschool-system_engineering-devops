<img height="50" align="right" src="https://raw.githubusercontent.com/fchavonet/fchavonet/refs/heads/main/assets/images/logo-holberton_school.webp" alt="Holberton School logo">

# Project title

## Table of contents

<details>
    <summary>
        CLICK TO ENLARGE 😇
    </summary>
    <a href="#description">Description</a>
    <br>
    <a href="#objectives">Objectives</a>
    <br>
    <a href="#requirements">Requirements</a>
    <br>
    <a href="#instructions">Instructions</a>
    <br>
    <a href="#tech-stack">Tech stack</a>
    <br>
    <a href="#files-description">Files description</a>
    <br>
    <a href="#installation_and_how_to_use">Installation and how to use</a>
    <br>
    <a href="#thanks">Thanks</a>
    <br>
    <a href="#authors">Authors</a>
</details>

## <span id="description">Description</span>

This project focuses on web infrastructure design, by creating diagrams and explaining the role of each component in a typical web stack.

The final goal is to be able to whiteboard different architectures and explain them clearly in an interview or peer-learning setting.

## <span id="objectives">Objectives</span>

At the end of this project, I should be able to explain to anyone, **without the help of Google**:

- Draw and explain a complete web stack.  
- Describe the role of each component (server, DNS, web server, application server, database).  
- Explain system redundancy and scaling principles.  
- Understand acronyms like LAMP, SPOF, and QPS.  
- Identify security concerns and monitoring strategies. 

## <span id="requirements">Requirements</span>

- Create diagrams for each task (whiteboard, paper or draw.io).  
- Upload screenshots of the diagrams to an image hosting service.  
- Link screenshots inside each task file.  
- Be ready to whiteboard live in front of staff or peers (no notes or computer).  
- Keep explanations short and precise (like in interviews). 

## <span id="instructions">Instructions</span>

### Mandatory

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
- File: `3-scale_up`.
<hr>
</details>

## <span id="tech-stack">Tech stack</span>

<p align="left">
    <img src="https://img.shields.io/badge/DRAW.IO-F08705?logo=diagramsdotnet&logoColor=white&style=for-the-badge" alt="Photoshop badge">
    <img src="https://img.shields.io/badge/PHOTOSHOP-011e37?logo=data:image/svg+xml;base64,PCFET0NUWVBFIHN2ZyBQVUJMSUMgIi0vL1czQy8vRFREIFNWRyAxLjEvL0VOIiAiaHR0cDovL3d3dy53My5vcmcvR3JhcGhpY3MvU1ZHLzEuMS9EVEQvc3ZnMTEuZHRkIj4KDTwhLS0gVXBsb2FkZWQgdG86IFNWRyBSZXBvLCB3d3cuc3ZncmVwby5jb20sIFRyYW5zZm9ybWVkIGJ5OiBTVkcgUmVwbyBNaXhlciBUb29scyAtLT4KPHN2ZyBmaWxsPSIjZmZmZmZmIiB2ZXJzaW9uPSIxLjEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiIHdpZHRoPSI4MDBweCIgaGVpZ2h0PSI4MDBweCIgdmlld0JveD0iMCAwIDUxMiA1MTIiIGVuYWJsZS1iYWNrZ3JvdW5kPSJuZXcgMCAwIDUxMiA1MTIiIHhtbDpzcGFjZT0icHJlc2VydmUiIHN0cm9rZT0iI2ZmZmZmZiI+Cg08ZyBpZD0iU1ZHUmVwb19iZ0NhcnJpZXIiIHN0cm9rZS13aWR0aD0iMCIvPgoNPGcgaWQ9IlNWR1JlcG9fdHJhY2VyQ2FycmllciIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIi8+Cg08ZyBpZD0iU1ZHUmVwb19pY29uQ2FycmllciI+IDxnIGlkPSIyMDY5YTQ2MGRjZjI4Mjk1ZTIzMWYzMTExZTAzNzU1MiI+IDxwYXRoIGRpc3BsYXk9ImlubGluZSIgZD0iTTQyNi4zMzMsMC41SDg1LjY2N0MzOC44MjUsMC41LDAuNSwzOC44MjUsMC41LDg1LjY2N3YzNDAuNjY3YzAsNDYuODQyLDM4LjMyNSw4NS4xNjcsODUuMTY3LDg1LjE2NyBoMzQwLjY2N2M0Ni44NDIsMCw4NS4xNjctMzguMzI1LDg1LjE2Ny04NS4xNjdWODUuNjY3QzUxMS41LDM4LjgyNSw0NzMuMTc1LDAuNSw0MjYuMzMzLDAuNXogTTI0NS4zMjksMjYwLjUyNCBjLTE3LjczNiwxNy43MzYtNDUuNjExLDI2LjA2NS03Ny4xMDMsMjYuMDY1Yy04LjMyNiwwLTE1LjkyNy0wLjM2NS0yMS43Mi0xLjQ1MXY5MS45NDVoLTQ0LjE1OVYxMzYuMzYzIGMxNS45MjctMi44OTUsMzguMDA5LTUuMDY5LDY4LjA1LTUuMDY5YzMyLjU4MiwwLDU2LjQ3Myw2Ljg3OCw3Mi4wMzksMTkuOTExYzE0LjQ4LDExLjk0NywyMy44OSwzMS4xMzEsMjMuODksNTMuOTM2IEMyNjYuMzI1LDIyOC4zMDksMjU5LjA4NiwyNDcuNDkyLDI0NS4zMjksMjYwLjUyNHogTTMzNy45ODEsMzgwLjcwNmMtMjEuMzU4LDAtNDAuNTQyLTUuMDY5LTUzLjU3NC0xMi4zMWw4LjY4Ny0zMi4yMTYgYzEwLjEzNSw2LjE1NCwyOS4zMjIsMTIuNjcxLDQ1LjI0OSwxMi42NzFjMTkuNTQ1LDAsMjguMjM2LTcuOTY0LDI4LjIzNi0xOS41NDljMC0xMS45NDMtNy4yMzktMTguMDk5LTI4Ljk2LTI1LjcgYy0zNC4zOTEtMTEuOTQ3LTQ4Ljg2Ni0zMC43NjktNDguNTA1LTUxLjQwM2MwLTMxLjEzMSwyNS43LTU1LjM4Myw2Ni42MDQtNTUuMzgzYzE5LjU0OSwwLDM2LjU2Miw1LjA2OSw0Ni42OTUsMTAuNDk2IGwtOC42ODcsMzEuNDkzYy03LjYwMi00LjM0Mi0yMS43MjEtMTAuMTM1LTM3LjI4NS0xMC4xMzVjLTE1LjkyOCwwLTI0LjYxNSw3LjYwMi0yNC42MTUsMTguNDZjMCwxMS4yMjQsOC4zMjYsMTYuNjU1LDMwLjc3LDI0LjYxOCBjMzEuODU0LDExLjU4Miw0Ni42OTYsMjcuODcxLDQ3LjA1OCw1My45MzdDNDA5LjY1MywzNTcuNTM5LDM4NC42NzgsMzgwLjcwNiwzMzcuOTgxLDM4MC43MDZ6IE0yMjEuOCwyMDYuOTUgYzAsMjguNTk4LTIwLjI3Myw0NC44ODctNTMuNTc0LDQ0Ljg4N2MtOS4wNDksMC0xNi4yODktMC4zNjItMjEuNzItMS44MDl2LTgyLjUzNGM0LjcwOC0xLjA4NSwxMy4zOTUtMi4xNzEsMjUuNzA0LTIuMTcxIEMyMDIuOTc5LDE2NS4zMjMsMjIxLjgsMTc5LjgwMywyMjEuOCwyMDYuOTV6Ij4gPC9wYXRoPiA8L2c+IDwvZz4KDTwvc3ZnPg==&logoColor=white&style=for-the-badge" alt="Photoshop badge">
    <img src="https://img.shields.io/badge/GIT-f05032?logo=git&logoColor=white&style=for-the-badge" alt="Git badge">
    <img src="https://img.shields.io/badge/GITHUB-181717?logo=github&logoColor=white&style=for-the-badge" alt="GitHub badge">
    <img src="https://img.shields.io/badge/MARKDOWN-000000?logo=markdown&logoColor=white&style=for-the-badge" alt="Markdown badge">
</p>

## <span id="files-description">Files description</span>

| **FILES**                                       | **DESCRIPTION**                                                             |
| :---------------------------------------------: | --------------------------------------------------------------------------- |
| `assets`                                        | Contains the resources required for the repository.                         |
| `0-simple_web_stack`                            | Task 0 response with screenshot links.                                      |
| `0-simple_web_stack.md`                         | Detailed explanation for Task 0 diagram.                                    |
| `1-distributed_web_infrastructure`              | Task 1 response with screenshot links.                                      |
| `1-distributed_web_infrastructure.md`           | Detailed explanation for Task 1 diagram.                                    |
| `2-secured_and_monitored_web_infrastructure`    | Task 2 response with screenshot links.                                      |
| `2-secured_and_monitored_web_infrastructure.md` | Detailed explanation for Task 2 diagram.                                    |
| `3-scale_up`                                    | Task 3 response with screenshot links.                                      |
| `3-scale_up.md`                                 | Detailed explanation for Task 3 diagram.                                    |
| `all_for_one.md`                                | Contains all diagram screenshots for a global overview and easy comparison. |
| `README.md`                                     | The README file you are currently reading 😉.                               |

## <span id="installation_and_how_to_use">Installation and how to use</span>

### Installation:

1. Clone this repository:
    - Open your preferred Terminal.
    - Navigate to the directory where you want to clone the repository.
    - Run the following command:

```bash
git clone https://github.com/fchavonet/holbertonschool-system_engineering-devops.git
```

2. Open the repository you've just cloned.

3. Navigate to the `web_infrastructure_design` directory:

```bash
cd web_infrastructure_design
```

You can also view all diagrams in a single file for a global overview by clicking [here](./all_for_one.md).

### How to use:

1. Open the `.md` files or the diagrams in the assets folder.

## <span id="thanks">Thanks</span>

- A big thank you to all my Holberton School peers for their help and support throughout this project.

## <span id="authors">Authors</span>

**Fabien CHAVONET**
- GitHub: [@fchavonet](https://github.com/fchavonet)
