Below are the tags used in the CIS roles on Windows Machines.


| Windows Server 2019 | Control Description |Applies to DC|Applies to Member Server|Applies to Standalone Server| Notes |
| -----------------|--------------------- | -----------------|--------------------- | --------------------- |-----------------|
| 1.1.1 | Enforce password history is set to {{ password_history }} or more passwords|X|X|X|
| 1.1.2 | Ensure maximum password age is set to "{{ password_expire_days }}" or fewer days, but not 0|X|X|X|
| 1.1.3 | Ensure minimum password age is set to "{{ password_min_days }}"|X|X|X|
| 1.1.4 | Ensure minimum password length is set to "{{ password_min_length }}"|X|X|X|
| 1.1.5 | Ensure 'Password must meet complexity requirements' is set to enbled|X|X|X|
| 1.1.6 | Ensure passwords are not stored with reversible encryption|X|X|X|
| 1.2 | Account Lockout Policy|X|X|X|
| 1.2.2 | Ensure Account lockout threshold is set to {{ account_lockout_threshold }} or fewer attempts, but not 0|X|X|X|
| 1.2.3 | Ensure Reset account lockout counter after is set to 15 or more minutes|X|X|X|
| 1.2.1 | Ensure Account lockout duration is set to {{ account_lockout_duration }}|X|X|X|
| 2.2.0 | User rights policy|X|X|X|
| 2.2.1 | Ensure Access Credential Manager as a trusted caller is set to No One|X|X|X|
| 2.2.2 | Ensure Access this computer from network is restricted|X| | |
| 2.2.3 | Ensure Access this computer from network is restricted| |X|X|
| 2.2.4 | Ensure Act as part of operating system is set to no one.|X|X|X|
| 2.2.5 | Add workstations to domain  set to administrators only|X|X|X|
| 2.2.6 | Ensure Adjust memory quotas for a process is restricted|X|X|X|
| 2.2.7 | Ensure Access this computer from console is restricted|X|X|X|
| 2.2.8 | Ensure allow long on through RDS is restricted (domain controllers)|X| | |
| 2.2.9 | Ensure allow long on through RDS is restricted (member or standalone servers)| | |X|
| 2.2.10 | Ensure backup operators are restricted|X|X|X|
| 2.2.[11,12] | Ensure the ability to change the time is restricted|X|X|X|
| 2.2.13 | Ensure Create a page file is set to Administrator|X|X|X|
| 2.2.14 | Ensure no one can create a token object|X|X|X|
| 2.2.15 | Ensure Create Token object is restricted|X|X|X|
| 2.2.16 | Ensure no one can create permanent shared objects|X|X|X|
| 2.2.17 | Ensure symbolic link creation is restricted (domain controller)|X|X|X|
| 2.2.18 | Ensure symbolic link creation is restricted (member or standalone server )|X|X|X|
| 2.2.19 | Ensure 'Debug programs' is set to 'Administrators'|X|X|X|
| 2.2.20 Deny accesss to this computer from network (domain computer)|X|X|X|
| 2.2.20 Deny accesss to this computer from network (domain computer)|X|X|X|
| 2.2.[22-25] | Ensure deny local, remote, and batch logons includes 'Guests'|X|X|X|
| 2.2.28 | Ensure 'Enable computer and user accounts to be trusted for delegation' is set to 'No One'| |X| |
| 2.2.29 | Ensure 'Debug programs' is set to 'Administrators'|X|X|X|
| 2.2.31 | Ensure 'Impersonate a client after authentication' is restricted|X|X|X|
| 2.2.33 | Ensure 'Increase scheduling priority' is restricted|X|X|X|
| 2.2.34 | Ensure 'Load and unload device drivers' is restricted|X|X|X|
| 2.2.35 | Ensure 'Lock pages in memory' is set to 'No One'|X|X|X|
| 2.2.36 | Ensure 'Log in as a batch job is set to 'Administrators'|X| | |
| 2.2.[37,38] | Ensure 'Manage auditing and security log' is set to Adminstrators|X|X|X|
| 2.2.39 | Ensure 'Modify an object label' is set to 'No One'|X|X|X|
| 2.2.40 | Ensure 'Modify firmware environment values' is set to 'Administrators'|X|X|X|
| 2.2.41 | Ensure 'Perform volume maintenance tasks' is set to 'Administrators'|X|X|X|
| 2.2.42 | Ensure 'Profile single process' is set to 'Administrators'|X|X|X|
| 2.2.43 | Ensure 'Profile system performance' is restricted|X|X|X|
| 2.2.44 | Ensure 'Replace a process level token' is restricted|X|X|X|
| 2.2.45 | Ensure 'Restore files and directories' is set to 'Administrators'|X|X|X|
| 2.2.46 | Ensure 'Shut down the System' is set to 'Administrators'|X|X|X|
| 2.2.47 | Ensure 'Synchronize directory service data' is set to 'No One'|X| | |
| 2.2.48 | Ensure 'Take ownership of files or other objects' is set to 'Administrators'|X|X|X|
| 2.3.1.2 | Ensure 'Accounts - Block Microsoft accounts' is set to 'Users can't add or log on with  Microsoft accounts'|X|X|X|
| 2.3.1.3 | Ensure 'Accounts - Guest account status' is set to 'Disabled'|X|X|X|
| 2.3.1.4 | Ensure 'Accounts - Limit local account use of blank passwords to console logon only' is set to 'Enabled'|X|X|X|
| 2.3.1.5 | Rename Administrator account|X|X|X|
| 2.3.1.6 | Rename Guest account|X|X|X|
| 2.3.2.1 | Force audit policy subcategories to override category settings|X|X|X|
| 2.3.2.2 | Ensure system does not shut down if unable to log security audits|X|X|X|
| 2.3.4.1 | Ensure only Administrators can format and eject removeable hardware|X|X|X|
| 2.3.4.2 | Prevent Users from installing print drivers|X|X|X|
| 2.3.5 | Domain controller specific settings|X| | |
| 2.3.5.1 | Allow server operators to schedule tasks|X| | |
| 2.3.5.2 | Require LDAP signing|X| | |
| 2.3.5.3 | Refuse machine account password changes set to disabled|X| | |
| 2.3.6 | Domain members specific settings (controllers and member servers)|X|X| |
| 2.3.6.1 | Digitally encrypt or sign secure channel data (always)|X|X| |
| 2.3.6.2 | Digitally secure channel data (when possible)|X|X| |
| 2.3.6.3 | Digitally sign secure channel data (when possible)|X|X| |
| 2.3.6.4 | Disable machine account password changes|X|X| |
| 2.3.6.5 | Maximum machine account password age|X|X| |
| 2.3.6.6 | Require strong session key|X|X| |
| 2.3.7 | Interactive Logon|X|X|X|
| 2.3.7.1 | Disable CAD Requirement|X|X|X|
| 2.3.7.2 | Don't disply last signed in user|X|X|X|
| 2.3.7.3 | Machine inactivtiy limit set to {{ inactivity_timeout }} but not 0|X|X|X|
| 2.3.7.6 | Number of cached logins set to {{ cached_logins }} or fewer| |X| |
| 2.3.7.7 | Number of days for password change warning {{ cached_logins }}|X|X|X|
| 2.3.7.8 | Require domain controller authentication to unlock workstation|X|X|X|
| 2.3.7.9 | Smart-card removal behavior|X|X|X|
| 2.3.8.1 | Require SMB packet signing|X|X|X|
| 2.3.8.2 | Sign communications (if server agrees)|X|X|X|
| 2.3.8.3 | send uncencrypted password to third-party SMB servers|X|X|X|
| 2.3.9.1 | SMB inactivty suspension|X|X|X|
| 2.3.9.2 | Digitally sign communications (always)|X|X|X|
| 2.3.9.3 | Digitally sign communications (if client agrees)|X|X|X|
| 2.3.9.4 | Disconnect clients when logon hours expire|X|X|X|
| 2.3.9.5 | SPN target name validation level|X|X|X|
| 2.3.10.2 | Do not allow enumeration of SAM accounts|X|X|X|
| 2.3.10.3 | Do not allow enumeration of SAM accounts and shares| |X| |
| 2.3.10.4 | Do not allow storage of passwords and creds for network auth|X|X|X|
| 2.3.10.5 | Let 'Everyone' permissions apply to anonymous users is disabled|X|X|X|
| 2.3.10.6 | Named pipes can be accessed anonymously (DC only)|X| | |
| 2.3.10.7 | Named pipes can be accessed anonymously (member servers)| |X|X|
| 2.3.10.8 | Remotely accessible registry paths|X|X|X|
| 2.3.10.9 | Remotely accessible registry paths and subpaths|X|X|X|
| 2.3.10.10 | Restrict anonymous access to named pipes|X|X|X|
| 2.3.10.11 | Restrict anonymous access to named pipes|X|X|X|
| 2.3.10.12 | Clear all shares that can be accessd anonymously|X|X|X|
| 2.3.10.13 | Local users authenticate as themselves|X|X|X|
| 2.3.11.1 | Use machine ID for NTLM|X|X|X|
| 2.3.11.2 | Disallow LocalSystem NULL session fallback|X|X|X|
| 2.3.11.3 | Disallow PKU2U auth requests|X|X|X|
| 2.3.11.4 | Supported Kerberos encryption types|X|X|X|
| 2.3.11.5 | Do not store LAN Manager hash on password change|X|X|X|
| 2.3.11.6 | Force Logoff when logon hours expire|X|X|X|
| 2.3.11.7 | LAN Manager authentication - Send NTLMv2 reponse, refuse LM & NTLM|X|X|X|
| 2.3.11.8 | LDAP Client signing|X|X|X|
| 2.3.13.1 | Disable system from shuting down without having to log on|X|X|X|
| 2.3.15.1 | Require case insensitivity for now windows subsystems|X|X|X|
| 2.3.15.2 | Streghten default permissions of system objects|X|X|X|
| 2.3.17.1 | Ensure UAC, admin approval mode for built-in admin account is enabled|X|X| |
| 2.3.17.2 | Ensure UAC, behavior of the elevation prompt for admins|X|X|X|
| 2.3.17.3 | Ensure UAC, behavior of the elevation prompt for standard users|X|X|X|
| 2.3.17.4 | Ensure UAC, direct app installations prompt for elevation|X|X|X|
| 2.3.17.5 | Ensure UAC, Only elevate UIAccess aps that are installed in secure location|X|X|X|
| 2.3.17.6 | Ensure UAC, Run all admins in Admin Approval Mode|X|X|X|
| 2.3.17.7 | Ensure UAC, Switch to secure desktop when prompting for elevation|X|X|X|
| 2.3.17.8 | Ensure UAC, Virtualize file and registry write failures to per-user locations|X|X|X|
| 17.1.1 | Ensure Audit credential validation is set to 'success and failure'|X|X|X|
| 17.1.2 | Ensure Kerberos Authentication Service is set to 'success and failure'|X|X|X|
| 17.1.3 | Ensure Kerberos Service Ticket Operations is set to 'success and failure'|X|X|X|
| 17.2.1 | Ensure Application Group Management is set to 'success and failure'|X|X|X|
| 17.2.2 | Ensure Computer Account Management is set to 'success and failure'|X| | |
| 17.2.3 | Ensure Distribution Group Management is set to 'success and failure'|X| | |
| 17.2.4 | Ensure Other Account Management Events is set to 'success and failure'|X| | |
| 17.2.5 | Ensure Security Group Management is set to 'success and failure'|X|X|X|
| 17.2.6 | Ensure User Account Management is set to 'success and failure'|X|X|X|
| 18.1.1.1 | Ensure "Prevent enabling lock screen camera" is enabled|X|X|X|
| 18.1.1.2 | Ensure 'Prevent enabling lock screen slide show' is enabled|X|X|X|
| 18.1.2.1 | Ensure 'Allow users to enable online speech recognition services' is disabled|X|X|X|
| 18.1.2.2 | Ensure 'Allow Online Tips' is disabled|X|X|X|
| 18.3.1 | Ensure 'Apply UAC restrictions to local accounts on network logons' is enabled|X|X|X|
| 18.3.2 | Disable SMBv1 client driver|X|X|X|
| 18.3.3 | Disable SMBv1 server - Doesn't exist in 2019 but the setting won't hurt|X|X|X|
| 18.3.4 | Ensure 'Enabled Structured Exception Handling Overwrite Protection' is enabled|X|X|X|
| 18.3.5 | Ensure 'Extended Protection for LDAP Authentication (DCs only)' is enabled; always|X| | |
| 18.3.6 | Set NetBT Node type to P-Node|X|X|X|
| 18.3.7 | Ensure 'WDigest Authentication' is disabled|X|X|X|
| 18.4.1 | Ensure 'Enable automatic Logon' is disabled|X|X|X|
| 18.4.2 | Disabled IPv6 IP source routing|X|X|X|
| 18.4.3 | Disabled IPv4 IP source routing|X|X|X|
| 18.4.4 | Disallow ICMP redirects from ovrriding OSPF routes|X|X|X|
| 18.4.5 | TCP Keep alive Time|X|X|X|
| 18.4.6 | Allow computer to ignore NetBIOS name release requests except from WINS servers|X|X|X|
| 18.4.7 | Disable 'Allow IRDP to detet and configure Default Gateway addresses'|X|X|X|
| 18.4.8 | Enable Save DLL Search mode|X|X|X|
| 18.4.9 | Screen saver grace time|X|X|X|
| 18.4.10 | Max IPv6 TCP retransmissions|X|X|X|
| 18.4.12 | Percentage where event log will generate a warning|X|X|X|
| 18.5.4.1 | DNS Client - Turn off multicast name resolution|X|X|X|
| 18.5.5.1 | Disable Font providers|X|X|X|
| 18.5.8.1 | Disable insecure guest logons|X|X|X|
| 18.5.9.1 | Disble Mapper I/0|X|X|X|
| 18.5.9.2 | Disble Responder Driver|X|X|X|
| 18.5.10.1 | Turn off MS Peer-to-Peer Networking Services|X|X|X|
| 18.5.11.2 | Prohibit installation of Nework bridge on DNS domain network|X|X|X|
| 18.5.11.3 | Prohibit use of internet Connection Sharing on DNS domain network|X|X|X|
| 18.5.11.4 | domain users to elevate when setting a network's location|X|X|X|
| 18.5.19.2 | Disable IPV6|X|X|X|
| 18.5.20.1 | Disable configuration of wireless settings using windows Connect Now|X|X|X|
| 18.5.20.3 | Disable Windows Connect Now Wizards|X|X|X|
| 18.5.21.1 | Number of simultaneous connections to the internet or windows domain is 3|X|X|X|
| 18.5.21.2 | Prohibit connection to non-domain networks when connected to domain network| |X| |
| 18.7.1.1 | Turn off notifications network usage|X|X|X|
| 18.8.3.1 | Disable including command line in process creation events|X|X|X|
| 18.8.4.1 | Force updated oracle Remediation Clients|X|X|X|
| 18.8.4.2 | Remote host allows delegation of non-exportable credentials|X|X|X|
| 18.8.5.1 | Turn on virtualization based security|X|X|X|
| 18.8.5.6 | Disable Credential guard on DCs|X| | |
| 18.8.14.1 | Enable Boot-Start driver initialization Policy|X|X|X|
| 18.8.21.[2-3] | Configure registry Policy processing|X|X|X|
| 18.8.21.4 | Disable 'Continue experiences on this device'|X|X|X|
| 18.8.21.5 | Diable background refresh of Group Policy|X|X|X|
| 18.8.22.1.1 | Turn off downloading of print drivers over HTTP|X|X|X|
| 18.8.22.1.2 | Turn off handwriting personalization data sharing|X|X|X|
| 18.8.22.1.3 | Enable hand writing recognition error reporting|X|X|X|
| 18.8.22.1.4 | Turn off ICW if URL connection is referring to microsoft.com|X|X|X|
| 18.8.22.1.5 | Turn off Internet download for Web publishing and online ordering wizards|X|X|X|
| 18.8.22.1.6 | Turn off printing over HTTP|X|X|X|
| 18.8.22.1.7 | Turn off REgistration if URL connection is referring to microsoft.com|X|X|X|
| 18.8.22.1.8 | Turn off search companion content file updates|X|X|X|
| 18.8.22.1.9 | Turn off the order prints picture task|X|X|X|
| 18.8.22.1.10 | Turn off the Publish to Web task for files and folders|X|X|X|
| 18.8.22.1.11 | Turn off the WMC Experience Improvement Program|X|X|X|
| 18.8.22.1.12 | Turn off WCEIP|X|X|X|
| 18.8.22.1.13 | Turn off Windows Error Reporting (part 1)|X|X|X|
| 18.8.22.1.13 | Turn off Windows Error Reporting (part 2)|X|X|X|
| 18.8.25.1 | Support device auth using certificate|X|X|X|
| 18.8.26.1 | Enable Enumberation policy for external devices|X|X|X|
| 18.8.27.1 | Disallow copying of user input methods to the system account|X|X|X|
| 18.8.28.1 | Block user from shoing account details at sign-in|X|X|X|
| 18.8.28.2 | Do not display network selection UI|X|X|X|
| 18.8.28.3 | Do not enumerate connected users on domain joined computers|X|X|X|
| 18.8.28.4 | Do not enumerate local users on domain-joined computers| |X| |
| 18.8.28.5 | Turn off app notifications on the lock screen|X|X|X|
| 18.8.28.6 | Turn off picture password sign-in|X|X|X|
| 18.8.28.7 | Disable convenience PIN sign-in|X|X|X|
| 18.8.31.1 | Disallow clipboard sync across devices|X|X|X|
| 18.8.31.2 | Disallow uplod of user activities|X|X|X|
| 18.8.34.6.1 | Disallow network connectivity during connected standby (battery)|X|X|X|
| 18.8.34.6.2 | Disable network connectivity during connected standby (plugged in)|X|X|X|
| 18.8.34.6.3 | Require password when computer wakes (battery)|X|X|X|
| 18.8.34.6.4 | Require password when computer wakes (plugged in)|X|X|X|
| 18.8.36.1 | Disable offer remote assistance|X|X|X|
| 18.8.36.2 | Disable solicited remote assistance|X|X|X|
| 18.8.37.1 | Enable RPC Endpoint Mapper Client|X|X|X|
| 18.8.37.2 | Restrict Unauthenticated RPC clients| |X| |
| 18.8.47.5.1 | Disable MSDT Interactive communication with support provider (if disabled cannot send support data to microsoft during support session)|X|X|X|
| 18.8.47.11.1 | Disable PerfTrack|X|X|X|
| 18.8.49.1 | Turn off advertising ID|X|X|X|
| 18.8.52.1.1 | enable Windows NTP Client|X|X|X|
| 18.8.52.1.2 | Disable Windows NTP Server| |X| |
| 18.9.4.1 | Disallow a window app to share data between users|X|X|X|
| 18.9.6.1 | Allow Microsoft Accounts to be optional|X|X|X|
| 18.9.8.1 | Disallow Autoplay for non-volume devices|X|X|X|
| 18.9.8.2 | Do not execute any autorun commands|X|X|X|
| 18.9.8.3 | Turn off Autoplay|X|X|X|
| 18.9.10.1.1 | Configure enhanced anti-spoofing|X|X|X|
| 18.9.12.1 | Disallow use of camera|X|X|X|
| 18.9.13.1 | Enabled microsoft consumer experiences|X|X|X|
| 18.9.14.1 | Ensure Require pin for pairing is set|X|X|X|
| 18.9.15.1 | Do not display the password reveal button|X|X|X|
| 18.9.15.2 | Disable enumerate administrator accounts on elevation|X|X|X|
| 18.9.16.1 | Ensure Allow Telemetry is set to 0 - Enterprise Only or 1 - Basic|X|X|X|
| 18.9.16.2 | Disable authenticated proxy usage|X|X|X|
| 18.9.16.3 | Do not show feedback notifications|X|X|X|
| 18.9.16.4 | Disable toggler user control over insider builds|X|X|X|
| 18.9.26.1.1 | Disable Application Event Log behavior when the log file reaches max size|X|X|X|
| 18.9.26.1.2 | Set Application maximum log size|X|X|X|
| 18.9.26.2.1 | Disable Security Event Log behavior when the log file reaches max size|X|X|X|
| 18.9.26.2.2 | Set Security maximum log size|X|X|X|
| 18.9.26.3.1 | Disable Setup Event Log behavior when the log file reaches max size|X|X|X|
| 18.9.26.3.2 | Set Setup maximum log size|X|X|X|
| 18.9.26.4.1 | Disable System Event Log behavior when the log file reaches max size|X|X|X|
| 18.9.26.4.2 | Set System maximum log size|X|X|X|
| 18.9.30.2 | Enable data execution prevention for Explorer|X|X|X|
| 18.9.30.3 | Turn on hep termination on corruption|X|X|X|
| 18.9.30.4 | Turn on shell protocol protected mode|X|X|X|
| 18.9.39.2 | Turn off location|X|X|X|
| 18.9.43.1 | Disallow message servvice cloud sync|X|X|X|
| 18.9.44.1 | Block all consumer Microsoft acount user authentication|X|X|X|
| 18.9.52.1 | Prevent the usage of OneDrive for file storage|X|X|X|
| 18.9.59.2.2 | Do not allow passwords to be saved|X|X|X|
| 18.9.59.3.2.1 | Restrict RDS Susers to a single RDS session|X|X|X|
| 18.9.59.3.3.1 | Do not allow COM port redirection|X|X|X|
| 18.9.59.3.3.2 | Do not allow drive redirection|X|X|X|
| 18.9.59.3.3.3 | Do not allow LPT port redirection|X|X|X|
| 18.9.59.3.3.4 | Do not allow PnP device redirection|X|X|X|
| 18.9.59.3.9.1 | Always prompt for password upon connection|X|X|X|
| 18.9.59.3.9.2 | Require secure RPC communication|X|X|X|
| 18.9.59.3.9.3 | Require TLS security layer for RDP connections|X|X|X|
| 18.9.59.3.9.4 | Require user auth for remote connections|X|X|X|
| 18.9.59.3.9.5 | Set client connection encryption level|X|X|X|
| 18.9.59.3.10.1 | Set time limit for active but idle RDS Sessions|X|X|X|
| 18.9.59.3.10.2 | Set time limit for disconnected sessions|X|X|X|
| 18.9.59.3.11.1 | Delete temp folders upon exit|X|X|X|
| 18.9.59.3.11.2 | Use temporary folders per session|X|X|X|
| 18.9.60.1 | Prevent downloading of enclosures|X|X|X|
| 18.9.61.2 | Disallow Cloud Search|X|X|X|
| 18.9.61.3 | Allow indexing of encrypted files|X|X|X|
| 18.9.66.1 | Turn off KMS Client Online AVS Validation|X|X|X|
| 18.9.77.3.1 | Do not Configure local setting override for reporting to MAPS|X|X|X|
| 18.9.77.3.2 | Do not Join Microsoft MAPS|X|X|X|
| 18.9.77.7.1 | Turn on behavior monitoring|X|X|X|
| 18.9.77.9.1 | Disable Watson Events|X|X|X|
| 18.9.77.10.1 | Scan removable drives|X|X|X|
| 18.9.77.10.2 | Turn on Email scanning|X|X|X|
| 18.9.77.13.1.1 | Configure Attack Surface Reduction rules|X|X|X|
| 18.9.77.13.1.2 | Configure Attack Surface Reduction rules and set state for each ASR rule|X|X|X|
| 18.9.77.13.3.1 | Block users and apps from accessing dangerous websites|X|X|X|
| 18.9.77.14 | Configure detection for potentially unwanted applications|X|X|X|
| 18.9.77.15 | Turn on Windows Defender Antivirus|X|X|X|
| 18.9.80.1.1 | Enable Windows Defender SmartScreen|X|X|X|
| 18.9.84.1 | Disallow suggested apps in Windows Ink Workspace|X|X|X|
| 18.9.84.2 | Disallow Windows Ink Workspace|X|X|X|
| 18.9.85.1 | Do not allow user control over installs|X|X|X|
| 18.9.85.2 | Do not install with elevated privileges|X|X|X|
| 18.9.85.3 | Enable Interent Explorder security prompt for Installer Scripts|X|X|X|
| 18.9.86.1 | Do not sign in last user after a restart|X|X|X|
| 18.9.95.1 | Turn off PowerShell Transcription|X|X|X|
| 18.9.97.1.1 | Allow Basic WinRM authentication|X|X|X|
| 18.9.97.1.2 | Allow WinRM unencrypted traffic|X|X|X|
| 18.9.97.1.3 | Disallow Digest Authentication|X|X|X|
| 18.9.97.2.1 | Allow Basic WinRM authentication|X|X|X|
| 18.9.97.2.2 | Disallow remote server management through WinRM|X|X|X|
| 18.9.97.2.3 | Disallow uncncrypted WinRM traffic|X|X|X|
| 18.9.97.2.4 | Disallow WinRM from storing RunAs credentials|X|X|X|
| 18.9.98.1 | Disallow Remote Shell Acccess|X|X|X|
| 18.9.99.2.1 | Prevent users from modifying settings|X|X|X|
| 18.9.102.1.1 | Disable preview builds|X|X|X|
| 18.9.102.2 | Configure Automatic Updates|X|X|X|
| 18.9.102.2 | Configure Automatic Updates|X|X|X|
| 18.9.102.3 | Configure update download and patching day|X|X|X|
| 18.9.102.3 | Configure update download and patching time|X|X|X|
| 18.9.102.4 | Restart after updates even if user is logged in|X|X|X|
| 19.6.6.1.1 | off Help Expereience Improvement Program|X|X|X|
| 19.7.4.1 | Do not preserve information in file attachments|X|X|X|
| 19.7.4.2 | Notify antivirus programs when opening attachments|X|X|X|
