# Cat Clinic Tycoon

**Cat Clinic Tycoon** is a comprehensive management application designed for veterinary practices. Built using Google Apps Script, it integrates seamlessly with Slack (using the free plan) and includes an OpenAI helper to assist with in-app guidance and code adjustments. The app features a playful, retro GUI inspired by the original Roller Coaster Tycoon game.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

Cat Clinic Tycoon is designed to streamline operations at a veterinary medical practice by offering a suite of integrated modules, including:

- Employee Database & HR Management
- Standard Operating Procedures (SOP) Development & Management
- Onboarding, Attendance, and Time Tracking
- Appointment Flow Whiteboard with drag-and-drop scheduling
- Employee Training & Development Tracking
- Project, Meeting, and Feedback Management
- Internal Social and Engagement Tools (e.g., kudos, badges)
- Customizable Dashboards for staff and management
- Slack integration for notifications, task capture, and dashboard updates
- OpenAI helper integration for context-aware assistance and code modifications

---

## Features

- **Employee & HR Management:**  
  CRUD operations for employee records, onboarding workflows, role-based access, and attendance tracking.

- **Operational Modules:**  
  Visual appointment management, project and meeting scheduling, and detailed SOP management.

- **Employee Engagement:**  
  Internal chat/social features, gamification through badges, and streamlined feedback channels.

- **Dashboard & UI:**  
  Custom dashboards tailored for different roles with a nostalgic Roller Coaster Tycoon aesthetic.

- **Integrations:**  
  Slack (free version) for real-time notifications and task management, plus an OpenAI helper for guided code updates.

---

## Technology Stack

- **Frontend/GUI:**  
  Google Apps Script HTML Service (with custom CSS and JavaScript).

- **Backend:**  
  Google Apps Script, with data stored in Google Sheets (or another supported database).

- **Integrations:**  
  - **Slack:** For notifications, task capture, and dashboard updates.
  - **OpenAI Helper:** Provides in-app guidance using a "rosetta stone" file to understand the app's structure.

- **Version Control & Documentation:**  
  GitHub for code hosting, version control, and maintaining the project documentation.

---

## Getting Started

### Prerequisites

- A Google account to use Google Apps Script and Google Sheets.
- A GitHub account for version control.
- Access to Slack (free plan) for integration testing.

### Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/your-username/Cat-Clinic-Tycoon.git
   cd Cat-Clinic-Tycoon

2. **Set Up Google Apps Script:**

   - Open Google Apps Script (https://script.google.com/).
   - Create a new project and link it to your GitHub repository if desired.
   - Copy the code from the repository into your Apps Script project.

3. **Configure Slack Integration:**

   - Review the integration settings in the code.
   - Add your Slack webhook or API tokens as necessary, ensuring they conform to the free plan's limitations.

4. **Run Initial Setup Scripts:**

   - Execute the initial setup functions in the Apps Script environment to configure your database and settings.

---

## Project Structure

```
Cat-Clinic-Tycoon/
├── DESIGN_DOC.md         # Comprehensive design document outlining app architecture, modules, and roadmap.
├── README.md             # This file.
├── src/                  # Source code for the Google Apps Script project.
│   ├── main.gs           # Main Apps Script file.
│   ├── employeeManager.gs# Employee & HR Management module.
│   ├── appointments.gs   # Appointment Flow Whiteboard module.
│   ├── slackIntegration.gs # Slack integration scripts.
│   ├── openaiHelper.gs   # OpenAI Helper integration.
│   └── ...               # Additional modules as needed.
└── assets/               # Images, CSS, and other static assets.
```

---

## Documentation

- **Design Document:**  
  Refer to [DESIGN_DOC.md](https://github.com/annamintz30/Cat-Clinic-Tycoon/blob/main/DESIGN_DOC.md) for detailed design notes, module breakdown, and the project roadmap.

- **Update Workflow:**  
  This project uses GitHub for version control. Regular commits and updates to both the code and design document will ensure that new features and improvements are tracked over time.

---

## Contributing

Contributions are welcome! Please follow these guidelines:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Submit a pull request with a detailed description of your changes.
4. Update the design document if your changes affect the overall architecture or functionality.

---

## License

[MIT License](LICENSE)

---

Happy coding and have fun building Cat Clinic Tycoon!
```

---

This README provides a clear overview of the project, its features, and guidance on getting started. You can update it as the project evolves and refer back to it each time you update the design document or add new modules.
