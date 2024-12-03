# CBP Programmer API Scripts

This repository provides scripts for working with **CBP Programmer APIs**, in two configurations:  
1. **BPMicro SOCA Mode**  
2. **Client SOCA Mode**

The scripts facilitate socket management, device placement, and site handling based on the chosen SOCA mode.

## Overview of SOCA Modes

### 1. **BPMicro SOCA Mode (Default)**  
     In this mode, the BPWin application automatically manages the opening and closing of sockets.  
   - **Behavior:**  
     - The methods `SiteOpened` and `SiteClosed` are no-ops (do nothing).  
     - Events `NotifyOpenSite` and `NotifyCloseSite` are not raised.  
---
### 2. **Client SOCA Mode**  
     In this mode, the client’s mechanical handler system controls socket operations.  
   - **Behavior:**  
     - The CBpProgrammer object raises events (`NotifyOpenSite`, `NotifyCloseSite`) to prompt socket operations.  
     - The client responds by calling methods (`SiteOpened`, `SiteClosed`) to confirm socket status.  
---

## Features

- **Supports two SOCA modes**: BPMicro SOCA and Client SOCA.  
- **Automates device placement and picking** based on socket status.
- **Simulates idle event loop** for handling socket events such as opening and closing sites, and placing or picking devices.

---
