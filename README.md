# 🚀 E-Commerce Website Using Docker, Kubernetes & Istio Service Mesh

*A Cloud-Native Microservices-Based E-Commerce Platform*

This project demonstrates how a modern **e-commerce application** can be built using a **microservices architecture**, containerized using **Docker**, orchestrated with **Kubernetes**, and monitored using a **service mesh** (Istio with Kiali, Grafana, and Jaeger).

It showcases **scalability**, **fault tolerance**, **observability**, and **real-world cloud-native engineering practices**.

---

## 📌 **Table of Contents**

* [Overview](#-overview)
* [Architecture](#-architecture)
* [Tech Stack](#-tech-stack)
* [Microservices](#-microservices)
* [Docker Setup](#-docker-setup)
* [Kubernetes Deployment](#-kubernetes-deployment)
* [Istio Service Mesh](#-istio-service-mesh)
* [Monitoring & Observability](#-monitoring--observability)
* [Screenshots](#-screenshots)
* [Conclusion](#-conclusion)
* [Team](#-team)

---

# 🌐 Overview

This project implements a **cloud-native microservices e-commerce website**, inspired by the "Online Boutique" architecture.

Using:

* **Docker** → containerization
* **Kubernetes** → orchestration & scaling
* **Istio** → traffic management, load balancing, and security
* **Kiali / Grafana / Jaeger** → full observability

The goal is to demonstrate how distributed microservices can be deployed, scaled, traced, and monitored efficiently.

As explained in the publication **(page 26–32)** , the system solves real modern challenges in:

* dependency management
* service isolation
* traffic visibility
* monitoring interactions between microservices
* ensuring high resilience and fault tolerance

---

# 🏗 Architecture

A complete microservices-based architecture consisting of independent services such as:

* Frontend
* Product Catalog
* Cart
* Checkout
* Payment
* Email
* Shipping
* Currency
* Ads
* Recommendation
* Redis Cache
* Load Generator

Each service runs inside **its own Docker container**, deployed as **Kubernetes pods**, and connected via **Istio sidecar proxies**.

---

# 🛠 Tech Stack

### **Backend & Infrastructure**

* **Docker**
* **Kubernetes**
* **Istio Service Mesh**
* **Redis**
* **gRPC / REST APIs**

### **Monitoring & Tracing**

* **Grafana (Telemetry & dashboards)**
* **Kiali (service graph & traffic visualization)**
* **Jaeger (distributed tracing)**

### **Cloud-Native Principles**

* Microservices
* Service isolation
* Autoscaling
* Observability

---

# 📦 Microservices

From the implementation section of the publication (pages 30–31) :

| Service             | Description                                             |
| ------------------- | ------------------------------------------------------- |
| **Frontend**        | User interface for browsing products and placing orders |
| **Product Catalog** | Stores & serves product data                            |
| **Cart**            | Manages user shopping carts                             |
| **Checkout**        | Coordinates orders, payments & processing               |
| **Payment**         | Integrates with payment gateways                        |
| **Email**           | Sends transactional emails                              |
| **Shipping**        | Handles order shipment logic                            |
| **Currency**        | Converts currencies dynamically                         |
| **Ads**             | Displays targeted ads                                   |
| **Recommendation**  | Generates personalized recommendations                  |
| **Redis**           | High-performance caching                                |
| **Load Generator**  | Simulates real user traffic for testing                 |

---

# 🐳 Docker Setup

Each microservice contains its own `Dockerfile`.

Example structure from publication :

```bash
# Build docker image
docker build -t service-name .

# Run container
docker run -d -p 8080:8080 service-name
```

All images are then pushed to a container registry (local or cloud).

---

# ☸ Kubernetes Deployment

Kubernetes manages:

* Pods
* ReplicaSets
* Scaling
* Load balancing
* Rolling updates

Example deployment workflow :

```bash
kubectl apply -f deployment.yaml
kubectl get pods
kubectl get services
```

---

# 🔀 Istio Service Mesh

Istio adds:

* **Traffic management**
* **Load balancing**
* **Retry policies**
* **Circuit breaking**
* **Zero-code security + mTLS**
* **Telemetry collection**

Each microservice is automatically injected with a **sidecar envoy proxy**.

The Kiali dashboard shows how traffic flows between services with real-time metrics.

---

# 📊 Monitoring & Observability

### **Grafana** 

Used for:

* Telemetry dashboards
* Error tracking
* Request/response times
* Performance monitoring

### **Jaeger** 

Provides:

* End-to-end request tracing
* Root-cause diagnosis
* Visual DAG of service calls

Together, they give a **complete view of system health**.

---

# 🖼 Screenshots

Here’s what the system looks like (from various figures):

### **🛍 Frontend UI**

Modern e-commerce interface.
Includes:

* Product listing
* Product details
* Cart & checkout

### **📈 Kiali Service Graph**

Shows all microservices and live traffic flow.

### **📊 Grafana Dashboard**

Real-time metrics for latency, errors, uptime.

### **🕵️ Jaeger Tracing**

Distributed tracing across all services.

---

# 🧾 Conclusion

As concluded in the study :

This project demonstrates how **containerization + Kubernetes + Istio** provide:

* ✔️ High scalability
* ✔️ Strong isolation
* ✔️ Automated deployments
* ✔️ Traffic management
* ✔️ Deep observability
* ✔️ Modern cloud-native e-commerce architecture

It represents a **complete end-to-end microservices system** with real industry-level technologies.

---

*(Rajiv Gandhi Institute of Technology — Department of Computer Engineering)*
Publication: *E-Commerce Websites Through Containerization, Kubernetes Orchestration, and Istio Service Mesh Monitoring*.

---
