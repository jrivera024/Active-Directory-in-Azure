# Active-Directory-in-Azure

## Lab Set Up

1. Create Virtual Network & Subnet

2. Create Domain Controller (DC-1)
  - VM Name: DC-1
  - OS: Windows Server 2022
  - Username: labuser
  - Password: Cyberlab123!
    
    <img width="411" height="165" alt="image" src="https://github.com/user-attachments/assets/5d31def1-c66d-4d07-a4e5-babb34a6adb4" />

**Post-Deployment:**
  - Set DC-1’s NIC Private IP Address to Static (in Azure Portal).

    <img width="555" height="453" alt="image" src="https://github.com/user-attachments/assets/1b93c17b-7cae-4d54-b9c0-08827d32afd6" />

  - Log into DC-1 via RDP.
  - Disable Windows Firewall (for testing connectivity only)

    <img width="378" height="453" alt="image" src="https://github.com/user-attachments/assets/08b0f97b-17aa-446b-a2e6-595e0c0b6540" />

    
3. Create Client VM (Client-1)
  - VM Name: Client-1
  - OS: Windows 10
  - Username: labuser
  - Password: Cyberlab123!
**Post-Deployment:**
  - Set Client-1’s DNS settings to point to DC-1’s Private IP Address.
  - Azure Portal → Client-1 NIC → DNS → Custom → Enter DC-1’s private IP.

    <img width="507" height="393" alt="image" src="https://github.com/user-attachments/assets/871e4fa5-32dc-4293-97ac-83b433ae5570" />

  - Restart Client-1 from Azure Portal.
      
4. Test Connectivity
  - Log into Client-1.
  - Open Command Prompt / PowerShell.
  - Run:
    - ping <DC-1 private IP> Ping should succeed.
  - Run:
    - ipconfig /all DNS settings should show DC-1’s private IP address.
   
<img width="600" height="628" alt="image" src="https://github.com/user-attachments/assets/e6ab83f4-e1a0-421e-a1ad-0a84e7092837" />

---




