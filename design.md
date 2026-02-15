# System Design Document

## 1. Overall Architecture
The system follows a layered architecture:

Presentation Layer → Application Layer → AI Engine → Database → SMS Notification Layer

## 2. Modules

### User Module
- Registration/Login
- Profile creation
- Eligibility questionnaire

### AI Matching Module
- Rule-based eligibility engine
- Income-based filtering
- Location-based filtering
- Category-based filtering

### Scheme Module
- Scheme database
- Eligibility rules storage
- Required document storage
- Deadline management

### Notification Module
- SMS reminder before deadline

### Admin Module
- Add/update schemes
- Modify eligibility rules
- Monitor system usage

## 3. AI Matching Logic
The system collects user inputs and applies rule-based conditions.

Example:
IF age ≥ 18 AND income ≤ ₹2,50,000
THEN eligible for XYZ Scheme.

## 4. Database Design

Users Table:
- User_ID
- Name
- Mobile
- Age
- Income
- Location

Schemes Table:
- Scheme_ID
- Scheme_Name
- Eligibility_Rules
- Required_Documents
- Deadline

Matching History Table:
- User_ID
- Scheme_ID
- Date_Checked

## 5. Security Design
- OTP-based authentication
- Input validation
- Admin role control
- Secure database access

## 6. Future Scalability
- Multi-state expansion
- Integration with government databases
- Advanced ML-based prediction
