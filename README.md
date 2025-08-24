# 🜂 Grimoire Street • Specialties Tracker

This tracker powers the **Specialties Availability (Students Only)** table and the **Student Roster** on your site.
It automatically loads data from `tracker.json` in this repository and updates whenever you commit changes.

> **Important:** The tracker **only tracks students** (Years 1–7 in a Hogwarts House).
> **Adults are uncapped and not tracked**—they do not appear in counts or the roster.

---

## 📂 Files in This Repo

```
specialities/
 ├─ tracker.json   ← Main data file (edit this for student roster changes)
 ├─ index.html     ← Tracker webpage (reads tracker.json automatically)
 └─ README.md      ← This guide
```

---

## 📝 Adding a New Student

1. Open **`tracker.json`** in GitHub.
2. Click the **pencil icon** (Edit).
3. Scroll to the bottom (before the closing `]`).
4. Copy the template below and paste it on a **new line**:

```json
{
  "specialty": "Parselmouth",
  "character": "Full Name Here",
  "house": "Gryffindor",
  "year": "1",
  "player": "@DiscordName#0000",
  "status": "Approved",
  "app": "https://link.to/application",
  "notes": "Optional notes here"
}
```

5. Update the fields:

| Field     | Type   | Allowed Values                                                                                                | Notes                       |
| --------- | ------ | ------------------------------------------------------------------------------------------------------------- | --------------------------- |
| specialty | string | Parselmouth, Occlumens, Legilimens, Seer, Metamorphmagus, Blood Curse Bearer, Obscurial, Wandless Magic Adept | Must match exactly          |
| character | string | Any full name                                                                                                 | Student’s full name         |
| house     | string | Gryffindor, Hufflepuff, Ravenclaw, Slytherin                                                                  | Students must be in a House |
| year      | string | `"1"`–`"7"`                                                                                                   | Students only               |
| player    | string | Discord handle like `@Name#1234`                                                                              |                             |
| status    | string | Approved, Pending, On Hiatus, Retired, Deceased                                                               |                             |
| app       | string | URL to application/profile                                                                                    |                             |
| notes     | string | Any extra info (optional)                                                                                     |                             |

6. **Add a comma** `,` **after the block** unless it’s the last entry.
7. Click **Commit changes** to save.

---

## 🚫 Adults Are Not Tracked

* Adults are **uncapped** and **excluded** from this tracker’s counts and roster.
* If you include adults in `tracker.json`, they will be **ignored** by the page because they are not students.

---

## ✏️ Editing a Student

* Find the student’s `{ ... }` block in `tracker.json`.
* Change any values (name, status, year, etc.).
* Click **Commit changes**.

---

## ❌ Removing a Student

* Delete the student’s `{ ... }` block.
* Keep commas correct:

  * Every entry **except the last** needs a comma after the closing brace `}`.
  * The last entry must **not** have a trailing comma.

---

## 📄 JSON Template (Copy & Paste)

Use this when adding a new **student**:

```json
[
  {
    "specialty": "Parselmouth",
    "character": "Full Name Here",
    "house": "Gryffindor",
    "year": "1",
    "player": "@DiscordName#0000",
    "status": "Approved",
    "app": "https://link.to/application",
    "notes": "Optional notes here"
  }
]
```

> When adding multiple students, copy just the inner `{ ... }` block and paste it on a new line above the closing `]`, adding commas between entries.

---

## ✅ Example with Two Students

```json
[
  {
    "specialty": "Parselmouth",
    "character": "Ivy Blackthorne",
    "house": "Slytherin",
    "year": "5",
    "player": "@PlayerOne",
    "status": "Approved",
    "app": "https://link.to/app1",
    "notes": "Known for keeping snakes in the dorms"
  },
  {
    "specialty": "Seer",
    "character": "Alaric Moon",
    "house": "Ravenclaw",
    "year": "6",
    "player": "@PlayerTwo",
    "status": "Pending",
    "app": "https://link.to/app2",
    "notes": "Has visions during thunderstorms"
  }
]
```

---

## ⚠️ Common Mistakes

* **Missing commas** — every entry except the last needs a trailing comma.
* **Wrong quotes** — JSON requires `"double quotes"` for all strings.
* **Specialty typos** — must match exactly (e.g., `Parselmouth`, not `parselmouth`).
* **Non-student entries** — adults won’t appear in the tracker; only include students you want shown.

---

## 🔄 Live Updates

* After you **Commit changes** to `tracker.json`, the tracker webpage shows the new data after a refresh.
* No changes to `index.html` are needed.
