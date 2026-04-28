# Resume Analyser

An AI-powered resume analysis web application built with Spring Boot and Google Gemini AI.

---

## What It Does

- Upload your resume (PDF/DOCX) and select a target job role
- Get an ATS score and optimization score out of 100
- View pros, cons, and improvement suggestions
- See relevant job listings based on your role
- Sign in with Google or register with email

---

## Tech Stack

- **Backend:** Java, Spring Boot
- **Database:** MySQL
- **AI:** Google Gemini 2.5 Flash
- **Authentication:** JWT, Google OAuth2
- **Email:** Brevo API
- **Job Listings:** Adzuna API

---

### 2. Open in IDE

Open in **IntelliJ IDEA** or **Eclipse** and let Maven download dependencies from `pom.xml`.

### 3. Configure `application.properties`

```properties
# MySQL Database
spring.datasource.url=your_DB_URL
spring.datasource.username=your_DB_USERNAME
spring.datasource.password=your_DB_PASSWORD

# Google Sign-In
spring.security.oauth2.client.registration.google.client-id=your_GCP_ID
spring.security.oauth2.client.registration.google.client-secret=your_GCP_SECRET

# Gemini AI
genKey=your_GEMINI_API_KEY

# Brevo Email
apiKey=your_BREVO_MAIL_API

# Adzuna Job API
application-id=your_ADZUNA_APP_ID
application-api-key=your_ADZUNA_API_KEY
```

### 4. Run the Application

Run `ResumeAnalyserApplication.java` and open:

```
http://localhost:8080/
```

---

## Notes

- Only **MySQL** is supported for the database.
- Email service works only with **Brevo API**.
- AI analysis is done via **Gemini 2.5 Flash**. If the model changes, update it in `appService.java`.
- AI results are for learning purposes and should not be taken as professional career advice.
