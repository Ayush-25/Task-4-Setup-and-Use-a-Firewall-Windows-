# Firewall Configuration — Cyber Security Internship Task 4
*Setting up and testing basic firewall rules on a Windows system*

## Objective
Configure and test basic firewall rules to allow or block traffic. This task helps develop awareness of network traffic filtering, firewall rule creation, and testing system security controls.

## Tools Used
- **Windows Defender Firewall with Advanced Security**  
- **PowerShell (for command-line rule management)**  
- Target: Local PC (`127.0.*.1`)  

## Methodology and Steps

**Step 1:** Opened Windows Defender Firewall with Advanced Security and verified inbound rules.
*Screenshot:*
<img width="1297" height="635" alt="Screenshot 2025-09-26 151633" src="https://github.com/user-attachments/assets/f6b94445-c9fb-4d3c-94e2-ecf2377e15ce" />


**Step 2:** Listed current firewall rules:
*Screenshot:*
<img width="1296" height="496" alt="Screenshot 2025-09-26 151701" src="https://github.com/user-attachments/assets/07ddbe8d-2be6-431f-9655-45d0039b30b5" />


**Step 3:** Added rule to block inbound traffic on TCP port 23 (Telnet).  
GUI Steps: Inbound Rules → New Rule → Port → TCP → Specific Local Port: 23 → Next → Block the connection → Next → Apply to Domain, Private, Public → Next → Name: `Block_Telnet` → Finish  
PowerShell Alternative:
*Screenshot:*
<img width="1296" height="413" alt="Screenshot 2025-09-26 152115" src="https://github.com/user-attachments/assets/fb2223be-5bed-4ace-8954-a4d50d69e1a7" />


**Step 4:** Tested the rule:  
Installed Telnet client if needed:  
Telnet connection failed, confirming firewall block.  
*Screenshot:*  
<img width="935" height="448" alt="Screenshot 2025-09-26 152537" src="https://github.com/user-attachments/assets/10715224-b48e-42a2-b35a-2e0961be9fa1" />


**Step 5:** Added rule to allow SSH (TCP port 22).  
GUI Steps: Inbound Rules → New Rule → Port → TCP → Specific Local Port: 22 → Next → Allow the connection → Next → Apply to Domain, Private, Public → Next → Name: `Allow_SSH` → Finish  
PowerShell Alternative:
*Screenshot:*  
<img width="891" height="311" alt="Screenshot 2025-09-26 153025" src="https://github.com/user-attachments/assets/0d1eeb6b-1e8b-4dd7-a59d-abec5d2c89eb" />


**Step 6:** Removed test block rule to restore original state.  
GUI Steps: Right-click `Block_Telnet` → Delete  
PowerShell Alternative:
*Screenshot:*  
<img width="889" height="406" alt="Screenshot 2025-09-26 153240" src="https://github.com/user-attachments/assets/2cb65f41-70c5-4f78-b029-9790c9cd0593" />

**Step 7:** Documented commands used:

**Step 8:** Summarized how firewall filters traffic:  
A firewall filters network traffic based on rules defined by the user or system. Inbound rules control traffic entering the system; outbound rules control traffic leaving it. Rules can filter by port number, protocol (TCP/UDP), IP address, or application. Blocking Telnet (port 23) prevented unauthorized incoming connections. Allowing SSH (port 22) permitted secure access. Removing the test rule restored the original state, demonstrating how firewalls allow only authorized traffic and block unauthorized access.

## Summary of Findings

| Rule Applied               | Port | Action | Result                         |
|----------------------------|------|--------|--------------------------------|
| Block_Telnet               | 23   | Block  | Telnet connections blocked     |
| Allow_SSH                  | 22   | Allow  | SSH connections allowed        |
| Remove Block_Telnet        | 23   | N/A    | Restored original state        |

## Recommended Actions
1. Configure firewall rules for critical ports based on system role.  
2. Regularly review and update firewall rules to match security policies.  
3. Test firewall rules to ensure unauthorized access is blocked.  
4. Document all changes and maintain screenshots for audit purposes.

## Files Included for GitHub Submission
- `README.md` → this documentation 

## Conclusion
Task demonstrated how to:  
- Create, test, and remove firewall rules on a Windows system  
- Block unauthorized services (Telnet) and allow authorized access (SSH)  
- Understand firewall filtering logic and network traffic management  

**Practical skills gained:** firewall configuration, rule testing, traffic filtering understanding, PowerShell-based firewall management.

## Contact
**Ayush Singh**  
Email: ayushsinghfeb2502@gmail.com

