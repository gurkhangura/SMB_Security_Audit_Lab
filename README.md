# SMB Security Audit Lab

Conducted an internal network security assessment using Kali Linux to exploit SMB vulnerabilities on a Windows endpoint. Performed reconnaissance, user enumeration, and targeted credential attacks to gain administrative access and verify post-exploitation risks.

## Phase 1: Network Reconnaissance
**Action:** Performed network reconnaissance using Nmap to identify exposed SMB and RPC services.

![Network Reconnaissance](1_Network_Reconnaissance.jpg)

## Phase 2: SMB Enumeration
**Action:** Conducted SMB enumeration with `enum4linux` to identify valid usernames and domain/workgroup information.

![SMB Enumeration](2_SMB_Enumeration.jpg)

## Phase 3: Credential Attack
**Action:** Generated custom username and password wordlists for credential testing. Utilized `NetExec` to perform targeted dictionary attacks against the exposed SMB services.

![NetExec Brute Force](3_NetExec_Brute_Force.jpg)

## Phase 4: System Authentication
**Action:** Successfully identified valid credentials (`administrator:password`) and authenticated to the target system via `smbclient`.

![SMB Authentication](4_SMB_Authentication.jpg)

## Phase 5: Post-Exploitation & File System Access
**Action:** Navigated the administrative `C$` share to verify full read/write access to the root file system.

![File System Access](5_FileSystem_Access.jpg)

**Proof of Concept:** Created a proof-of-concept text file locally on Kali Linux and remotely transferred it to the target's desktop via SMB to demonstrate write privileges.

![Payload Upload](6_Payload_Upload.jpg)

**Target Verification:** Confirmed the payload was successfully deposited and readable on the endpoint.

![Windows Proof](7_Windows_Proof.jpg)
