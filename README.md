# Smart Traffic Fine Management System (STFMS)

A comprehensive web-based traffic fine management system designed for Sri Lanka's traffic police department. This system streamlines the process of issuing, managing, and paying traffic fines through a modern, user-friendly interface.

## 🚀 Project Overview

The Smart Traffic Fine Management System is a full-stack web application that digitizes the traditional traffic fine management process. It provides separate interfaces for different user roles including Traffic Police Officers, Drivers, Administrators, and Motor Traffic Department officials.

### Key Features
- **Multi-role Authentication System** - Separate dashboards for different user types
- **Real-time Fine Issuance** - Traffic officers can issue fines instantly
- **Online Payment Processing** - Drivers can pay fines online
- **Comprehensive Analytics** - Detailed reports and charts for all stakeholders
- **Revenue License Verification** - Integration with vehicle registration data
- **Past Fine History** - Complete driver violation history tracking
- **Responsive Design** - Works seamlessly on desktop and mobile devices

## 🛠️ Tech Stack

### Backend Technologies
- **PHP 8.0+** - Server-side scripting language
- **MySQL/MariaDB** - Relational database management
- **Apache/Nginx** - Web server

### Frontend Technologies
- **HTML5** - Markup language
- **CSS3** - Styling with custom animations
- **JavaScript (ES6+)** - Client-side functionality
- **Bootstrap 4** - Responsive UI framework
- **Chart.js** - Data visualization and analytics
- **Font Awesome** - Icon library
- **jQuery** - DOM manipulation and AJAX

### Development Tools
- **phpMyAdmin** - Database administration
- **Git** - Version control
- **XAMPP/WAMP** - Local development environment

## 📊 Database Schema

The system uses a well-structured MySQL database with the following main tables:

### Core Tables
- **`admins`** - System administrators
- **`driver`** - Driver information and credentials
- **`tpo`** - Traffic Police Officers
- **`mtd`** - Motor Traffic Department officials
- **`issued_fines`** - Fine tickets issued to drivers
- **`fine_tickets`** - Available fine provisions and amounts
- **`revenue_license`** - Vehicle registration data

### Key Relationships
- Foreign key constraints between `issued_fines` and `driver`/`tpo` tables
- Unique constraints on email addresses and license IDs
- Auto-incrementing primary keys for efficient data management

## 🏗️ System Architecture

### User Roles & Permissions

#### 1. **Traffic Police Officer (TPO)**
- Issue new traffic fines
- Search driver information
- View past fines issued by the officer
- Check revenue license validity
- View reported fines dashboard

#### 2. **Driver**
- View pending and paid fines
- Make online payments
- Access fine history and analytics
- Update profile information
- View provision details

#### 3. **Administrator**
- Manage traffic police officers
- View system-wide analytics
- Manage fine provisions
- Monitor all issued fines
- Access comprehensive reports

#### 4. **Motor Traffic Department (MTD)**
- Register new drivers
- Manage driver database
- View registration statistics
- Access driver information

### System Workflow

1. **Fine Issuance Process**
   - Traffic officer logs into the system
   - Searches for driver by license ID
   - Selects appropriate fine provision
   - Issues fine with location and court details
   - System generates unique reference number

2. **Payment Process**
   - Driver receives notification of fine
   - Logs into driver portal
   - Views pending fines
   - Processes online payment
   - Receives payment confirmation

3. **Administrative Oversight**
   - Real-time monitoring of all activities
   - Comprehensive reporting and analytics
   - User management and system configuration

## 🚀 Installation & Setup

### Prerequisites
- PHP 8.0 or higher
- MySQL 5.7+ or MariaDB 10.3+
- Apache/Nginx web server
- XAMPP/WAMP (for local development)

### Installation Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/smart-traffic-fine-management-system.git
   cd smart-traffic-fine-management-system
   ```

2. **Database Setup**
   - Import the `stfms.sql` file into your MySQL database
   - Create a database named `stfms`
   - Update database credentials in `connection.php`

3. **Configure Database Connection**
   ```php
   // Update connection.php with your database details
   $dbhost = "localhost";
   $dbuser = "your_username";
   $dbpassword = "your_password";
   $dbname = "stfms";
   ```

4. **Web Server Configuration**
   - Place the project files in your web server's document root
   - Ensure PHP extensions are enabled (mysqli, session, etc.)
   - Configure virtual host if needed

5. **Access the Application**
   - Navigate to `http://localhost/smart-traffic-fine-management-system`
   - Use the provided sample login credentials

