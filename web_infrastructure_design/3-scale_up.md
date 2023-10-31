<img  height="50px" align="right" src="https://apply.holbertonschool.com/holberton-logo.png">

# 3. Scale up

## 📄 Description

This is the diagram of a three-server web infrastructure that hosts the website that is reachable via `www.foobar.com`.
It must be secured, serve encrypted traffic, and be monitored.

It contains two load balancers (HAProxy), four global servers, each with one web server (NGINX), one application server, application files (code base), and the two databases (MySQL) are split components.
The security is ensured by a full SSL certificate, firewalls at every link point, and monitoring clients (data collectors for Sumo Logic or other monitoring services)."

## 📑 Diagram

<img align="center" src="https://raw.githubusercontent.com/fchavonet/holbertonschool-system_engineering-devops/main/web_infrastructure_design/assets/3-scale_up.png">

## 🎓 Specifics about this infrastructure

- **Why Add Load Balancers as a Cluster?**

    We add two load balancers configured as a cluster for redundancy and high availability. If one load balancer fails, the other can seamlessly take over, ensuring uninterrupted service. This minimizes the risk of a single point of failure.

- **Separating Components onto Individual Servers:**

    We split the components (web server, application server, and database) onto separate servers for better resource management and isolation. It enhances security, performance, and scalability. Isolating components also simplifies troubleshooting and maintenance.

The design splits the components onto individual servers, improving the overall infrastructure's flexibility and reliability. It's particularly useful for applications that need to scale and adapt to changing workloads. The load balancer cluster ensures that traffic is evenly distributed and provides resilience against load balancer failures.