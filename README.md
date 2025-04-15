# Cloud Native Web Application Infrastructure

This repository serves as the central hub for my cloud-native web application project. This full-stack implementation demonstrates building, deploying, and managing cloud-native applications with emphasis on AWS infrastructure, CI/CD pipelines, security best practices, and infrastructure automation.

## Table of Contents
- [Overview](#overview)
- [Project Repositories](#project-repositories)
- [Skills & Technologies](#skills--technologies)
- [Project Development Phases](#project-development-phases)
- [Infrastructure Architecture](#infrastructure-architecture)
- [CI/CD Pipeline](#cicd-pipeline)
- [Security Measures](#security-measures)

## Overview

This project demonstrates the implementation of a production-ready, full-stack cloud-native web application using modern AWS infrastructure. The application architecture follows industry best practices for security, scalability, and reliability while maintaining cost efficiency.

### Project Highlights:

- **Robust Full-Stack Application:**
  - React.js frontend with responsive design principles
  - Node.js/Express.js backend implementing RESTful architecture
  - MySQL relational database with optimized schema design
  - S3 integration for scalable object storage

- **Enterprise-Grade Infrastructure:**
  - Complete IaC deployment with Terraform
  - Multi-AZ, auto-scaling architecture
  - Defense-in-depth security model
  - Comprehensive monitoring and observability

- **DevOps Excellence:**
  - Fully automated CI/CD pipeline
  - Immutable infrastructure with custom AMIs
  - Blue-green deployment methodology
  - Comprehensive testing and validation

- **Security-First Design:**
  - Encryption in transit and at rest
  - Least privilege access controls
  - Secure secret management
  - Regular security scanning and updates

## Project Repositories

The architecture is divided into three distinct repositories following microservices best practices:

### 1. [Web Application Repository]([https://github.com/yourusername/webapp](https://github.com/CSYE6225-Network-Strctrs-Cloud-Cmpting/webapp))
The application layer implementing both frontend and backend components:
- **Frontend:** Interactive React.js single page application
- **Backend:** Node.js/Express.js RESTful API architecture
- **Features:**
  - User authentication and authorization
  - File management with secure upload/download capabilities
  - Health monitoring endpoints
  - Stateless design for horizontal scalability
  - Integration with S3 for object storage

**Technical Highlights:**
- React component architecture with hooks
- Express middleware for request processing
- MySQL ORM integration
- Advanced error handling with standardized responses
- Containerized local development environment
- Comprehensive Jest test suite for API validation
- SystemD service configuration for production reliability

### 2. [Infrastructure as Code Repository]([https://github.com/yourusername/tf-aws-infra](https://github.com/CSYE6225-Network-Strctrs-Cloud-Cmpting/tf-aws-infra))
Enterprise-grade Infrastructure as Code (IaC) implementation using Terraform:
- **Network Layer:** Complete VPC architecture with public/private subnet segregation
- **Compute Layer:** Auto-scaling EC2 deployment with custom AMI integration
- **Data Layer:** Managed RDS MySQL configuration with multi-AZ options
- **Security Layer:** Defense-in-depth approach with multiple security controls

**Implementation Details:**
- Modular Terraform architecture for reusability
- Environment-specific configuration with variable injection
- State management with remote backend for team collaboration
- Advanced IAM role and policy configurations
- Resource tagging strategy for cost allocation and management
- CI/CD integration with automated validation

### 3. [Serverless Functions Repository]([https://github.com/yourusername/lambda-functions](https://github.com/CSYE6225-Network-Strctrs-Cloud-Cmpting/serverless))
Event-driven serverless architecture components:
- **Notification System:** Lambda-based email delivery service
- **Scheduled Tasks:** Automated maintenance and monitoring functions
- **Event Processing:** S3 and other AWS service event handlers

**Technical Features:**
- Node.js Lambda runtime optimization
- IAM least-privilege implementation
- CloudWatch integration for observability
- Infrastructure as Code deployment
- Comprehensive error handling and retry mechanisms

## Skills & Technologies

### AWS Services
- **Compute:** EC2, Lambda, Auto Scaling
- **Storage:** S3, EBS
- **Database:** RDS (MySQL/PostgreSQL)
- **Networking:** VPC, Security Groups, Route53, Application Load Balancer
- **Security:** IAM, KMS, Secret Manager, Certificate Manager
- **Monitoring:** CloudWatch

### Development & Operations
- **Frontend:** React.js
- **Backend:** Node.js, Express.js
- **Database:** MySQL (RDS)
- **Infrastructure as Code:** Terraform
- **CI/CD:** GitHub Actions
- **Virtualization:** Packer for custom AMIs
- **Version Control:** Git, GitHub
- **Authentication & Security:** HTTPS/SSL, IAM roles
- **Monitoring & Logging:** CloudWatch

## Project Development Phases

### Phase 1: Web Application Development
- Created React frontend and Node.js/Express.js backend
- Implemented RESTful API with health check endpoint
- Set up GitHub repositories with proper workflows
- Created shell script for application bootstrapping

### Phase 2: AWS Organization & IAM Setup
- Configured AWS organizations with dev and demo accounts
- Implemented IAM users and groups with proper permissions
- Created shell script for application setup
- Implemented API testing with Jest

### Phase 3: Networking Infrastructure
- Created VPC, subnets, internet gateway, and route tables
- Implemented GitHub Actions workflow for Terraform validation
- Set up branch protection rules for secure collaboration

### Phase 4: Infrastructure as Code & Custom AMIs
- Built custom AMI with Packer
- Created EC2 instances using Terraform
- Implemented security groups
- Set up CI/CD pipeline for AMI creation

### Phase 5: Database & Storage
- Implemented MySQL RDS instance
- Created S3 bucket with proper lifecycle policies
- Updated user-data scripts for database connection
- Set up file upload/download functionality
- Configured system services for auto-start

### Phase 6: Monitoring, DNS & Logging
- Configured domain and DNS settings
- Implemented CloudWatch agent for logging and metrics
- Set up custom metrics for API calls
- Created email service configuration

### Phase 7: Auto-scaling & Load Balancing
- Implemented auto-scaling groups based on metrics
- Configured application load balancer
- Updated security groups for proper access control
- Set up DNS records for load balancer

### Phase 8: CI/CD & Security Enhancements
- Enhanced CI/CD pipeline with automated deployment
- Implemented KMS encryption for sensitive data
- Set up Secret Manager for database credentials
- Added SSL/TLS certificates
- Configured auto-deployment with instance refresh

## Infrastructure Architecture

The application follows a modern cloud-native architecture implementing best practices for security, scalability, and reliability:

### Network Architecture


#### Multi-Tier Design:

1. **Public-Facing Layer:**
   - Application Load Balancer with SSL termination
   - WAF integration for enhanced security
   - Route53 DNS management with health checks
   - Redundant deployment across multiple availability zones

2. **Application Layer:**
   - Auto-scaling EC2 instances in private subnets
   - Elastic IP for NAT Gateway
   - Immutable infrastructure with custom AMIs
   - Instance profile-based security

3. **Data Persistence Layer:**
   - Multi-AZ RDS MySQL deployment
   - Encryption at rest via KMS
   - Automated backups with retention policies
   - S3 bucket with lifecycle management
   
4. **Security Controls:**
   - Defense-in-depth security model
   - Granular IAM permissions
   - Network segmentation with security groups
   - KMS-managed encryption keys
   - Secret Manager for credential rotation

### Availability and Disaster Recovery
- Multi-AZ deployment for high availability
- Auto-scaling for performance and reliability
- Automated backup and recovery procedures
- Infrastructure as Code for environment replication

## CI/CD Pipeline

The project implements a fully automated DevOps workflow for continuous integration and deployment:



### Development Workflow
- Git-flow branching strategy
- Feature branch isolation
- Pull request code review process
- Automated code quality and security scanning
- Required status checks for branch protection

### Continuous Integration
- GitHub Actions workflow automation
- Comprehensive test suite execution
- Static code analysis
- Infrastructure validation with Terraform
- Application packaging and artifact generation

### Continuous Deployment
1. **Build Phase:**
   - Application artifact creation and versioning
   - Packer-based AMI building with automated provisioning
   - AMI hardening and security scanning
   - Cross-account AMI sharing with defined permissions

2. **Deployment Phase:**
   - Atomic launch template updates
   - Blue-green deployment via instance refresh
   - Progressive traffic shifting
   - Automated health verification and rollback capability
   - Notification and alerting integration

### Monitoring & Observability
- Custom CloudWatch dashboards
- API performance and error rate metrics
- Infrastructure health monitoring
- Real-time log aggregation and analysis
- Alert thresholds with automated notifications

## Security Measures

Security has been implemented as a fundamental design principle throughout the application stack:

### Data Protection

- **Encryption in Transit:**
  - TLS 1.3 for all external communications
  - Certificate management through AWS Certificate Manager
  - Secure communication between application tiers

- **Encryption at Rest:**
  - KMS-managed encryption keys with automated rotation
  - S3 bucket server-side encryption
  - RDS encryption for database storage
  - EBS volume encryption for compute instances

### Access Control

- **Identity Management:**
  - Strict IAM role-based access with least privilege principle
  - Short-lived, automatically rotated credentials
  - Multi-factor authentication enforcement
  - Service control policies at organization level

- **Network Security:**
  - Defense-in-depth network architecture
  - Security group isolation with granular rules
  - Private subnets for sensitive components
  - Network ACLs for additional protection layer

### Application Security

- **Secure Development:**
  - Input validation and output encoding
  - Protection against OWASP Top 10 vulnerabilities
  - Regular dependency scanning
  - Static code analysis in CI pipeline

- **Operational Security:**
  - Immutable infrastructure deployment
  - Automated security patching
  - Comprehensive logging and monitoring
  - Incident response procedures

## Performance Optimization

The application architecture includes several performance-enhancing features:

- Auto-scaling based on CPU and custom metrics
- CloudFront distribution for static assets
- Read replicas for database query optimization
- Connection pooling for database efficiency
- Caching strategies at multiple tiers

## Cost Optimization

- Right-sized infrastructure components
- Auto-scaling to match demand patterns
- S3 Intelligent-Tiering for storage cost efficiency
- Reserved instances for predictable workloads
- Resource tagging for cost allocation

## Future Enhancements

Planned improvements to the architecture include:

- Container-based deployment with ECS/EKS
- API Gateway integration for microservices
- Enhanced monitoring with Prometheus/Grafana
- Automated database migration procedures
- Integration with AWS WAF for enhanced security
