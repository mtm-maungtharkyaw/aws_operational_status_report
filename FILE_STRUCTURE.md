# Template Files Structure

**Last Updated:** 2026-07-01

## Overview
This directory contains AWS operational report templates for the HoHoEmi project (INNER_HOHOEMI-383).

---

## File Structure

```
templates/
├── README.md                              [Main entry point - Overview of all templates]
├── AWS_Report_Templates_Data_Table.md     [Data structure reference for all reports]
│
├── Individual Report Templates (Fillable):
│   ├── ecs-report-template.md             [ECS operational report template]
│   ├── aurora-report-template.md          [Aurora Serverless v2 report template]
│   ├── dynamodb-report-template.md        [DynamoDB report template]
│   ├── nlb-report-template.md             [Network Load Balancer report template]
│   ├── efs-report-template.md             [Elastic File System report template]
│   ├── synthetics-report-template.md      [CloudWatch Synthetics report template]
│   └── monthly-summary-template.md        [Cross-service monthly summary template]
```

---

## File Purposes

### 📄 README.md
- **Purpose:** Main overview and navigation hub
- **Contains:**
  - Description of each service report
  - Links to data table sections
  - Links to individual report templates
  - Report structure explanation
  - Usage guidelines
  - Health indicators & scoring system

### 📊 AWS_Report_Templates_Data_Table.md
- **Purpose:** Data structure reference
- **Contains:**
  - Detailed tables showing all metrics for each report
  - Section breakdowns
  - Time period categorization
  - Analysis points for each metric
  - Quick reference for data collection

### 📝 Individual Report Templates (7 files)
- **Purpose:** Fillable templates for generating monthly reports
- **Usage:** Copy and fill in with actual metrics from CloudWatch
- **Format:** Markdown tables with placeholder values

---

## Report Coverage

| Report Template | Service | Status |
|----------------|---------|--------|
| ecs-report-template.md | Amazon ECS | ✅ Documented |
| aurora-report-template.md | Aurora Serverless v2 | ✅ Documented |
| dynamodb-report-template.md | Amazon DynamoDB | ✅ Documented |
| nlb-report-template.md | Network Load Balancer | ✅ Documented |
| efs-report-template.md | Elastic File System | ✅ Documented |
| synthetics-report-template.md | CloudWatch Synthetics | ✅ Documented |
| monthly-summary-template.md | Cross-Service Summary | ✅ Documented |

**Total Services Covered:** 6 AWS services + 1 summary report

---

## How to Use

### For New Users:
1. Start with **README.md** for overview
2. Review **AWS_Report_Templates_Data_Table.md** to understand data requirements
3. Copy individual report templates when generating reports

### For Report Generation:
1. Choose the appropriate template (e.g., `ecs-report-template.md`)
2. Collect metrics from CloudWatch
3. Fill in the template with actual values
4. Save as `ecs-report-YYYY-MM.md` (or similar naming convention)

### For Data Collection:
1. Use **AWS_Report_Templates_Data_Table.md** as checklist
2. Reference the "Appendix" section in each template for data sources
3. Follow time period breakdowns (Night/Morning/Afternoon/Evening)

---

## Links Between Files

```
README.md
    ↓ Links to →
    ├── AWS_Report_Templates_Data_Table.md (for each service)
    ├── ecs-report-template.md
    ├── aurora-report-template.md
    ├── dynamodb-report-template.md
    ├── nlb-report-template.md
    ├── efs-report-template.md
    ├── synthetics-report-template.md
    └── monthly-summary-template.md

AWS_Report_Templates_Data_Table.md
    ↓ Referenced by →
    └── README.md (Table of Contents links)
```

---

## Consistency Check

✅ All individual templates have corresponding data table entries  
✅ README.md links to all templates  
✅ Monthly summary covers all 6 services  
✅ All files use consistent structure (Config, Metrics, Health, Recommendations)  
✅ No duplicate files  
✅ No orphaned files  

---

## Notes

- **No files should be deleted** - all serve specific purposes
- Templates are designed to be copied and filled, not modified directly
- Keep this directory structure intact for consistency
- When adding new service templates, update both README.md and AWS_Report_Templates_Data_Table.md

---

**Generated:** 2026-07-01  
**Project:** HoHoEmi (INNER_HOHOEMI-383)
