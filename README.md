# campuspulse-complaint-core
Complaint Management Core Module
# 📋 CampusPulse — Complaint Management Core Module

[![Spring Boot](https://img.shields.io/badge/Spring--Boot-3.x-brightgreen.svg)](https://spring.io/projects/spring-boot)
[![Spring Data JPA](https://img.shields.io/badge/Spring--Data-JPA-blue.svg)](https://spring.io/projects/spring-data-jpa)
[![Thymeleaf](https://img.shields.io/badge/UI-Thymeleaf-005F0F.svg)](https://www.thymeleaf.org/)

## 📌 Module Overview
The **Complaint Management Core** module powers the end-to-end complaint lifecycle. It manages complaint registration, multipart file evidence uploads, lifecycle state transitions (`PENDING` $\rightarrow$ `IN_PROGRESS` $\rightarrow$ `RESOLVED`), Spring Data JPA Specifications for multi-criteria search, optimistic concurrency locking, AI category classification integration, and student feedback rating collection.

---

## 🏗️ Repository Architecture & Directory Structure

```text
campuspulse-complaint-core/
├── src/main/java/com/campuspulse/complaints/
│   ├── config/             # MultipartConfig, StorageProperties
│   ├── controller/         # ComplaintController, FeedbackController
│   ├── dto/                # ComplaintDTO, FeedbackDTO, SearchCriteriaDTO
│   ├── entity/             # Complaint.java, Category.java, Feedback.java
│   ├── event/              # ComplaintSubmittedEvent.java, ComplaintStatusChangedEvent.java
│   ├── repository/         # ComplaintRepository, FeedbackRepository
│   └── service/            # ComplaintService, StorageService, AIClient
├── src/main/resources/
│   ├── templates/          # Thymeleaf views (complaint-form.html, history.html)
│   └── static/             # CSS badge styles & JavaScript form validators
├── Dockerfile
├── pom.xml
└── README.md

