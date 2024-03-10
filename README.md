# FileXpress

This is a server-rendered file sharing application built with the Express.js framework, EJS (Embedded JavaScript templates), and MongoDB. It allows you to share files without the need to create an account. Download links will expire 24 hours after being shared for the first time.

## Live Demo

[FileXpress](http://filexpress.ap-south-1.elasticbeanstalk.com/)

## Features

- **No Account Required**: Share files without the hassle of creating an account.
- **Lossless Photo Sharing**: Share photos without compression.
- **File History**: Admins can view all uploaded files by visiting `/uploaded-files`. A high security code will be required.
- **File Cleanup**: Files older than 24 hours can be deleted by visiting the `/uploaded-files`.
- **QR Code Generation**: A QR code is displayed to allow file downloading.
- **Email Sharing**: Send emails with the file link, or simply copy the link and share it with them.

## Getting Started

To get the application up and running, follow these steps:

1. Clone the repository:

   ```CLI
   git clone https://github.com/hssaluja25/FileXpress
   ```

2. Install dependencies:

   ```CLI
   npm install
   ```

3. Set up the required environment variables (e.g., MongoDB connection string, port, etc.) in a `.env` file.

   ```.env
   PORT=3000
   MONGODB_CONNECTION_URL='lorem-ipsum'
   APP_BASE_URL='http://localhost:3000'
   HIGH_SECURITY_CODE='lorem-ipsum'
   SMTP_HOST='smtp.gmail.com'
   SMTP_PORT=587
   MAIL_USER='example@gmail.com'
   MAIL_PASSWORD='lorem ipsum'
   ```

4. Start the server: `npm run dev`
5. Access the application in your web browser at `http://localhost:PORT` (replace `PORT` with the port number specified in your environment variables).

## Usage

1. Visit the application in your web browser.
2. Click the "Upload File" button and select the file you want to share.
3. Once the file is uploaded, you will see the upload link and a QR code.
4. Copy the upload link and share it, or send an email with the link.
5. The recipient can use the link or scan the QR code to download the shared file.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
