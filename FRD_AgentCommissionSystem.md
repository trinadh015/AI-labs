# Functional Requirements Document
## Agent Performance & Commission Tracking System

### 1. Document Overview
- **Project:** Agent Performance & Commission Tracking System
- **Date:** 2026-02-06
- **Version:** 1.0
- **Status:** In Development

### 2. Executive Summary
This system enables insurance company administrators to manage agent sales, calculate commissions automatically, and track performance metrics transparently, reducing manual errors and improving agent motivation.

### 3. Stakeholders
- Insurance Company Administrators
- Insurance Sales Agents
- Finance Department
- Compliance & Audit Team

### 4. User Roles & Permissions

#### 4.1 Administrator
- Add/Edit/Delete Agent Profiles
- Manage Commission Rules
- View All Reports & Dashboards
- Export Data & Audit Logs
- Manage System Users

#### 4.2 Agent
- View Own Profile
- Record Sales/Policies
- View Personal Dashboard (KPIs, Commissions)
- View Personal Reports

### 5. Functional Requirements

| ID   | Requirement | User Type | Priority | Status |
|------|------------|-----------|----------|---------|
| FR1  | User Login with Email & Password | Admin, Agent | High | Pending |
| FR2  | JWT Token-Based Authentication | System | High | Pending |
| FR3  | Add New Agent Profile | Admin | High | Pending |
| FR4  | Edit Agent Profile | Admin | High | Pending |
| FR5  | Search Agents by Name/Region | Admin | Medium | Pending |
| FR6  | Record New Policy Sale | Agent, Admin | High | Pending |
| FR7  | View Recorded Sales History | Agent, Admin | High | Pending |
| FR8  | Define Commission Rules | Admin | High | Pending |
| FR9  | Edit Commission Rules | Admin | High | Pending |
| FR10 | Automatic Commission Calculation | System | High | Pending |
| FR11 | View Agent Dashboard (Sales, KPIs) | Agent | High | Pending |
| FR12 | View Admin Dashboard (All Agents) | Admin | High | Pending |
| FR13 | Export Reports (CSV/Excel) | Admin | Medium | Pending |
| FR14 | Generate Audit Logs | System | High | Pending |
| FR15 | Role-Based Access Control | System | High | Pending |

### 6. Data Requirements
- Agent profiles (name, email, region, target amount, status)
- Policy data (policy type, premium, tenure, status, issue date)
- Sales records (agent, policy, date, commission calculated)
- Commission rules (policy type, premium thresholds, tenure, percentage)
- Performance metrics (total sales, commission earned, target achieved, KPIs)
- Audit logs (user actions, timestamp, changes made)

### 7. Non-Functional Requirements
- Response Time: < 2 seconds for API calls
- Uptime: 99.9%
- Database backups: Daily
- Security: AES-256 encryption for sensitive data
- Scalability: Support 1000+ agents
- Compliance: GDPR, data privacy standards

### 8. Business Rules
1. Commission is calculated only for approved sales
2. Tenure must be > 0 months for commission eligibility
3. Premium threshold applies based on policy type
4. Agents cannot edit commission rules
5. All transactions must be audited and logged

### 9. Use Cases

#### UC1: Agent Login
**Actor:** Agent
**Steps:**
1. Navigate to login page
2. Enter username and password
3. System validates credentials
4. System generates JWT token
5. Agent is redirected to personal dashboard

#### UC2: Admin Creates Commission Rule
**Actor:** Administrator
**Steps:**
1. Navigate to Commission Rules page
2. Click "New Rule"
3. Enter policy type, min premium, tenure, percentage
4. Submit form
5. System creates rule and reloads commission engine

#### UC3: Record Policy Sale
**Actor:** Agent
**Steps:**
1. Navigate to Sales Entry page
2. Select policy type and agent
3. Enter premium amount and tenure
4. Submit
5. System calculates commission automatically
6. Sale and commission records created

#### UC4: View Agent Performance Dashboard
**Actor:** Agent
**Steps:**
1. Login as agent
2. View dashboard with KPIs
3. See total sales, commissions earned, target achievement
4. View list of recent sales

#### UC5: Export Audit Report
**Actor:** Administrator
**Steps:**
1. Navigate to Reports section
2. Click "Export Commission Report"
3. System generates CSV file
4. File is downloaded

### 10. Acceptance Criteria
- All API endpoints respond within 2 seconds
- Commission calculations are accurate to 2 decimal places
- All user actions are logged in audit trail
- Role-based access is enforced on all pages
- System supports concurrent users without performance degradation