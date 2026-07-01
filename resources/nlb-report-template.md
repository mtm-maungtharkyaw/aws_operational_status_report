# NLB (Network Load Balancer) Operational Status Report - [Month] [Year]

## Environment: [ENV]

**Report Period:** [Start Date] - [End Date]  
**Generated:** [Date]  
**Prepared by:** [Your Name]

---

## 1. Configuration

| Setting | Value |
|---------|-------|
| Load Balancer Name | [env]-nlb |
| Type | Network Load Balancer |
| Scheme | Internal / Internet-facing |
| Availability Zones | [AZ1], [AZ2] |
| Private IPs | [IP1], [IP2] |
| VPC | [vpc-id] |
| DNS Name | [nlb-dns-name] |
| Target Type | IP / Instance |

### Target Group

| Setting | Value |
|---------|-------|
| Target Group Name | [target-group-name] |
| Protocol | TCP / TLS / UDP |
| Port | XXXX |
| Health Check Protocol | TCP / HTTP / HTTPS |
| Health Check Interval | XX seconds |
| Healthy Threshold | X |
| Unhealthy Threshold | X |

---

## 2. Traffic Metrics

### Active Flow Count

| Metric | Value | Status |
|--------|-------|--------|
| Average Flows | X,XXX | ⚪ Normal |
| Peak Flows | XX,XXX | ⚪/🟡/🔴 |
| Peak Time | [Date], [Time] JST | [Context] |
| Minimum Flows | XXX | |

### Flow Pattern by Time of Day

| Time Period (JST) | Average Flows | Peak Flows |
|-------------------|---------------|------------|
| 00:00-06:00 (Night) | XXX | XXX |
| 06:00-12:00 (Morning) | X,XXX | X,XXX |
| 12:00-18:00 (Afternoon) | XX,XXX | XX,XXX |
| 18:00-24:00 (Evening) | X,XXX | X,XXX |

### Analysis

**Traffic Status:** ✅ Healthy / 🟡 Warning / 🔴 Critical

**Observations:**
- [Traffic pattern observations]
- [Peak usage periods]
- [Any unusual traffic spikes]

---

## 3. Data Transfer

### Processed Bytes

| Metric | Value |
|--------|-------|
| Total Bytes (Month) | XXX GB |
| Average per Day | XX GB/day |
| Peak Day | [Date] - XX GB |
| Average Throughput | X.X MB/s |
| Peak Throughput | XX MB/s |

### Data Transfer by Direction

| Direction | Total (Month) | Average/Day |
|-----------|---------------|-------------|
| Inbound | XXX GB | XX GB |
| Outbound | XXX GB | XX GB |
| **Total** | **XXX GB** | **XX GB** |

### Analysis

**Data Transfer Status:** ⚪ Normal / 🟡 High / 🔴 Unusual

**Observations:**
- [Data transfer patterns]
- [Comparison with previous month]

---

## 4. Target Health

### Health Status Overview

| Metric | Value | Status |
|--------|-------|--------|
| Average Healthy Hosts | X hosts | ⚪/🟡/🔴 |
| Average Unhealthy Hosts | X hosts | ⚪/🟡/🔴 |
| Total Registered Targets | X hosts | |
| Health Check Success Rate | XX% | ⚪/🟡/🔴 |

### Health Status Timeline

| Week | Avg Healthy | Avg Unhealthy | Health % |
|------|-------------|---------------|----------|
| Week 1 | X | X | XX% |
| Week 2 | X | X | XX% |
| Week 3 | X | X | XX% |
| Week 4 | X | X | XX% |

### Target Health Events

| Date | Event | Duration | Impact | Reason |
|------|-------|----------|--------|--------|
| [Date], [Time] JST | Target unhealthy | [Duration] | [Impact] | [Reason] |
| [Date], [Time] JST | Target recovered | - | - | [Resolution] |

### Analysis

**Target Health Status:** ✅ Healthy / 🟡 Warning / 🔴 Critical

**Observations:**
- [Health check observations]
- [Any recurring health issues]
- [Target availability patterns]

---

## 5. Connection Metrics

### New Flow Count

| Metric | Value |
|--------|-------|
| Average New Flows/min | XXX |
| Peak New Flows/min | X,XXX |
| Peak Time | [Date], [Time] JST |
| Total New Flows (Month) | XXX,XXX |

### Connection Duration

| Metric | Value |
|--------|-------|
| Average Connection Duration | XX seconds |
| Longest Connection | XX minutes |

### Analysis

**Connection Pattern:** ⚪ Normal / 🟡 Unusual

**Observations:**
- [Connection pattern observations]
- [Short vs long-lived connections]

---

## 6. Error Metrics

### Connection Errors

| Metric | Count | Rate |
|--------|-------|------|
| TCP Target Reset Count | XXX | X.XX% |
| TCP ELB Reset Count | XXX | X.XX% |
| Client TLS Negotiation Errors | XXX | X.XX% |
| Target TLS Negotiation Errors | XXX | X.XX% |

### Error Timeline

| Week | TCP Resets | TLS Errors | Total Errors |
|------|------------|------------|--------------|
| Week 1 | XXX | XX | XXX |
| Week 2 | XXX | XX | XXX |
| Week 3 | XXX | XX | XXX |
| Week 4 | XXX | XX | XXX |

### Analysis

