# Assignment II

## Overview of Tasks
This repository contains all tasks completed for the Oracle Pluggable Database Assignment II. The main objectives were:  

1. Create a new Pluggable Database (PDB) with a dedicated user.  
2. Create and delete a temporary PDB.  
3. Access Oracle Enterprise Manager (EM Express) to verify tasks.  
4. Document all work professionally with evidence for submission.

---

## Oracle Environment Used
- **Oracle Database Version:** 21c Express Edition (XE)  
- **SQL*Plus Version:** 21.0.0.0.0  
- **EM Express URL:** https://localhost:5500/em  
- **Operating System:** Windows 10

---

## Explanation of Each Task

### Task 1: Create a New PDB
- **PDB Name:** ha_pdb_27654 
- **User Created:** Happy_plsqlauca_27654 
- **Password:** Password123 (kept secure)  
- Steps:
  1. Connected to the container database (CDB) as SYSDBA in SQL*Plus.  
  2. Created the PDB using `CREATE PLUGGABLE DATABASE`.  
  3. Opened the PDB and verified it is in **OPEN** state.  
  4. Created a user inside the PDB and confirmed login.  
- **Screenshots:** `screenshots/pdb_creation.png`, `screenshots/pdb_open.png`, `screenshots/pdb_user.png`

### Task 2: Create and Delete a Temporary PDB
- **Temporary PDB Name:** ha_to_delete_pdb_2024101  
- Steps:
  1. Created the temporary PDB using `CREATE PLUGGABLE DATABASE`.  
  2. Verified its existence using `SELECT * FROM DBA_PDBS`.  
  3. Closed and deleted the PDB completely using `DROP PLUGGABLE DATABASE INCLUDING DATAFILES`.  
  4. Confirmed deletion from DBA_PDBS.  
- **Screenshots:** `screenshots/temp_pdb_creation.png`, `screenshots/temp_pdb_deletion.png`

### Task 3: Oracle Enterprise Manager (EM Express)
- Accessed EM Express in browser at https://localhost:5500/em.  
- Verified dashboard shows:
  - All created PDBs  
  - PDB status (OPEN)  
  - User inside PDB (`Happy_plsqlauca_2024101`)  
- **Screenshot:** `screenshots/em_dashboard.png`
  
---

## Challenges Faced
1. **OEM Access Issue:**  
   - The `emctl` command was not recognized in Windows.  
   - **Solution:** Used EM Express via browser at port 5500, which is built into Oracle 21c XE.  

2. **Ensuring Correct Naming Conventions:**  
   - Carefully followed assignment instructions for PDB and user names to avoid errors.

---

## Integrity Statement
I declare that all work presented in this repository is my own. Any assistance received has been acknowledged. All screenshots and evidence represent actual work performed in my Oracle environment.

✔ Repository is PUBLIC
✔ README is complete
✔ screenshots folder exists
✔ All screenshots are visible
✔ PDB name is correct: ha_pdb_27654
✔ Username correct: happy_plsqlauca_27654
