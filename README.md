# VeeamDR-Lab
Veeam Backup &amp; Disaster Recovery Lab
## Overview
Home lab simulating enterprise backup and disaster recovery 
using Veeam Agent for Windows (Free Edition). Built on a 
domain-joined Windows machine (CLIENTPC) running in 
Parallels Desktop on macOS.

## Technologies Used
- Veeam Agent for Microsoft Windows (Free Edition)
- Windows Server (Parallels VM)
- Backup types: Full backup, Incremental backup
- File-level restore

## What I Built
- Configured local backup repository at C:\VeeamBackups\
- Created and ran full backup — 20GB captured
- Created incremental backup — 633MB (97% smaller)
- Built a 3-point restore chain verified in File Explorer
- Simulated ransomware attack by deleting critical files
- Performed successful file-level restore in 5 seconds
- Investigated domain folder redirection — identified why 
  redirected Desktop paths require expanded backup scope

## Disaster Recovery Scenario
**Scenario:** Ransomware attack — critical business files deleted  
**File recovered:** critical-business-data.txt  
**Recovery method:** Veeam file-level restore  
**RTO achieved:** 5 seconds  
**RPO:** Less than 10 minutes  
**Errors:** 0  

## Key Learnings
- Full backups capture everything. Incrementals capture 
  only changes — 20GB became 633MB on second run.
- RPO is real — files created and deleted between backup 
  windows cannot be recovered. Backup frequency matters.
- Domain-joined machines may redirect Desktop/Documents 
  to network paths. Backup scope must account for this.
- The restore matters more than the backup — tested and 
  verified end-to-end recovery, not just backup creation.

## Screenshots
[See /screenshots folder]
 
