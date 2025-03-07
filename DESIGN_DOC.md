# Cat Clinic Tycoon – Design Document

## 1. Overview

**Objective:**  
Cat Clinic Tycoon is a comprehensive management application for veterinary practices built with Google Apps Script. The app integrates with Slack (free plan) and features an OpenAI helper to assist with in-app code modifications. The UI is inspired by the retro aesthetic of Roller Coaster Tycoon, making it both playful and user-friendly.

**Key Principles:**
- **Modularity:** Each module encapsulates related functionalities.
- **User Intuitiveness:** Clear navigation and comprehensive documentation for ease of use.
- **Scalability & Maintainability:** Version control with GitHub and a well-organized codebase.
- **Integration-Ready:** Seamless integration with Slack and external APIs (e.g., OpenAI).

---

## 2. Architecture Overview

**Technology Stack:**
- **Frontend/GUI:**  
  Built using Google Apps Script’s HTML Service with custom CSS/JavaScript to emulate a retro style.
- **Backend:**  
  Google Apps Script handles business logic and data processing. Data is primarily stored in Google Sheets.
- **Integrations:**  
  - **Slack:** For notifications, task capture, and dashboard updates.  
  - **OpenAI Helper:** Uses a "rosetta stone" file to interpret the project structure and assist with guided changes.
- **Version Control:**  
  Git and GitHub manage code revisions and branch organization.

**Data Flow:**
- Users interact with the GUI, which triggers Apps Script functions.
- Data operations are performed (e.g., updating employee records, scheduling appointments) and synced with Google Sheets.
- Notifications and task updates are sent to Slack.
- The OpenAI helper analyzes the project (using the rosetta stone file) to assist with maintenance and new feature implementation.

---

## 3. Module Breakdown

### A. Employee & HR Management
- **Employee Database:**  
  - CRUD operations for employee records (contact info, roles, certifications, etc.).
- **HR Functions & Onboarding:**  
  - Onboarding workflows and role-based access, with Slack notifications.
- **Attendance & Time Tracking:**  
  - Clock in/out functionality and automated alerts for policy violations.

### B. Operational & Management Functions
- **Appointment Whiteboard:**  
  - A visual, drag-and-drop scheduling interface for managing appointments.
- **Project & Meeting Management:**  
  - Scheduling meetings, managing tasks, and recording meeting notes.
- **Employee Training & Development:**  
  - Tracking training progress, 1-on-1 meetings, quarterly reviews, and professional development.

### C. Employee Engagement & Feedback
- **Internal Social Module:**  
  - Chat interface with kudos/high-fives and a badge system for gamification.
- **Feedback & Communication:**  
  - Tools for anonymous and non-anonymous feedback to management, with status tracking.

### D. Dashboard & User Interface
- **Customizable Dashboards:**  
  - Role-specific dashboards (for support staff and management) displaying tasks, reminders, and training updates.
- **Retro Aesthetic:**  
  - A UI design that pays homage to Roller Coaster Tycoon, balancing nostalgia with modern usability.

### E. Integrations & Advanced Features
- **Slack Integration:**  
  - Real-time notifications, task capture, and dashboard updates, complying with the Slack free plan.
- **OpenAI Helper Module:**  
  - Uses a rosetta stone file to understand the codebase and assist with modifications under restricted permissions.

---

## 4. Project Structure & Branching Strategy

**Folder Structure (current layout):**

Cat-Clinic-Tycoon/
├── DESIGN_DOC.md         # This design document
├── README.md             # Project overview and instructions
├── src/
│   ├── common/           # Shared utilities and configuration files
│   ├── modules/
│   │   ├── employeeManagement/   # Employee & HR Management module
│   │   │   └── main.gs
│   │   ├── appointmentWhiteboard/ # Appointment Whiteboard module
│   │   │   ├── main.gs
│   │   │   └── calendar.gs
│   │   ├── slackIntegration/      # Slack integration scripts
│   │   │   ├── main.gs
│   │   │   └── notifier.gs
│   │   ├── openaiHelper/          # OpenAI helper module
│   │   │   ├── main.gs
│   │   │   └── rosettaStone.gs
│   │   └── employeeTraining/      # Employee Training & Development module
│   │       ├── main.gs
│   │       └── progressTracker.gs
└── assets/              # CSS, images, and other static assets


**Branching Strategy:**
- Each module is developed on its own feature branch:
  - `feature/employee-management`
  - `feature/appointment-whiteboard`
  - `feature/slack-integration`
  - `feature/openai-helper`
  - `feature/employee-training`
- Branches are pushed to GitHub for isolated development and later merged into the main branch when complete.

---

## 5. Development Environment & Workflow

**Local Setup:**
- **Google Apps Script Integration:**  
  The project is linked to a Google Apps Script project using `clasp`. Use `clasp push` to update the online project and `clasp pull` to sync changes made online.
- **Code Editor:**  
  Visual Studio Code is set up with essential extensions (ESLint, Prettier, Markdown All in One, GitLens, GitHub integration) to improve productivity.
- **Git Workflow:**  
  Branches are managed locally with Git and pushed to GitHub, ensuring that feature development is isolated and versioned properly.

**Workflow:**
1. Edit locally in VS Code.
2. Commit changes on the appropriate feature branch.
3. Use `clasp` to synchronize the Apps Script project.
4. Merge and deploy changes as modules become complete and tested.

---

## 6. Progress Update

**Completed:**
- **Repository Setup:**  
  - GitHub repository established with a detailed README and this design document.
  - Feature branches for modules (Employee Management, Appointment Whiteboard, Slack Integration, OpenAI Helper, Employee Training) created.
  - Folder structure for each module implemented.

**Next Steps:**
- Develop and test core modules locally.
- Integrate Google Apps Script with the GitHub repository using `clasp`.
- Set up local development environment in Visual Studio Code with necessary extensions.
- Begin prototyping core functionality (e.g., Employee Management CRUD operations and Appointment Whiteboard interactions).

---

## 7. Future Considerations

- **Testing & Deployment:**  
  Develop testing procedures and automate deployment processes.
- **Documentation Updates:**  
  Continuously update this design document as new features and changes are implemented.
- **User Feedback:**  
  Incorporate feedback from real users to refine the modules and workflow.

