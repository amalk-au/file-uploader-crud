# File Uploader CRUD

A personal file storage application inspired by platforms like Google Drive. Upload, organise, manage and download files and folders through a web interface.

**Live Demo:**[File Uploader CRUD](https://nodejs-file-uploader-crud.onrender.com)

## Features

- **Authentication:** Session-based authentication using Passport.js.

- **Session Persistence:** Store user sessions in PostgreSQL using Prisma Session Store.

- **File Upload:** Upload files using Multer middleware.

- **Folder Management:** Create and organise folders.

- **File Details:** View file metadata, including name, size and upload timestamp.

- **File Downloads:** Download uploaded files.

- **File Storage:** Store uploaded files on the local filesystem.

- **Database:** Store file metadata, user information and sessions using PostgreSQL.

## Screenshots

Screenshots of the application are available in [`docs/screenshots`](docs/screenshots/).

## Tech Stack

- **Backend:** Node.js, Express.js

- **Database:** PostgreSQL

- **ORM:** Prisma

- **Authentication:** Passport.js, Passport Local

- **Session Management:** Express Session, Prisma Session Store

- **File Upload:** Multer

- **Password Hashing:** bcryptjs

- **Templating Engine:** EJS

- **Validation:** Express Validator

- **File Storage:** Local filesystem

- **Cloud Storage:** Supabase Storage (planned integration)

## Getting Started

### Prerequisites

- Node.js

- NPM

- PostgreSQL database

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

**Note:** User registration is not currently implemented. An existing user record is required to authenticate.

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
├── storage/           # File upload and storage configuration
├── validators/        # Input validation
├── views/             # EJS templates
├── app.js             # Application entry point
├── package.json       # Dependencies and scripts
├── package-lock.json
├── LICENSE
└── README.md
```

## Future Improvements

The following features are planned or require further development:

- Implement user registration.

- Associate files and folders with individual users.

- Implement file renaming.

- Implement folder renaming.

- Implement moving files between folders.

- Integrate cloud storage using Supabase Storage or another cloud storage provider.

- Improve file and folder management functionality.

## License

This project is licensed under the GNU General Public License v3.0 (GPL-3.0). See the [LICENSE](LICENSE) file for details.

## Author

**Amal K.**

- GitHub: [@amalk-au](https://github.com/amalk-au)

- Portfolio: [amalk.au](https://www.amalk.au)

- Repository: [file-uploader-crud](https://github.com/amalk-au/file-uploader-crud)
