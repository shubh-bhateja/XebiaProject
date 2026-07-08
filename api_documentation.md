# Workforce API Documentation

This is a comprehensive list of all the API endpoints and features currently available in your backend. All routes are prefixed with `/api`.

---

## 🔐 Authentication (`/api/auth`)
Handles user logins, sessions, and password management.
- `POST /api/auth/login` - Authenticate a user and receive tokens.
- `POST /api/auth/refresh` - Refresh access tokens using a refresh token cookie.
- `POST /api/auth/logout` - Invalidate tokens and log the user out.
- `POST /api/auth/forgot-password` - Request a password reset link.
- `POST /api/auth/reset-password` - Reset password using a valid token.
- `POST /api/auth/change-password` - Change password while logged in.
- `GET /api/auth/profile` - Fetch the currently logged-in user's profile and employee data.

---

## 🏢 Organization (`/api/organization`)
Manages company structure.
- `GET /api/organization/departments` - List all departments.
- `POST /api/organization/departments` - Create a new department.
- `PUT /api/organization/departments/:id` - Update department details.
- `DELETE /api/organization/departments/:id` - Remove a department.

---

## 👥 Employees (`/api/employees`)
Employee record management.
- `GET /api/employees` - List all employees.
- `GET /api/employees/:id` - Get a specific employee's details.
- `POST /api/employees` - Register a new employee.
- `PUT /api/employees/:id` - Update employee details.
- `DELETE /api/employees/:id` - Remove an employee.

---

## 🕒 Attendance (`/api/attendance`)
Time tracking and presence.
- `GET /api/attendance/my` - View logged-in user's attendance records.
- `GET /api/attendance/team` - View team attendance (Manager/HR).
- `POST /api/attendance/clock-in` - Clock in for the day.
- `POST /api/attendance/clock-out` - Clock out for the day.
- `POST /api/attendance/correction` - Request attendance correction.
- `POST /api/attendance/correction/:id/review` - Approve or reject correction.

---

## 🌴 Leaves (`/api/leaves`)
Time off management.
- `GET /api/leaves/my` - View logged-in user's leave requests.
- `GET /api/leaves/pending` - View pending leave requests for approval.
- `POST /api/leaves/apply` - Submit a new leave request.
- `POST /api/leaves/review/:id` - Approve or reject a leave request.

---

## 💰 Payroll (`/api/payroll`)
Salary and compensation.
- `GET /api/payroll/history` - View payroll history.
- `POST /api/payroll/run` - Process/run payroll for a given month.

---

## 🎯 Projects & Tasks (`/api/projects`)
Work management.
- `GET /api/projects` - List all projects.
- `POST /api/projects` - Create a new project.
- `GET /api/projects/tasks` - View all tasks.
- `POST /api/projects/tasks` - Create a new task.
- `PUT /api/projects/tasks/:id` - Update task status/details.

---

## 📈 Performance (`/api/performance`)
Reviews and appraisals.
- `GET /api/performance` - View performance reviews.
- `POST /api/performance` - Create a new performance review.

---

## 🤝 Recruitment (`/api/recruitment`)
Hiring pipeline.
- `GET /api/recruitment/candidates` - View all job candidates.
- `POST /api/recruitment/candidates` - Add a new candidate.
- `PUT /api/recruitment/candidates/:id` - Update candidate status (e.g., offer letter).
- `POST /api/recruitment/candidates/:id/analyze-resume` - Use AI to analyze a candidate's resume and get a match score.

---

## 💻 Assets (`/api/assets`)
Inventory and hardware tracking.
- `GET /api/assets` - View all company assets (laptops, monitors, etc.).
- `POST /api/assets` - Add a new asset.
- `PUT /api/assets/:id` - Update asset assignment/status.

---

## 🎫 Tickets (`/api/tickets`)
IT and Support requests.
- `GET /api/tickets` - View all support tickets.
- `POST /api/tickets` - Raise a new support ticket.
- `PUT /api/tickets/:id` - Update ticket status (resolve, assign, etc.).

---

## 🤖 AI Assistant (`/api/ai`)
- `POST /api/ai/chat` - Chat with the Gemini-powered AI Assistant for workforce queries.

---

## 🩺 System (`/api`)
- `GET /api/health` - Health check endpoint to verify database connectivity and server uptime.
- `GET /` - Root endpoint indicating server is running.
