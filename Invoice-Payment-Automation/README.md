# Automated Invoice Payment Tracking using Zapier

## 1. Project Overview

This project implements an automated invoice payment tracking workflow using
Zapier, Gmail, and Google Sheets. The automation identifies pending invoices,
sends personalized payment requests, captures payment confirmations through
email replies, and automatically updates the corresponding invoice status.

The workflow reduces manual follow-up and provides an automated mechanism for
maintaining the latest payment status of invoices.

---

## 2. Objective

The objective of this project is to automate the invoice payment follow-up
and confirmation process.

The workflow is designed to:

- Identify invoices with Pending payment status.
- Send automated and personalized payment request emails.
- Detect payment confirmation replies.
- Identify the corresponding invoice using the Invoice ID.
- Automatically update the invoice status to Completed.

---

## 3. Tools & Technologies

- Zapier
- Google Sheets
- Gmail
- Formatter by Zapier
- Looping by Zapier

---

## 4. Input Data

The invoice records are maintained in Google Sheets with the following fields:

| Field | Description |
|---|---|
| Sr | Serial number of the invoice |
| Invoice ID | Unique identifier for each invoice |
| Type | Type of invoice |
| Name | Name associated with the invoice |
| Amount | Invoice payment amount |
| Account No | Payment account number |
| Bank Name | Bank associated with the account |
| Status | Current payment status |

---

# 5. Workflow Architecture

The solution consists of two interconnected Zaps.

### Zap 1 – Automated Payment Request
Identifies pending invoices and sends personalized payment request emails.

[View Zap 1 – Payment Request Automation](https://zapier.com/templates/details/automate-payment-request-reminders-86dba6?secret=MTp0ZW1wbGF0ZTpja0FiQ2d6Q2Z5MFA0S1FsTVNZUkxzRENxa2puUFRLXzZXVURUUzBySFdROnVwMzJyNQ)

Google Sheets  
↓  
Identify Pending Invoices  
↓  
Loop Through Invoices  
↓  
Gmail Payment Request  
↓  
Recipient Receives Email

### Zap 2 – Automated Payment Confirmation
Detects "Payment Done" replies, extracts the Invoice ID, and updates the
corresponding invoice status in Google Sheets.

[View Zap 2 – Payment Confirmation Automation](https://zapier.com/templates/details/update-invoice-from-payment-confirmation-85b7dc?secret=MTp0ZW1wbGF0ZTpZa0pQSHVZelJUWWdhT25pN0dtNlh1ek9BSG1sWV9QYkVmLTZMTmZUaWhZOmFzNGJ4OQ)

Recipient Replies "Payment Done"  
↓  
Gmail Detects Reply  
↓  
Filter Validates Payment Confirmation  
↓  
Formatter Extracts Invoice ID  
↓  
Google Sheets Finds Invoice  
↓  
Google Sheets Updates Status  
↓  
Payment Status = Completed

---

# 6. Key Automation Features

- Automated identification of pending invoices
- Personalized payment request emails
- Dynamic invoice information mapping
- Individual processing through looping
- Email-based payment confirmation
- Automatic Invoice ID extraction
- Automated Google Sheets status update
- Reduced manual payment follow-up

---

# 7. Outcome

The automation establishes an end-to-end workflow for invoice payment
tracking, connecting invoice identification, payment communication, payment
confirmation, and status updating within a single automated process.

The workflow demonstrates how no-code automation can integrate multiple
business applications to reduce repetitive manual activities.

---

# 8. Zapier Links

- https://zapier.com/templates/details/automate-payment-request-reminders-86dba6?secret=MTp0ZW1wbGF0ZTpja0FiQ2d6Q2Z5MFA0S1FsTVNZUkxzRENxa2puUFRLXzZXVURUUzBySFdROnVwMzJyNQ
- 
