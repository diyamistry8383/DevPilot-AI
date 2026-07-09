# DevPilot AI – Database Design

---

# 1. Database Overview

DevPilot AI uses PostgreSQL as the primary relational database.

The database is designed using normalization principles to avoid redundancy while maintaining scalability.

The system supports multiple organizations, teams, projects, sprints, AI modules, and future integrations.

---

# 2. Main Entities

- Users
- Organizations
- Teams
- Projects
- Sprints
- Tasks
- Task Comments
- AI Chats
- Reports
- Notifications
- Skills
- Resume
- Learning Recommendations
- Integrations
- Audit Logs

---

# 3. Users Table

Stores all registered users.

Fields

- id
- full_name
- email
- password
- role
- profile_image
- designation
- department
- experience
- created_at
- updated_at

---

# 4. Organizations Table

Stores company information.

Fields

- id
- organization_name
- address
- website
- created_at

---

# 5. Teams Table

Stores engineering teams.

Fields

- id
- organization_id
- team_name
- manager_id
- description

---

# 6. Projects Table

Stores software projects.

Fields

- id
- project_name
- description
- team_id
- start_date
- end_date
- status

---

# 7. Sprints Table

Fields

- id
- project_id
- sprint_name
- sprint_goal
- start_date
- end_date
- status

---

# 8. Tasks Table

Fields

- id
- sprint_id
- assigned_to
- title
- description
- priority
- story_points
- status
- due_date
- estimated_hours
- actual_hours

---

# 9. AI Chats Table

Stores AI conversations.

Fields

- id
- user_id
- prompt
- response
- model
- created_at

---

# 10. Resume Table

Stores AI generated resumes.

Fields

- id
- user_id
- resume_version
- ats_score
- generated_file
- generated_at

---

# 11. Learning Recommendation Table

Fields

- id
- user_id
- skill
- recommendation
- source
- completed

---

# 12. Reports Table

Fields

- id
- report_name
- report_type
- generated_by
- generated_at

---

# 13. Notifications Table

Fields

- id
- user_id
- title
- message
- type
- is_read

---

# 14. Integrations Table

Fields

- id
- integration_name
- api_key
- status

---

# 15. Audit Logs

Stores all important activities.

Fields

- id
- user_id
- activity
- created_at

---

# 16. Entity Relationships

Organization

↓

Teams

↓

Projects

↓

Sprints

↓

Tasks

↓

Reports

Users

↓

AI Chats

↓

Resume

↓

Learning Recommendation

↓

Notifications

---

# 17. Future Database Extensions

- GitHub Repository Data
- Slack Messages
- AI Embeddings
- Knowledge Base
- Meeting Notes
- AI Memory