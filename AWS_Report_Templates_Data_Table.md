# AWS Report Templates - Data Table Format

**Project:** HoHoEmi (INNER_HOHOEMI-383)  
**Generated:** 2026-07-01  
**Purpose:** Quick reference table for all AWS operational report templates

This document provides a structured overview of all AWS service monitoring report templates. Each report includes configuration details, performance metrics, health assessments, and actionable recommendations.

---

## Table of Contents
1. [ECS Report](#1-ecs-report)
2. [Aurora Serverless v2 Report](#2-aurora-serverless-v2-report)
3. [DynamoDB Report](#3-dynamodb-report)
4. [NLB Report](#4-nlb-report)
5. [EFS Report](#5-efs-elastic-file-system-report)
6. [CloudWatch Synthetics Report](#6-cloudwatch-synthetics-report)

---

## Report Overview

| Service | Key Metrics | Time Breakdown | Health Indicators |
|---------|-------------|----------------|-------------------|
| **ECS** | CPU, Memory, Task Count, Auto-scaling | 4 time periods (Night/Morning/Afternoon/Evening) | CPU, Memory, Task Availability, Resource Efficiency |
| **Aurora Serverless v2** | CPU, Memory, ACU, Connections, Storage, Latency | 4 time periods for ACU | CPU, Memory, ACU Scaling, Connections, Performance |
| **DynamoDB** | RCU/WCU, Throttling, Latency, Storage, Errors | 4 time periods for Operations | Read/Write Performance, Latency, Throttling, Storage Growth |
| **NLB** | Traffic, Data Transfer, Target Health, Errors | 4 time periods for Traffic | Traffic Volume, Target Health, Error Rate, Performance |
| **EFS** | Storage, I/O Operations, Throughput, Performance | 4 time periods for I/O | Storage Growth, I/O Operations, Throughput, Performance, Backup |
| **Synthetics** | Availability, Response Time, Failures | 4 time periods for Success Rate & Latency | Availability, Response Time, Failure Rate |

---

## 1. ECS Report

| Section | Category | Metrics/Information | Time Breakdown | Analysis |
|---------|----------|---------------------|----------------|----------|
| **1. Resource Configuration** | Setup | • Cluster name & region<br>• CPU per task (units/vCPU)<br>• Memory per task (MB/GB)<br>• Auto-scaling (enabled/disabled)<br>• Min/Max tasks<br>• Scaling metric & target<br>• Cooldown periods | N/A | Configuration overview |
| **2. CPU Utilization** | Performance | • Monthly avg/peak/min (%)<br>• Peak time with context<br>• Lowest time with context | • Night (00:00-06:00)<br>• Morning (06:00-12:00)<br>• Afternoon (12:00-18:00)<br>• Evening (18:00-24:00) | • Observations<br>• Key findings<br>• Health status (✅🟡🔴) |
| **3. Memory Utilization** | Performance | • Monthly avg/peak/min (%)<br>• Peak time with context<br>• Lowest time with context | • Night (00:00-06:00)<br>• Morning (06:00-12:00)<br>• Afternoon (12:00-18:00)<br>• Evening (18:00-24:00) | • Usage observations<br>• Concerns<br>• Health status (✅🟡🔴) |
| **4. Task Status** | Capacity | • Auto-scaling status<br>• Min/max tasks<br>• Avg/min/max running tasks<br>• Scale-out/in event counts<br>• Task restarts<br>• Capacity headroom | • Night (00:00-06:00)<br>• Morning (06:00-12:00)<br>• Afternoon (12:00-18:00)<br>• Evening (18:00-24:00) | • Auto-scaling performance<br>• Task availability<br>• Health status (✅🟡🔴) |
| **5. Resource Efficiency** | Cost | • Per-task CPU allocation<br>• Per-task memory allocation<br>• Total reserved vs used<br>• CPU efficiency %<br>• Memory efficiency %<br>• Cost per task<br>• Monthly cost (min/avg/max) | • Minimum scenario<br>• Average scenario<br>• Peak scenario<br>• Maximum capacity | • Efficiency assessment<br>• Optimization recommendations |
| **6. Health Summary** | Overall | • CPU score (1-10)<br>• Memory score (1-10)<br>• Task availability score<br>• Resource efficiency score<br>• Overall score | N/A | • Strengths<br>• Concerns<br>• Risks |
| **7. Incidents & Issues** | Operations | • Incident details<br>• Date, time, duration<br>• Impact & severity<br>• Root cause<br>• Resolution<br>• CloudWatch alarms | N/A | Incident timeline |
| **8. Recommendations** | Action Items | • Immediate actions (<1 month)<br>• Short-term (1-3 months)<br>• Long-term (3-6 months) | N/A | Priority, reason, action, owner |
| **9. Appendix** | Reference | • Data collection methods<br>• Related resources<br>• Cluster/service/task info | N/A | Documentation |

---

## 2. Aurora Serverless v2 Report

| Section | Category | Metrics/Information | Time Breakdown | Analysis |
|---------|----------|---------------------|----------------|----------|
| **1. Configuration** | Setup | • Cluster ID & engine version<br>• Min/Max ACU limits<br>• Instance count<br>• Multi-AZ status<br>• Backup retention<br>• Encryption status | N/A | Configuration overview |
| **2. CPU Utilization** | Performance | • Monthly avg/peak/min (%)<br>• Peak time with context<br>• Status indicators | N/A | • CPU pattern observations<br>• Health assessment (✅🟡🔴) |
| **3. Memory** | Performance | • Avg/min freeable memory (GB)<br>• Memory pressure incidents<br>• % memory used<br>• Pressure timestamps | N/A | • Usage patterns<br>• Pressure incidents<br>• Health status (✅🟡🔴) |
| **4. ACU Utilization** | Capacity | • Avg/peak/min ACU values<br>• Peak time with context<br>• % of max capacity used | • Night (00:00-06:00)<br>• Morning (06:00-12:00)<br>• Afternoon (12:00-18:00)<br>• Evening (18:00-24:00) | • Scaling effectiveness<br>• Capacity headroom<br>• Health status (✅🟡🔴) |
| **5. Database Connections** | Performance | • Avg/peak connections<br>• Peak time with context<br>• Connection limit<br>• % of limit used | N/A | • Connection patterns<br>• Spike identification<br>• Health status (✅🟡🔴) |
| **6. Storage** | Capacity | • Total storage (GB)<br>• Monthly growth (GB & %)<br>• Previous month comparison<br>• Weekly breakdown | • Week 1-4 tracking | • Growth rate assessment<br>• 3/6-month projections |
| **7. Performance Metrics** | Performance | • Read/write latency (avg/peak ms)<br>• Read/write IOPS (avg/peak)<br>• Network throughput (MB/s)<br>• Receive/transmit rates | N/A | • Latency observations<br>• IOPS patterns<br>• Bottleneck identification<br>• Health status (✅🟡🔴) |
| **8. Health Summary** | Overall | • CPU score (1-10)<br>• Memory score (1-10)<br>• ACU scaling score<br>• Connections score<br>• Performance score<br>• Overall score | N/A | • Strengths<br>• Concerns<br>• Risks |
| **9. Incidents & Issues** | Operations | • Incident details<br>• Date, time, duration<br>• Impact & severity<br>• Root cause & resolution<br>• CloudWatch alarms | N/A | Incident timeline |
| **10. Recommendations** | Action Items | • Immediate actions (<1 month)<br>• Short-term (1-3 months)<br>• Long-term (3-6 months) | N/A | Priority, reason, action, owner |
| **11. Appendix** | Reference | • Data collection methods<br>• Configuration details<br>• Database name, port, etc. | N/A | Documentation |

---

## 3. DynamoDB Report

| Section | Category | Metrics/Information | Time Breakdown | Analysis |
|---------|----------|---------------------|----------------|----------|
| **1. Configuration** | Setup | • Table name & purpose<br>• Billing mode (On-Demand/Provisioned)<br>• Encryption status<br>• Point-in-time recovery<br>• Deletion protection<br>• Auto-scaling settings (if provisioned) | N/A | Configuration overview |
| **2. Read Operations** | Performance | • Avg/peak consumed RCU<br>• Total read requests<br>• % of provisioned capacity<br>• Read throttle events & rate<br>• Peak throttle time | • Night (00:00-06:00)<br>• Morning (06:00-12:00)<br>• Afternoon (12:00-18:00)<br>• Evening (18:00-24:00) | • Read pattern observations<br>• Throttling analysis<br>• Capacity adequacy<br>• Health status (✅🟡🔴) |
| **3. Write Operations** | Performance | • Avg/peak consumed WCU<br>• Total write requests<br>• % of provisioned capacity<br>• Write throttle events & rate<br>• Peak throttle time | • Night (00:00-06:00)<br>• Morning (06:00-12:00)<br>• Afternoon (12:00-18:00)<br>• Evening (18:00-24:00) | • Write pattern observations<br>• Throttling analysis<br>• Capacity adequacy<br>• Health status (✅🟡🔴) |
| **4. Latency** | Performance | • Read latency (avg, P50, P95, P99, max)<br>• Write latency (avg, P50, P95, P99, max) | N/A | • Latency trends<br>• Performance bottlenecks<br>• Health status (✅🟡🔴) |
| **5. Storage** | Capacity | • Total size (GB)<br>• Item count<br>• Average item size<br>• Monthly growth (GB & %)<br>• Weekly breakdown | • Week 1-4 tracking | • Growth pattern<br>• 3/6-month projections<br>• Status (⚪🟡🔴) |
| **6. Error Metrics** | Operations | • System errors<br>• User errors<br>• Conditional check failures<br>• Error rates | N/A | • Error pattern analysis<br>• Root causes<br>• Status (✅🟡🔴) |
| **7. Global Secondary Indexes** | Capacity | • Read/write capacity per GSI<br>• Avg consumed RCU/WCU<br>• Index size & item count<br>• Throttle events<br>• Average latency | Per GSI | • GSI performance<br>• Efficiency assessment |
| **8. Time to Live (TTL)** | Maintenance | • TTL enabled status<br>• TTL attribute name<br>• Items deleted monthly<br>• Avg deletions per day | N/A | • TTL effectiveness<br>• Cleanup assessment |
| **9. Health Summary** | Overall | • Read performance score (1-10)<br>• Write performance score<br>• Latency score<br>• Throttling score<br>• Storage growth score<br>• Overall score | N/A | • Strengths<br>• Concerns<br>• Risks |
| **10. Cost Analysis** | Cost | • Read/write request costs<br>• Provisioned capacity costs<br>• Storage costs (table & backup)<br>• Total monthly cost | N/A | Cost breakdown by category |
| **11. Recommendations** | Action Items | • Immediate actions (<1 month)<br>• Short-term (1-3 months)<br>• Long-term (3-6 months) | N/A | Priority, reason, action, owner |
| **12. Incidents & Issues** | Operations | • Incident details<br>• Date, time, duration<br>• Impact & severity<br>• Root cause & resolution<br>• CloudWatch alarms | N/A | Incident timeline |
| **13. Appendix** | Reference | • Data collection methods<br>• Table schema<br>• Access patterns | N/A | Documentation |

---

## 4. NLB (Network Load Balancer) Report

| Section | Category | Metrics/Information | Time Breakdown | Analysis |
|---------|----------|---------------------|----------------|----------|
| **1. Configuration** | Setup | • LB name, type, scheme<br>• Availability zones & IPs<br>• VPC & DNS name<br>• Target type<br>• Target group settings<br>• Health check config | N/A | Configuration overview |
| **2. Traffic Metrics** | Performance | • Avg/peak/min active flows<br>• Peak time with context | • Night (00:00-06:00)<br>• Morning (06:00-12:00)<br>• Afternoon (12:00-18:00)<br>• Evening (18:00-24:00) | • Traffic patterns<br>• Peak usage periods<br>• Unusual spikes<br>• Health status (✅🟡🔴) |
| **3. Data Transfer** | Capacity | • Total bytes monthly (GB)<br>• Average per day<br>• Peak day<br>• Avg/peak throughput (MB/s)<br>• Inbound/outbound breakdown | N/A | • Transfer patterns<br>• Month-over-month comparison<br>• Status (⚪🟡🔴) |
| **4. Target Health** | Operations | • Avg healthy/unhealthy hosts<br>• Health check success rate<br>• Weekly health timeline<br>• Health events (date, duration, impact) | • Week 1-4 tracking | • Health check observations<br>• Recurring issues<br>• Availability patterns<br>• Health status (✅🟡🔴) |
| **5. Connection Metrics** | Performance | • Avg/peak new flows per min<br>• Total new flows monthly<br>• Avg/longest connection duration | N/A | • Connection patterns<br>• Short vs long-lived<br>• Status (⚪🟡) |
| **6. Error Metrics** | Operations | • TCP target reset count<br>• TCP ELB reset count<br>• Client/target TLS errors<br>• Error rates<br>• Weekly error breakdown | • Week 1-4 tracking | • Error patterns<br>• Root causes<br>• Status (✅🟡🔴) |
| **7. Performance & Latency** | Performance | • Response time (avg, P50, P95, P99) | N/A | • Latency observations<br>• Performance trends<br>• Health status (✅🟡🔴) |
| **8. Access Logs Summary** | Operations | • Total requests logged<br>• Log files generated<br>• Total log size<br>• S3 bucket<br>• Top traffic sources | N/A | Log statistics |
| **9. Health Summary** | Overall | • Traffic volume score (1-10)<br>• Target health score<br>• Error rate score<br>• Performance score<br>• Overall score | N/A | • Strengths<br>• Concerns<br>• Risks |
| **10. Cost Analysis** | Cost | • NLB hour charges<br>• LCU costs<br>• Data transfer costs<br>• Inter-AZ transfer<br>• Total monthly cost | N/A | Cost breakdown |
| **11. Recommendations** | Action Items | • Immediate actions (<1 month)<br>• Short-term (1-3 months)<br>• Long-term (3-6 months) | N/A | Priority, reason, action, owner |
| **12. Incidents & Issues** | Operations | • Incident details<br>• Date, time, duration<br>• Impact & severity<br>• Root cause & resolution<br>• CloudWatch alarms | N/A | Incident timeline |
| **13. Security & Access** | Security | • IP whitelist status<br>• CIDR blocks & purpose<br>• Security group rules | N/A | Security posture |
| **14. Appendix** | Reference | • Data collection methods<br>• Related resources (ARNs)<br>• Registered targets | N/A | Documentation |

---

## 5. EFS (Elastic File System) Report

| Section | Category | Metrics/Information | Time Breakdown | Analysis |
|---------|----------|---------------------|----------------|----------|
| **1. Configuration** | Setup | • File System ID<br>• Performance mode (General Purpose/Max I/O)<br>• Throughput mode (Bursting/Elastic/Provisioned)<br>• Encryption status<br>• Availability zones<br>• Lifecycle management<br>• Backup schedule & retention | N/A | Configuration overview |
| **2. Storage Utilization** | Capacity | • Total storage (GB)<br>• Monthly growth (GB & %)<br>• Average daily storage<br>• Previous month comparison<br>• Weekly breakdown | • Week 1-4 tracking | • Growth assessment<br>• 3/6-month projections<br>• Status (⚪🟡🔴) |
| **3. I/O Operations** | Performance | • Avg/peak read ops per min<br>• Avg/peak write ops per min<br>• Peak times with context<br>• Total operations monthly | • Night (00:00-06:00)<br>• Morning (06:00-12:00)<br>• Afternoon (12:00-18:00)<br>• Evening (18:00-24:00) | • I/O pattern observations<br>• Peak usage periods<br>• Health status (✅🟡🔴) |
| **4. Throughput** | Performance | • Avg/peak read MB/s<br>• Avg/peak write MB/s<br>• Peak times<br>• Baseline & burst limits<br>• % of baseline used | N/A | • Throughput adequacy<br>• Mode assessment<br>• Health status (✅🟡🔴) |
| **5. Performance Metrics** | Performance | • Average client connections<br>• Peak connections<br>• % IO limit (avg/peak)<br>• Times > 80%<br>• Burst credit balance (if applicable)<br>• Credits depleted count | N/A | • Client connection patterns<br>• I/O limit observations<br>• Credit analysis<br>• Health status (✅🟡🔴) |
| **6. Backup Status** | Operations | • Backup schedule & retention<br>• Successful backups count & %<br>• Failed backups<br>• Average backup size & duration<br>• Backup details table | N/A | • Backup success rate<br>• Failure reasons<br>• Status (✅🟡🔴) |
| **7. Connected Resources** | Operations | • Mount targets (AZ, ID, IP, status)<br>• ECS tasks connected | N/A | Resource mapping |
| **8. Health Summary** | Overall | • Storage growth score (1-10)<br>• I/O operations score<br>• Throughput score<br>• Performance score<br>• Backup score<br>• Overall score | N/A | • Strengths<br>• Concerns<br>• Risks |
| **9. Cost Analysis** | Cost | • Standard storage costs<br>• IA storage costs<br>• Read/write request costs<br>• Provisioned throughput costs<br>• Total monthly cost | N/A | Cost breakdown by category |
| **10. Recommendations** | Action Items | • Immediate actions (<1 month)<br>• Short-term (1-3 months)<br>• Long-term (3-6 months) | N/A | Priority, reason, action, owner |
| **11. Incidents & Issues** | Operations | • Incident details<br>• Date, time, duration<br>• Impact & severity<br>• Root cause & resolution | N/A | Incident timeline |
| **12. Appendix** | Reference | • Data collection methods<br>• Configuration details<br>• Security group & VPC info | N/A | Documentation |

---

## 6. CloudWatch Synthetics Report

| Section | Category | Metrics/Information | Time Breakdown | Analysis |
|---------|----------|---------------------|----------------|----------|
| **1. Configuration** | Setup | • Canary name & purpose<br>• Runtime version<br>• Schedule frequency<br>• Monitored URL<br>• Host header<br>• VPC execution settings<br>• Subnets & security group | N/A | Configuration overview |
| **2. Availability & Success Rate** | Performance | • Success rate %<br>• Total/successful/failed runs<br>• Uptime %<br>• Weekly success rate breakdown<br>• SLA target vs actual | • Night (00:00-06:00)<br>• Morning (06:00-12:00)<br>• Afternoon (12:00-18:00)<br>• Evening (18:00-24:00) | • Availability patterns<br>• Downtime periods<br>• SLA compliance<br>• Health status (✅🟡🔴) |
| **3. Response Time & Latency** | Performance | • Avg/P50/P90/P95/P99/max/min duration<br>• Weekly duration trend<br>• Target response time<br>• Target met status | • Night (00:00-06:00)<br>• Morning (06:00-12:00)<br>• Afternoon (12:00-18:00)<br>• Evening (18:00-24:00) | • Latency patterns<br>• Performance degradation<br>• Response time trends<br>• Health status (✅🟡🔴) |
| **4. Failure Analysis** | Operations | • Total failures & %<br>• Network errors<br>• HTTP errors (4xx/5xx)<br>• Timeout errors<br>• Failed runs detail table<br>• Failure by day of week<br>• Root cause analysis | N/A | • Failure patterns<br>• Common causes<br>• Correlation analysis<br>• Status (✅🟡🔴) |
| **5. Screenshots & Artifacts** | Operations | • Screenshots captured/failed<br>• Total size<br>• S3 bucket<br>• HAR files generated | N/A | Artifact statistics |
| **6. Alerts & Notifications** | Operations | • SNS notification counts<br>• Recipients<br>• CloudWatch alarms triggered | N/A | Alert summary |
| **7. Health Summary** | Overall | • Availability score (1-10)<br>• Response time score<br>• Failure rate score<br>• Overall score | N/A | • Strengths<br>• Concerns<br>• Risks |
| **8. SLA Compliance** | Performance | • Uptime % target vs actual<br>• Response time target vs actual<br>• Error rate target vs actual<br>• SLA met status | N/A | • SLA compliance status<br>• Breach analysis |
| **9. Cost Analysis** | Cost | • Canary run costs<br>• Screenshot storage costs<br>• VPC execution costs<br>• Total monthly cost | N/A | Cost breakdown |
| **10. Recommendations** | Action Items | • Immediate actions (<1 month)<br>• Short-term (1-3 months)<br>• Long-term (3-6 months) | N/A | Priority, reason, action, owner |
| **11. Incidents & Issues** | Operations | • Incident details<br>• Date, time, duration<br>• Impact & severity<br>• Root cause & resolution | N/A | Incident timeline |
| **12. Appendix** | Reference | • Data collection methods<br>• Monitored endpoint details<br>• Canary script summary | N/A | Documentation |

---
