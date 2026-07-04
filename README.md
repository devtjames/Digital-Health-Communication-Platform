# Digital Health Communication Platform

![Laravel](https://img.shields.io/badge/Laravel-12-FF2D20?style=flat-square&logo=laravel&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-8.2+-777BB4?style=flat-square&logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL%20%2F%20MariaDB-8.0+-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Blade](https://img.shields.io/badge/Views-Laravel%20Blade-FF2D20?style=flat-square)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-3.x-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Chart.js](https://img.shields.io/badge/Charts-Chart.js-FF6384?style=flat-square&logo=chartdotjs&logoColor=white)

Digital Health Communication Platform is a Laravel-based academic MVP for remote patient care and monitoring. It connects admins, doctors, and patients through appointments, patient profiles, health readings, automatic alerts, simple messaging, consultation notes, prescriptions, and role-specific dashboards.

The project is built as a clean Laravel MVC application using Blade templates, Tailwind CSS, Laravel Breeze authentication, Eloquent relationships, role middleware, MySQL migrations, Chart.js dashboards, and PHPUnit feature tests.

## Features

- Responsive landing page for the digital health platform
- Laravel Breeze authentication with registration, login, logout, and password reset
- Role-based access for admin, doctor, and patient users
- Admin dashboard with system totals, recent alerts, and charts
- Doctor dashboard with linked patients, pending appointments, open alerts, readings, and messages
- Patient dashboard with upcoming appointment, latest prescription, health reading, alert, quick links, and chart
- Admin doctor management with create, edit, update, activate, and deactivate workflows
- Patient registration and profile management
- Appointment booking between patients and active doctors
- Doctor appointment approval, completion, cancellation, and notes
- Patient health reading submission
- Automatic alert detection for abnormal readings
- Doctor patient monitoring page with bio data, appointments, readings, alerts, prescriptions, notes, and messaging
- Simple non-real-time doctor-patient messaging
- Consultation notes and prescriptions linked to doctors, patients, and appointments
- Responsive tables, forms, cards, dashboard layout, and mobile sidebar
- SVG favicon, web manifest, and polished public UI
- Feature tests covering the major user flows

## Screenshots

### Public And Authentication

| Home | Login | Register |
| --- | --- | --- |
| ![Homepage](docs/screenshots/home.png) | ![Login page](docs/screenshots/login.png) | ![Registration page](docs/screenshots/register.png) |

| Forgot Password |
| --- |
| ![Forgot password page](docs/screenshots/forgot-password.png) |

### Admin Pages

| Dashboard | Doctors | Create Doctor |
| --- | --- | --- |
| ![Admin dashboard](docs/screenshots/admin-dashboard.png) | ![Admin doctors page](docs/screenshots/admin-doctors.png) | ![Create doctor page](docs/screenshots/admin-create-doctor.png) |

| Edit Doctor | Patients | Appointments |
| --- | --- | --- |
| ![Edit doctor page](docs/screenshots/admin-edit-doctor.png) | ![Admin patients page](docs/screenshots/admin-patients.png) | ![Admin appointments page](docs/screenshots/admin-appointments.png) |

| Alerts |
| --- |
| ![Admin alerts page](docs/screenshots/admin-alerts.png) |

### Doctor Pages

| Dashboard | Appointments | Appointment Details |
| --- | --- | --- |
| ![Doctor dashboard](docs/screenshots/doctor-dashboard.png) | ![Doctor appointments page](docs/screenshots/doctor-appointments.png) | ![Doctor appointment details](docs/screenshots/doctor-appointment-details.png) |

| Patients | Patient Monitoring | Health Readings |
| --- | --- | --- |
| ![Doctor patients page](docs/screenshots/doctor-patients.png) | ![Doctor patient monitoring page](docs/screenshots/doctor-patient-monitoring.png) | ![Doctor health readings page](docs/screenshots/doctor-health-readings.png) |

| Alerts | Alert Details | Messages |
| --- | --- | --- |
| ![Doctor alerts page](docs/screenshots/doctor-alerts.png) | ![Doctor alert details](docs/screenshots/doctor-alert-details.png) | ![Doctor messages page](docs/screenshots/doctor-messages.png) |

| Conversation | Create Prescription | Create Consultation Note |
| --- | --- | --- |
| ![Doctor conversation page](docs/screenshots/doctor-conversation.png) | ![Create prescription page](docs/screenshots/doctor-create-prescription.png) | ![Create consultation note page](docs/screenshots/doctor-create-consultation-note.png) |

### Patient Pages

| Dashboard | Profile | Appointments |
| --- | --- | --- |
| ![Patient dashboard](docs/screenshots/patient-dashboard.png) | ![Patient profile page](docs/screenshots/patient-profile.png) | ![Patient appointments page](docs/screenshots/patient-appointments.png) |

| Book Appointment | Health Readings | Submit Health Reading |
| --- | --- | --- |
| ![Book appointment page](docs/screenshots/patient-book-appointment.png) | ![Patient health readings page](docs/screenshots/patient-health-readings.png) | ![Submit health reading page](docs/screenshots/patient-submit-health-reading.png) |

| Alerts | Messages | Conversation |
| --- | --- | --- |
| ![Patient alerts page](docs/screenshots/patient-alerts.png) | ![Patient messages page](docs/screenshots/patient-messages.png) | ![Patient conversation page](docs/screenshots/patient-conversation.png) |

| Prescriptions | Consultation Notes |
| --- | --- |
| ![Patient prescriptions page](docs/screenshots/patient-prescriptions.png) | ![Patient consultation notes page](docs/screenshots/patient-consultation-notes.png) |

## Tech Stack

- Laravel 12
- PHP 8.2+
- MySQL or MariaDB
- Laravel Breeze authentication
- Laravel Blade views
- Tailwind CSS
- Alpine.js
- Chart.js
- Playwright for screenshot capture
- PHPUnit feature tests

## Requirements

Before running the project, make sure you have:

- PHP 8.2 or newer
- Composer
- MySQL or MariaDB
- Node.js and npm
- XAMPP, WAMP, Laragon, Herd, or another PHP/MySQL stack
- Chrome if you want to regenerate screenshots using the included script
- SMTP credentials if you want real password reset emails

## Project Structure

```text
.
|-- app/
|   |-- Http/
|   |   |-- Controllers/
|   |   `-- Middleware/
|   |-- Models/
|   `-- Services/
|-- database/
|   |-- factories/
|   |-- migrations/
|   `-- seeders/
|-- docs/
|   `-- screenshots/
|-- public/
|   |-- images/
|   |-- favicon.svg
|   `-- site.webmanifest
|-- resources/
|   |-- css/
|   |-- js/
|   `-- views/
|       |-- admin/
|       |-- auth/
|       |-- doctor/
|       |-- layouts/
|       |-- patient/
|       `-- welcome.blade.php
|-- routes/
|-- scripts/
|   `-- capture-screenshots.cjs
|-- tests/
|-- composer.json
|-- package.json
`-- vite.config.js
```

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/digital-health-communication.git
cd digital-health-communication
```

### 2. Install PHP dependencies

```bash
composer install
```

### 3. Install frontend dependencies

```bash
npm install
```

### 4. Create the environment file

```bash
cp .env.example .env
```

On Windows PowerShell:

```powershell
Copy-Item .env.example .env
```

### 5. Generate the application key

```bash
php artisan key:generate
```

## Environment Setup

Update your `.env` file:

```env
APP_NAME="Digital Health Communication"
APP_ENV=local
APP_DEBUG=true
APP_URL=http://localhost:8000

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=digital_health_communication
DB_USERNAME=root
DB_PASSWORD=

SESSION_DRIVER=database
CACHE_STORE=database
QUEUE_CONNECTION=database

MAIL_MAILER=log
MAIL_FROM_ADDRESS="hello@example.com"
MAIL_FROM_NAME="${APP_NAME}"
```

For real password reset emails, replace the mail settings with SMTP credentials:

```env
MAIL_MAILER=smtp
MAIL_HOST=smtp.example.com
MAIL_PORT=587
MAIL_USERNAME=your_smtp_username
MAIL_PASSWORD=your_smtp_password
MAIL_SCHEME=smtp
MAIL_FROM_ADDRESS="support@example.com"
MAIL_FROM_NAME="${APP_NAME}"
```

Do not commit your real `.env`, database password, or SMTP credentials.

## Database Setup

Create a MySQL/MariaDB database:

```sql
CREATE DATABASE digital_health_communication;
```

Run migrations and seed the admin user:

```bash
php artisan migrate --seed
```

## Default Login Details

The default seeded account is:

```text
Role: Admin
Email: admin@digitalhealth.test
Password: password
```

Normal users can register from the public registration page. Registered users are assigned the patient role by default.

For screenshot/demo data, run:

```bash
npm run screenshots
```

That script creates or updates these local demo accounts:

```text
Admin:   admin@digitalhealth.test / password
Doctor:  doctor@digitalhealth.test / password
Patient: patient@digitalhealth.test / password
```

## Running Locally

Run the Laravel development server:

```bash
php artisan serve
```

Open:

```text
http://localhost:8000
```

If you are actively editing frontend assets, run Vite too:

```bash
npm run dev
```

For a production-style asset build:

```bash
npm run build
```

## Common Workflows

### Patient remote care flow

1. Register as a patient.
2. Update the patient profile and emergency contact details.
3. Book an appointment with an active doctor.
4. Wait for the doctor to approve the appointment.
5. Submit health readings.
6. View alerts generated from abnormal readings.
7. Message the doctor.
8. View prescriptions and consultation notes.

### Doctor monitoring flow

1. Log in as a doctor.
2. View assigned appointments.
3. Approve, complete, or cancel appointments.
4. Open linked patient monitoring pages.
5. Review health readings and alert history.
6. Send messages to patients.
7. Add consultation notes and prescriptions.

### Admin management flow

1. Log in as the seeded admin.
2. Create and manage doctors.
3. View registered patients.
4. View appointments across the platform.
5. Review all alerts.
6. Use dashboard charts for a quick system overview.

## Screenshot Capture

The repository includes a screenshot helper:

```bash
npm run screenshots
```

It captures the main public, auth, admin, doctor, and patient pages. Screenshots are saved in two places:

```text
../Health Communication Screenshots
docs/screenshots
```

The parent folder is useful for your local project documentation archive. The `docs/screenshots` folder is included so GitHub can render images in this README.

If Chrome is installed in a non-default location, run:

```powershell
$env:CHROME_PATH="C:\Path\To\chrome.exe"
npm run screenshots
```

If your local server uses a different URL, run:

```powershell
$env:APP_SCREENSHOT_URL="http://localhost:8000"
npm run screenshots
```

## Testing

Run the test suite:

```bash
php artisan test
```

The project includes feature tests for:

- Authentication and password reset
- Role dashboard access
- Admin doctor management
- Patient profile management
- Appointment booking
- Health monitoring
- Automatic alert detection
- Doctor-patient messaging
- Prescriptions and consultation notes
- Final defense/demo flow

## Deployment Notes

For shared hosting or cPanel, point your domain or subdomain document root to Laravel's `public` folder.

Example:

```text
health.yourdomain.com -> /path-to-project/public
```

Your live `.env` should use the domain only:

```env
APP_URL=https://health.yourdomain.com
```

Do not add `/public` to `APP_URL`.

After uploading updated code, run:

```bash
php artisan down
composer install --no-dev --optimize-autoloader
npm ci
npm run build
php artisan migrate --force
php artisan optimize:clear
php artisan config:cache
php artisan route:cache
php artisan view:cache
php artisan up
```

## Security Notes

- Never commit `.env` or real credentials.
- Use HTTPS in production.
- Keep admin passwords strong and rotate demo passwords after deployment.
- Do not expose password values in forms, screenshots, or seed output.
- Use real SMTP credentials only on trusted environments.
- Keep dashboard routes protected by `auth` and role middleware.
- Review role permissions before adding new modules.
- Keep abnormal health alert rules transparent and easy to defend academically.

## Troubleshooting

### Forgot password email does not arrive

By default, local password reset emails are logged because `.env` uses:

```env
MAIL_MAILER=log
```

Check the Laravel log:

```text
storage/logs/laravel.log
```

Use SMTP credentials if you want real email delivery.

### Charts do not display

Rebuild frontend assets:

```bash
npm install
npm run build
php artisan optimize:clear
```

### The dashboard is empty

Run:

```bash
php artisan migrate --seed
```

Then log in with:

```text
admin@digitalhealth.test
password
```

### Screenshots fail to capture

Make sure the Laravel server is running:

```bash
php artisan serve
```

Then run:

```bash
npm run screenshots
```

If Chrome is not found, set `CHROME_PATH` as shown in the screenshot section.

### Old CSS or JavaScript still appears

Clear caches and hard refresh:

```bash
php artisan optimize:clear
npm run build
```

Then press:

```text
Ctrl + F5
```

## Repository Notes

For a clean GitHub repository:

- Commit the Laravel source files.
- Commit `docs/screenshots` if you want README screenshots to render on GitHub.
- Do not commit `vendor/`, `node_modules/`, `.env`, local database dumps, or cache files.
- Keep generated screenshots updated after major UI changes.
- Replace `YOUR_USERNAME` in the clone command before publishing.

## Contact

For project review, collaboration, or support, reach out at:

```text
mail.devtjames@gmail.com
```
