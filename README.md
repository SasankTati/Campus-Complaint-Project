MRU Campus Complaint Management System

A front-end prototype of a campus complaint portal for Malla Reddy University. Students file complaints, department staff resolve them, and admins monitor everything. It is a single index.html file with no build step and no dependencies.

Status: prototype. Data is stored in the browser (localStorage), so nothing is shared between devices yet.

Features

Core

Complaint form with category, description, location (block, floor, room) and photo attachment
Unique ticket ID and status tracking: Submitted, In Progress, Resolved
Role-based access: student, department staff, admin
Account creation and sign-in with a university ID or email
Auto-routing of each complaint to the right department
Priority levels (Low, Medium, High) and anonymous filing
Staff and admin dashboard to assign, update and reroute tickets

Workflow

Comment thread between student and handler
In-app notifications, plus simulated SMS/WhatsApp alerts
Auto-escalation when a ticket passes its deadline (High 1 day, Medium 3, Low 7)
Student feedback rating after resolution
Search and filter by status and category
"Me too" votes and duplicate detection

Admin and extras

Analytics: complaints per category, average resolution time, average rating
Audit log sealed with a hash chain (blockchain-style tamper check)
CSV copy and PDF export (browser print)
English, Telugu and Hindi interface
Dark mode, mobile-friendly layout, FAQ, public feed
Points and badges for students
Keyword-based auto-categorization and voice dictation
Run it

Open index.html in any modern browser. No server needed.

Quick demo: use the Student, Staff or Admin buttons on the sign-in screen. Students can also create their own account.

In the admin view, Simulate +3 days moves the clock forward so you can see auto-escalation.

Deploy with GitHub Pages
Push this repository to GitHub.
Go to Settings > Pages.
Under Build and deployment, choose Deploy from a branch, select main and / (root), then save.
After a minute, the site is live at https://<your-username>.github.io/<repo-name>/.
Known limitations
Data lives only in the visitor's browser.
Passwords use a simple hash, which is fine for a demo but not secure.
Staff and admin accounts are demo-only; a real system would have admins issue them.
SMS/WhatsApp, voice and categorization features are simplified stand-ins.
Telugu and Hindi translations should be reviewed by native speakers.
Roadmap
Backend and database (for example Node.js with PostgreSQL, or Firebase)
Real authentication with university email verification
Real email and SMS notifications
Cross-device data and shared complaints
Proper PDF and Excel export



## License

MIT. See [LICENSE](LICENSE).
