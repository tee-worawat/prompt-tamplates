# PRD Template Usage Guide

This guide explains how to use the PRD (Product Requirements Document) template for building data pipelines similar to the CodeVenture data pipelines project.

## 📋 Overview

The PRD template (`PRD_TEMPLATE.md`) is a comprehensive document template designed to help teams create consistent, thorough requirements documents for data pipeline projects. It's based on the patterns, architecture, and best practices from the existing CodeVenture data pipelines repository.

## 🎯 When to Use This Template

Use this PRD template when:
- Building new data pipelines for dashboard optimization
- Creating ETL/ELT processes for analytics
- Setting up scheduled data processing workflows
- Migrating from direct database queries to pre-processed data
- Adding new metrics or data sources to existing systems

## 🚀 Quick Start

### Step 1: Copy the Template
```bash
# Copy the template to your project directory
cp PRD_TEMPLATE.md [YOUR_PROJECT_NAME]_PRD.md
```

### Step 2: Replace Placeholders
Search for all instances of `[TO BE REPLACED BY: ...]` and replace with your specific information.

### Step 3: Customize Sections
Review each section and adapt it to your project's specific needs.

### Step 4: Review and Approve
Share with stakeholders for review and approval before implementation.

## 📝 Template Structure Guide

### 1. Executive Summary
**Purpose**: High-level project overview for stakeholders
**Key Replacements**:
- `[PROJECT_NAME]` → Your specific project name
- `[Source system]` → Your data source (e.g., MongoDB, PostgreSQL, APIs)
- `[Target dashboard/application]` → Your consuming application
- `[Expected improvement]` → Performance targets (e.g., "60-80% faster")

### 2. Objectives & Success Metrics
**Purpose**: Define measurable goals
**Key Replacements**:
- `[Target time]` → Response time goals (e.g., "< 200ms")
- `[Expected load]` → User capacity (e.g., "1000+ concurrent users")
- `[Target uptime]` → Reliability requirements (e.g., "99.9%")

### 3. Scope & Requirements
**Purpose**: Define what's included and excluded
**Key Replacements**:
- `[Primary entity]` → Main data entity (e.g., "User Dashboard Metrics")
- `[Specific metrics]` → Actual metrics you'll calculate
- `[Time period]` → Data retention period (e.g., "last 12 months")

### 4. Technical Architecture
**Purpose**: Define system design and data flow
**Key Replacements**:
- `[Source systems]` → Your data sources
- `[Target collections]` → Your output destinations
- `[Deployment target]` → Your platform (e.g., "AWS MWAA", "EC2")

### 5. Data Specifications
**Purpose**: Define data models and processing logic
**Key Replacements**:
- `[Source collection/table]` → Your input data structure
- `[Primary Output Collection/Table]` → Your main output structure
- `[Specific aggregation logic]` → Your business logic

### 6. Implementation Plan
**Purpose**: Define project timeline and phases
**Key Replacements**:
- `[Primary data source]` → Your main data input
- `[Primary metrics]` → Your key calculations
- Adjust timeline based on project complexity

## 🔧 Common Replacement Patterns

### Data Sources
```markdown
# Replace with your actual data sources:
[TO BE REPLACED BY: Source systems] → "MongoDB collections", "PostgreSQL tables", "REST APIs", "CSV files"
```

### Metrics Examples
```markdown
# Replace with your actual metrics:
[TO BE REPLACED BY: Specific metrics] → "user engagement scores", "sales analytics", "performance KPIs", "completion rates"
```

### Deployment Targets
```markdown
# Replace with your deployment platform:
[TO BE REPLACED BY: Target platform] → "AWS MWAA", "Google Cloud Composer", "Azure Data Factory", "Local Docker"
```

### Database Types
```markdown
# Replace with your database:
[TO BE REPLACED BY: Database type] → "MongoDB", "PostgreSQL", "MySQL", "BigQuery", "Snowflake"
```

