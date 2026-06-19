# Phase 1: Amazon Cognito User Pool Configuration

## Objective

The goal of this phase is to create a secure identity management system for the university portal using Amazon Cognito. This configuration provides authentication, Multi-Factor Authentication (MFA), strong password policies, and role-based access through user groups.

---

## Purpose

Amazon Cognito provides a fully managed identity service for authentication and authorization. In this phase, a User Pool is created to support both Students and Professors while enforcing security best practices.

Features implemented:

* Email-based sign-in
* Strong password requirements
* Multi-Factor Authentication (MFA)
* Self-service account recovery
* Role-based user groups

---

## Configuration Summary

### User Pool Information

| Setting            | Value                       |
| ------------------ | --------------------------- |
| User Pool Name     | UniversityPortalUsers       |
| Application Type   | Traditional Web Application |
| Sign-In Method     | Email                       |
| Required Attribute | Email                       |

---

### Password Policy

| Setting                     | Configuration |
| --------------------------- | ------------- |
| Password Policy Mode        | Custom        |
| Minimum Length              | 8 characters  |
| Uppercase Letters           | Required      |
| Lowercase Letters           | Required      |
| Numbers                     | Required      |
| Special Characters          | Required      |
| Temporary Password Validity | 7 Days        |

---

### Multi-Factor Authentication

| Setting                   | Configuration          |
| ------------------------- | ---------------------- |
| MFA Enforcement           | Required               |
| Second Factor             | TOTP Authenticator App |
| Account Recovery          | Self-Service Enabled   |
| Preferred Recovery Method | Email                  |
| Fallback Recovery Method  | SMS                    |

---

### User Groups

Two groups were created to support Role-Based Access Control (RBAC):

#### Students

Purpose:

* Access course materials
* View grades
* Access assignments

Future Permissions:

* Read-only access to DynamoDB resources

---

#### Professors

Purpose:

* Manage course records
* Upload assignments
* Perform administrative actions

Future Permissions:

* Read and write access to DynamoDB resources

---

## Implementation Steps

### Step 1: Create User Pool

* Open Amazon Cognito.
* Navigate to **User Pools → Create User Pool**.
* Select **Traditional Web Application**.
* Name the application:

```
UniversityPortalUsers
```

* Configure sign-in using Email only.
* Require Email as a user attribute.
* Create the user directory.

---

### Step 2: Configure Authentication

Enabled:

* Email sign-in
* Required Multi-Factor Authentication
* TOTP Authenticator App

Account recovery:

* Self-service enabled
* Email as the preferred recovery option
* SMS as fallback

---

### Step 3: Configure Password Policy

Custom password requirements:

* Minimum length of 8 characters
* Uppercase letter required
* Lowercase letter required
* Number required
* Special character required

Temporary passwords expire after seven days.

---

### Step 4: Create User Groups

Created the following groups:

1. Students
2. Professors

These groups will later be associated with IAM roles to provide fine-grained access control.

---

## Security Controls Implemented

* Multi-Factor Authentication (MFA)
* Strong password policy
* Email-based authentication
* Self-service account recovery
* Role-Based Access Control (RBAC)

---

## Outcome

At the completion of this phase, the Amazon Cognito User Pool was successfully configured to provide secure identity management for the university portal.

The environment is now prepared for:

* Application client configuration
* Hosted UI integration
* User creation and testing
* IAM role mapping
* Fine-grained access control
* Frontend authentication integration

---

## Status

✅ Completed
