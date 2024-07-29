# Tact-Connect


# Tact-Connect (Web Chat Application)

Tact-Connect is a web chat application designed to enhance communication through real-time messaging, integrated email functionality, and scheduled messaging. It leverages modern web technologies to provide a seamless and user-friendly experience.

## Features

- **Real-time Messaging**: Users can send and receive messages instantly.
- **Email Integration**: Users can send emails directly from within the app.
- **Scheduled Messaging**: Users can schedule messages for future delivery using PHP cron jobs.

## Technologies Used

- **Frontend**: HTML, CSS, JavaScript
- **Backend**: PHP
- **Database**: MySQL
- **Email Integration**: PHP mail function or third-party email service API 
- **Scheduled Messaging**: PHP cron jobs

## Installation

### Prerequisites

- PHP 7.4 or higher
- MySQL
- Composer (PHP package manager)
- A web server (e.g., Apache, Nginx)

### Clone the Repository

```bash
git clone https://github.com/yourusername/tact-connect.git
cd tact-connect
```

### Install Dependencies

```bash
composer install
```

### Set Up the Database

1. Create a new MySQL database named `tact_connect`.
2. Import the `tact_connect.sql` file located in the `database` directory to set up the necessary tables.
3. Configure your database settings in the `.env` file:
   ```
   DB_HOST=localhost
   DB_NAME=tact_connect
   DB_USER=your_username
   DB_PASS=your_password
   ```

### Configure Email Settings

In the `.env` file, set up your email configuration:

```
MAIL_HOST=smtp.yourmailprovider.com
MAIL_PORT=587
MAIL_USERNAME=your_email@example.com
MAIL_PASSWORD=your_email_password
MAIL_ENCRYPTION=tls
MAIL_FROM_ADDRESS=your_email@example.com
MAIL_FROM_NAME="Tact-Connect"
```

### Set Up Scheduled Messaging

1. Open your terminal and type `crontab -e` to edit the cron jobs.
2. Add the following line to schedule the `send_scheduled_messages.php` script to run every minute:
   ```
   * * * * * /usr/bin/php /path/to/tact-connect/scripts/send_scheduled_messages.php
   ```

### Run the Application

1. Start your web server.
2. Open your browser and go to `http://localhost/tact-connect`.

## Usage

- **Real-time Messaging**: Log in and start a chat with other users. Messages will be delivered instantly.
- **Email Integration**: Use the integrated email feature to send emails from within the app.
- **Scheduled Messaging**: Schedule messages for future delivery by selecting the desired time and date.

## Contributing

We welcome contributions! Please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License.

