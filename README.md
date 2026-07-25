#  Website Delivery with Amazon CloudFront

##  Project Overview

This project demonstrates how to securely host and deliver a static website using **Amazon S3 and Amazon CloudFront**.

The project focuses on configuring an Amazon S3 bucket as the origin for a CloudFront distribution and delivering website content globally through the CloudFront Content Delivery Network (CDN).

As part of the implementation, **Origin Access Control (OAC)** was configured to allow CloudFront to securely access the private S3 bucket. This project provided practical experience in setting up secure and scalable website delivery using AWS cloud services.

---

##  Architecture

```text id="5j8k2p"
                    ┌──────────────────────┐
                    │        User          │
                    │   Web Browser        │
                    └──────────┬───────────┘
                               │
                               │ HTTPS Request
                               ▼
                    ┌──────────────────────┐
                    │    Amazon CloudFront │
                    │     CDN Distribution │
                    └──────────┬───────────┘
                               │
                               │ Secure Access
                               │ Using OAC
                               ▼
                    ┌──────────────────────┐
                    │      Amazon S3       │
                    │   Private Bucket     │
                    │                      │
                    │  Static Website      │
                    │  HTML / CSS / JS     │
                    └──────────────────────┘
```

---

##  AWS Services Used

| AWS Service                     | Purpose                                                         |
| ------------------------------- | --------------------------------------------------------------- |
| **Amazon S3**                   | Stores the static website files                                 |
| **Amazon CloudFront**           | Delivers website content globally through a CDN                 |
| **Origin Access Control (OAC)** | Provides secure access from CloudFront to the private S3 origin |

---

##  How It Works

1. Static website files are uploaded to an **Amazon S3 bucket**.
2. The S3 bucket is configured as the origin for an **Amazon CloudFront distribution**.
3. **Origin Access Control (OAC)** is configured to securely connect CloudFront with the S3 bucket.
4. A bucket policy is configured to allow the CloudFront distribution to access the required S3 objects.
5. A user accesses the website through the CloudFront distribution URL.
6. CloudFront retrieves the requested content from the S3 origin.
7. CloudFront delivers the website content to the user through the CDN.

---

##  Project Objectives

* Learn how to host static website files using Amazon S3.
* Understand how Amazon CloudFront delivers website content.
* Configure an S3 bucket as a CloudFront origin.
* Implement Origin Access Control (OAC).
* Secure the S3 bucket by restricting direct public access.
* Configure an appropriate S3 bucket policy for CloudFront access.
* Understand how a Content Delivery Network improves website delivery.
* Test the website through the CloudFront distribution URL.

---

##  Security Configuration

The project uses **Origin Access Control (OAC)** to secure communication between Amazon CloudFront and the S3 origin.

The S3 bucket is kept private, while CloudFront is granted permission to retrieve the website objects. This prevents users from directly accessing the S3 bucket and ensures that website content is delivered through the CloudFront distribution.

The bucket policy is configured to allow the required CloudFront distribution to access objects in the S3 bucket.

---

## 📂 Repository Structure

```text id="t0k7zp"
website-delivery-with-cloudfront/
│
├── README.md
│
├── index.html
├── style.css
├── script.js
│
├── screenshots/
│   ├── s3.png
│   ├── cloudfront.png
│   ├── origin-access-control.png
│   └── final-website.png
│
└── documentation/
    └── project-documentation.pdf
```

> **Note:** The code filenames shown above are examples. If your three uploaded files have different names, keep the actual filenames in this section.

---

##  Website Files

The repository contains the source files used to build the static website.

* **HTML** – Defines the structure and content of the website.
* **CSS** – Defines the visual styling and layout.
* **JavaScript** – Provides client-side functionality and interactions.

---

##  Project Screenshots

The `screenshots` folder contains visual evidence of the project implementation.

The screenshots demonstrate:

* Amazon S3 bucket configuration.
* Website files stored in the S3 bucket.
* Amazon CloudFront distribution configuration.
* Origin Access Control (OAC) configuration.
* S3 bucket policy configuration.
* Final website accessed through the CloudFront distribution URL.

---

## 📑 Project Documentation

The complete project documentation is available in the `documentation` folder.

📄 **Project Documentation:**
`documentation/project-documentation.pdf`

The documentation provides additional details about the project implementation, AWS configuration, security settings, and project outcomes.

---

##  Key Learnings

Through this project, I gained practical experience in:

* Amazon S3 static website hosting.
* Amazon CloudFront CDN configuration.
* Configuring CloudFront distributions.
* Setting up Origin Access Control (OAC).
* Securing S3 origins using bucket policies.
* Understanding CloudFront and S3 integration.
* Delivering website content through a global CDN.
* Understanding secure cloud-based website delivery.

---

##  Project Outcome

Successfully configured and deployed a static website using **Amazon S3 and Amazon CloudFront**.

The project demonstrates how CloudFront can securely deliver website content stored in a private S3 bucket using **Origin Access Control (OAC)**.

This project strengthened my practical understanding of **AWS S3, CloudFront, CDN concepts, Origin Access Control, bucket policies, and secure website delivery**.

---

##  Technologies & Services Used

* **Amazon S3**
* **Amazon CloudFront**
* **Origin Access Control (OAC)**
* **HTML**
* **CSS**
* **JavaScript**
* **AWS Cloud**

---

 **This project was completed as part of my hands-on learning and practical experience with AWS Cloud and website delivery technologies.**