**Error Status:** ✅ Low / 🟡 Moderate / 🔴 High

**Observations:**
- [Error pattern analysis]
- [Root causes of errors]

---

## 7. Performance & Latency

### Response Time (if HTTP/HTTPS health checks)

| Metric | Value |
|--------|-------|
| Average Response Time | XX ms |
| P50 Latency | XX ms |
| P95 Latency | XX ms |
| P99 Latency | XXX ms |

### Analysis

**Performance Status:** ✅ Healthy / 🟡 Warning / 🔴 Critical

**Observations:**
- [Latency observations]
- [Performance trends]

---

## 8. Access Logs Summary

### Log Statistics

| Metric | Value |
|--------|-------|
| Total Requests Logged | XXX,XXX |
| Log Files Generated | XXX |
| Total Log Size | XX GB |
| S3 Bucket | [bucket-name] |

### Top Traffic Sources (if applicable)

| Source IP/Range | Requests | % of Total |
|-----------------|----------|------------|
| [IP/CIDR] | XX,XXX | XX% |
| [IP/CIDR] | XX,XXX | XX% |
| [IP/CIDR] | XX,XXX | XX% |

---

## 9. Summary & Health Status

### Overall Status: ✅ Healthy / 🟡 Warning / 🔴 Critical

| Category | Status | Score |
|----------|--------|-------|
| Traffic Volume | ✅/🟡/🔴 | X/10 |
| Target Health | ✅/🟡/🔴 | X/10 |
| Error Rate | ✅/🟡/🔴 | X/10 |
| Performance | ✅/🟡/🔴 | X/10 |
| **Overall** | **✅/🟡/🔴** | **X.X/10** |

### Key Highlights

✅ **Strengths:**
- [Strength 1]
- [Strength 2]

🟡 **Areas of Concern:**
- [Concern 1]
- [Concern 2]

⚠️ **Risks:**
- [Risk 1]
- [Risk 2]

---

## 10. Cost Analysis

### NLB Costs

| Item | Value | Monthly Cost |
|------|-------|--------------|
| NLB Hour Charges | 720 hours | $XX.XX |
| LCU (Load Balancer Capacity Units) | XXX LCU-hours | $XX.XX |
| **Total NLB Cost** | | **$XX.XX** |

### Data Transfer Costs

| Item | Volume | Monthly Cost |
|------|--------|--------------|
| Data Processed | XXX GB | $X.XX |
| Inter-AZ Transfer | XXX GB | $X.XX |
| **Total Transfer Cost** | | **$X.XX** |

### Total Cost

| Category | Monthly Cost |
|----------|--------------|
| NLB Charges | $XX.XX |
| Data Transfer | $X.XX |
| **Total** | **$XX.XX** |

---

## 11. Recommendations

### Immediate Actions (Within 1 Month)

1. **[Recommendation Title]**
   - Priority: High / Medium / Low
   - Reason: [Reason]
   - Action: [Specific action]
   - Owner: [Team/Person]

### Short-term Improvements (1-3 Months)

2. **[Recommendation Title]**
   - Priority: High / Medium / Low
   - Current: [Current state]
   - Proposed: [Proposed change]
   - Benefit: [Expected benefit]
   - Cost Impact: [Cost impact]

### Long-term Optimizations (3-6 Months)

3. **[Recommendation Title]**
   - Priority: High / Medium / Low
   - Action: [What to do]
   - Benefit: [Expected benefit]

---

## 12. Incidents & Issues

### [Month] [Year] Incidents

#### Incident #[X]: [Title]

| Detail | Information |
|--------|-------------|
| Date | [Date], [Time] JST |
| Duration | [Duration] |
| Impact | [Impact description] |
| Severity | Low / Medium / High / Critical |
| Root Cause | [Root cause] |
| Resolution | [How it was resolved] |

### CloudWatch Alarms Triggered

| Alarm | Trigger Count | Status |
|-------|---------------|--------|
| [Alarm name] | X | ✅/⚠/🔴 |

---

## 13. Security & Access

### IP Whitelist Status

| CIDR Block | Purpose | Status |
|------------|---------|--------|
| [CIDR] | [Purpose] | ✅ Active |
| [CIDR] | [Purpose] | ✅ Active |

### Security Group Rules

| Direction | Protocol | Port | Source | Purpose |
|-----------|----------|------|--------|---------|
| Inbound | TCP | XXXX | [CIDR] | [Purpose] |
| Outbound | TCP | XXXX | [Target] | [Purpose] |

---

## 14. Appendix

### A. Data Collection Methods

- **Source:** AWS CloudWatch Metrics, NLB Access Logs
- **Collection Period:** [Start Date] - [End Date]
- **Sampling Interval:** [Interval]
- **Tools Used:** AWS CLI, CloudWatch Console, S3

### B. Related Resources

- Load Balancer ARN: `[arn]`
- Target Group ARN: `[arn]`
- VPC: `[vpc-id]`
- Subnets: `[subnet-ids]`
- Security Groups: `[sg-ids]`

### C. Registered Targets

| Target ID | Availability Zone | Status |
|-----------|-------------------|--------|
| [IP/Instance] | [AZ] | ✅ Healthy / ❌ Unhealthy |

---

**Report End**

*Generated: [Date]*  
*Next Report Due: [Next Month]*  
*Document: INNER_HOHOEMI-383 - NLB Operational Status Report*
