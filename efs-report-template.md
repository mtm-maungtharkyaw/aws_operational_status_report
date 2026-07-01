# EFS Operational Status Report - [Month] [Year]

## Environment: [ENV]

**Report Period:** [Start Date] - [End Date]  
**Generated:** [Date]  
**Prepared by:** [Your Name]

---

## 1. Configuration

| Setting | Value |
|---------|-------|
| File System ID | fs-XXXXXXXXX |
| Performance Mode | General Purpose / Max I/O |
| Throughput Mode | Bursting / Elastic / Provisioned |
| Encryption | Enabled |
| Availability Zones | [AZ1], [AZ2] |
| Lifecycle Management | Enabled / Disabled |
| Backup | Enabled (Daily [Time] JST, X-day retention) |

---

## 2. Storage Utilization

### Overview

| Metric | Value | Status |
|--------|-------|--------|
| Total Storage | XX.X GB | |
| Growth (Month) | +X.X GB | ⚪ Normal / 🟡 High / 🔴 Critical |
| Growth Rate | +X.X% | |
| Average Daily | XX.X GB | |
| Previous Month | XX.X GB | |

### Storage Trend

| Week | Average Storage | Growth from Previous |
|------|-----------------|---------------------|
| Week 1 | XX.X GB | - |
| Week 2 | XX.X GB | +X.X GB |
| Week 3 | XX.X GB | +X.X GB |
| Week 4 | XX.X GB | +X.X GB |

### Analysis

**Growth Assessment:** ⚪ Normal / 🟡 High / 🔴 Critical

**Observations:**
- [Storage growth pattern]
- [Unusual growth periods]

**Projections:**
- Estimated storage in 3 months: XX GB
- Estimated storage in 6 months: XX GB

---

## 3. I/O Operations

### Overview

| Metric | Read | Write |
|--------|------|-------|
| Average Ops/min | X,XXX | X,XXX |
| Peak Ops/min | XX,XXX | XX,XXX |
| Peak Time | [Date], [Time] JST | [Date], [Time] JST |
| Total Operations (Month) | XXX,XXX | XXX,XXX |

### I/O Pattern by Time of Day

| Time Period (JST) | Avg Read Ops/min | Avg Write Ops/min |
|-------------------|------------------|-------------------|
| 00:00-06:00 (Night) | XXX | XXX |
| 06:00-12:00 (Morning) | X,XXX | XXX |
| 12:00-18:00 (Afternoon) | X,XXX | X,XXX |
| 18:00-24:00 (Evening) | XXX | XXX |

### Analysis

**I/O Pattern Status:** ✅ Healthy / 🟡 Warning / 🔴 Critical

**Observations:**
- [I/O pattern observations]
- [Peak usage periods]

---

## 4. Throughput

### Overview

| Metric | Read | Write |
|--------|------|-------|
| Average MB/s | X.X MB/s | X.X MB/s |
| Peak MB/s | XX.X MB/s | XX.X MB/s |
| Peak Time | [Date], [Time] JST | [Date], [Time] JST |

### Throughput Limits

| Configuration | Baseline | Burst (if applicable) |
|---------------|----------|----------------------|
| [Mode] | XX MB/s | XX MB/s |
| Current Usage (Avg) | X.X MB/s (X% of baseline) | |
| Current Usage (Peak) | XX.X MB/s (XX% of baseline) | |

### Analysis

**Throughput Status:** ✅ Healthy / 🟡 Warning / 🔴 Critical

**Assessment:**
- Average usage: X% of baseline
- Peak usage: XX% of baseline
- [Assessment of whether current throughput mode is adequate]

---

## 5. Performance Metrics

### Client Connections

| Metric | Value | Status |
|--------|-------|--------|
| Average Connections | X clients | ⚪ Healthy |
| Peak Connections | XX clients | ⚪ Healthy / 🟡 Warning |
| Peak Time | [Date], [Time] JST | |

### Percent IO Limit

