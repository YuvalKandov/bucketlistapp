# 🪣 Bucket List Tracker – AWS Serverless Application

A full-stack **serverless** web application that lets users create and manage their personal bucket-list items.  
Built with **React** on the frontend and **AWS Amplify (Gen 2)** on the backend to showcase cloud-native architecture.

---

## 🚀 Overview

The **Bucket List Tracker** demonstrates how multiple AWS services integrate to create a secure, scalable, and fully managed serverless app.  
It provides authentication, an API layer, persistent NoSQL data storage, and media uploads — all deployed automatically through **Infrastructure-as-Code (IaC)** using Amplify’s CDK-based backend.

---

## 🧱 Architecture

| Layer | AWS Service | Description |
|-------|--------------|-------------|
| **Frontend** | AWS Amplify Hosting + React | User interface hosted on Amplify; interacts with backend via Amplify libraries |
| **Authentication** | Amazon Cognito | Handles user sign-up, sign-in, and access tokens |
| **API** | AWS AppSync (GraphQL) | Secure API endpoint that connects the app to DynamoDB |
| **Database** | Amazon DynamoDB | Stores user bucket-list items (`BucketItem` model) |
| **Storage** | Amazon S3 | Stores user-uploaded images under `media/<identityId>/…` |
| **Infrastructure as Code** | AWS Amplify Gen 2 (CDK under the hood) | Backend deployed and managed automatically from code |

---

## 🧩 Features

- 🔐 **User Authentication** — Secure email-based login via Cognito  
- 🗂️ **GraphQL API** — Managed through AppSync; supports create/read/update/delete  
- 💾 **Serverless Data Storage** — Items persisted in DynamoDB  
- 🖼️ **Image Uploads** — Each user stores private images in S3  
- ⚙️ **Infrastructure-as-Code** — Entire stack deployed through Amplify CDK without manual console setup  

---

## 🧠 Learning Focus

This project served as an introduction to **AWS serverless architecture** and **Infrastructure-as-Code** concepts:
- Understanding how Amplify provisions Cognito, AppSync, DynamoDB, and S3 automatically  
- Working with the Amplify SDK (`aws-amplify`, `@aws-amplify/ui-react`) in a React environment  
- Exploring Amplify’s **sandbox** environment for rapid backend iteration  
- Seeing how high-level IaC compares to manual CDK/Terraform deployment  

---

## ⚙️ Technologies Used

- **Frontend:** React 19, Vite, Amplify UI React  
- **Backend:** AWS Amplify Gen 2, AppSync, DynamoDB, S3, Cognito  
- **Languages:** JavaScript (ES2022)  
- **IaC:** Amplify Gen 2 (CDK-based)  
- **Auth Flow:** Email sign-up + Cognito User Pools  

---

## 🧭 Next Steps

This project was a starting point for mastering AWS serverless and IaC.  
Future goals:
- Re-create this stack manually using **AWS CDK** to understand each resource definition  
- Add **monitoring (CloudWatch)** and **logging**  
- Implement **custom Lambda resolvers** for more complex backend logic  

---

## 🧑‍💻 Author

**Yuval Kandov**  
Cloud-focused Computer Science student at Afeka College  
Exploring AWS Cloud, DevOps, and Infrastructure-as-Code  
[GitHub @YuvalKandov](https://github.com/YuvalKandov)
