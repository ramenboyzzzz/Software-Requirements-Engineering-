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
As stated in REQ_DC002 in Section 3.6 (Design Constraints), Table 3.73 (Design Constraints), The application shall rely on real-time campus infrastructure data (e.g., elevators, pathways), which may be constrained by sensor availability and network latency. The university's IoT infrastructure is acknowledged, but there is a lack of functional solutions to reduce human dependency.