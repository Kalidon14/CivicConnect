
---

# **CivicConnect – Smart City Issue Reporter**

## **Overview**

CivicConnect is a web platform for citizens to report city issues (potholes, trash, streetlights, etc.) and for staff to manage and resolve them. Features include geo-tagging, upvoting issues, and staff audit trails for accountability.

---

## **Tech Stack**

* **Frontend:** HTML, Tailwind CSS, Vue.js, Axios
* **Map:** Leaflet.js + OpenStreetMap
* **Backend:** PHP (vanilla)
* **Database:** MySQL
* **Storage:** Local folder or baka cloud

---

## **Features**

### Citizen

* Report issues with description, category, photo, and geo-location.
* Upvote issues to prioritize them.
* Track status of reported issues.

### Staff

* View and filter reported issues by status or upvotes.
* Update status: Pending → In Progress → Resolved.
* Audit trail logs staff actions.

---

## **Database Tables**

1. **users:** `id, name, email, password_hash, role`
2. **issues:** `id, title, description, category, latitude, longitude, photo_path, reported_by, timestamp, status`
3. **upvotes:** `id, user_id, issue_id, timestamp`
4. **audit_trail:** `id, issue_id, staff_id, old_status, new_status, timestamp`

---

## **Setup**

1. Clone repo:

```bash
git clone https://github.com/yourusername/CivicConnect.git
```

2. Create MySQL database `civicconnect`.
3. Import `database.sql` with all tables.
4. Update `backend/config.php` with DB credentials.
5. Run via local server (XAMPP).
6. Open in browser: `http://localhost/CivicConnect/`.

---

## **Folder Structure**

```
add lang maya
```

---

## **Usage Workflow**

1. Citizen registers/login → reports issue → pin on map → optional photo.
2. Citizens upvote existing issues → issues get prioritized.
3. Staff views issues → updates status → audit trail recorded.
4. Citizens track issue resolution.

---

## **Future Enhancements**

* Cloud storage for images.
* Push notifications for status updates.
* Analytics dashboard for staff.
* Mobile-friendly responsive UI.

---

## **License**

MIT License – Free for personal and academic use.

---

