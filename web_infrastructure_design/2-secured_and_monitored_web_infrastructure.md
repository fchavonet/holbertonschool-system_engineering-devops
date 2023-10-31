<img  height="50px" align="right" src="https://apply.holbertonschool.com/holberton-logo.png">

# Secured and monitored web infrastructure

## 📄 Description

This is the diagram of a three-server web infrastructure that hosts the website that is reachable via `www.foobar.com`.
It must be secured, serve encrypted traffic, and be monitored.

It contains one load balancer (HAProxy), two global servers, each with one web server (NGINX), one application server, application files (code base), and one database (MySQL).
The security is ensured by 1 SSL certificate, 3 firewalls, and 3 monitoring clients (data collectors for Sumo Logic or other monitoring services).

## 📑 Diagram

<img align="center" src="https://raw.githubusercontent.com/fchavonet/holbertonschool-system_engineering-devops/main/web_infrastructure_design/assets/2-secured_and_monitored_web_infrastructure.png">

## 🎓 Specifics about this infrastructure

- **What are firewalls for?**

    Tey are added to secure the infrastructure by controlling incoming and outgoing traffic, preventing unauthorized access, and safeguarding against malicious activity.

- **Why is the traffic served over HTTPS?**

    To encrypt the data transmitted between users and the website, ensuring confidentiality and data integrity. It protects against eavesdropping and data tampering.

- **What monitoring is used for?**

    It's used to track the performance, availability, and security of the infrastructure. It helps in identifying issues, optimizing resource usage, and ensuring system reliability.

- **How the monitoring tool is collecting data?**

    Monitoring tools collect data from monitoring clients, which gather information from various parts of the infrastructure, such as system metrics, application logs, and network activity. This data is then transmitted to monitoring services for analysis.

- **Explain what to do if you want to monitor your web server QPS:**

    To monitor the web server's Query Per Second (QPS), you would set up the monitoring tool to collect and analyze web server performance metrics, including request/response times and the number of queries processed per second.

## ⚠️ Issues with this infrastructure

- Terminating SSL at the load balancer can be an issue as it exposes the decrypted traffic internally. To address this, you may consider end-to-end encryption within the infrastructure to maintain security.

- Having a single MySQL server capable of accepting writes is a single point of failure (SPOF). If it fails, write operations are disrupted. Implementing a high-availability database cluster would address this issue.

- Having servers with identical components may be a problem if there's no diversity or redundancy. If one component fails, it could affect all servers in the same way. Consider diversifying components and introducing redundancy to enhance reliability.
