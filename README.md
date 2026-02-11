### **Overview**

The **Scarlet Template Automator** is a specialized PowerShell utility designed to manage the `report_template.txt` file used within the SybylineNetwork/Scarlet ecosystem. It allows administrators to schedule automated content swaps—such as adding event-specific information— without manual intervention or the need to modify application source code.

### **Key Features**

* **Dynamic Scheduling:** Automatically switches between "Standard" and "Special Event" moderation templates based on dates defined in an external configuration file.
* **User-Agnostic Deployment:** Utilizes Windows environment variables to automatically detect and target the correct local AppData path regardless of the logged-in user.
* **Self-Healing Loop:** Runs as a background process that re-verifies the file integrity every 60 seconds, ensuring manual edits by users do not break the template standard.
* **Modular Design:** Separates logic (PowerShell), schedule (Text), and content (Text), allowing non-technical coordinators to update report text or dates easily.

### **Repository Structure**

* `UpdateTemplate.ps1`: The core logic engine.
* `Install_Shortcut.bat`: Automated deployment script for Windows Startup integration.
* `config.txt`: The scheduling interface (Start/End dates).
* `template_standard.txt`: The default report content.
* `template_special.txt`: The promotional/event report content.

### **Installation**

1. Clone the repository to a local directory in C:/.
2. Configure your dates in `config.txt`.
3. Run `Install_Shortcut.bat` to enable persistence on boot.

### **PLEASE MAKE SURE YOU READ THE READ ME.TXT FILE!**
