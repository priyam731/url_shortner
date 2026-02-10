# URL Shortener Service

Simple, maintainable backend for shortening links and tracking clicks.

## The Tech Stack

- **Node.js & Express**: Core server framework.
- **MongoDB**: Database for users, URLs, and analytics.
- **EJS**: Server-side rendering (keeps the frontend simple).
- **Auth**: Custom in-memory session management.

## Key Implementation Notes

- **Architecture**: Standard MVC pattern (Models, Views, Controllers).
- **Authentication**:
  - Uses `service/auth.js` to map session IDs to users.
  - _Note_: This is in-memory only. Restarting the server wipes active sessions.
  - _Scaling_: If we scale to multiple instances, we'll need to move this state to Redis.

## Quick Start

1.  **Database**: Ensure a local MongoDB instance is running.
2.  **Install**:
    ```bash
    npm install
    ```
3.  **Run**:
    ```bash
    npm start
    ```
4.  **Access**: Server runs on port `8001` by default.
