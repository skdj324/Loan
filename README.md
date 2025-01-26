# Loan Management System

A comprehensive loan management system with CIBIL and CRIF Highmark integration.

## Project Structure

```
loan/
├── .vscode/                  # VS Code configuration
├── assets/                   # Static assets (images, fonts)
├── backend/                  # PHP backend
│   ├── api/                 # API endpoints
│   ├── includes/            # Common includes
│   └── services/           # Business logic services
│       ├── CIBILService.php
│       ├── CRIFHighmarkService.php
│       ├── ICICIBankService.php
│       ├── KYCService.php
│       ├── RazorpayService.php
│       └── SMSService.php
├── css/                      # CSS styles
├── dashboard/               # Admin and user dashboards
│   ├── admin/              # Admin interface
│   └── user/               # User interface
├── database/               # Database related files
│   ├── migrations/        # Database migrations
│   ├── init.php          # Database initialization
│   └── schema.sql        # Database schema
├── frontend/              # Frontend components
├── js/                    # JavaScript files
├── modules/               # Reusable modules
├── composer.json          # PHP dependencies
├── database.sql          # Database dump
└── index.html            # Main entry point
```

## Features

- User Authentication and Authorization
- Loan Application Processing
- - CIBIL Report Generation
- CRIF Highmark Integration
- KYC Verification
- Payment Integration (Razorpay)
- SMS Notifications
- Admin Dashboard
- User Dashboard

## Setup Instructions

1. Clone the repository
2. Install PHP dependencies:
   ```bash
   composer install
   ```

3. Set up the database:
   ```bash
   mysql -u root -p < database/schema.sql
   ```

4. Configure environment variables:
   - Copy `.env.example` to `.env`
   - Update database credentials
   - Add API keys for services
   - 
5. Start the development server:
   ```bash
   php -S localhost:8000
   ```

## API Documentation

### Authentication
- POST `/api/auth/login`
- POST `/api/auth/register`
- POST `/api/auth/logout`

### Loan Management
- POST `/api/loan/apply`
- GET `/api/loan/status/{id}`
- GET `/api/loan/list`

### Reports
- GET `/api/reports/cibil/{user_id}`
- GET `/api/reports/crif/{user_id}`

### Admin Operations
- GET `/api/admin/loans`
- PUT `/api/admin/loan/approve/{id}`
- PUT `/api/admin/loan/reject/{id}`
- ## Security

- Input validation and sanitization
- CSRF protection
- XSS prevention
- Rate limiting
- SQL injection prevention
- Secure password hashing

## Dependencies

- PHP >= 7.4
- MySQL >= 5.7
- Composer
- Required PHP extensions:
  - PDO
  - mysqli
  - curl
  - json

## Contributing

1. Fork the repository
2. Create a feature branch4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
3. Commit your changes