| Metric | Value | Status |
|--------|-------|--------|
| Average % IO Limit | XX% | ⚪/🟡/🔴 |
| Peak % IO Limit | XX% | ⚪/🟡/🔴 |
| Peak Time | [Date], [Time] JST | |
| Times > 80% | X occurrences | |

### Burst Credit Balance (if Bursting mode)

| Metric | Value | Status |
|--------|-------|--------|
| Average Credits | X.X TB | ⚪/🟡/🔴 |
| Minimum Credits | X.X TB | ⚪/🟡/🔴 |
| Credits Depleted | X times | |

### Analysis

**Performance Status:** ✅ Healthy / 🟡 Warning / 🔴 Critical

**Observations:**
- [Client connection observations]
- [I/O limit observations]
- [Burst credit observations if applicable]

---

## 6. Backup Status

### Overview

| Metric | Value |
|--------|-------|
| Backup Schedule | Daily at [Time] JST |
| Backup Retention | X days |
| Successful Backups | XX/XX (XX%) |
| Failed Backups | X |
| Average Backup Size | XX.X GB |
| Average Backup Duration | XX minutes |

### Backup Details

| Date | Status | Size | Duration | Notes |
|------|--------|------|----------|-------|
| [Date] | ✅/❌ | XX GB | XX min | [Notes if failed] |
| [Date] | ✅/❌ | XX GB | XX min | |

### Analysis

**Backup Status:** ✅ Healthy / 🟡 Warning / 🔴 Critical

**Observations:**
- [Backup success rate]
- [Any backup failures and reasons]

---

## 7. Connected Resources

### Mount Targets

| Availability Zone | Mount Target ID | IP Address | Status |
|-------------------|-----------------|------------|--------|
| [AZ1] | fsmt-XXXXX | X.X.X.X | ✅ Available |
| [AZ2] | fsmt-XXXXX | X.X.X.X | ✅ Available |

### ECS Tasks

| Service | Task Count | Status |
|---------|------------|--------|
| [service-name] | X tasks | ✅ Connected |

---

## 8. Summary & Health Status

### Overall Status: ✅ Healthy / 🟡 Warning / 🔴 Critical

| Category | Status | Score |
|----------|--------|-------|
| Storage Growth | ✅/🟡/🔴 | X/10 |
| I/O Operations | ✅/🟡/🔴 | X/10 |
| Throughput | ✅/🟡/🔴 | X/10 |
| Performance | ✅/🟡/🔴 | X/10 |
| Backup | ✅/🟡/🔴 | X/10 |
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

## 9. Cost Analysis

### Storage Costs

| Metric | Value | Monthly Cost |
|--------|-------|--------------|
| Standard Storage | XX.X GB | $XX.XX |
| IA Storage (if any) | XX.X GB | $XX.XX |
| **Total Storage** | | **$XX.XX** |

### Request Costs

| Metric | Count | Monthly Cost |
|--------|-------|--------------|
| Read Requests | XXX,XXX | $X.XX |
| Write Requests | XXX,XXX | $X.XX |
| **Total Requests** | | **$X.XX** |

### Total EFS Cost

| Item | Monthly Cost |
|------|--------------|
| Storage | $XX.XX |
| Requests | $X.XX |
| Throughput (if provisioned) | $X.XX |
| **Total** | **$XX.XX** |

---

## 10. Recommendations

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

## 11. Incidents & Issues

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

---

## 12. Appendix

### A. Data Collection Methods

- **Source:** AWS CloudWatch Metrics
- **Collection Period:** [Start Date] - [End Date]
- **Sampling Interval:** [Interval]
- **Tools Used:** AWS CLI, CloudWatch Console

### B. Configuration Details

- File System ID: `fs-XXXXXXXXX`
- Creation Date: [Date]
- Security Group: `[security-group-id]`
- VPC: `[vpc-id]`

---

**Report End**

*Generated: [Date]*  
*Next Report Due: [Next Month]*  
*Document: INNER_HOHOEMI-383 - EFS Operational Status Report*
