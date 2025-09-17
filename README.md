# Prescription Webapp (JDBC)

A simple **Spring MVC + JDBC web application** for managing prescriptions, patients, doctors, and pharmacies.
This project demonstrates working with **databases in Java** using **Spring Boot, JDBC, and SQL**.

---

## 🚀 Features

* **Create prescriptions** — doctors can create new prescriptions linked to patients and drugs.
* **Fill prescriptions** — pharmacists can validate and fill prescriptions with cost calculation.
* **Patient & doctor validation** — ensures only valid IDs/names are used.
* **Drug & pharmacy lookup** — fetches info from the database before processing.
* **Refill tracking** — decrements refills and tracks fill history.

---

## 🛠️ Tech Stack

* **Java 17+**
* **Spring Boot / Spring MVC**
* **Spring JDBC (`JdbcTemplate`)**
* **MySQL (or any JDBC-compatible DB)**
* **Maven** for build & dependency management

---

## 📂 Project Structure

```
src/main/java/application/
    ControllerDoctor.java
    ControllerPatientCreate.java
    ControllerPatientUpdate.java
    ControllerPrescriptionCreate.java
    ControllerPrescriptionFill.java
    MainApplication.java

src/main/java/view/
    DoctorView.java
    PatientView.java
    PrescriptionView.java
```

---

## ⚙️ Setup & Run

### 1️⃣ Clone the repository

```bash
git clone https://github.com/r-siddiq/Prescription-Webapp-JDBC.git
cd Prescription-Webapp-JDBC
```

### 2️⃣ Build with Maven

```bash
./mvnw clean package
```

### 3️⃣ Run the app

```bash
./mvnw spring-boot:run
```

### 4️⃣ Access in browser

```
http://localhost:8080
```

---

## 🗄️ Database Setup

1. Create a MySQL (or other JDBC) database.
2. Import the schema (tables: `doctor`, `patient`, `prescription`, `drug`, `pharmacy`, `prescription_fill`, `drug_cost`).
3. Update your `application.properties` (or `application.yml`) with DB connection settings:

   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/prescriptions
   spring.datasource.username=root
   spring.datasource.password=yourpassword
   spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
   ```

---

## 📖 Example Endpoints

* **New prescription form:**
  `GET /prescription/new`

* **Create prescription:**
  `POST /prescription`

* **Fill prescription form:**
  `GET /prescription/fill`

* **Process prescription fill:**
  `POST /prescription/fill`

---

## ✅ Status

This is a **portfolio project** highlighting JDBC and Spring MVC.
It’s not production-ready, but it demonstrates **database interaction, form handling, and MVC patterns** in a clean way.
