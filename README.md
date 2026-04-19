# PES-VCS: Version Control System Report

**Name:** Surya Naik

**SRN:** PES2UG24CS540

**Section:** I

**Course:** Operating Systems (Unit 4 – Orange Program Assignment)

---

##  Project Overview

**PES-VCS** is a specialized version control system built from scratch in C. It implements core Git concepts like content-addressable storage, trees, staging (index), and commit history. The project demonstrates OS-level concepts such as file handling, atomic writes, and filesystem organization.

---

##  Phase 1: Object Storage

* Implemented `object_write` and `object_read`
* Stored objects using SHA-256 hash
* Used directory sharding (`.pes/objects/xx/...`)
* Ensured atomic writes using temp file + rename

###  Screenshots

![Phase1-1](screenshots/Phase1/1a.jpeg)
![Phase1-2](screenshots/Phase1/1b.jpeg)

---

##  Phase 2: Tree Objects

* Implemented `tree_from_index`
* Converted flat index → hierarchical structure
* Stored directory structure as tree objects

###  Screenshots

![Phase2-1](screenshots/Phase2/2a.jpeg)
![Phase2-2](screenshots/Phase2/2b.jpeg)

---

##  Phase 3: Index (Staging Area)

* Implemented `index_add`, `index_load`, `index_save`
* Stored file metadata in `.pes/index`
* Managed staging area like Git

###  Screenshots

![Phase3-1](screenshots/Phase3/3a.jpeg)
![Phase3-2](screenshots/Phase3/3b.jpeg)

---

##  Phase 4: Commit System

* Implemented `commit_create`
* Stored commit metadata (author, message, parent)
* Updated HEAD atomically

###  Screenshots

![Phase4-1](screenshots/Phase4/4a.jpeg)
![Phase4-2](screenshots/Phase4/4b.jpeg)
![Phase4-3](screenshots/Phase4/4c.jpeg)

---

##  Final Integration

* Integrated all modules into `pes` command
* Verified complete workflow using test script

###  Screenshots

![Final-1](screenshots/Final/final1.jpeg)
![Final-2](screenshots/Final/final2.jpeg)

---

##  Conclusion

This project helped understand:

* How Git works internally
* File system operations in OS
* Data integrity using hashing
* Version control design

---

##  Status

✔ Phase 1 completed
✔ Phase 2 completed
✔ Phase 3 completed
✔ Phase 4 completed
✔ Final integration successful

---

##  Commands Used

```bash
make all
./test_objects
./test_tree
./test_sequence.sh
```

---
