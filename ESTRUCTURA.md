# ESTRUCTURA.md

## Project Structure for Recoconstructora MX

### Frontend Folder Organization
- **src/**: Source files for the frontend application.
  - **components/**: Reusable UI components.
  - **pages/**: Page components that represent different routes.
  - **assets/**: Static assets such as images and styles.
  - **hooks/**: Custom React hooks.

### Backend Folder Organization
- **src/**: Source files for the backend application.
  - **controllers/**: Business logic controllers.
  - **models/**: Data models and schema definitions.
  - **routes/**: API route definitions.
  - **middlewares/**: Custom middleware functions.
  - **config/**: Configuration files.

### Database Tables Description
1. **Users**: Stores user information.
   - id: Integer, Primary Key
   - username: String, Unique
   - password: String
   - role_id: Integer, Foreign Key

2. **Roles**: Defines user roles.
   - id: Integer, Primary Key
   - name: String

3. **Permissions**: Defines permissions for roles.
   - id: Integer, Primary Key
   - name: String

4. **Projects**: Stores project details.
   - id: Integer, Primary Key
   - name: String
   - description: Text

### Role and Permissions Matrix
| Role       | Permission  |
|------------|-------------|
| Admin      | All permissions |
| User       | Create, Read, Update |
| Guest      | Read only   |

### Deployment Instructions
1. Clone the repository: `git clone <repo-url>`.
2. Navigate to the project directory.
3. Install dependencies:
   ```bash
   npm install
   ```
4. Set up environment variables.
5. Start the server:
   ```bash
   npm start
   ```

### Security Features
- JWT Authentication for secure user sessions.
- Input validation and sanitization to prevent SQL Injection.
- HTTPS support for secure data transmission.

### Main Features List
- User authentication and authorization.
- Project management functionalities.
- Real-time notifications for project updates.
- Role-based access control (RBAC).