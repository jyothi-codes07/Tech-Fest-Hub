# TechFestHub

### Technical Fest Event Management System

TechFestHub is a web-based event management platform developed using **Java Servlets, JSP, JDBC, and Oracle Database**. It provides a centralized platform for students to explore technical events, register individually or in teams, and manage their registrations.

Administrators can create and manage events, control registration availability, and monitor participants through a dedicated dashboard.

## Key Features

### Student Module
- Student sign-up and login with session-based authentication.
- Browse, search, and explore technical events.
- View detailed event information, including date, venue, and registration fee.
- Register for events individually or as a team.
- Select event tracks during registration.
- Simulated payment process.
- View and cancel event registrations.

### Admin Module
- Separate admin authentication and dashboard.
- Create and update technical events.
- Open or close event registrations.
- Manage event status and details.
- View registrations and participant information.

## Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Java (JDK 21) |
| Frontend | HTML, CSS, JavaScript |
| Backend | Java Servlets, JSP |
| Database | Oracle Database XE |
| Connectivity | JDBC |
| Architecture | DAO Pattern |
| Build Tool | Maven |
| Server | Apache Tomcat 9 |
| IDE | Eclipse |

## Application Architecture

TechFestHub follows a layered architecture for better organization and separation of responsibilities.

```text
Browser
   |
JSP / HTML / CSS / JavaScript
   |
Java Servlets
   |
DAO Layer
   |
JDBC
   |
Oracle Database
```

## Database

The application uses Oracle Database XE to manage:

- **USERS:** Student and administrator account information.
- **EVENTS:** Technical event details and registration settings.
- **REGISTRATIONS:** Student registrations, team details, and registration status.

Database scripts are available in the `database/` directory:

- `schema.sql` – Database structure.
- `sample-data.sql` – Sample records.

## Getting Started

### Prerequisites

- JDK 21
- Eclipse IDE with Maven support
- Apache Tomcat 9
- Oracle Database XE

### Installation

**1. Clone the repository**

```bash
git clone https://github.com/jyothi-codes07/Tech-Fest-Hub.git
```

**2. Import into Eclipse**

Go to:

`File → Import → Maven → Existing Maven Projects`

Select the folder containing `pom.xml`.

**3. Configure the database**

Execute the following SQL scripts in Oracle Database XE:

```text
database/schema.sql
database/sample-data.sql
```

**4. Configure JDBC**

Update the database username and password in `DBConnection.java` according to your local Oracle configuration.

Database URL:

```text
jdbc:oracle:thin:@localhost:1521:xe
```

**5. Run the application**

Configure Apache Tomcat 9 in Eclipse and select:

`Right Click Project → Run As → Run on Server`

Example application URL:

```text
http://localhost:8080/TechFestHub_Simplified/
```

The context root may vary depending on your Eclipse configuration.

## Future Enhancements

- Real payment gateway integration.
- Email notifications for event registrations.
- QR-code-based event check-in.
- Automated participation certificates.
- Advanced admin analytics.
- Event attendance tracking.

## Project Information

**Project Name:** TechFestHub

**Domain:** Web Development

**Project Type:** Academic Collaborative Project

---

*Developed as an academic project to explore Java web development, database management, and event registration systems.*
