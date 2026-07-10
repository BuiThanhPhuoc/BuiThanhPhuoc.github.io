---
title: "Voice-Driven Construction Management System"
date: 2026-07-04
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

{{% notice note %}}
📌 **Info:** Project article for **Voice-Driven Construction Management System (VDCMS)** - a construction management system with voice reporting and an AWS-oriented deployment architecture.
{{% /notice %}}

# Voice-Driven Construction Management System

## Overview

**Voice-Driven Construction Management System (VDCMS)** is a construction management system designed to support project management, task assignment, progress tracking, and field reporting. The key feature of the system is voice-based reporting, allowing engineers to record progress updates and convert the audio into text to reduce manual typing.

The project is implemented as a web application with a React/Vite frontend, a Node.js/Express backend, a MySQL database, and Socket.IO for real-time features. For AWS deployment, the system is mapped to an architecture using CloudFront, S3, WAF, ALB, EC2, RDS MySQL, SQS, Transcribe, SES, Cognito, Secrets Manager, Systems Manager, CloudWatch, and VPC.

## Project Objectives

The main goal of VDCMS is to build a construction management system that is closer to a real working environment than a basic CRUD application. The system needs to support role-based access control, project management, task assignment, progress reporting, document management, incident handling, internal chat, and voice-based reporting.

Through this project, I practiced several important parts of software development, including requirement analysis, database design, backend/frontend implementation, authentication, cloud deployment, end-to-end testing, and basic security review.

## User Roles

The system includes three main roles:

* **Admin:** Manages users, all projects, reports, documents, and system-wide activity.
* **Manager:** Manages assigned projects, assigns tasks to engineers, tracks progress, approves requests, and reviews project reports.
* **Engineer:** Views assigned tasks, updates checklists, submits progress reports, records voice reports, requests deadline extensions, and reports field incidents.

Separating roles helps the system control access more clearly. Each user can only perform actions within the scope of their responsibility, such as Managers working only on their own projects and Engineers updating only assigned tasks.

## Main Features

The main features include account management, project management, task assignment, deadline tracking, progress reporting, acceptance checklists, document management, internal chat, notifications, incident handling, and voice reporting.

For Engineers, the system focuses on field usability. Users can view tasks, update status, submit reports with voice recordings, save local drafts, and attach images or information related to incidents. For Managers and Admins, the system supports progress tracking, report review, pending request management, and project-based data management.

## Technical Architecture

The frontend is built with **React/Vite**, using React Router for navigation and role-specific layouts. The backend is built with **Node.js/Express**, connected to **MySQL** for business data, and uses **Socket.IO** for real-time features such as chat and notifications.

When deployed on AWS, the frontend can be built and stored on **Amazon S3**, then distributed through **Amazon CloudFront**. User requests pass through **AWS WAF** and an **Application Load Balancer** before reaching the backend running on **Amazon EC2** in a private subnet. The main relational data is stored in **Amazon RDS MySQL**, while files and voice recordings are stored privately in **Amazon S3**.

## Voice Processing Workflow

The voice reporting workflow is the most important part of the project. An Engineer can record a progress report, then the system stores the audio file in S3 and creates a processing task in the database. The task is sent to **Amazon SQS** for asynchronous processing, so the backend does not need to keep the user waiting while transcription is running.

A worker running on EC2 receives messages from SQS, calls **Amazon Transcribe** to convert Vietnamese or English speech into text, and then updates the result back into the system. If processing fails, the message can be moved to a Dead-Letter Queue for inspection and retry. This approach makes the speech-to-text workflow more reliable and more suitable for a production-oriented environment.

## Security and Operations

VDCMS applies several basic security practices such as role-based authorization, HttpOnly cookies for access tokens, refresh token rotation, session revocation during logout or password changes, upload file validation, and preventing secrets from being exposed to the frontend.

At the AWS layer, the system is designed with RDS in private subnets, private S3 storage, signed URLs for media access, WAF protection for abnormal requests, Secrets Manager for sensitive values, and Systems Manager for EC2 administration without opening direct SSH access.

## Results Achieved

During the project, I analyzed business requirements, designed the database, built the backend and frontend, completed the Admin, Manager, and Engineer workflows, and mapped the system to an AWS architecture. I also tested the end-to-end flow through CloudFront, handled issues related to WAF, S3 permissions, and Transcribe, and confirmed that Vietnamese speech-to-text conversion worked successfully.

This project helped me understand how to combine web application development with cloud deployment. Beyond writing code, I learned more about architecture design, access control, file processing, asynchronous queues, AWS service configuration, and resource cleanup after testing to avoid unnecessary costs.

## Conclusion

Voice-Driven Construction Management System helped me connect web development knowledge with AWS services in a practical project. The system not only manages projects and tasks, but also supports voice-based field reporting, making data entry more convenient for users. Through this project, I gained more experience with React, Express, MySQL, Socket.IO, AWS deployment, asynchronous processing, and system security. This is an important foundation for building more practical cloud projects in the future.
