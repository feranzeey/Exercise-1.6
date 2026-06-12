# Root Cause Analysis

## Technical Findings

Database CPU utilization exceeded 90%.

This caused:

Database Latency
↓
Authentication Service Failure
↓
Payment Service Failure
↓
API Gateway Timeouts

## Evidence

CloudWatch Metrics:
- CPU > 90%
- Increased query latency

Application Logs:
- Database connection timeout errors

Service Metrics:
- Authentication service restart events observed

## Root Cause

Insufficient database capacity during peak traffic.