**Title:**  
Logout Button Non-Functional in Safari Browser  

**Description:**  
The logout button fails to respond when clicked in the Safari browser. Users attempting to log out experience no action or feedback, trapping them in an active session. 
This issue occurs consistently across tested Safari versions but does not manifest in other browsers (e.g., Chrome, Firefox).  

**Steps to Reproduce:**  
1. Launch **Safari** browser (any supported version).  
2. Navigate to the application login page.  
3. Authenticate with valid credentials.  
4. After successful login, locate and click the **Logout button**.  
5. Observe the button’s behavior.  

**Expected vs Actual Behavior:**  
- **Expected:** Clicking the logout button terminates the session and redirects the user to the login page or a confirmation screen.  
- **Actual:** The logout button exhibits no response—no redirection, error message, or session termination. The user remains logged in.  

**Environment (if known):**  
- **Browser:** Safari (all versions, including latest stable release)  
- **OS:** macOS (Catalina 10.15+), iOS (14.0+)  
- **Device:** MacBook Pro, iMac, iPad, iPhone (reproducible across devices)  
- **Application Version:** v2.5.0 (if unspecified, note: "All versions post-login feature")  

**Severity:**  
**High**  
- **Impact:** Critical security and usability issue:  
  - Prevents users from securely ending sessions.  
  - Risks unauthorized access to accounts on shared devices.  
  - Violates session management compliance standards (e.g., GDPR, CCPA).  
- **Urgency:** Requires immediate resolution for Safari users.  

---  
**Notes for Engineering:**  
- Suspect JavaScript event handlers or Safari-specific CSP restrictions.  
- Check for console errors (e.g., `TypeError: null is not an object`) in Safari DevTools.  
- Regression testing needed for cross-browser compatibility post-fix.
