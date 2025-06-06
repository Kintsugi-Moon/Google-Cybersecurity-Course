# Linux File Permissions Portfolio Entry

## Activity Summary
In this exercise, I practiced using Linux commands to examine and manage file permissions. The goal was to understand how file permissions affect user access and how to modify them safely using the command line. This skill is essential for protecting sensitive data and maintaining secure systems.

## Scenario
I was presented with a situation where I needed to identify and adjust file permissions for a group project folder. Some users had more access than necessary, and others did not have the access they needed.

## Commands Used and Why

- **`ls -l`**  
  Used to list files in the directory along with their permissions. This helped me determine which files needed changes.

- **`chmod`**  
  Used to update file permissions. For example, `chmod 644 filename` was used to allow the owner to read/write while giving read-only access to others.

- **`chown`**  
  Used to change file ownership when files needed to be reassigned. For instance, `chown user:group filename` ensured the correct user and group were responsible for a file.

- **`umask`**  
  Checked the default permission settings for newly created files. This helped me understand how permissions are applied by default.

## What I Learned
This activity taught me how critical it is to set the correct permissions to prevent unauthorized access. I also learned how to use key commands like `chmod` and `chown` effectively. File permissions are not just a technical detail—they’re a frontline defense in cybersecurity.

## Questions I Still Have
How do large organizations automate permission management across many users and directories without introducing risk?
