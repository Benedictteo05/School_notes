### Core Principles of Information Security (CIA)

**Confidentiality**
- Rules limiting who has access to information.
- Ensures that only authorized users are able to access information.
- Measures are put in place to prevent data from falling into the hands of people who do not have the authorization to access said information. 
- 3 types of Authentication
	- Something you know.
	- Something you are.
	- Something you have.

**Integrity**
- Rules governing how and when information is modified by authorized users. 
- Ensures that information remains consistent and unaltered.
- Information stored in database, etc. must be protected through access controls and accepted procedure to change the data.
- Measures such as:
	- One way hashes.
	- Password protection using hash function.

**Availability**
- Assurance that people who are authorized to access information are able to do so.
- Ensures that the data, or the system, is available for authorized user when required.
- Ensuring availability requires routine maintenance and upgrading of hardware, software and operating system environments.
- Security incidents that breaches availability:
	- Distributed Denial of Service (DDOS).
	- Maintenance issue. 
		- i.e. server hardware failure
	- Natural disasters. 
		- i.e. fire and flooding

##### CIA Extensions
**Authenticity**
- Ensures that an individual is who he claims to be.

**Non-repudiation**
- Ability to verify a sender had sent the message to a recipient.
- Either party cannot deny later that they did not send or received the message.


### Vulnerability and Threat
**Vulnerability**
- Weakness in an information system, system security procedures, internal controls, or implementation that could be exploited or trigged by a threat source.

**Threat**
- Any circumstance or event with the potential to adversely impact organizational operations (e.g. mission, functions, image, reputation), organizational assets, or individuals through an information system via unauthorized access, destruction, disclosure, modification of information, and/or denial of service.

| Availability Requirements | Explanation |
|--------------------------|--------------|
|Low | There is minimal impact on business if the assets are not available for up to 7 days|
|Medium | There is significant impact on business if assets are not available for up to 48 hours|
|High | The asset is required on a 24/7 basis|

### Operational Model of Security

##### Security equation:
**PROTECTION = PREVENTION + ( DETECTION + RESPONSE )**

- Prevention
	- Access Control, Firewalls, Encryption.
- Detection
	- Audit logs, Intrusion Detection Systems, Honey Pots.
- Response
	- Backups, Incident response team, Computer forensics.

### Approaches to Security
Establishing a set of "best practices" for limiting access can help to secure systems and their data.

- Least Privilege
	- A subject should have only the necessary rights and privileges to perform its task with no additional permissions. 
	- Before an OS is configured, an overall plan should be devised and standardized methods should be developed to ensure that a solid security baseline is actually implemented.

- Separation of Duties
	- Ensures that for any given task, more than one individual needs to be involved. The task is broken into different duties, each of which is accomplished by a separate individual.
	- No single individual can abuse the system for his or her own gain.
	- More than one individual is required when a single person could accomplish the task, thus potentially increasing the cost of the task. 
	- Task proceeding through several steps causes delay.

- Implicit Deny
	- Often a series of rules will be used to determine authorization to specific services for employees. 
	- If a particular situation is not covered by any of the other rules, implicit deny approach states that access should not be granted.

- Mandatory vacations
	- Sensitive positions within an organization, an audit of the employees' activities is usually scheduled while they are away on vacation.
	- This helps to break the daily routine of staff who plans to conduct fraud on a day-to-day basis.

### Security trends and incidents
