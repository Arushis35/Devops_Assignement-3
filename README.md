# Devops_Assignement-3
# 🖥️ Linux User & Group Management (System Administration Task)

## 📌 Overview
This project demonstrates basic Linux system administration tasks, including:

- System auditing  
- User management  
- Group management  
- Employee onboarding simulation  

It is useful for beginners learning Linux administration or preparing for DevOps roles.

---

## ⚙️ Part 1: Initial System Audit

These commands help gather system and user-related information.

```bash
# Check user identity (UID, GID, groups)
id

# Display current username
whoami

# Show logged-in users
who

# Show user activity
w

# View login history
last

# Display system information
uname -a

# Show hostname
hostname

# Check system uptime
uptime
```

---

## 👥 Part 2: Department Setup

Creating groups to represent departments.

```bash
# Create developers group
sudo groupadd developers

# Create QA group
sudo groupadd qa

# Verify groups
grep -E 'developers|qa' /etc/group

# Display all groups
cat /etc/group
```

---

## 👨‍💻 Part 3: Employee Onboarding

Simulating onboarding of employees into different departments.

```bash
# Create users and assign groups
sudo useradd -m -G developers aman
sudo useradd -m -G developers ritu
sudo useradd -m -G qa karan

# Set passwords
sudo passwd aman
sudo passwd ritu
sudo passwd karan

# Verify users
id aman
id ritu
id karan

# Check group members
getent group developers
getent group qa
```

---

## 📂 Project Structure

```
.
├── README.md
└── scripts/
    └── user_group_setup.sh (optional)
```

---

## 🚀 How to Use

1. Clone the repository:
```bash
git clone https://github.com/your-username/your-repo-name.git
```

2. Navigate into the project:
```bash
cd your-repo-name
```

3. Run commands manually or via script:
```bash
bash user_group_setup.sh
```

---

## ⚠️ Notes

- Requires sudo/root privileges  
- Tested on Linux distributions like Ubuntu  
- Ensure you understand each command before running  

---

## 🎯 Learning Outcomes

- Understand Linux user and group management  
- Learn system auditing commands  
- Practice basic administrative tasks  
- Simulate real-world onboarding process  

---

## 📜 License
This project is for educational purposes only.