### Sample Login Credentials

| Role | Email | Password |
|------|-------|----------|
| Traffic Police Admin | stfmssample@gmail.com | cha123456 |
| Motor Traffic Department | stfmssample@gmail.com | cha123456 |
| Traffic Police Officer | stfmssample@gmail.com | cha123456 |
| Driver | stfmssample@gmail.com | cha123456 |

## 📱 Features in Detail

### Dashboard Analytics
- **Real-time Statistics** - Live counters for fines, users, and revenue
- **Interactive Charts** - Monthly trends, payment status, and user activity
- **Role-specific Views** - Customized dashboards for each user type

### Fine Management
- **Automated Fine Calculation** - Pre-configured fine amounts based on violations
- **Reference Number Generation** - Unique tracking for each issued fine
- **Status Tracking** - Real-time updates on payment status
- **Court Integration** - Automatic court date assignment

### Payment System
- **Online Payment Processing** - Secure payment gateway integration
- **Payment History** - Complete transaction records
- **Receipt Generation** - Digital payment confirmations
- **Multiple Payment Methods** - Support for various payment options

### User Management
- **Role-based Access Control** - Secure authentication and authorization
- **Profile Management** - User information updates and password changes
- **Session Management** - Secure login/logout functionality
- **Password Recovery** - Email-based password reset system

## 🔒 Security Features

- **Password Encryption** - MD5 hashing for stored passwords
- **Session Management** - Secure PHP sessions with proper validation
- **SQL Injection Prevention** - Prepared statements and input validation
- **Access Control** - Role-based permissions and authentication
- **Data Validation** - Server-side and client-side input validation

## 📊 Analytics & Reporting

### Available Reports
- **Monthly Fine Statistics** - Trends and patterns in fine issuance
- **Payment Analytics** - Revenue tracking and payment success rates
- **User Activity Reports** - Registration and usage statistics
- **Officer Performance** - Individual officer fine issuance metrics

### Data Visualization
- **Interactive Charts** - Bar charts, line graphs, and doughnut charts
- **Real-time Updates** - Live data refresh without page reload
- **Export Capabilities** - Data export for external analysis
- **Custom Date Ranges** - Flexible reporting periods

## 🎨 User Interface

### Design Principles
- **Responsive Design** - Mobile-first approach with Bootstrap framework
- **Modern UI/UX** - Clean, intuitive interface design
- **Accessibility** - WCAG compliant design elements
- **Cross-browser Compatibility** - Works on all major browsers

### Key UI Components
- **Dashboard Cards** - Information-rich display components
- **Data Tables** - Sortable and searchable data presentation
- **Modal Dialogs** - Interactive forms and confirmations
- **Navigation Menus** - Role-based navigation structure

## 🚀 Future Enhancements

### Planned Features
- **Mobile Application** - Native iOS and Android apps
- **SMS Notifications** - Automated fine notifications via SMS
- **QR Code Integration** - Quick fine lookup using QR codes
- **API Development** - RESTful API for third-party integrations
- **Advanced Analytics** - Machine learning-based insights
- **Multi-language Support** - Sinhala and Tamil language support

### Technical Improvements
- **Framework Migration** - Upgrade to modern PHP frameworks (Laravel/CodeIgniter)
- **Database Optimization** - Query optimization and indexing
- **Caching Implementation** - Redis/Memcached for improved performance
- **Microservices Architecture** - Scalable service-oriented design

## 🤝 Contributing

We welcome contributions to improve the Smart Traffic Fine Management System. Please follow these guidelines:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Guidelines
- Follow PSR-12 coding standards for PHP
- Write meaningful commit messages
- Add comments for complex logic
- Test your changes thoroughly
- Update documentation as needed

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Team

- **Project Lead** - [Your Name]
- **Backend Development** - [Developer Name]
- **Frontend Development** - [Developer Name]
- **Database Design** - [Developer Name]
- **UI/UX Design** - [Designer Name]

## 📞 Support

For support and inquiries:
- **Email**: stfms@gmail.com
- **Phone**: +94 714590249
- **Documentation**: [Help Guide](help.php)

## 🙏 Acknowledgments

- Uva Wellassa University for project support
- Sri Lanka Police Department for requirements and feedback
- Open source community for various libraries and frameworks
- Contributors and testers who helped improve the system

---

**Note**: This system is designed specifically for Sri Lanka's traffic management requirements and follows local regulations and procedures. For deployment in other countries, appropriate modifications to fine amounts, legal provisions, and administrative processes would be required.