## 📊 Example Replacements

Here's an example of how to replace placeholders for a "Student Analytics Pipeline":

### Before (Template):
```markdown
**Project Name**: [TO BE REPLACED BY: Specific project name, e.g., "Student Progress Analytics Pipeline"]
**Purpose**: This document outlines the requirements for building a data processing pipeline that transforms raw [TO BE REPLACED BY: Source system, e.g., "MongoDB collections"] data into optimized, query-ready collections for [TO BE REPLACED BY: Target dashboard/application, e.g., "student dashboard"] consumption.
```

### After (Filled):
```markdown
**Project Name**: Student Progress Analytics Pipeline
**Purpose**: This document outlines the requirements for building a data processing pipeline that transforms raw MongoDB collections data into optimized, query-ready collections for student dashboard consumption.
```

## 🏗️ Architecture Patterns

The template follows these established patterns from the CodeVenture repository:

### ETL-VLP Pattern
- **Extract**: Pull data from source systems
- **Transform**: Calculate metrics and aggregations
- **Validate**: Ensure data quality and business rules
- **Load**: Upsert into optimized collections
- **Publish**: Update metadata and trigger notifications

### Repository Structure
```
project-data-pipelines/
├── dags/                    # Airflow DAGs
├── common/                  # Reusable components
│   ├── io/                  # Data adapters
│   ├── transforms/          # Business logic
│   └── utils/               # Helper functions
├── tests/                   # Unit tests
└── .github/workflows/       # CI/CD
```

### Naming Conventions
- **DAG IDs**: `project_domain_subject_v1`
- **Task IDs**: `extract_*`, `transform_*`, `validate_*`, `load_*`, `publish_*`
- **Collections**: Environment variable configuration

## 🎨 Customization Guidelines

### Required Customizations
1. **Project-specific metrics** and calculations
2. **Data source connections** and schemas
3. **Deployment platform** configuration
4. **Business rules** and validation logic
5. **Performance requirements** and SLAs

### Optional Customizations
1. **Additional sections** for specific compliance needs
2. **Extended monitoring** requirements
3. **Custom security** requirements
4. **Integration** with specific tools or platforms

### Sections to Remove
- Remove sections that don't apply to your project
- Simplify technical requirements if using managed services
- Adjust timeline based on team capacity and project scope

## ✅ Quality Checklist

Before finalizing your PRD, ensure:

- [ ] All `[TO BE REPLACED BY: ...]` placeholders are filled
- [ ] Technical architecture matches your infrastructure
- [ ] Data models reflect actual source and target schemas
- [ ] Implementation timeline is realistic
- [ ] Success metrics are measurable
- [ ] Risk mitigation strategies are appropriate
- [ ] Stakeholders have reviewed and approved

## 🔄 Template Updates

The template is based on the current CodeVenture data pipelines patterns. When updating:

1. **Review existing patterns** in the main repository
2. **Update template** to reflect new best practices
3. **Version the template** with change log
4. **Communicate changes** to the team

## 📚 Additional Resources

- [CodeVenture Data Pipelines Repository](../README.md)
- [Setup Guide](../SETUP.md)
- [Deployment Guide](../DEPLOYMENT.md)
- [Data Pipeline Requirements](../rules/data-pipelines-basics.md)
- [Development Rules](../rules/rules.md)

## 🤝 Contributing

To improve this template:

1. **Identify gaps** in current template coverage
2. **Propose improvements** based on real project experience
3. **Submit changes** via pull request
4. **Update this guide** to reflect template changes

## 📞 Support

For questions about using this template:

- **Technical questions**: Check the main repository documentation
- **Template improvements**: Create an issue or pull request
- **Project-specific help**: Consult with your team's data engineering lead

---

**Template Version**: 1.0  
**Last Updated**: [Current Date]  
**Based On**: CodeVenture Data Pipelines v1.0
