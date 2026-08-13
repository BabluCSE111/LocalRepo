# INT251 – Malware Analysis and Cyber Defence

## Session 1 – Introduction to Malware (Concise Notes)

### Malware

**Definition:** Malware (Malicious Software) is software designed to damage systems, steal data, disrupt operations, or gain unauthorized access.

---

## Characteristics of Malware

* Performs unauthorized actions.
* Harms systems or users.
* Can spread through files, networks, emails, or downloads.
* May steal, modify, encrypt, or delete data.

---

## Objectives of Malware

* Steal sensitive information.
* Damage or destroy data.
* Disrupt system operations.
* Gain unauthorized access.
* Spy on user activities.
* Demand ransom.

---

## Common Infection Sources

* Email attachments
* Pirated software
* Malicious websites
* USB/Pen drives
* Software vulnerabilities
* Fake applications

---

## Malware vs Benign Software

| Malware                   | Benign Software    |
| ------------------------- | ------------------ |
| Malicious purpose         | Legitimate purpose |
| Damages systems           | Helps users        |
| Unauthorized actions      | Authorized actions |
| May steal or destroy data | Does not harm data |

---

## Basic Malware Lifecycle

1. Infection
2. Activation (Execution)
3. Replication (if applicable)
4. Payload (Malicious action)

---

## Examples of Malware

* Virus
* Worm
* Trojan Horse
* Ransomware
* Spyware
* Keylogger

---

## Prevention Methods

* Install antivirus software.
* Keep software updated.
* Avoid unknown email attachments.
* Download software from trusted sources.
* Use strong passwords.
* Regularly back up important data.

---

## One-Line Revision

* **Malware** → Malicious software.
* **Benign Software** → Legitimate software.
* **Objective** → Steal, damage, disrupt, or spy.
* **Infection Sources** → Email, USB, Internet, pirated software.
* **Prevention** → Antivirus, updates, safe browsing, backups.
# INT251 – Malware Analysis and Cyber Defence

## Session 2 – Types of Malware (Concise Notes)

### Malware

Malware is malicious software designed to damage systems, steal data, or gain unauthorized access.

---

## 1. Virus

**Definition:** Malware that attaches to a host file and becomes active only when the infected file is executed.

**Key Points**

* Needs a host file.
* Requires user execution.
* Infects other files.
* Performs a malicious payload.

**Memory:** Virus = Host

---

## 2. Worm

**Definition:** Self-replicating malware that spreads automatically through networks without a host file or user execution.

**Key Points**

* No host file required.
* Self-replicating.
* Spreads through networks.
* Infects multiple computers quickly.

**Memory:** Worm = Network

---

## 3. Trojan Horse

**Definition:** Malware disguised as legitimate software to trick users into installing it.

**Key Points**

* Appears legitimate.
* Requires user installation.
* Does not self-replicate.
* Often creates a backdoor.

**Memory:** Trojan = Fake Software

---

## 4. Ransomware

**Definition:** Malware that encrypts files and demands payment for decryption.

**Key Points**

* Encrypts files.
* Demands ransom.
* Blocks access to data.

**Memory:** Ransomware = Encrypt + Money

---

## 5. Spyware

**Definition:** Malware that secretly monitors user activities and steals information.

**Key Points**

* Steals personal information.
* Monitors user activity.
* Runs secretly.

**Memory:** Spyware = Watch

---

## 6. Keylogger

**Definition:** A type of spyware that records every keystroke.

**Key Points**

* Records keyboard input.
* Steals usernames and passwords.
* Operates secretly.

**Memory:** Keylogger = Record Keys

---

## Virus vs Worm

| Virus              | Worm              |
| ------------------ | ----------------- |
| Needs host file    | No host file      |
| Requires execution | No execution      |
| Infects files      | Infects computers |
| Slower spread      | Faster spread     |

---

## One-Line Revision

* Virus → Host file
* Worm → Self-replicating
* Trojan → Fake software
* Ransomware → Encrypts files
* Spyware → Steals information
* Keylogger → Records keystrokes
# INT251 – Malware Analysis and Cyber Defence

## Session 3 – Malware Classification, Virus & Worm (Concise Notes)

### Malware Classification

**Definition:** Malware classification is the process of grouping malware based on its **behavior, infection method, propagation (spreading method), and purpose**.

**Why is it needed?**

* Helps identify malware.
* Helps choose the correct detection and removal method.
* Improves incident response.

---

# Virus

## Definition

A **virus** is malware that attaches to a **host file or program** and becomes active only when the infected host is executed.

## Characteristics

* Requires a host file.
* Requires user execution.
* Replicates by infecting other files.
* Performs a malicious payload.

## Virus Life Cycle

Host File
↓
Execution
↓
Replication
↓
Payload

## Key Terms

* **Host:** File or program carrying the virus.
* **Execution:** Running the infected file.
* **Replication:** Copying itself to other files.
* **Payload:** Harmful action (delete, modify, encrypt files, etc.).

**Memory:** **HERP**

* H – Host
* E – Execution
* R – Replication
* P – Payload

---

# Worm

## Definition

A **worm** is a standalone, self-replicating malware that spreads automatically through networks without requiring a host file or user execution.

## Characteristics

* No host file required.
* No user execution required.
* Self-replicating.
* Scans networks for vulnerable computers.
* Spreads very quickly.

## Worm Working

Infect Computer
↓
Scan Network
↓
Find Vulnerable Systems
↓
Copy Itself
↓
Repeat

---

# Virus vs Worm

| Virus                | Worm                               |
| -------------------- | ---------------------------------- |
| Needs host file      | No host file                       |
| Needs user execution | No user execution                  |
| Infects files        | Infects computers through networks |
| Slower spread        | Faster spread                      |
| Dependent on host    | Standalone program                 |

---

# One-Line Revision

* **Malware Classification** → Grouping malware by behavior and spreading method.
* **Virus** → Host file + Execution.
* **Worm** → Standalone + Self-replicating + Network spreading.
* **Replication** → Copying itself.
* **Payload** → Harmful action after activation.
* **Golden Rule:** **Virus = Host | Worm = Network**
## Static Analysis — Information Collected

**Static Analysis = Do not run the sample → Collect and examine its information.**

- **SHA-256** → File fingerprint.
- **MZ** → PE file signature.
- **Entropy** → Measures randomness of the file/section.
- **PE Headers** → Information about the file structure.
- **`.text`** → Executable code/instructions.
- **`.data`** → Writable data/variables.
- **`.rdata`** → Read-only data.
- **`.rsrc`** → Resources such as icons and version information.
- **Strings** → Readable text found inside the file.
- **Imports/Exports** → APIs/functions used or provided by the file.
- **Metadata** → Basic file information.

### 🧠 Remember

> **Static Analysis = Don't Run → Collect Information → Understand the Sample**
