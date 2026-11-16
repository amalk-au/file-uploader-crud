# File Uploader CRUD

A personal file storage application inspired by platforms like Google Drive. Upload, organise, manage and download files through a web interface.

## Features

- **Authentication:** User authentication using Passport.js and local strategy.

- **Session Management:** Persistent sessions using Express Session and Prisma Session Store.

- **File Upload:** Upload files using Multer.

- **File Management:** View file details, including name, size and upload date.

- **File Downloads:** Download uploaded files.

- **Folder Management:** Create folders to organise uploaded files.

- **File Deletion:** Remove uploaded files and their database records.

## How It Works

The application uses Express.js to handle HTTP requests and EJS to render the user interface.

1.  **Authentication:** Passport.js authenticates users using their username and password. Express Session maintains their login state, with session data persisted in PostgreSQL through Prisma Session Store.

2.  **File Upload:** Multer handles file uploads using disk storage. Uploaded files are saved to the local filesystem, organised into folders.

3.  **Database:** Prisma ORM manages PostgreSQL operations. File metadata, including the original filename, generated filename, file path and size, is stored in the database.

4.  **File Management:** The application retrieves stored metadata to display uploaded files and their details. Users can download or delete files through the application.

5.  **Folder Organisation:** Folder information is stored in PostgreSQL and used to organise uploaded files.

## Screenshots

See [`docs/screenshots`](docs/screenshots/) for application screenshots.

## Tech Stack

- **Runtime:** Node.js

- **Backend:** Express.js

- **Database:** PostgreSQL

- **ORM:** Prisma

- **Authentication:** Passport.js, Passport Local

- **Session Management:** Express Session, Prisma Session Store

- **File Upload:** Multer

- **Templating:** EJS

- **Password Hashing:** bcryptjs

- **Validation:** Express Validator

- **Storage:** Local filesystem

## Getting Started

### Prerequisites

- Node.js

- NPM

- PostgreSQL

### Installation

1.  Clone the repository:

    ```
    git clone https://github.com/amalk-au/file-uploader-crud.git
    ```

2.  Navigate to the project directory:

    ```
    cd file-uploader-crud
    ```

3.  Install dependencies:

    ```
    npm install
    ```

4.  Create a `.env` file in the root directory:

    ```
    DATABASE_URL="your_postgresql_connection_string"
    SESSION_SECRET="your_session_secret"
    APP_PORT=3000
    HOME_FOLDER=uploads
    ```

5.  Generate the Prisma client:

    ```
    npx prisma generate
    ```

6.  Run database migrations:

    ```
    npx prisma migrate dev --name init
    ```

7.  Start the application:

    ```
    npm start
    ```

8.  Open your browser:

    ```
    http://localhost:3000
    ```

## Project Structure

```
file-uploader-crud/
├── controllers/       # Application controllers
├── db/                # Prisma database queries
├── docs/
│   └── screenshots/   # Application screenshots
├── prisma/            # Prisma schema and migrations
├── routes/            # Application routes
├── security/          # Authentication and session configuration
├── storage/           # Local file storage and Multer configuration
├── validators/        # Input validation
├── views/             # EJS templates
├── app.js             # Application entry point
├── package.json       # Dependencies and scripts
├── package-lock.json
├── LICENSE
└── README.md
```

## Future Improvements

- Implement user registration.

- Associate files and folders with individual users.

- Implement file and folder renaming.

- Implement moving files between folders.

- Improve file upload validation and error handling.

- Integrate cloud storage using Supabase or Cloudinary.

- Improve file and folder management functionality.

## License

This project is licensed under the GNU General Public License v3.0 (GPL-3.0). See the [LICENSE](LICENSE) file for details.

## Author

**Amal K.**

- GitHub: [@amalk-au](https://github.com/amalk-au)

- Portfolio: [amalk.au](https://www.amalk.au)

- Repository: [file-uploader-crud](https://github.com/amalk-au/file-uploader-crud)
