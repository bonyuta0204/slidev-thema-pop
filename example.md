---
theme: ./
title: Modern Cloud Architecture
subtitle: Building Scalable and Resilient Systems
---

# Modern Cloud Architecture

<Badge>2025 Edition</Badge>

---
layout: center
---

# Key Pillars of Cloud Architecture

---

# Cloud Architecture Pillars

<MenuList :items="[
  'Scalability',
  'Reliability',
  'Security',
  'Cost Optimization',
  'Performance'
]" />

---

# Cloud Architecture Pillars

<MenuList :items="[
  'Scalability',
  'Reliability',
  'Security',
  'Cost Optimization',
  'Performance'
]" :activeIndex="0"/>

---

# Scalability Patterns

## Designing for Growth

- Horizontal scaling
- Microservices architecture
- Stateless design
- Load balancing

---

# Cloud Architecture Pillars

<MenuList :items="[
  'Scalability',
  'Reliability',
  'Security',
  'Cost Optimization',
  'Performance'
]" :activeIndex="2"/>

---

# Security Best Practices

<BoxList :items="[
  'Zero Trust Model',
  'Defense in Depth'
]"/>

---

# Security Best Practices

<BoxList :items="[
  'Zero Trust Model',
  'Defense in Depth'
]" :activeIndex="0"/>

---
layout: image-right
image: https://images.unsplash.com/photo-1558494949-ef010cbdcc31
---

# Infrastructure as Code

```yaml
resources:
  webserver:
    type: compute.v1.instance
    properties:
      machineType: e2-medium
      zone: us-central1-a
      networkInterfaces:
        - network: global/networks/default
      disks:
        - boot: true
          autoDelete: true
          initializeParams:
            sourceImage: projects/debian-cloud/global/images/family/debian-11
```

---
layout: center
---

# Deployment Strategies

---

# Deployment Options

<MenuList :items="[
  'Blue-Green Deployment',
  'Canary Releases',
  'Feature Flags',
  'Rolling Updates'
]" />

---
layout: default
---

# Learn More

[Cloud Architecture Center](https://cloud.google.com/architecture) · [AWS Well-Architected](https://aws.amazon.com/architecture/well-architected/) · [Azure Architecture Center](https://learn.microsoft.com/azure/architecture/)

<Badge>Thank You!</Badge>
