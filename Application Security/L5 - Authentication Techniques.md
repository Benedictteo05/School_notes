### Types of authentication methods
- What a user knows (knowledge)
	- Password
	- Pin
- What a user has (possession)
	- NRIC, Passport
	- [[L5 - Authentication Techniques#^183ff1|OTP (One time password)]]
- What a user is (inherence)
	- Standard biometrics
		- e.g. Fingerprints, Retina, Face
	- Behavioral biometrics
		- Keystroke dynamics;
		- Voice recognition
		- Computer foot printing
		- Gait (Pattern of movement)
	- Cognitive biometrics
		- Memorable events
		- Identify specific faces

### Outdated Web authentication methods
- What you know 
	- Old authentication methods such as login & passwords is no longer suffice due to common web vulnerabilities as well as the growing sophistication of hacking tools.
	- More than 1 person may gain access to the same account due to:
		- Illegal sharing of account
		- Stealing of accounts

### Attacks on Authentication System
**Attacks**
- XSS attacks
- Brute-force attempts using bots
- SQL injection attack
- Multiple login attempts from a single IP

### Preventive measures to protect Authentication System
**Prevention**
- Limiting the frequency of online login attempts to an account through various actions:
	- Enforcing multi-factor authentication, Anti-bots (e.g. CAPTCHA), or other forms of verification.
	- Locking an account after a specified number of login attempts is reached.
	- Prohibiting multiple sessions for single user and location-based verification.

### Multi-factor Authentication
- Granting access to a website or application by presenting two or more pieces of evidence (or factors) to an authentication mechanism:
	- Knowledge 
	- Possession
	- Inherence
- Implement multi-factor authentication to prevent automated (bot), credential stuffing, brute force, and stolen credential re-user attacks.

### 2-Factor Authentication (2FA)
^183ff1
- e.g. An online banking system where a login control (what you know) required a second factor authentication such as SMS/Token/Email/etc (possession).
- Is 2FA required for all websites

**Steps for 2FA (SMS OTP)**
1. System verifies userid and password
2. System generates 6 digits SMS OTP to user
	- Save a copy of OTP values and date/time created in db
3. System prompts user for OTP
4. System check if OTP entered is valid
	- Valid if OTP matches the one save in db
	- if OTP matches, check if OTP is received before the expired date/time
5. If user request OTP again due to timeout, repeat (step 2 - 4)
6. System create session and redirect to homepage

**Authenticator App**
- Free security app that can protect your account (e.g. Google, Microsoft, Website) against password theft.
- The Authenticator app (IOS/Android) generates a random code used to verify your identity when you're logging into various services.

### Attacks on Login Form
- Recommended to have a more generalized warning message like "Invalid login".
- Instead of "username does not exist" or "Wrong password".
- Brute force using bots.
	- An attempt to crack a password using a trial and error approach and hoping, eventually, to guess correctly.
	- Using a tool such as **Burp Intruder** in Burp Suite, hacker would load a list of possible usernames and cycle through HTTP POST requests to the login form examining the response.
	- A HTTP response that matches "invalid password" indicates the username is valid. Hacker could then move onto attacking the password using the same process with a common password list.

### CAPTCHA
- Completely Automated Public Turing test to tell Computer and Humans Apart.
- Created at Carnegie Mellon University in 2000.
- Websites need CAPTCHAs to guard against the "bots" of spammers and other computer underworld types.

**Types of CAPTCHA:**
- Text-Based Captcha
- Invisible ReCaptcha
- Mathematical Captcha
- Image-Based Captcha
- Interactive Captcha

### Account Lockout
- To disable user account if consistently receive high login failures.
- Allow locked account to be recovered.
	- Automatically after certain duration.
	- Manually using Web forms with user challenge.
- Fail-safe rule

### Prevention multiple session on single account
- To deter the ability for users to overlap sessions for a single user account.
- Send warning notifications to affected users and close either sessions.
- Monitor against database stored session to detect overlapping.