
Questions:
1. what is the current react version using
2. useMemo difference b/w v16 and v19 react versions?
#  User Management Assignment
## Frontend Requirements

### 1. Tech Stack

- Use **React + TypeScript**. 

### 2. User Input Form

- Display a form at the **top of the page**.
- The form must contain:
    - **Name** (text input, required)
    - **Email** (email input, required, must be valid)
- Provide an **Add User / Create** button.

### 3. Form Behavior

- On submit:
    - Call the backend API to create a user.
    - On success:
        - Add the user to the table.
        - Clear the form.
    - On failure:
        - Show appropriate validation or error messages. 

Done
### 4. Users Table

- Display a table **below the form**.
- Table columns:
    - **Name**
    - **Email**
    - **Actions**
- Each row represents a single user.

### 5. Actions Column

For each user row, provide the following actions:

- **Edit**
    - Allow updating the user’s name and/or email.
    - Editing can be done via:
        - Inline editing, or
        - Reusing the form (prefill values).
    - Save changes by calling the backend API.
- **Delete**
    - Remove the user.
    - Optional: show a confirmation prompt before deleting.
    - Must call the backend API before removing from UI.

### 6. General Frontend Expectations

- Users must be created **only via the form**.
- Handle loading and error states.
- Use clean, readable code and proper state management.

## Backend Requirements (Simple)

### 1. Tech Stack

- Use **Node.js + Express + TypeScript**.

### 2. API Endpoints

- **POST** `**/users**`
    - Create a user.
    - Validate required fields and email format.
- **GET** `**/users**`
    - Return all users.
- **PUT** `**/users/:id**`
    - Update a user’s name and/or email.
- **DELETE** `**/users/:id**`
    - Delete a user by ID.

### 3. Data & Responses

- Data can be stored **in-memory** (no database required).
- All responses must be in **JSON** format.

### 4. General Backend Expectations

- Enable **CORS** for frontend access.
- Handle basic validation and errors.


#  round 2: 

React + Typescript  assignment 


question 1: 
```
type a = 1 | 2 | 3 
type b = "test"
```
output should be:
```
c = 1-test | 2-test | 3-test
```

question 2: 



## User Management Assignment

## Frontend Requirements
c = 1-test | 2-test | 3-test
### 1. Tech Stack

- Use **React + TypeScript**.

### 2. User Input Form

- Display a form at the **top of the page**.
- The form must contain:
    - **Name** (text input, required)
    - **Email** (email input, required, must be valid)
- Provide an **Add User / Create** button.

### 3. On Submit - Handle validations and add the user to the table. Optionally show success or error states.

### 4. Users Table

- Display a table **below the form**.
- Table columns:
    - **Name**
    - **Email**
    - **Actions**
- Each row represents a single user.

### 5. Actions Column

For each user row, provide the following actions:

- **Edit**
    - Allow updating the user’s name and/or email.
    - Editing can be done via:
        - Inline editing, or
        - Reusing the form (prefill values).
    - Save changes by calling the backend API.
- **Delete**
    - Remove the user.
    - Optional: show a confirmation prompt before deleting.
    - Must call the backend API before removing from UI.

### 6. General Frontend Expectations

- Users must be created **only via the form**.
- Handle loading and error states.
- Use clean, readable code and proper state management.


