
1.  Assumption: We have access to the system via SSH and want to read files from another folder that a specific user can read.
2. Mount NFS share
3. Create a local user with the same UID as the specific user
4. Upload a shell that has the `SUID` of that specific user
5. Run the shell via the SSH user

If the NFS server has the setting `no_root_squash` enabled, we can even create a root shell.
https://github.com/Tib3rius/Pentest-Cheatsheets/blob/master/privilege-escalation/linux/linux-examples.rst#nfs
