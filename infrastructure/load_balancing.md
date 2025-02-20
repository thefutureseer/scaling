# Load Balancing

## Introduction
Load balancing is a crucial aspect of building scalable and highly available applications. It ensures that incoming traffic is distributed across multiple servers to optimize resource utilization, prevent overload, and improve response times.

---

## Why Load Balancing?
- **Improves Performance**: Distributes traffic to prevent bottlenecks.
- **Enhances Availability**: Prevents downtime by rerouting traffic to healthy servers.
- **Scalability**: Supports horizontal scaling by adding or removing instances.
- **Security**: Protects against DDoS attacks and ensures redundancy.

---

## Types of Load Balancing
### 1️⃣ **DNS Load Balancing**
- Uses **multiple IP addresses** for a single domain.
- Provides **geographic distribution** of traffic.
- Limited control over real-time traffic distribution.

### 2️⃣ **Layer 4 Load Balancing (Transport Layer)**
- Operates at the **TCP/UDP level**.
- Routes traffic based on **IP addresses and ports**.
- Example: **AWS Elastic Load Balancer (ELB), Nginx, HAProxy**.

### 3️⃣ **Layer 7 Load Balancing (Application Layer)**
- Operates at the **HTTP/HTTPS level**.
- Routes traffic based on **URL paths, headers, cookies**.
- Example: **NGINX, Traefik, AWS ALB, Envoy**.

---

## Load Balancing Algorithms
### ✅ **Round Robin**
- Distributes requests sequentially across servers.
- Best for **equal resource distribution**.

### ✅ **Least Connections**
- Directs traffic to the server with the **fewest active connections**.
- Best for **handling uneven traffic loads**.

### ✅ **IP Hash**
- Routes traffic based on **client IP addresses**.
- Ensures session persistence.

### ✅ **Weighted Round Robin**
- Assigns higher priority to powerful servers.
- Best for **heterogeneous server environments**.

---

## Load Balancing in Cloud Platforms
| Cloud Provider | Load Balancer | Features |
|---------------|--------------|----------|
| AWS | Elastic Load Balancer (ELB) | Supports TCP, HTTP, HTTPS, WebSockets |
| GCP | Cloud Load Balancer | Global distribution, autoscaling |
| Azure | Azure Load Balancer | Layer 4 balancing for TCP/UDP |

---

## Best Practices
✅ **Use Auto Scaling**: Ensure that new instances spin up automatically under high load.
✅ **Enable Health Checks**: Regularly monitor backend services to detect failures.
✅ **Implement Caching**: Use CDN and in-memory stores (Redis) to reduce server load.
✅ **SSL Termination**: Offload SSL processing to the load balancer to reduce backend CPU usage.
✅ **Monitor & Log**: Use observability tools (Prometheus, Grafana) to track traffic patterns and health metrics.

---

## Conclusion
Load balancing is a key component of scalable architecture. Choosing the right strategy depends on traffic patterns, infrastructure, and business requirements. Implementing proper load balancing techniques ensures optimal performance, security, and availability for your application.

---

### 🔗 **Further Reading (The docs)**
- [NGINX Load Balancing Guide](https://www.nginx.com/resources/glossary/load-balancing/)
- [AWS Elastic Load Balancing](https://aws.amazon.com/elasticloadbalancing/)
- [Kubernetes Load Balancing](https://kubernetes.io/docs/concepts/services-networking/service/)
