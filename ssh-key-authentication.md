# SSH Key Authentication

## Goal
Configure SSH public-key authentication from my Mac to the Ubuntu server, keeping the private key on my Mac.
## Evidence
Observed an Accepted publickey log entry. Its fingerprint matched my Mac’s lab public key and the single entry in Ubuntu’s authorized_keys. The successful authentication demonstrated possession of the matching private key; the file entry alone only showed that the public key was authorized.
## Troubleshooting
I initially searched for authorized_keys on my Mac and received “No such file or directory.” I used whoami, hostname, and pwd to identify the machine and account, then repeated the check in my Ubuntu SSH session.
## Conclusion
Verified that my Mac successfully authenticated as labadmin using the intended SSH key. Password authentication remains enabled; this test did not configure key-only access.
