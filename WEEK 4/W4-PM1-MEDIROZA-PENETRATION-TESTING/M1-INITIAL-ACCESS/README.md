# M1 — Initial Access

## Objective

Attack the website and retrieve 3 confidential patient PDF lab reports.

## Approach

I started by carrying out reconnaissance against the target to understand what was publicly accessible and to identify possible entry points.

The project brief required me to:

- Conduct reconnaissance on the target.
- Identify exposed entry points.
- Analyse the behaviour of authentication mechanisms.
- Look for weaknesses in how the application handled user input.
- Gain access to a restricted area of the site.

## 1. Target

I accessed:

`https://medirozahospital.com`

## 2. Website Reconnaissance

I reviewed the publicly accessible areas of the website and the available navigation.

The walkthrough showed:

- Home
- About
- Doctors
- Contact
- Patient Portal
- Staff Login

## 3. Staff Login

I opened the **Staff Login** page.

The page contained:

- Staff ID
- Password
- Sign in

It also displayed:

**Internal staff access only.**

This provided an authentication point to examine as part of the assessment.

## 4. Public Pages Reviewed

### Doctors

I opened the Doctors page and reviewed the information presented about the hospital's doctors.

### Contact

I opened the Contact page and reviewed the displayed address, phone number, email, and opening hours.

### Home

I returned to the homepage and reviewed the main content, including **Book an appointment**, **Meet our doctors**, and **Our Departments**.

The page also displayed:

**“Compassionate care, advanced medicine.”**

### About

I opened the About page and reviewed information covering the hospital, its values, and accreditation.

## 5. Authentication and Input Testing

I then documented the behaviour observed while testing the identified authentication mechanism and application input.

| Test Area | Result |
|---|---|
| Authentication behaviour | To be recorded from evidence |
| User input behaviour | To be recorded from evidence |
| Application response | To be recorded from evidence |
| Weakness identified | To be recorded from evidence |

## 6. Restricted Area and Retrieval

Once the weakness is confirmed, I will document the exact path used to reach the restricted area and retrieve the three patient PDF reports.

| Step | Evidence |
|---|---|
| Entry point identified | `04-entry-point.png` |
| Authentication behaviour | `05-authentication-testing.png` |
| Input handling | `06-input-testing.png` |
| Restricted access | `07-restricted-area.png` |
| Patient PDF 1 | `08-patient-report-1.png` |
| Patient PDF 2 | `09-patient-report-2.png` |
| Patient PDF 3 | `10-patient-report-3.png` |

## Deliverable

- Proof of access.
- The 3 retrieved PDF lab reports.
