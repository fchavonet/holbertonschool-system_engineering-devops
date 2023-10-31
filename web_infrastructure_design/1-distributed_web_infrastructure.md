<img  height="50px" align="right" src="https://apply.holbertonschool.com/holberton-logo.png">

# Distributed web infrastructure

## 📄 Description

This is the diagram of a three server web infrastructure that hosts the website that is reachable via `www.foobar.com`.

It contains one load-balancer (HAPROXY), two global servers, each with one web server (NGINX), one application server, application files (code base) and one database (MySQL).

## 📑 Diagram

<img align="center" src="https://raw.githubusercontent.com/fchavonet/holbertonschool-system_engineering-devops/main/web_infrastructure_design/assets/1-distributed_web_infrastructure.png">

## 🎓 Specifics about this infrastructure

- **Why Add a load-balancer?**

    Adding a load-balancer to distribute incoming traffic evenly across multiple application servers. This provides redundancy and ensures high availability. If one application server fails, the load balancer routes traffic to the remaining healthy servers.

- **What distribution algorithm your load balancer is configured with and how it works?**

    The load-balancer is configured with a Round Robin distribution algorithm. It works by sequentially forwarding each new request to the next server in line, distributing the load evenly.

- **Is your load-balancer enabling an Active-Active or Active-Passive setup?**

    The load balancer enables an Active-Active setup. In an Active-Active setup, both application servers are actively processing requests simultaneously. In an Active-Passive setup, one server is active, and the other is on standby, becoming active only if the primary server fails.

- **How a database Primary-Replica (Master-Slave) cluster works?**

    In this configuration, the Primary node is the master database that handles write operations (INSERT, UPDATE, DELETE), while the Replica node(s) are slaves that replicate data from the Primary. Read operations can be distributed to Replicas.

- **What is the difference between the Primary node and the Replica node in regard to the application?**

    The Primary node is responsible for handling write operations and maintaining the authoritative copy of the data. The Replica nodes copy data from the Primary and are used for read operations, reducing the load on the Primary and providing data redundancy.

## ⚠️ Issues with this infrastructure

- The load-balancer can become a SPOF (Single Point Of Failure) if it fails. To address this, you can implement a redundant load-balancer.

- The absence of a firewall poses a security risk, as it doesn't protect the infrastructure from unauthorized access or attacks.

- Lack of HTTPS leaves the infrastructure vulnerable to data interception and tampering during transmission. Implementing HTTPS is crucial for security.

- The infrastructure lacks monitoring, making it challenging to detect and respond to issues proactively. Monitoring tools should be implemented to ensure the system's health and performance.
