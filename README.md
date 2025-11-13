#  User Management Simulation Script

A lightweight Bash script that simulates the creation of Linux user accounts and group assignments based on a structured input file. Ideal for testing automation logic without modifying the actual system.

---

##  Input Format

The script reads from a file named `users.txt`, where each line follows this format:
Developer onboarding list
light; sudo,dev,www-data Madhu; sudo kumar; dev,www-data

- Lines starting with `#` are treated as comments and ignored.
- Whitespace is automatically stripped.
- Each user is assigned a simulated password and group list.

---

.
├── user_management.sh       # Main Bash script
├── users.txt                # Input file with user data
├── secure/
│   └── user_passwords.txt   # Generated passwords (auto-created)
├── logs/
│   └── user_management.log  # Log of simulated actions (auto-created)
└── README.md                # This file


##  Features

- Parses usernames and group memberships from a text file
- Simulates user creation (no real system changes)
- Generates secure 12-character random passwords
- Logs all actions to `./logs/user_management.log`
- Saves credentials to `./secure/user_passwords.txt`
- Creates secure local directories for logs and credentials

---

## Usage

Make the script executable:

chmod +x user_management.sh


Create and populate the users.txt file:

Example:

# Sample users
light; sudo,dev,www-data
Madhu; sudo
kumar; dev,www-data


Run the script:

sudo bash create_user.sh


Check outputs:

Passwords → ./secure/user_passwords.txt

Logs → ./logs/user_management.log


 Security Notes
- Passwords and logs are stored with 600 permissions for privacy.
- This script does not create real users or groups — it is safe for testing.
- Ideal for validating input formats and automation logic before deploying a production script.





---




