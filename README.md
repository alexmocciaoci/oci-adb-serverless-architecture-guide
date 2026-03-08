# OCI Autonomous Database Serverless – Architecture & Security Reference

## Overview

This repository provides a technical architecture and operational reference for deploying, securing, and operating **Oracle Autonomous Database Serverless (ADB-S)** on **Oracle Cloud Infrastructure (OCI)**.

The documentation focuses on enterprise architecture patterns, security design, auditing architecture, and client connectivity models for Autonomous Database Serverless environments.

The material is based on real implementation scenarios and field testing.

All customer-specific information, hostnames, identifiers, and network parameters have been replaced with generic placeholders.

---

## Architecture Scope

This repository covers key architectural components and operational patterns for enterprise ADB-S deployments:

- Autonomous Database Serverless service architecture
- OCI **Control Plane vs Data Plane** operational model
- Private Endpoint network architecture patterns
- Secure connectivity using **TCPS and mTLS**
- **IAM Database Token** authentication architecture
- **Zero Trust Packet Routing (ZPR)** policy model
- **Oracle Data Safe** integration and auditing architecture
- Unified Audit Trail architecture and retention model
- Control plane logging via **OCI Audit**
- Operational monitoring via **OCI Monitoring** and **OCI Events**
- Automatic backup architecture and recovery model
- Enterprise onboarding process for database services

---

## Repository Contents

## Repository Structure

docs/
├── adb-serverless-service-catalog.pdf
├── adb-client-iam-token-windows.pdf


### ADB-S Technical Service Catalog

Enterprise architecture documentation describing:

- service components
- network architecture scenarios
- security architecture
- auditing and monitoring model
- backup architecture
- operational governance

### ADB-S Client Connectivity Guide

Technical configuration guide for connecting to Autonomous Database Serverless using **IAM Database Token authentication**, including:

- Oracle Instant Client configuration
- SQL*Plus connectivity
- SQL Developer (OCI Thick / JDBC Thin)
- Wallet configuration
- OCI CLI token generation

---

## Security Architecture Model

The architecture described in this repository follows a **defense-in-depth security model** composed of multiple layers:

**Network Layer**

Private Endpoint deployment inside OCI Virtual Cloud Networks with controlled access via NSG and Security Lists.

**Identity Layer**

OCI IAM authentication using **IAM Database Token**, eliminating static database credentials.

**Transport Security**

Encrypted communication via **TCPS / mTLS**.

**Policy Enforcement**

Intent-based security using **OCI Zero Trust Packet Routing (ZPR)**.

**Database Auditing**

Native **Unified Auditing** combined with **Oracle Data Safe Activity Auditing**.

**Control Plane Governance**

Infrastructure operations tracked via **OCI Audit Logs**.

---

## Observability and Monitoring

Operational visibility is provided through multiple OCI services:

- **OCI Monitoring** – service metrics and operational alerts
- **OCI Events** – event-driven operational monitoring
- **OCI Audit** – control-plane activity logging
- **Unified Audit Trail** – database-level activity auditing

---

## Intended Audience

This repository is intended for:

- OCI Cloud Architects  
- Oracle Database Engineers  
- Security Architects  
- DevOps / Platform Engineers  
- Enterprise Architecture teams

It assumes familiarity with **Oracle Database architecture, OCI networking, and IAM policy models**.

---

## Disclaimer

This repository is a technical architecture reference.

All infrastructure identifiers, network parameters, and hostnames have been anonymized and replaced with placeholders.
