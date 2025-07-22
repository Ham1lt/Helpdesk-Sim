# 🖥️ Helpdesk Simulation Project

This hands-on project simulates the role of an IT Helpdesk Technician by setting up a virtual support environment using **Active Directory** on a Windows Server EC2 instance and managing tickets through **ServiceNow**. The goal was to walk through everyday helpdesk scenarios in a realistic cloud-based lab.

---

## 🚀 What This Project Covers

In this simulation, I recreated a typical helpdesk workflow by:

- Launching a **Windows Server** on AWS EC2
- Installing and configuring **Active Directory Domain Services (AD DS)**
- Setting up a free **ServiceNow Developer Instance** for ticketing
- Performing common helpdesk operations:
  - Creating and managing user accounts
  - Resetting user passwords
  - Managing security groups
  - Handling user incidents and access requests via ServiceNow

This lab was designed to help me understand how real-world helpdesk environments function—especially in hybrid cloud setups.

---

## ☁️ EC2 + Windows Server Setup

### ✅ Step 1: Launch the EC2 Instance

- Used AWS Console to launch a **Windows Server 2019 Base** instance
- Instance type: `t3.xlarge` (4 vCPU, 16 GB RAM)
- Opened RDP (port 3389) and generated a key pair for remote access

### ✅ Step 2: Initial Configurations

- Connected to the instance via Remote Desktop (RDP)
- Renamed the computer to `windows` for easier AD management
- Assigned a static private IP address via AWS settings

---

## 🧱 Active Directory Configuration

### 🔧 Installing AD DS

- Installed **Active Directory Domain Services (AD DS)** through Server Manager
- Promoted the instance to a Domain Controller
- Created a new forest and domain: `livetest.local`

### 🔍 DNS Setup

- Verified DNS setup automatically during the AD installation
- Ensured forward and reverse lookup zones were created and working

---

## 👤 Active Directory Helpdesk Tasks

### 👥 User Management

- Created user accounts in **Active Directory Users and Computers (ADUC)**
- Example user: `Trey Brown`, with email and login credentials

### 🔐 Group Management

- Created a security group: `LiveTestGroup`
- Added users to groups for basic access control and group policy management

### 🔄 Password Reset

- Simulated password resets as part of day-to-day user support
- Enabled “Password never expires” for demonstration purposes

---

## 🧾 ServiceNow Integration

### 🧪 Developer Instance Setup

- Registered for a free **ServiceNow Developer Instance**
- Activated the **ITSM** (IT Service Management) application

### 🛠️ Incident Simulation

Created sample tickets for:

- User account lockouts
- Password reset requests
- Access requests (e.g., shared folders)

Each ticket included:

- User context and description of the issue
- Action taken (e.g., unlocked user, reset password, group assignment)

---

## 📸 Screenshots (Optional)

You can include screenshots in a `/screenshots` folder to visualize:

- User creation in ADUC
- Group memberships
- Sample ServiceNow tickets and resolution workflows

---

## ✅ Project Outcomes

By completing this lab, I:

- Practiced provisioning and managing cloud-hosted Windows servers
- Set up and administered a functional Active Directory environment
- Handled realistic IT helpdesk scenarios from both the technical and ticketing side

This project helped reinforce my ability to manage users and solve issues—core responsibilities for support and system admin roles.

---

## 🔗 Resources Used

- [AWS EC2 Documentation](https://docs.aws.amazon.com/ec2/)
- [Microsoft Active Directory Documentation](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/)
- [ServiceNow Developer Portal](https://developer.servicenow.com/)

---

## 🎥 Demo Videos

- [Video 1: AD Setup Walkthrough](https://www.loom.com/share/2d24aa2e4e0f4127af02a07ed65c7a30?sid=2539a6ef-4331-46f8-9a09-9e0f76eeb1fb)
- [Video 2: ServiceNow Ticket Creation](https://www.loom.com/share/20a10c0458a54a298af613110afe8f48?sid=a027b5be-f0f3-4c02-9a94-80c7d9598981)
- [Video 3: Helpdesk Scenarios](https://www.loom.com/share/a9a53f1251064b6696ed969b2e2bf708?sid=2830ab68-7144-4a7c-88c3-488618e8bd86)
