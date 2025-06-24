# Data Leak Analysis - Least Privilege Assessment

## Incident Summary
A customer success representative received access to a folder with internal documents. The manager who shared the folder forgot to unshare it. The representative accidentally shared the full folder link with a business partner, who posted it on social media.

## Issues
- Least privilege was not followed; access to sensitive documents was granted unnecessarily.
- No controls were in place to restrict or expire shared access.
- The folder permissions allowed the accidental exposure of confidential files.

## NIST SP 800-53: AC-6 Summary
AC-6 from NIST SP 800-53 emphasizes assigning the minimum access necessary for users to do their jobs. Control enhancements recommend auditing user privileges and implementing time-restricted access to ensure data privacy and minimize exposure.

## Recommendations
1. Enforce role-based access control to ensure users only access what they need.
2. Use automatic expiration on shared folder permissions to prevent lingering access.

## Justification
These recommendations reinforce the principle of least privilege. Time-limited access prevents forgotten shares, and role-based access ensures employees do not have unnecessary access to sensitive data. Together, they reduce the likelihood of data leaks from internal mistakes.
