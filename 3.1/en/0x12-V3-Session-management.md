# V3: Session Management Verification Requirements

## Control Objective

One of the core components of any web-based application is the mechanism by which it controls and maintains the state for a user interacting with it. This is referred to this as Session Management and is defined as the set of all controls governing state-full interaction between a user and the web-based application.

Ensure that a verified application satisfies the following high level session management requirements:

* Sessions are unique to each individual and cannot be guessed or shared
* Sessions are invalidated when no longer required and timed out during periods of inactivity.


## Security Verification Requirements

| # | Description | L1 | L2 | L3 | Since |
| --- | --- | --- | --- | -- | -- |
| **3.2** | Verify that sessions are invalidated when the user logs out. | ✓ | ✓ | ✓ | 1.0 |
| **3.3** | Verify that sessions timeout after a specified period of inactivity. |  |  | ✓ | 1.0 |
| **3.4** | Verify that sessions timeout after an administratively-configurable maximum time period regardless of activity (an absolute timeout). |  | ✓ | ✓ | 1.0 |
| **3.5** | Verify that all pages that require authentication have easy and visible access to logout functionality. | ✓ | ✓ | ✓ | 1.0 |
| **3.6** | Test that the session ID is never disclosed in URLs, error messages, or logs. This includes verifying that the application does not support URL rewriting of session cookies. |  |  | ✓ | 1.0 |
| **3.7** | Verify that all successful authentication and re-authentication generates a new session and session id. | ✓ | ✓ | ✓ | 1.0 |
| **3.10** | Verify that only session ids generated by the application framework are recognised as active by the application. |  | ✓ | ✓ | 1.0 |
| **3.11** | Test session IDs against criteria such as their randomness, uniqueness, resistance to statistical and cryptographic analysis and information leakage. | ✓ | ✓ | ✓ | 1.0 |
| **3.12** | Verify that session IDs stored in cookies are scoped using the 'path' attribute; and have the 'HttpOnly' and 'Secure' cookie flags enabled. | ✓ | ✓ | ✓ | 3.0 |
| **3.17** | Verify that the application tracks all active sessions. And allows users to terminate sessions selectively or globally from their account.  |  | ✓ | ✓ | 3.0 |
| **3.18** | Verify for high value applications that the user is prompted with the option to terminate all other active sessions after a successful change password process. |  |  | ✓ | 3.1 |
| **3.1** | TBA | ✓ | ✓ | ✓ | 1.0 |


## References

For more information, see also:

* [OWASP Testing Guide 4.0: Session Management Testing](https://www.owasp.org/index.php/Testing_for_Session_Management)
* [OWASP Session Management Cheat Sheet](https://www.owasp.org/index.php/Session_Management_Cheat_Sheet)
