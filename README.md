# Deploying a Full Stack Ecommerce Website on Kubernetes with Istio Service Mesh

Welcome to the deployment project for a full-stack Ecommerce website on Kubernetes using the powerful Istio Service Mesh. This project covers a wide range of topics, providing a comprehensive guide to deploying, managing, and securing microservices in a Kubernetes environment with Istio. 

## Project Overview

Utilizing JHipster, I have developed a microservice-webapp application with a Java-based backend and a ReactJs frontend.

My setup involves a Kubernetes single-node cluster, configured for production use, orchestrating these microservices to form a dynamic Ecommerce website. Istio is my service mesh of choice, which is employed to enhance the capabilities of our microservices. Please find below the attached Microservice Architecture deployment on Kubernetes Cluster along with Istio.
<br>
<div align="center">
    <img src="https://github.com/Adi2023/Kubernetes_IstioService_Deployment/blob/master/MicroService-Architecture-on-istio.jpg" width="800">
</div>
<br>

This project will be focusing on key features such as:

### Traffic Management

- **Load Balancing:** Distributed incoming traffic evenly across microservice instances to optimize performance and resource utilization.
- **Canary Deployments:** Safely roll out new features by gradually introducing updates to a small subset of users before a full deployment.
- **A/B Testing:** Experimented with different versions of a microservice to gather insights into user preferences and performance metrics.
- **Fault Injections:** Simulated real-world failure scenarios to ensure system resilience and graceful degradation.

### Routing and Traffic Splits

- **Dynamic Routing:** Controlled and managed traffic flow between microservices based on custom routing rules.
- **Traffic Splits:** Gradually shift traffic between different versions of microservices to minimize the impact of changes.

### Timeouts, Circuit Breaking, and Retries

- **Timeouts:** Set response time limits for microservices to prevent slow or unresponsive components from affecting the entire system.
- **Circuit Breaking:** Implemented mechanisms to prevent cascading failures by isolating problematic services.
- **Retries:** Handled transient failures gracefully by configuring the service mesh to retry failed requests.

## Security Implementations

As part of our commitment to security, the project delves into various Istio features aimed at securing our Ecommerce application:

- **Oauth2 Proxy Authentication:** Implemented robust user authentication mechanisms to ensure that only authorized entities interact with our microservices using OAuth2 authentication. To understand how this works, please go through the below flowchart:
<br>
<p align="center">
  <img src="https://github.com/Adi2023/Kubernetes_IstioService_Deployment/blob/master/Outh2-Istio.jpg" width="400" style="margin-right: 10px;"/>
  <img src="https://github.com/Adi2023/Kubernetes_IstioService_Deployment/blob/master/Oauth2-SequenceDiagram.png" width="400" style="margin-left: 10px;"/>
</p>
- **Peer Authentication:** Enforcing mutual TLS (mTLS) authentication between microservices for secure communication.
- **Request Authentication:** Protecting endpoints by validating JWT tokens to ensure the legitimacy of incoming requests.
- **Authorization:** Controlled access to microservices based on predefined policies to enhance security.
- **Network Policies:** Enforcing fine-grained network traffic control with Kubernetes network policies, isolating specific microservices like invoice and product from unauthorized access.
- **Docker Image Scanning:** Utilized Trivy for scanning Docker images for vulnerabilities, ensuring secure and reliable containers in production.
- **Kube-Bench Integration:** Implemented kube-bench for assessing Kubernetes cluster security based on CIS benchmarks, ensuring adherence to best practices.
- **Non-Root User Privileges:** Deployed containers with non-root user privileges to enhance security and minimize the impact of potential exploits.
- **Certificate Management:** Implemented and managed SSL/TLS certificates for secure communication.

## Monitoring the Application

Monitoring the application is a key aspect to know how our application behaves under various conditions. I have used the famous monitoring duo - Prometheus and Grafana. As Kiali goes well with Istio Mesh I have used it for monitoring my traffic state of the application. 


- **Prometheus and Grafana:** Deploy Prometheus for monitoring and Grafana for visualizing metrics, providing insights into the performance and health of microservices.
- **Kiali:** Utilize Kiali for observability into the service mesh, including topology visualization and tracing of service interactions.


## Getting Started

Feel free to get started with this microservice architecture and play around with additional Istio features.

## Contributions

Contributions and feedback are welcome! If you encounter issues, have suggestions, or want to contribute, please feel free to open an issue or submit a pull request.

Please feel free to provide your suggestions as this will help me to learn more about Istio Mesh along with additional Kubernetes concepts. 
Happy Learning! 

Let's build and deploy resilient, scalable, and secure Ecommerce applications together! 🚀
