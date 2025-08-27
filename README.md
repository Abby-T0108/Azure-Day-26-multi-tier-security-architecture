# Azure-Day-26-multi-tier-security-architecture
Project Overview

This project showcases the deployment of a secure 3-tier enterprise network architecture in Microsoft Azure. 
The design implements Zero Trust principles and defense-in-depth, demonstrating how to protect cloud workloads against modern threats.

Architecture Highlights
1. Three-Tier Model: Web -> Application -> Database
2. Network Segmentation: Dedicated subnets with controlled east–west traffic
3. Application Gateway with WAF: Protects web apps against OWASP Top 10 attacks
4. Azure Bastion: Secure administrative access with no exposed public IPs
5. NSGs: Enforced least privilege policies between tiers

Security Outcomes
1. Database accessible only from the application tier
2. WAF successfully blocked simulated SQL injection and XSS attempts
3. Admin access available only through Azure Bastion
4. No direct internet access to internal resources
5. Network traffic fully logged for auditing and analysis

Internet
    │
    ▼
┌─────────────────────┐
│ Application Gateway │ ── WAF Protection
└─────────────────────┘
           │
           ▼
    ┌─────────────┐      ┌─────────────┐      ┌─────────────┐
    │ Web Subnet  │ ──── │ App Subnet  │ ──── │ DB Subnet   │
    └─────────────┘      └─────────────┘      └─────────────┘
           │                      │                      │
           ▼                      ▼                      ▼
    [Web Servers]         [App Servers]          [Database]
                                    │
                                    ▼
                            ┌─────────────┐
                            │   Bastion   │
                            └─────────────┘


Skills Demonstrated
1. Multi-tier cloud security architecture design
2. NSG and WAF configuration for defense-in-depth
3. Zero Trust access controls with Bastion
4. Traffic flow analysis and security validation
5. Aligning deployments with Azure Security Benchmark and NIST CSF

Learning Outcomes
1. This project demonstrates the ability to:
2. Architect secure, enterprise-grade Azure environments
3. Apply best practices for cloud compliance and resilience
4. Deliver production-ready network security solutions

Project Status
* Day: 26 of 100 Days of Cloud Deployment
* Status: Complete



