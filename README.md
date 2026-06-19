# aws-secure-student-portal

# 🎓 Secure University Student Portal Authentication with Amazon Cognito

## 📌 Project Overview

This project demonstrates how to design and implement a secure identity and access management solution for a university student portal using AWS-native services.

The portal allows thousands of students to securely access grades, assignments, and learning materials, while professors receive elevated privileges to manage and upload course content.

To protect sensitive academic data and maintain privacy, the system enforces:

- Multi-Factor Authentication (MFA)
- Strong password policies
- Role-Based Access Control (RBAC)
- Secure user authentication and authorization

This project simulates how a Cloud Security Engineer secures user identities and manages controlled access across multiple user roles in AWS.

---

# 🏛 Scenario

A university is building a centralized student portal that serves two types of users:

### Students
- Access grades
- View assignments
- Download learning materials

### Professors
- Manage course records
- Upload assignments
- Access administrative functions

Because the platform contains sensitive academic information, the system must provide:

- Multi-Factor Authentication (MFA)
- Strong password requirements
- Role-based access control (RBAC)
- Secure user authentication
- Controlled access based on user roles

---

# ☁️ Solution Architecture

This project uses **Amazon Cognito** as the identity provider to handle authentication and authorization.

### User Authentication
- Create an Amazon Cognito User Pool
- Configure password policies
- Enable Multi-Factor Authentication (MFA)
- Enable self-service sign-up and login

### Role-Based Access Control
- Create separate user groups:
  - **Students**
  - **Professors**
- Assign permissions based on group membership

### Frontend Integration
- Configure a Cognito App Client
- Configure a Cognito Hosted Domain
- Integrate with a frontend application using OIDC Quick Setup
- Ensure only authenticated users can access the portal

This architecture provides strong identity protection while delivering a seamless user experience.

---

# 🎯 Objectives

This project provides hands-on experience with identity and access management, one of the core domains of cloud security.

By completing this project, you will learn how to:

- Configure Amazon Cognito User Pools
- Enforce password policies
- Implement Multi-Factor Authentication (MFA)
- Create user groups and role-based access controls
- Manage user identities securely
- Integrate Cognito authentication with a frontend application
- Implement an authentication flow using OpenID Connect (OIDC)

---

# 🛠 AWS Services Used

| Service | Purpose |
|-----------|---------|
| **Amazon Cognito User Pool** | User authentication and group management |
| **Amazon Cognito App Client** | Secure frontend authentication |
| **AWS IAM** | Role mapping and permissions |
| **Amazon Cognito Hosted UI** | Secure login interface |
| **React + OIDC** | Frontend application |

---

# 👨‍💻 Project Implementation Steps

## Step 1: Create a Cognito User Pool
- Configure custom password policies
- Enable Multi-Factor Authentication (MFA)
- Enable self-service registration

---

## Step 2: Configure a Cognito App Client
- Create an application client
- Configure callback URLs
- Enable authentication flows

---

## Step 3: Configure a Hosted Domain
- Create a Cognito-hosted login page
- Enable secure sign-in and sign-out

---

## Step 4: Create User Groups
Create two groups:

### Students
Standard access to:

- Grades
- Assignments
- Course materials

### Professors
Elevated access to:

- Course management
- Uploading records
- Administrative actions

---

## Step 5: Create and Test User Accounts

Create test users for both groups:

### Student User
- Verify account creation
- Test MFA
- Confirm login access

### Professor User
- Verify elevated permissions
- Test MFA enforcement
- Confirm group membership

---

## Step 6: Integrate Frontend Authentication

Configure:

- Cognito Hosted UI
- OpenID Connect (OIDC)
- React frontend

Users authenticate through Amazon Cognito before accessing the university portal.

---

## 🔐 Security Controls Implemented

### Multi-Factor Authentication (MFA)
Provides an additional layer of account protection.

### Strong Password Policies
Enforces:

- Minimum password length
- Uppercase letters
- Lowercase letters
- Numbers
- Special characters

### Role-Based Access Control (RBAC)
Permissions are assigned according to user group membership.

### Verified User Access
Only authenticated and authorized users can access protected resources.

---

# 🧪 Validation and Testing

The following functionality is tested:

- User registration
- User authentication
- MFA enforcement
- Password policy compliance
- Student access permissions
- Professor elevated permissions
- Group membership
- Secure frontend login
- OIDC authentication flow

---

# ✅ Project Outcomes

After completing this project:

- Students can securely access their own course materials.
- Professors receive group-based elevated privileges.
- Multi-Factor Authentication protects user accounts.
- Strong password policies improve account security.
- Authentication is integrated seamlessly into the frontend application.
- User identities and permissions are centrally managed within AWS.

---

# 📚 Skills Demonstrated

- AWS Identity and Access Management
- Amazon Cognito User Pools
- Multi-Factor Authentication (MFA)
- Password Policies
- Role-Based Access Control (RBAC)
- OpenID Connect (OIDC)
- Secure Authentication Flows
- Cloud Security Best Practices
- Identity and Access Management (IAM)
- Frontend Authentication Integration

---

# 📁 Repository Structure

```text
.
├── README.md
├── architecture-diagram/
├── screenshots/
├── frontend-app/
├── documentation/
└── assets/
```

---

# 🏗 Architecture

```text
Users
   │
   ▼
Amazon Cognito Hosted UI
   │
   ▼
Amazon Cognito User Pool
   │
 ┌─────────────┬─────────────┐
 ▼                           ▼
Students Group          Professors Group
   │                           │
   └─────────────┬─────────────┘
                 ▼
        React Frontend Application
                 ▼
          University Student Portal
```

---

## 🚀 Author

Cloud Security Engineer Portfolio Project

Built using AWS best practices for secure identity and access management.
