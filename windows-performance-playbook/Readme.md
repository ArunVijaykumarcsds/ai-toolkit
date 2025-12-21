# Windows Performance Optimization Guide
## PowerShell & CMD Commands for System Health

![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D6?style=flat&logo=windows)
![PowerShell](https://img.shields.io/badge/PowerShell-5.1%2B-5391FE?style=flat&logo=powershell)
![License](https://img.shields.io/badge/License-Educational-green)

---

## 📚 Introduction

### Why Does Windows Performance Degrade Over Time?

Your Windows PC doesn't slow down because it's "getting old." Performance degradation happens due to several technical reasons:

- **Fragmented files** — Files split across your hard drive, increasing read/write time
- **Corrupted system files** — Windows updates, crashes, or malware can damage critical system files
- **Temporary file buildup** — Apps create thousands of temporary files that never get cleaned
- **Disk errors** — Bad sectors and file system errors accumulate on drives
- **Background processes** — Apps you installed months ago still run in the background
- **Power plan misconfiguration** — Your PC might be running in power-saving mode when it doesn't need to

### How PowerShell and CMD Help

Windows includes powerful built-in command-line tools that can:

- Scan and repair corrupted system files
- Check disk integrity and fix errors
- Remove gigabytes of temporary files
- Analyze power consumption
- Defragment and optimize drives
- Identify resource-hogging processes

**The best part?** These tools are free, native to Windows, and don't require third-party software that might install bloatware or charge subscription fees.

---

## 👥 Who Should Use This Guide

### Students
If you're using an older laptop for school and it's become frustratingly slow, these commands can help you recover performance without buying new hardware.

### Developers
Running IDEs, virtual machines, and build tools taxes your system. Regular maintenance using these commands keeps your development environment responsive.

### Low-End PC Users
Got a budget laptop with 4GB RAM and a slow HDD? These optimization techniques can make a significant difference in daily usability.

### IT Support & Tech Learners
Whether you're studying for CompTIA A+ or helping family with tech issues, understanding these commands is essential for Windows troubleshooting.

---

## ⏰ When Should You Use Performance Commands?

Recognize these symptoms? It's time to optimize your system:

### Slow Boot Times
- **Symptom**: Windows takes 5+ minutes to reach the desktop
- **Likely Cause**: Corrupted startup files, disk errors, or fragmented system files
- **Solution**: Run `chkdsk`, `sfc`, and `DISM` commands

### Disk Errors & Warnings
- **Symptom**: "Windows detected a hard disk problem" notifications
- **Likely Cause**: Bad sectors or file system corruption
- **Solution**: Run `chkdsk /f /r` to scan and repair

### Application Freezing
- **Symptom**: Programs frequently stop responding or crash
- **Likely Cause**: Corrupted system libraries, RAM issues, or disk errors
- **Solution**: Run `sfc /scannow` and check memory usage

### Low Disk Space (Despite Cleanup)
- **Symptom**: "Low Disk Space" warning even after deleting files
- **Likely Cause**: Hidden temp files, old Windows updates, or system restore points
- **Solution**: Use `cleanmgr` and `DISM` cleanup commands

### General Sluggishness
- **Symptom**: Everything just feels slower than it used to
- **Likely Cause**: Multiple factors — fragmentation, temp files, background processes
- **Solution**: Follow the complete workflow in this guide

---

## 🔧 Core Performance Commands

### 1. `chkdsk /f /r`

**What It Does**  
Check Disk (chkdsk) scans your hard drive for file system errors and physical disk problems. The `/f` flag fixes file system errors, while `/r` locates bad sectors and recovers readable information.

**When to Use It**
- After unexpected shutdowns or crashes
- When you see disk error messages
- Before formatting or major system changes
- If files are corrupting or disappearing randomly

**Why It Improves Performance**  
File system errors force Windows to retry read/write operations multiple times, causing delays. Bad sectors make the disk head work harder to locate data. By fixing these issues, chkdsk ensures your disk operates at optimal speed.

**How to Use**
```cmd
chkdsk C: /f /r
```

**Important Notes:**
- Requires Administrator privileges
- Needs to schedule on reboot (type `Y` when prompted)
- Can take 1-5 hours on large drives
- Your PC will restart and run the scan before Windows loads

**Safety Level:** ⚠️ **Safe** — Read-only analysis with repair options. Does not delete user files.

---

### 2. `cleanmgr`

**What It Does**  
Disk Cleanup Manager (cleanmgr) removes temporary files, system cache, old Windows updates, and other unnecessary data that accumulates over time.

**When to Use It**
- Low disk space warnings
- After major Windows updates
- Monthly maintenance routine
- Before installing large applications

**Why It Improves Performance**  
Freeing up disk space reduces the time Windows spends managing files. It also prevents the drive from becoming fragmented. Additionally, clearing cache forces apps to rebuild with fresh data, often resolving strange bugs.

**How to Use**
```cmd
cleanmgr /sageset:1
cleanmgr /sagerun:1
```

Or for automated cleanup with more options:
```cmd
cleanmgr /verylowdisk
```

**What Gets Removed:**
- Temporary Internet files
- Downloaded program files
- Recycle Bin contents
- Temporary files
- Thumbnails
- Old Windows installation files

**Safety Level:** ✅ **Very Safe** — Only removes files Windows considers safe to delete. You can review selections before cleaning.

---

### 3. `sfc /scannow`

**What It Does**  
System File Checker (sfc) scans all protected Windows system files and replaces corrupted versions with correct copies from a cached folder (`C:\Windows\WinSxS`).

**When to Use It**
- After malware removal
- When Windows features stop working
- Blue screen errors (BSOD)
- Programs crash with "DLL not found" errors
- Before major troubleshooting

**Why It Improves Performance**  
Corrupted system files cause Windows to behave unpredictably—crashes, slowdowns, or features failing silently. Repairing these files restores system stability and eliminates the overhead of error-handling routines.

**How to Use**
```cmd
sfc /scannow
```

**How to Read Results:**
- "Windows Resource Protection did not find any integrity violations" — Your system is healthy
- "Windows Resource Protection found corrupt files and successfully repaired them" — Issues fixed
- "Windows Resource Protection found corrupt files but was unable to fix some of them" — Run DISM (see below), then run `sfc /scannow` again

**Safety Level:** ✅ **Very Safe** — Only repairs Microsoft-signed system files. Does not touch user data or third-party programs.

---

## 🚀 Additional Recommended Commands

### 4. `DISM /Online /Cleanup-Image /RestoreHealth`

**What It Does**  
Deployment Image Servicing and Management (DISM) repairs the Windows system image and component store. Think of it as a deeper repair tool than SFC—it fixes the repair source itself.

**When to Use It**
- SFC reports it cannot fix certain files
- Windows Update fails repeatedly
- After in-place upgrade issues
- Store apps won't install or update

**Why It Improves Performance**  
If the Windows component store is corrupted, SFC can't repair system files properly. DISM fixes the store first, enabling SFC to work correctly. This resolves deeper system issues that manifest as performance problems.

**How to Use**
```powershell
DISM /Online /Cleanup-Image /CheckHealth
DISM /Online /Cleanup-Image /ScanHealth
DISM /Online /Cleanup-Image /RestoreHealth
```

Run them in order:
1. **CheckHealth** — Quick check (seconds)
2. **ScanHealth** — Thorough scan (5-10 minutes)
3. **RestoreHealth** — Downloads and repairs (10-30 minutes)

**Safety Level:** ✅ **Safe** — Downloads official files from Windows Update. Requires internet connection.

---

### 5. `powercfg /energy`

**What It Does**  
Analyzes your system's energy efficiency over 60 seconds and generates a detailed HTML report showing battery drain issues, power plan problems, and inefficient devices.

**When to Use It**
- Laptop battery drains faster than normal
- PC runs hot or fans spin constantly
- Diagnosing sleep/hibernation issues
- Optimizing desktop power consumption

**Why It Improves Performance**  
Power plans affect CPU speed, disk spin-down times, and background activity. Understanding energy inefficiencies helps you configure optimal performance settings.

**How to Use**
```cmd
powercfg /energy
```

Wait 60 seconds, then open the generated report:
```cmd
C:\Windows\System32\energy-report.html
```

**Key Things to Look For:**
- USB devices preventing sleep
- Inefficient power plan settings
- CPU usage during idle time
- Processes requesting timers

**Safety Level:** ✅ **Read-Only** — Analysis tool that creates a report. Makes no changes to your system.

---

### 6. `Get-Process | Sort CPU -Descending`

**What It Does**  
PowerShell command that lists all running processes sorted by CPU usage, showing you exactly what's consuming your processor resources.

**When to Use It**
- PC feels slow but you don't know why
- Fan runs at full speed
- CPU usage is high (Task Manager shows 80%+)
- Identifying malware or unwanted programs

**Why It Improves Performance**  
Many programs run in the background without your knowledge. This command helps you identify resource hogs so you can close or uninstall them.

**How to Use**
```powershell
Get-Process | Sort CPU -Descending | Select -First 10
```

For memory usage instead:
```powershell
Get-Process | Sort WS -Descending | Select -First 10
```

**How to Read Output:**
- **CPU** — Processor time used (higher = more CPU intensive)
- **WS (Working Set)** — RAM currently used
- **PM (Private Memory)** — Memory reserved by the process

**Safety Level:** ✅ **Read-Only** — Just displays information. To actually stop a process, research it first (don't kill system processes).

---

### 7. `Remove-Item $env:TEMP\* -Recurse -Force`

**What It Does**  
PowerShell command that deletes all files in your temporary folders. The `$env:TEMP` variable points to `C:\Users\YourName\AppData\Local\Temp`.

**When to Use It**
- Low disk space issues
- After installing/uninstalling software
- Monthly maintenance
- Before running Disk Cleanup

**Why It Improves Performance**  
Temp folders can grow to gigabytes of old installation files, crash dumps, and app cache. Clearing them frees space and ensures apps create fresh temp files instead of reusing potentially corrupted ones.

**How to Use**
```powershell
Remove-Item $env:TEMP\* -Recurse -Force -ErrorAction SilentlyContinue
```

Also clean the system temp folder:
```powershell
Remove-Item C:\Windows\Temp\* -Recurse -Force -ErrorAction SilentlyContinue
```

**Important:**
- Close all programs first
- Some files will be "in use" — that's normal (hence `-ErrorAction SilentlyContinue`)
- Run as Administrator for system temp folder

**Safety Level:** ⚠️ **Safe with Caution** — Only deletes temp files. Never use `Remove-Item` on other folders without understanding the command.

---

### 8. `Optimize-Volume -DriveLetter C -Defrag -Verbose`

**What It Does**  
Defragments traditional hard drives (HDDs) or optimizes solid-state drives (SSDs) by reorganizing file layout for faster access.

**When to Use It**
- HDD only: When fragmentation is above 10% (check with `Optimize-Volume -DriveLetter C -Analyze`)
- Monthly maintenance on HDDs
- After copying/deleting large numbers of files

**Why It Improves Performance**  
On HDDs, fragmented files are split across the disk. The read head must physically move to different locations, slowing access. Defragmentation consolidates file pieces. On SSDs, this command runs TRIM to mark deleted blocks for reuse.

**How to Use**

For HDD (Defragmentation):
```powershell
Optimize-Volume -DriveLetter C -Defrag -Verbose
```

For SSD (TRIM/Optimize):
```powershell
Optimize-Volume -DriveLetter C -ReTrim -Verbose
```

**Check fragmentation first:**
```powershell
Optimize-Volume -DriveLetter C -Analyze
```

**Important:**
- Windows automatically optimizes weekly (check Task Scheduler)
- Never defragment SSDs manually—it reduces lifespan (use `-ReTrim` instead)
- Can take 1-4 hours on heavily fragmented HDDs

**Safety Level:** ✅ **Safe** — Windows built-in tool. Cannot damage data. SSDs should only use `-ReTrim` not `-Defrag`.

---

## 🛡️ Beginner Safety Guidelines

### Running as Administrator

Most performance commands require elevated privileges. Here's how to safely run as Administrator:

**Method 1: Command Prompt as Admin**
1. Press `Win + X`
2. Select "Command Prompt (Admin)" or "Windows PowerShell (Admin)"
3. Click "Yes" on the UAC prompt

**Method 2: Run Dialog**
1. Press `Win + R`
2. Type `cmd` or `powershell`
3. Press `Ctrl + Shift + Enter` (runs as admin)

**Never:**
- Run random scripts from the internet as Admin
- Disable UAC (User Account Control) permanently
- Execute commands you don't understand just because someone told you to

---

### Commands to Avoid Without Research

Some commands can cause serious problems. Never run these without understanding what they do:

❌ **DO NOT RUN:**
```cmd
rd /s /q C:\                    # Deletes your entire C: drive
format C:                        # Formats your drive
del /f /s /q C:\*.*             # Deletes all files on C:
reg delete HKLM /f              # Corrupts Windows registry
takeown /f C:\Windows /r        # Changes Windows file ownership
```

⚠️ **Use with Extreme Caution:**
```cmd
chkdsk /f                       # Safe, but requires reboot
diskpart                        # Can accidentally format drives
bcdedit                         # Can make Windows unbootable
netsh winsock reset            # Resets network settings (fixable)
```

**Golden Rule:** If you found a command on a forum or YouTube video, search for it on official Microsoft documentation before running it.

---

### Backup Reminders

Before running maintenance commands, take these precautions:

**Create a System Restore Point:**
```cmd
wmic.exe /Namespace:\\root\default Path SystemRestore Call CreateRestorePoint "Before Performance Optimization", 100, 7
```

Or manually:
1. Press `Win + R`, type `sysdm.cpl`, press Enter
2. Go to "System Protection" tab
3. Click "Create"
4. Name it "Before Performance Optimization"

**Backup Important Files:**
- Documents, photos, projects to external drive or cloud storage
- Browser bookmarks and passwords (export from browser settings)
- Application settings (varies by app)

**Create a Bootable USB:**
Download Windows Media Creation Tool from Microsoft and create a recovery drive. If something goes wrong, you can boot from USB and repair Windows.

---

## 📋 Best Practice Workflow

Follow this step-by-step order for safe and effective system optimization:

### Step 1: Create Backup
- Create System Restore Point
- Backup important files

### Step 2: Run Initial Diagnostics
```powershell
# Check disk health (read-only)
Get-PhysicalDisk

# Check fragmentation (HDD only)
Optimize-Volume -DriveLetter C -Analyze

# Generate power report
powercfg /energy
```

### Step 3: Clean Temporary Files
```powershell
# Clear user temp
Remove-Item $env:TEMP\* -Recurse -Force -ErrorAction SilentlyContinue

# Clear system temp (as Admin)
Remove-Item C:\Windows\Temp\* -Recurse -Force -ErrorAction SilentlyContinue

# Run Disk Cleanup
cleanmgr /verylowdisk
```

### Step 4: Repair System Files
```cmd
# Step 1: Repair Windows image
DISM /Online /Cleanup-Image /RestoreHealth

# Step 2: Scan and repair system files
sfc /scannow
```

### Step 5: Check and Repair Disk
```cmd
# Schedule disk check for next reboot
chkdsk C: /f /r
# Restart when prompted
```

### Step 6: Optimize Drive
```powershell
# For HDD
Optimize-Volume -DriveLetter C -Defrag -Verbose

# For SSD
Optimize-Volume -DriveLetter C -ReTrim -Verbose
```

### Step 7: Identify Resource Hogs
```powershell
# Check CPU usage
Get-Process | Sort CPU -Descending | Select -First 10

# Check memory usage
Get-Process | Sort WS -Descending | Select -First 10
```

### Step 8: Review and Optimize
- Review power report and adjust settings
- Disable unnecessary startup programs
- Uninstall unused applications
- Update drivers and Windows

**Recommended Frequency:**
- Weekly: Temp file cleanup
- Monthly: Full workflow
- Quarterly: Deep clean with disk check

---

## 📊 Quick Reference Table

| Command | Purpose | When to Use | Risk Level |
|---------|---------|-------------|------------|
| `chkdsk C: /f /r` | Scan and repair disk errors | Disk errors, crashes, before formatting | ⚠️ Safe (Requires reboot) |
| `cleanmgr` | Remove temporary and unnecessary files | Low disk space, monthly maintenance | ✅ Very Safe |
| `sfc /scannow` | Repair corrupted system files | BSODs, DLL errors, after malware | ✅ Very Safe |
| `DISM /RestoreHealth` | Repair Windows component store | SFC can't fix files, Update issues | ✅ Safe (Needs internet) |
| `powercfg /energy` | Analyze power efficiency | Battery drain, overheating diagnosis | ✅ Read-Only |
| `Get-Process \| Sort CPU` | List processes by CPU usage | Identify resource hogs | ✅ Read-Only |
| `Remove-Item $env:TEMP\*` | Clear temporary folders | Low disk space, monthly cleanup | ⚠️ Safe (Use carefully) |
| `Optimize-Volume -Defrag` | Defragment HDD / Optimize SSD | HDD >10% fragmented, monthly HDD | ✅ Safe (SSD: use -ReTrim) |

**Legend:**
- ✅ **Very Safe** — Cannot cause problems
- ⚠️ **Safe** — No data risk, but requires Admin or system changes
- ⚠️ **Safe with Caution** — Powerful command, use exact syntax
- ❌ **Dangerous** — Can break Windows if misused

---

## ✅ Conclusion

Windows performance optimization doesn't require expensive third-party software or sketchy "PC cleaner" tools. The built-in PowerShell and CMD utilities provide everything you need to maintain a healthy, fast system.

**Key Takeaways:**

1. **Regular maintenance prevents problems** — Don't wait until your PC is unusable. Run these commands monthly.

2. **Understanding is more important than memorizing** — You now know *why* each command works, not just *what* it does.

3. **Safety first** — Always create restore points, never run commands you don't understand, and backup important data.

4. **Context matters** — Not every slow PC needs `chkdsk /f /r`. Use the right tool for the actual problem.

5. **Combine with good practices** — These commands work best alongside keeping drivers updated, uninstalling bloatware, and avoiding shady downloads.

**Remember:** A well-maintained Windows installation can run smoothly for years. The difference between a "slow computer" and a "fast computer" is often just proper maintenance—not hardware age.

---

## 📄 License & Disclaimer

### Educational Use

This guide is provided for **educational purposes only**. It is intended to help users learn about Windows system maintenance and optimization.

### Disclaimer

- **No Warranty:** The information is provided "as-is" without any guarantees. While these are standard Windows utilities, improper use can cause system issues.

- **Backup Your Data:** Always create backups before performing system maintenance. The author is not responsible for data loss.

- **Use at Your Own Risk:** System administration requires care and attention. If you're uncomfortable with a command, research it further or consult an IT professional.

- **Not Professional IT Advice:** This guide does not replace professional IT support for business-critical systems. For enterprise environments, consult your IT department.

- **Test in Safe Environments:** When learning, consider practicing on a virtual machine or non-critical system first.

### Contributing

Found an error or want to suggest improvements? Contributions are welcome! Please ensure all suggested commands are:
- Official Microsoft utilities
- Properly documented with safety warnings
- Tested and verified

### Resources

**Official Microsoft Documentation:**
- [Windows Command Reference](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/windows-commands)
- [PowerShell Documentation](https://docs.microsoft.com/en-us/powershell/)
- [Windows Performance Analyzer](https://docs.microsoft.com/en-us/windows-hardware/test/wpt/windows-performance-analyzer)

---

**Made with ❤️ for Windows users who want to understand their system**

**Developed by:** Arun VK  
**Contact:** arunvk207@gmail.com

*Last Updated: December 2025*