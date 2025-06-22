# SRS ChangeLog

### Change 1
#### Description of change
Removed REQ_DC008 from Table 3.73 (Design Constraints), Section 3 (Requirements)
#### Date
2025-06-21
#### Author
Morgan
#### Reason
Conflicts with needs of stakeholders

### Change 2
#### Description of change
Added REQ_SSA0015 to Table 3.74 (Availability), Section 3 (Requirements)
| REQ_SSA015        | The system shall have an offline mode which provides properties of a physical map                     | High         | Goh Chun Yong |
#### Date
2025-06-21
#### Author
Morgan
#### Reason
To fufill needs of stakeholders (End-users)

### Change 3
#### Description of change
Added REQ_SSA0016 to Table 3.74 (Availability), Section 3 (Requirements)
| REQ_SSA016        |         | High         | Goh Chun Yong |
#### Date
2025-06-22
#### Author
Morgan
#### Reason
To fufill needs of stakeholders (University Administration)

### Change 4
#### Description of change  
Changed REQ_UCA005: Rephrased “Admin able to view ongoing and upcoming events, include location of the events.” to “The administrator shall be able to view all ongoing and upcoming events along with their respective locations.”
#### Date  
2025-06-21
#### Author  
Nazim
#### Reason  
To correct grammatical structure and clearly express the scope of the functionality as per formal specification norms.

### Change 5
#### Description of change  
Changed REQ_UCA003: Rephrased “Admin able to modify events to events calendar.” to “The administrator shall be able to update existing events in the event calendar.”
#### Date  
2025-06-21
#### Author  
Nazim
#### Reason  
To clarify action type (“modify”) and correct prepositional error for technical accuracy.

### Change 6
#### Description of change
Changed user characteristics description: Rephrased “Familiar with campus buildings like facilities, and some event locations that relevant to their workplace.” to “Familiar with campus buildings such as Faculties and relevant event locations associated with their workplace.”
#### Date
2025-06-21
#### Author
Nazim
#### Reason
To replace vague and grammatically incorrect expressions with precise and contextually accurate terminology.

### Change 7
#### Description of change  
Changed visitor expectations: Rephrased “Like students.” to “Visitors are expected to possess basic smartphone skills similar to students.”
#### Date  
2025-06-21
#### Author  
Nazim
#### Reason  
To replace a fragment with a full, meaningful sentence clearly stating user capability expectations.

### Change 8
#### Description of change  
Changed REQSQ007: Rephrased “Delete and save changes buttons for desire action.” to “The interface shall show ‘Delete’ and ‘Save Changes’ buttons to allow administrators to perform event update actions.”
#### Date  
2025-06-21
#### Author  
Nazim
#### Reason  
To resolve vague intent and grammar issues by clearly defining UI elements and their purpose in the system.

### Change 9
#### Description of change
Added a new non-functional requirement (REQ_NFR_005) stating that the system must comply with PDPA/GDPR data protection standards for handling user preferences and login information.

#### Date
2025-06-21

#### Author
Amir Hamzah

#### Reason
To address missing legal and privacy compliance requirements in the original SRS.

### Change 10
Description of change
Introduced error handling requirements to describe how the system behaves during GPS signal loss, login failure, or service unavailability.

#### Date
2025-06-21

#### Author
Amir Hamzah

#### Reason
To ensure the system defines behavior for failure conditions and provides fallback mechanisms.

### Change 11
#### Description of change
Clarified guest user behavior by listing restricted features (e.g., event sign-up, feedback submission) and updating relevant use case flow.

#### Date
2025-06-21

#### Author
Amir Hamzah

#### Reason
To resolve ambiguity around guest user capabilities, ensuring functional coverage.

### Change 12
#### Description of change
Added REQ_FN_011 detailing when push notifications are sent (e.g., confirmed obstacle reports, updated events, facility outages).

#### Date
2025-06-21

#### Author
Amir Hamzah

#### Reason
To address the absence of functional triggers for push notification behavior.

### Change 13
#### Description of change
Added REQ_NFR_006 specifying that the UI must conform to WCAG 2.1 Level AA standards and support assistive features like screen readers and high-contrast modes.

#### Date
2025-06-22

#### Author
Amir Hamzah

#### Reason
To ensure compliance with accessibility standards critical for the system’s target users.

### Change 14
#### Description of change
Refined REQ_CRN_005 from “user-friendly” to a measurable requirement using UI heuristics: “The map interface shall allow users to find accessible routes within 3 clicks, with an average error rate of less than 10%.”

#### Date
2025-06-21

#### Author
Amir Hamzah

#### Reason
To make the requirement testable and align it with SMART criteria for usability.

### Change 15
#### Description of change
Corrected REQ_IO0703 to move “Toggle switch” from input field description to output display specification under system UI elements.

#### Date
2025-06-21

#### Author
Amir Hamzah

#### Reason
To resolve a classification error between input and output components in interface documentation.

### Change 16
#### Description of change
Resolved inconsistency between REQ_PR0009 and REQ_PR0014 by standardizing all real-time updates to reflect within 5 seconds under normal load, and allowing fallback up to 10 seconds under high load.

#### Date
2025-06-21

#### Author
Amir Hamzah

#### Reason
To fix conflicting requirements and provide a unified performance expectation.

### Change 17
#### Description of change
Added a requirement for disability-specific route customization: “The system shall allow users to select mobility preferences (e.g., avoid stairs, prefer ramps) which impact route calculation.”

#### Date
2025-06-21

#### Author
Amir Hamzah

#### Reason
To fulfill an implied accessibility feature based on the system’s inclusive navigation goals.

### Change 18 
#### Description of change  
Expanded REQ_ADMIN_003 to specify the exact system behavior after an administrator confirms a report. The system now updates the map, recalculates affected routes, sends notifications to impacted users, and logs the admin's action for traceability.  
#### Date  
2025-06-22  
#### Author  
Amir Hamzah  
#### Reason  
To fully describe the workflow and downstream effects of administrator confirmations based on the actual feedback management process.


### Change 19
#### Description of change
Included feedback handling workflow: admin can mark feedback as “resolved,” “in progress,” or “rejected,” and optionally reply to users.

#### Date
2025-06-21

#### Author
Amir Hamzah

#### Reason
To complete the feedback system logic and improve response transparency.

### Change 20
#### Description of change
Inserted a multi-language support requirement: “The application shall support at least English, Malay, and Mandarin languages, selectable at login.”

#### Date
2025-06-21

#### Author
Amir Hamzah

#### Reason
To accommodate diverse user backgrounds within the university community.

### Change 21
#### Description of change
Added integration error-handling behavior: “If facility or event APIs are unavailable, the system shall display a message and cache the last known data for up to 24 hours.”

#### Date
2025-06-21

#### Author
Amir Hamzah

#### Reason
To define system behavior during third-party system downtime and improve resilience.

