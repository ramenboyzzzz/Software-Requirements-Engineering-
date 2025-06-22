# Agreement Defects  

## Defect 1:
### Stakeholder: EndUsers
### Description:

As per REQ_DC008 in Table 3.73 (Design Constraints), offline mode will not be supported.
The questionnaire results (Section 3.8.1) indicate that stakeholders consider availability to be very important. Section 3.1 (Functions) ommited solutions to mitigate this availability concern, and a temporary solution is instead used to compensate.

### Possible Root Cause:
The engineers overemphasized on data validation to ensure users don't receive outdated information, leading to an oversight in considering the system's operational requirements for maintaining its availability.

## Defect 2:
### Stakeholders: University Admin
### Description:

As detailed in Section 3.1 (Functions), several critical operations within the system's functionalities are contingent upon human input. These include, but are not limited to, 3.1.1.6 Administrator add event, 3.1.1.7 Administrator edit event, 3.1.1.8 Administrator view users’ feedback, and 3.1.1.9 Administrator confirming report. A probable concern from the university regarding the potential resources required to consistently maintain the information validity of the system, given the manual nature of these functions.

### Possible Root Cause:
As stated in REQ_DC002 in Section 3.6 (Design Constraints), Table 3.73 (Design Constraints), "The application shall rely on real-time campus infrastructure data (e.g., elevators, pathways), which may be constrained by sensor availability and network latency". The university's IoT infrastructure is acknowledged, but there is a lack of functional solutions to reduce human dependency.

# Documentation Defects
## Defect 1:
### Conflict Type: Ambiguity in Requirement Statement

### Original Statement:
"Admin able to view ongoing and upcoming events, include location of the events."

### Description of Conflict:
It is in Use case REQ_UCA005
The sentence has structural issues and unclear intent about the inclusion of location data.

### Possible Root Cause:
Poor sentence construction and inconsistent phrasing.

## Defect 2:
### Conflict Type: Ambiguity in Requirement Statement

### Original Statement:
"Admin able to modify events to events calendar."

### Description of Conflict:
It is in Use case REQ_UCA003
The use of “to” is incorrect, and the sentence structure is unclear about intended functionality.

### Possible Root Cause:
Improper grammar and lack of formal language in requirement writing.

## Defect 3:
### Conflict Type: Ambiguity in Requirement Statement

### Original Statement:
"Familiar with campus buildings like facilities, and some event locations that relevant to their workplace."

### Description of Conflict:
It is in table 1.5 column 3 row 4
The sentence is grammatically incorrect and uses vague terminology ("facilities"), could also be a typo and facilities is faculties.

### Possible Root Cause:
Improper grammar and lack of formal language in requirement writing.

## Defect 4:
### Conflict Type: Ambiguity in Requirement Statement

### Original Statement:
"Like students."

### Description of Conflict:
It is in table 1.5 column 3 row 5
Entirely unclear and incomplete; lacks any actionable meaning.

### Possible Root Cause:
Placeholder or shorthand left unrefined in final documentation.

## Defect 5:
### Conflict Type: Ambiguity in Requirement Statement

### Original Statement:
"Delete and save changes buttons for desire action."

### Description of Conflict:
It is in table 3.7 column 2 row 5 line 4
The phrase "desire action" is incorrect, and the overall sentence is unclear regarding UI functionality.

### Possible Root Cause:
Informal grammar and vague terminology in describing user interface elements.

# SRS ChangeLog

## Morgan
### Change 1
- Removed REQ_DC008 from Table 3.73 (Design Constraints), Section 3 (Requirements)

### Change 2
- Added REQ_SSA002 to Table 3.74 (Availability), Section 3 (Requirements)
- REQ_SSA002 | The system shall have an offline mode which provides properties of a physical map | High | Morgan

