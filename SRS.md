**CSE6224 SOFTWARE REQUIREMENTS ENGINEERING**

![A black background with a black square AI-generated content may be
incorrect.](media/image1.png){width="3.96875in" height="1.15625in"}

**Tutorial Section: TT3L**

**Group No.: G3**

| **Chang Hoe Hin** | **241UC2415N** |
|-------------------|----------------|
| **Tee Kah Le**    | **241UC2414Z** |
| **Yee Si Shun**   | **241UC24157** |
| **Goh Chun Yong** | **241UC24158** |

Table of Contents

[1. Introduction [2](#introduction)](#introduction)

[1.1 Purpose [3](#purpose)](#purpose)

[1.2 Scope [3](#scope)](#scope)

[1.3 Product Overview [6](#product-overview)](#product-overview)

[1.3.1 Product Perspective
[7](#product-perspective)](#product-perspective)

[1.3.2 Product Functions [10](#product-functions)](#product-functions)

[1.3.2.1 End Users [10](#end-users)](#end-users)

[1.3.2.2 Admin [12](#admin)](#admin)

[1.3.3 User Characteristics
[13](#user-characteristics)](#user-characteristics)

[1.3.4 Limitations [13](#limitations)](#limitations)

[1.4 Definitions [14](#definitions)](#definitions)

[2. References [14](#references)](#references)

[3. Requirements [16](#requirements)](#requirements)

[3.1 Functions [17](#functions)](#functions)

[3.1.1 Sequence Diagram [17](#sequence-diagram)](#sequence-diagram)

[3.1.1.1 User Sign In [17](#user-sign-in)](#user-sign-in)

[3.1.1.2 Search location [18](#search-location)](#search-location)

[3.1.1.3 Show event calendar
[19](#show-event-calendar)](#show-event-calendar)

[3.1.1.4 Show event list [20](#show-event-list)](#show-event-list)

[3.1.1.5 Write Feedback/Report
[21](#write-feedbackreport)](#write-feedbackreport)

[3.1.1.6 Administrator add event
[23](#administrator-add-event)](#administrator-add-event)

[3.1.1.7 Administrator edit event
[24](#administrator-edit-event)](#administrator-edit-event)

[3.1.1.8 Administrator view users' feedback
[25](#administrator-view-users-feedback)](#administrator-view-users-feedback)

[3.1.1.9 Administrator confirming report
[26](#administrator-confirming-report)](#administrator-confirming-report)

[3.1.1.10 Route navigation [28](#route-navigation)](#route-navigation)

[3.2 Performance Requirements
[29](#performance-requirements)](#performance-requirements)

[3.3 Usability Requirements
[30](#usability-requirements)](#usability-requirements)

[3.4 Interface Requirements
[31](#interface-requirements)](#interface-requirements)

[3.4.1 External Interfaces
[32](#external-interfaces)](#external-interfaces)

[3.4.1.1 IO01 Login Page [32](#io01-login-page)](#io01-login-page)

[3.4.1.2 IO02 Navigation Page
[32](#io02-navigation-page)](#io02-navigation-page)

[3.4.1.3 IO03 Report Obstacle Page
[33](#io03-report-obstacle-page)](#io03-report-obstacle-page)

[3.4.1.4 IO04 Admin Event Dashboard Page
[34](#io04-admin-event-dashboard-page)](#io04-admin-event-dashboard-page)

[3.4.1.5 IO05 Submit Feedback Page
[35](#io05-submit-feedback-page)](#io05-submit-feedback-page)

[3.4.1.6 IO06 Travel Mode Option Page
[35](#io06-travel-mode-option-page)](#io06-travel-mode-option-page)

[3.4.1.7 IO07 Navigation Map Page
[36](#io07-navigation-map-page)](#io07-navigation-map-page)

[3.4.1.8 IO08 Navigation Map Sub Page
[37](#io08-navigation-map-sub-page)](#io08-navigation-map-sub-page)

[3.4.1.9 IO09 Event Calendar Page
[38](#io09-event-calendar-page)](#io09-event-calendar-page)

[3.4.1.10 IO10 Admin Feedback Dashboard Page
[39](#io10-admin-feedback-dashboard-page)](#io10-admin-feedback-dashboard-page)

[3.4.2 System Interfaces [40](#system-interfaces)](#system-interfaces)

[3.4.3 User Interfaces [40](#user-interfaces)](#user-interfaces)

[3.4.4 Hardware Interfaces
[41](#hardware-interfaces)](#hardware-interfaces)

[3.4.5 Software Interfaces
[41](#software-interfaces)](#software-interfaces)

[3.4.6 Communications interface
[41](#communications-interface)](#communications-interface)

[3.5 Logical database requirements
[42](#logical-database-requirements)](#logical-database-requirements)

[3.5.1 Class Diagram [43](#class-diagram)](#class-diagram)

[3.5.2 ERD [48](#erd)](#erd)

[3.5.1 University [48](#university)](#university)

[3.5.2 User [49](#user)](#user)

[3.5.3 Admin [49](#admin-1)](#admin-1)

[3.5.4 Location [49](#location)](#location)

[3.5.5 Event [49](#event)](#event)

[3.5.6 Facility [50](#facility)](#facility)

[3.5.7 Alert [50](#alert)](#alert)

[3.5.8 Route [50](#route)](#route)

[3.5.9 Feedback [51](#feedback)](#feedback)

[3.5.10 Confirmed Report [51](#confirmed-report)](#confirmed-report)

[3.6 Design Constraints [51](#design-constraints)](#design-constraints)

[3.7 Software System Attributes
[52](#software-system-attributes)](#software-system-attributes)

[3.7.1 Availability [52](#availability)](#availability)

[3.7.2 Reliability [52](#reliability)](#reliability)

[3.7.3 Security [53](#security)](#security)

[3.7.4 Maintainability [53](#maintainability)](#maintainability)

[3.7.5 Portability [53](#portability)](#portability)

[3.8 Supporting Information
[54](#supporting-information)](#supporting-information)

[3.8.1 Questionnaire [54](#questionnaire)](#questionnaire)

[3.8.2 Prototyping [64](#prototyping)](#prototyping)

[4. Verification [75](#verification)](#verification)

[4.1 Verification Approach
[76](#verification-approach)](#verification-approach)

[How [76](#how)](#how)

[Who [76](#who)](#who)

[When [76](#when)](#when)

[Where [77](#where)](#where)

[4.2 Verification Criteria
[77](#verification-criteria)](#verification-criteria)

[5. Appendices [78](#appendices)](#appendices)

[5.1 Assumptions and dependencies
[79](#assumptions-and-dependencies)](#assumptions-and-dependencies)

[5.2 Acronyms and Abbreviations
[80](#acronyms-and-abbreviations)](#acronyms-and-abbreviations)

# Introduction

## 1.1 Purpose {#purpose .unnumbered}

The purpose of the Campus Route Navigator (CRN) mobile application is to
provide real-time, accessibility-focused navigation across the
university campus. This software is designed to support individuals with
mobility challenges, such as wheelchair users, elderly individuals, and
those recovering from injury, by offering safe, inclusive, and optimized
route planning.

This application serves as an assistive tool that integrates with the
university's existing Facilities Management System and Event Calendar
System to dynamically reroute users based on live updates such as
elevator outages, construction zones, and event-related closures. The
CRN also empowers users to submit feedback or report obstacles,
improving the platform's responsiveness and adaptability over time.

The key purposes of the CRN are:

- To ensure every member of the university community can move
  independently and safely across the campus.

- To provide the fastest route between the user's current location to
  the desired location avoiding unwanted events (considering events like
  construction, elevator outages and temporary accommodations for
  events.)

- To provide personalized navigation based on individual accessibility
  needs and preferences and real-time campus conditions.

- To provide the listing of all the events that are happening and will
  happen in campus.

- To assist in decision-making by delivering current updates on physical
  barriers and route disruptions by listing all the available routes
  between the user's current location and desired destination.

- To enhance access to campus resources by allowing users to discover
  the availability of the facilities and accessibility of campus events
  with the events details directly from the app.

- To support continuous system improvement through user feedback
  mechanisms and usage analytics.

- To provide a platform for members to provide information about what is
  happening on the campus and report obstacles and submit feedback to
  the CRN.

This software operates as a mobile-only platform, available for Android
and iOS devices, and requires institutional login credentials to ensure
secure and personalized access.

## 1.2 Scope {#scope .unnumbered}

The Campus Route Navigator (CRN) is a mobile-only application designed
to improve campus accessibility by providing real-time, personalized
navigation for individuals with mobility challenges. Operating on both
Android and iOS devices, the system is intended to be used by students,
staff, faculty, and visitors of the university who require assistance
navigating around campus in a safe, efficient, and inclusive manner.

The CRN integrates with existing university systems, specifically the
Facilities Management System and the Event Calendar System, to deliver
real-time updates related to construction areas, elevator outages, and
event-related closures. The system dynamically recalculates routes to
reflect current campus conditions, ensuring that users are always
provided with the safest and most accessible pathways.

**Campus Route Navigator will be able to perform the following
functions:**

1.  *[Provide Accessible Route Planning Across Campus]{.underline}*

Generation of optimal navigation paths between two locations on campus,
tailored to individual accessibility preferences (e.g., avoiding stairs,
steep slopes).

2.  *[Provide Real-Time Updates]{.underline}*

> Integration with live data sources to reflect dynamic changes such as
> construction, maintenance, or temporary inaccessibility.

3.  *[Facility Access Integration]{.underline}*

> Allowing users to view available campus facilities and check their
> accessibility status.

4.  *[Event Integration]{.underline}*

Providing details about ongoing and upcoming campus events, along with
accessible routes and accommodations.

5.  *[Feedback and Reporting Mechanisms]{.underline}*

Enabling users to report issues like blocked ramps, inaccessible areas,
or other obstacles encountered during navigation.

6.  *[User Preferences]{.underline}*

Support for user-defined mobility preferences that influence route
planning.

7.  *[Admin Dashboard]{.underline}*

A separate administrative interface (not part of the mobile app) for
reviewing feedback, managing reports, and analysing system usage.

The CRN aims to provide a highly specialized, context-aware navigation
experience that improves campus inclusivity and empowers individuals
with diverse mobility needs to participate fully in campus life. Through
continuous feedback collection and seamless system integration, CRN
supports the university's commitment to digital accessibility and
user-cantered design.

The CRN system interacts with various user groups and integrates with
external institutional systems to ensure effective, real-time,
accessibility-aware campus navigation. Below is a detailed list of the
primary stakeholders and external systems involved in the operation of
CRN:

1.  Students, Staff, and Visitors (End Users)

- Role: Primary users of the mobile application.

- Responsibilities:

  - Use the app for real-time navigation across campus.

  - Customize accessibility preferences for personalized route planning.

  - Provide real-world feedback, report accessibility issues (e.g.,
    blocked ramps, faulty elevators), and suggest improvements to the
    system.

- Importance: Their interactions drive the core functionality and
  continuous improvement of the system.

2.  University Events Calendar System

- Role: External system integrated with CRN.

- Responsibilities:

  - Supplies real-time data on upcoming and ongoing university events.

  - Provides information on temporary changes in access (e.g., venue
    closures, roadblocks, or crowd control).

  - Offers details on special accessibility arrangements (e.g.,
    accessible seating, alternative entrances).

- Importance: Enables dynamic event-aware rerouting and enhances
  participation in campus activities.

3.  University Facilities Management System

- Role: External system integrated with CRN.

- Responsibilities:

  - Delivers real-time updates on infrastructure changes, including:

  - Construction areas,

  - Maintenance activities,

  - Elevator functionality and outages.

- Importance: Provides essential input for dynamic routing to avoid
  inaccessible or disrupted areas.

4.  Campus Maps and Infrastructure Plans

- Role: Foundational data source.

- Responsibilities:

  - Provides detailed digital layouts of:

  - Building locations,

  - Entrances and exits,

  - Elevators and staircases,

  - Ramps and pathways.

<!-- -->

- Importance: Forms the basis for generating and optimizing accessible
  route paths within the mobile application.

5.  University Administration and IT Department

- Role: System management and oversight.

- Responsibilities:

  - Manage and maintain system integration with campus databases and
    services.

  - Ensure user account creation, access control, and authentication
    using institutional credentials.

  - Update facility and event data sources regularly.

  - Monitor data security, privacy compliance, and system reliability.

- Importance: Ensures the system remains secure, updated, and aligned
  with university infrastructure and digital policies.

## 1.3 Product Overview {#product-overview .unnumbered}

### 1.3.1 Product Perspective {#product-perspective .unnumbered}

This section provides an overview of the Campus Route Navigator (CRN)
--- a mobile-exclusive application developed to enhance real-time,
accessibility-focused navigation across the university campus. It is
specifically tailored for individuals with mobility challenges,
including wheelchair users, elderly individuals, and those recovering
from injury, ensuring they can move around campus independently, safely,
and efficiently.

The CRN application leverages smart routing algorithms and real-time
data integration to provide safe, dynamic, and inclusive routes. By
combining static map infrastructure with live updates from Facilities
Management and Event Management systems, CRN adapts instantly to
changing campus conditions such as construction work, elevator outages,
and event-related closures, enabling barrier-free movement.

![](media/image2.png){width="3.2898042432195975in"
height="5.3437084426946635in"}

**Figure 1.1: System Overview Diagram**

**Mobile-Exclusive Platform:**

As a **mobile-only solution**, CRN is available on both **Android and
iOS** smartphones. Users authenticate through **institutional
credentials**, which enables personalized access and route customization
based on individual accessibility preferences.

Once logged in, users access an **interactive, map-based interface**
that provides step-by-step directions along accessible routes,
highlights temporary obstacles, and offers alternative paths as needed.

**Relationship to Larger System:**

The CRN is an integrated module within the university\'s broader mobile
service ecosystem, which includes digital campus services such as campus
maps, student/staff portals, notification systems, facilities data, and
event coordination tools. CRN extends these services by focusing
specifically on **accessible navigation**.

Key enhancements provided by CRN include:

- **Accessibility-aware routing** based on user preferences and physical
  mobility requirements.

- **Live data integration** with construction updates and elevator
  outage reports.

- **Event-aware navigation**, offering reroutes and temporary
  accessibility accommodations.

- **Feedback collection** from users to support continuous system
  improvement.

**Core Functionalities of CRN (Mobile App):**

**Table 1.1: Core Functionalities**

| **Feature**                                  | **Description**                                                                                                                                            |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Mobile-Based Accessible Route Planning**   | Users can select origin, and destination points to receive optimized routes that avoid stairs, steep slopes, or inaccessible paths.                        |
| **Real-Time Campus Condition Updates**       | CRN integrates with the Facilities Management system to receive real-time updates on construction, maintenance, and elevator outages.                      |
| **Event-Aware Navigation**                   | Uses the university\'s Event Calendar system to detect and reroute around temporary event setups, crowds, and accessibility arrangements.                  |
| **User Feedback Reporting**                  | Users can report route obstacles, issues, or make suggestions through the app. These reports influence live updates and future improvements.               |
| **Personalized Accessibility Preferences**   | Users can set personal navigation preferences (e.g., avoid steep slopes, prefer wide walkways) for more tailored guidance.                                 |
| **Facility and Event Access**                | Users can check real-time facility availability (e.g., accessible toilets, study areas) and see a live listing of ongoing or upcoming campus events.       |
| **Admin and Analytics Dashboard (Back-End)** | Campus administrators can use a web-based back-end system to monitor user engagement, manage feedback, and analyse trends to improve campus accessibility. |

![](media/image3.png){width="6.260415573053368in"
height="5.97916447944007in"}

**Figure 1.2: System Context Diagram**

Aligned with the university's mission to promote digital inclusion,
**Campus Route Navigator (CRN)** ensures that all members of the
university community --- particularly those with physical disabilities
--- can access timely, safe, and inclusive navigation services directly
from their mobile devices. It addresses the **project purpose** of
enabling safe, inclusive, and real-time campus navigation and aligns
with the **project scope** by:

- Offering personalized, mobile-based navigation to users with mobility
  needs.

- Integrating with campus facilities and event systems to respond
  dynamically to real-world disruptions.

- Providing a user-centric feedback loop to enhance system
  responsiveness and adaptability.

- Ensuring campus members can independently plan and complete safe
  routes, access events, and locate accessible facilities in real time.

**Table 1.2: Goals of the System**

| **Requirement ID** | **Goals**                                                                                                                   | **Author** |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------|------------|
| REQ_CRN_001        | The system shall make campus navigation easy and accessible for everyone.                                                   | Chun Yong  |
| REQ_CRN_002        | The system shall ensure all users can move around campus safely and efficiently.                                            | Chun Yong  |
| REQ_CRN_003        | The system shall provide real-time updates on accessibility issues to help users make better navigation decisions.          | Chun Yong  |
| REQ_CRN_004        | The system shall allow users to report encountered problems and submit suggestions.                                         | Chun Yong  |
| REQ_CRN_005        | The system shall provide an interactive, user-friendly map-based navigation interface.                                      | Chun Yong  |
| REQ_CRN_006        | The system shall allow users to access available campus facilities through integration with the facilities system.          | Chun Yong  |
| REQ_CRN_007        | The system shall allow users to view current campus events and receive relevant event-based navigation updates.             | Chun Yong  |
| REQ_CRN_008        | The system shall generate personalized navigation routes based on user accessibility preferences (e.g., avoid stairs).      | Chun Yong  |
| REQ_CRN_009        | The system shall enable secure login using institutional credentials to ensure user data privacy and personalized access.   | Chun Yong  |
| REQ_CRN_010        | The system shall dynamically reroute users in response to live data such as elevator outages, construction, or event zones. | Chun Yong  |
| REQ_CRN_011        | The system shall support continuous improvement by analysing user feedback and navigation data.                             | Chun Yong  |

### 1.3.2 Product Functions {#product-functions .unnumbered}

![](media/image4.png){width="6.260415573053368in"
height="4.489583333333333in"}**Figure 1.3: Use Case Diagram of CRN**

#### 1.3.2.1 End Users {#end-users .unnumbered}

![](media/image5.png){width="5.95833552055993in"
height="6.260415573053368in"}

**Figure 1.4: Use Case Diagram of Actor (End Users)**

**Table 1.3: Use Case Diagram of Actor (End Users)**

| **Use Case ID** | **Use Case Name**                   | **Description**                                                                       | **Author**    |
|-----------------|-------------------------------------|---------------------------------------------------------------------------------------|---------------|
| REQ_UCEU001     | Set Preference                      | Tailor navigation to individual accessibility needs.                                  | CHANG HOE HIN |
| REQ_UCEU002     | Report Obstacles                    | Notify campus authorities about accessibility issues.                                 | CHANG HOE HIN |
| REQ_UCEU003     | Submit feedback                     | Share user experiences to enhance system functionality.                               | CHANG HOE HIN |
| REQ_UCEU004     | Enter destination/starting location | Able to plan routes efficiently.                                                      | CHANG HOE HIN |
| REQ_UCEU005     | Log Out                             | Allow end users to log out.                                                           | CHANG HOE HIN |
| REQ_UCEU006     | Log in                              | Allow end users to securely log in into the platform and access personal preferences. | CHANG HOE HIN |
| REQ_UCEU007     | View Events                         | Allow end users to view ongoing and upcoming events, include location of the events.  | CHANG HOE HIN |
| REQ_UCEU008     | View campus facilities              | Access details about facilities and check their accessibility status.                 | CHANG HOE HIN |

#### 1.3.2.2 Admin {#admin .unnumbered}

![](media/image6.png){width="6.072915573053368in" height="5.21875in"}

**Figure 1.5: Use Case Diagram of Actor (Admin)**

**Table 1.4: Use Case Diagram of Actor (Admin)**

| **Use Case ID** | **Use Case Name**           | **Description**                                                                 | **Author**    |
|-----------------|-----------------------------|---------------------------------------------------------------------------------|---------------|
| REQ_UCA001      | Review feedback             | Administrator can access and review feedback submitted by end users.            | CHANG HOE HIN |
| REQ_UCA002      | Validate End Users' reports | Verify the accuracy of reported obstacles                                       | CHANG HOE HIN |
| REQ_UCA003      | Edit events                 | Admin able to modify events to events calendar.                                 | CHANG HOE HIN |
| REQ_UCA004      | Add events                  | Admin able to add events to events calendar.                                    | CHANG HOE HIN |
| REQ_UCA005      | View events                 | Admin able to view ongoing and upcoming events, include location of the events. | CHANG HOE HIN |
| REQ_UCA006      | Log Out                     | Allow admin to log out.                                                         | CHANG HOE HIN |
| REQ_UCA007      | Log In                      | Allow admin to securely log in into the platform.                               | CHANG HOE HIN |

### 1.3.3 User Characteristics {#user-characteristics .unnumbered}

This section describes the basic understanding and expected knowledge
from end users of the system as it will affect **CRN** software
performance. The following table illustrates the expected level for each
role.

**TABLE 1.5: User Characteristics**

| **Role**                             | **Consideration**                 | **Expected Knowledge**                                                                                     |
|--------------------------------------|-----------------------------------|------------------------------------------------------------------------------------------------------------|
| Students                             | Basic Smartphone Usage            | Know how to download and basic use of mobile applications.                                                 |
|                                      | General Digital Literacy          | Use search engine for information online and interaction with digital services.                            |
| Faculty and Staff                    | Moderate Digital Literacy         | Able to use digital tools like email for work and communication                                            |
|                                      | Familiarity with Campus Resources | Familiar with campus buildings like facilities, and some event locations that relevant to their workplace. |
| Visitors                             | Basic Smartphone Usage            | Like students                                                                                              |
|                                      | Limited or No Campus Familiarity  | Expected no knowledge of campus layout at all.                                                             |
| Administrators and Campus Management | High Digital Literacy             | Proficient use of various software applications.                                                           |
|                                      | Comprehensive Campus Knowledge    | Deep understanding campus of structure                                                                     |
|                                      | System-Specific Knowledge         | Require training to know how to interact with system interface.                                            |

### 1.3.4 Limitations {#limitations .unnumbered}

CRN faces also several limitations that could impact its functionality
and effectiveness. These include:

**1)Accuracy and Completeness of Data:**

- **Map Data:** The accuracy of the base map and the overlays for
  accessible routes and features will depend on the available data and
  the effort put into mapping.

- **Facility Information:** Heavily reliance regular updates from
  facility management. Information could be outdated or incomplete.

- **Event Information:** Not all events might have detailed
  accessibility information available.

**2)Real-time Updates:**

- **Dynamic Obstacles:** Construction, spills, or unexpected closures
  are no way to record unless there\'s a mechanism for immediate
  reporting and updating.

- **Event Changes:** Last-minute event changes or cancellations might
  not be reflected instantly in the system.

**3)Indoor Navigation Accuracy:**

- GPS signals are often weak or unavailable indoors.

**4)Network Dependency:**

- Functionality might be limited or unavailable in areas with poor
  connectivity as software performance depends on stable connectivity.

## 1.4 Definitions {#definitions .unnumbered}

Below are terms, phrases and words used in the document and its related
definition:

**Table 1.6: Definition**

| **Terms**                       | **Definition**                                                                                       |
|---------------------------------|------------------------------------------------------------------------------------------------------|
| Campus Route Navigator / CRN    | A digital platform that provides navigation system for campus and provides event info's.             |
| End Users                       | Includes faculty, staff, visitor and student.                                                        |
| Institutional Login Credentials | ID and password provided by university.                                                              |
| Live Data Sources               | Databases that provide real-time or near-real-time information.                                      |
| User-centered                   | System whose designs is based on the ways that people will use them and what they will do with them. |
| Dynamic Routing                 | Automatically choose preferred route depends on current conditions such as congestion, availability. |

# References

International Organization for Standardization, International
Electrotechnical Commission, & Institute of Electrical and Electronics
Engineers. (2018). \*Systems and software engineering --- Life cycle
processes --- Requirements engineering\* (Second edition). ISBN
978-1-5044-5302-8.

Roylance, J. (2023, 2 Mar). \*Campus design for access and inclusion\*
Retrieved from
<https://www.timeshighereducation.com/campus/campus-design-access-and-inclusion>

USA Wazeopedia. (2024, Dec 6). \*Android User Manual v2 (obsolete)\*
Retrieved from
<https://www.waze.com/discuss/t/android-user-manual-v2-obsolete/377755/2>

Bragg, L. (2021, Sep 22). \*Implementing a successful campus navigation
app\* Retrieved from
<https://www.mappedin.com/resources/blog/implementing-a-successful-campus-navigation-app/>

Tahir, R. Krogstie, J. (2023) \*Challenges in indoor-outdoor Campus
wayfinding using mobile navigation apps (Google Maps and Maze Map). \*
Retrieved from
<https://www.researchgate.net/figure/Challenges-in-indoor-outdoor-campus-wayfinding-using-mobile-navigation-apps-Google-Maps_fig2_373352977>

# Requirements

## 3.1 Functions {#functions .unnumbered}

This section described each functional requirement that the system must
perform by the end of development. Each functional requirement will be
detailed and supported with a sequence diagram.

###  3.1.1 Sequence Diagram {#sequence-diagram .unnumbered}

#### 3.1.1.1 User Sign In {#user-sign-in .unnumbered}

**Table 3.1: User Sign In**

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 24%" />
<col style="width: 25%" />
<col style="width: 24%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>ID</strong></th>
<th colspan="2">REQSQ001</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td>Sign In Account</td>
<td><strong>Version</strong></td>
<td>1.0</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Purpose</strong></td>
<td colspan="2">To allow end users to login or continue as guest</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Actor</strong></td>
<td colspan="2">User (Student / Visitor / University Staff /
Administrator)</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Precondition</strong></td>
<td colspan="2">Enter ID and password</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Postcondition</strong></td>
<td colspan="2">The end user will be logged into the system and the
system will display the current location map navigation model (Initial
page of the system).</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Main Flow</strong></td>
<td colspan="2"><ol type="1">
<li><p>Actor navigates to login Page</p></li>
<li><p>System displays the login Page</p></li>
<li><p>Actor fills in and submits their login credentials</p></li>
<li><p>System verified and submitted information</p></li>
<li><p>System authenticates the user into the system</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Alternate Scenario</strong></td>
<td colspan="2"><ol type="1">
<li><p>If the ID or password are invalid, the system displays an error
message for invalid information</p></li>
<li><p>When the fields are empty, the system will display an error
message</p></li>
</ol></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Author</strong></td>
<td colspan="2">YEE SI SHUN</td>
</tr>
</tbody>
</table>

![](media/image7.png){width="6.114584426946632in"
height="6.260415573053368in"}

**Figure 3.1: User Sign In Sequence Diagram**

#### 3.1.1.2 Search location {#search-location .unnumbered}

**Table 3.2: Search Location**

<table>
<colgroup>
<col style="width: 24%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 24%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>ID</strong></th>
<th colspan="2">REQSQ002</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td>Search destination</td>
<td><strong>Version</strong></td>
<td>1.0</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Purpose</strong></td>
<td colspan="2">Allows users to search for locations within the
campus.</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Actor</strong></td>
<td colspan="2">User (Student / Visitor / University Staff /
Administrator)</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Precondition</strong></td>
<td colspan="2">User is on the Searching Page.</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Postcondition</strong></td>
<td colspan="2">User able to search for locations within the
campus.</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Main Flow</strong></td>
<td colspan="2"><ol type="1">
<li><p>User enters current location or selects desire location or let
system enter the location by GPS.</p></li>
<li><p>If user perform typing, options such as “Faculty of Computer
&amp; Informatics” show up as new location underneath.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Alternate Scenario</strong></td>
<td colspan="2"><ol type="1">
<li><p>No results are being found</p></li>
<li><p>User cancels searching</p></li>
</ol></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Author</strong></td>
<td colspan="2">YEE SI SHUN</td>
</tr>
</tbody>
</table>

![](media/image8.png){width="6.261111111111111in"
height="4.834722222222222in"}

**Figure 3.2: Search location Sequence Diagram**

#### 3.1.1.3 Show event calendar {#show-event-calendar .unnumbered}

**Table 3.3: Show event calendar**

<table>
<colgroup>
<col style="width: 24%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 24%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>ID</strong></th>
<th colspan="2">REQSQ003</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td>Enter Event Calendar</td>
<td><strong>Version</strong></td>
<td>1.0</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Purpose</strong></td>
<td colspan="2">Browse calendar that displays events on date</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Actor</strong></td>
<td colspan="2">User (Student / Visitor / University Staff /
Administrator)</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Precondition</strong></td>
<td colspan="2">User is on the show event calendar page.</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Postcondition</strong></td>
<td colspan="2">User able to view current and upcoming events in
university.</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Main Flow</strong></td>
<td colspan="2"><ol type="1">
<li><p>Upper part generate calendar for viewing events based on
dates.</p></li>
<li><p>Bottom part provides specific even details and offers options
with delete or sign up for the date selected.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Alternate Scenario</strong></td>
<td colspan="2"><ol type="1">
<li><p>No events are available for the selected date</p></li>
<li><p>User is a guest person so register and delete options cannot be
perform</p></li>
</ol></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Author</strong></td>
<td colspan="2">GOH CHUN YONG</td>
</tr>
</tbody>
</table>

![A diagram of a function AI-generated content may be
incorrect.](media/image9.png){width="6.261111111111111in"
height="3.4347222222222222in"}

**Figure 3.3: Show event calendar Sequence Diagram**

#### 3.1.1.4 Show event list {#show-event-list .unnumbered}

**Table 3.4: Show event list**

<table>
<colgroup>
<col style="width: 24%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 24%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>ID</strong></th>
<th colspan="2">REQSQ004</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td>Show event list</td>
<td><strong>Version</strong></td>
<td>1.0</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Purpose</strong></td>
<td colspan="2">Check for current and incoming university
activities.</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Actor</strong></td>
<td colspan="2">User (Student / Visitor / University Staff /
Administrator)</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Precondition</strong></td>
<td colspan="2">User is on the Expand Page.</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Postcondition</strong></td>
<td colspan="2">User able to view current and upcoming events in
university.</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Main Flow</strong></td>
<td colspan="2"><ol type="1">
<li><p>User enters route navigation mode.</p></li>
<li><p>System list all the available events at the destination.</p></li>
<li><p>User can choose to continue navigating or stop.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Alternate Scenario</strong></td>
<td colspan="2"><ol type="1">
<li><p>No events available in the destination</p></li>
<li><p>Unable to retrieve event information</p></li>
</ol></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Author</strong></td>
<td colspan="2">GOH CHUN YONG</td>
</tr>
</tbody>
</table>

![A diagram of a software application AI-generated content may be
incorrect.](media/image10.png){width="6.261111111111111in"
height="2.678472222222222in"}

**Figure 3.4: Show event list Sequence Diagram**

#### 3.1.1.5 Write Feedback/Report {#write-feedbackreport .unnumbered}

**Table 3.5: Write feedback/report**

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 34%" />
<col style="width: 26%" />
<col style="width: 24%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>ID</strong></th>
<th colspan="2">REQSQ005</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td>User Write Feedback and Report</td>
<td><strong>Version</strong></td>
<td>1.0</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Purpose</strong></td>
<td colspan="2">Allow users send reports regarding campus conditions
that will need to be confirm by administrators or thoughts about
software.</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Actor</strong></td>
<td colspan="2">User (Student / Visitor / University Staff /
Administrator)</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Precondition</strong></td>
<td colspan="2">User presses the feedback button in navigation
page.</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Postcondition</strong></td>
<td colspan="2">User’s feedback/report is successfully submitted and
stored.</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Main Flow</strong></td>
<td colspan="2"><ol type="1">
<li><p>User navigates to feedback/report section in navigation
page</p></li>
<li><p>System presents a form or interface for the user to enter their
feedback/report details</p></li>
<li><p>User enters the required information and submits the
report</p></li>
<li><p>System sends the report data to the server</p></li>
<li><p>The server stores the report data in the feedback
database</p></li>
<li><p>The server sends a success message to the application</p></li>
<li><p>System displays a report success message to the user</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Alternate Scenario</strong></td>
<td colspan="2"><ol type="1">
<li><p>User cancels the feedback/report submission.</p></li>
<li><p>User enters invalid information.</p></li>
<li><p>System fails to send data to server.</p></li>
<li><p>Server fails to store data in database.</p></li>
</ol></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Author</strong></td>
<td colspan="2">YEE SI SHUN</td>
</tr>
</tbody>
</table>

![](media/image11.png){width="6.269444444444445in"
height="5.973611111111111in"}

**Figure 3.5: Write feedback/report Sequence Diagram**

#### 3.1.1.6 Administrator add event {#administrator-add-event .unnumbered}

**Table 3.6: Administrator adds event**

<table>
<colgroup>
<col style="width: 24%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 24%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>ID</strong></th>
<th colspan="2">REQSQ006</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td>Admin Adding Event</td>
<td><strong>Version</strong></td>
<td>1.0</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Purpose</strong></td>
<td colspan="2">Administrator able to create new event.</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Actor</strong></td>
<td colspan="2">Administrator</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Precondition</strong></td>
<td colspan="2">Administrator is logged into the Admin Dashboard and
accessed the event management section.</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Postcondition</strong></td>
<td colspan="2">A new event is successfully created.</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Main Flow</strong></td>
<td colspan="2"><ol type="1">
<li><p>Admins enter the event’s name, date, time and venue</p></li>
<li><p>Press button for saving the new event or cancel entry.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Alternate Scenario</strong></td>
<td colspan="2"><ol type="1">
<li><p>Administrator cancels the event creation</p></li>
<li><p>Input data is invalid</p></li>
<li><p>Unable to save the event data</p></li>
</ol></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Author</strong></td>
<td colspan="2">CHANG HOE HIN</td>
</tr>
</tbody>
</table>

![](media/image12.png){width="6.261111111111111in" height="4.2in"}

**Figure 3.6: Administrators add event Sequence Diagram**

#### 3.1.1.7 Administrator edit event {#administrator-edit-event .unnumbered}

**Table 3.7: Administrator edits event**

<table>
<colgroup>
<col style="width: 24%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 24%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>ID</strong></th>
<th colspan="2">REQSQ007</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td>Admin editing event</td>
<td><strong>Version</strong></td>
<td>1.0</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Purpose</strong></td>
<td colspan="2">Enables administrators to access and alter planned
events.</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Actor</strong></td>
<td colspan="2">Administrator</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Precondition</strong></td>
<td colspan="2">Administrator is logged into the admin dashboard and has
accessed the event management section.</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Postcondition</strong></td>
<td colspan="2">The selected event successfully updated.</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Main Flow</strong></td>
<td colspan="2"><ol type="1">
<li><p>Chose an event through calendar interface.</p></li>
<li><p>System shows event details.</p></li>
<li><p>Admins able to modify the event’s information in the input
fields.</p></li>
<li><p>Delete and save changes buttons for desire action.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Alternate Scenario</strong></td>
<td colspan="2"><ol type="1">
<li><p>Administrator cancels the edit</p></li>
<li><p>Input data invalid</p></li>
<li><p>Unable or error updating data</p></li>
<li><p>Event not found</p></li>
</ol></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Author</strong></td>
<td colspan="2">TEE KAH LE</td>
</tr>
</tbody>
</table>

![](media/image13.png){width="6.269444444444445in" height="4.2in"}

**Figure 3.7: Administrators edit event Sequence Diagram**

#### 3.1.1.8 Administrator view users' feedback {#administrator-view-users-feedback .unnumbered}

**Table 3.8: Administrators view user's feedback**

<table>
<colgroup>
<col style="width: 24%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 24%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>ID</strong></th>
<th colspan="2">REQSQ008</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td>View User Feedback</td>
<td><strong>Version</strong></td>
<td>1.0</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Purpose</strong></td>
<td colspan="2"><ul>
<li><p>Shows reports submitted by users regarding campus
conditions.</p></li>
<li><p>Shows feedback regarding software conditions.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Actor</strong></td>
<td colspan="2">Administrator</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Precondition</strong></td>
<td colspan="2">Administrator is logged into the admin dashboard</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Postcondition</strong></td>
<td colspan="2">Feedback and reports list are being show.</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Main Flow</strong></td>
<td colspan="2"><ol type="1">
<li><p>Admins can sort and view reports by category via dropdown
menu.</p></li>
<li><p>Every feedback card contains report ID, category, overview,
username, and time stamp that need to retrieve from database.</p></li>
<li><p>Admins can print report list as .pdf or other file
types.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Alternate Scenario</strong></td>
<td colspan="2"><ol type="1">
<li><p>No feedback reports are available</p></li>
<li><p>Error retrieving feedback reports</p></li>
</ol></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Author</strong></td>
<td colspan="2">TEE KAH LE</td>
</tr>
</tbody>
</table>

![A diagram of a software system AI-generated content may be
incorrect.](media/image14.png){width="6.268055555555556in"
height="3.772775590551181in"}

**Figure 3.8: Administrators view user's feedback Sequence Diagram**

#### 3.1.1.9 Administrator confirming report {#administrator-confirming-report .unnumbered}

**Table 3.9: Administrator confirming report**

<table>
<colgroup>
<col style="width: 15%" />
<col style="width: 26%" />
<col style="width: 12%" />
<col style="width: 45%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>ID</strong></th>
<th colspan="2">REQSQ009</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td>Admin confirming report</td>
<td><strong>Version</strong></td>
<td>1.0</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Purpose</strong></td>
<td colspan="2">Enable Administrators to validate user-submitted reports
regarding campus conditions that may affect route calculations.</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Actor</strong></td>
<td colspan="2">Administrator</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Precondition</strong></td>
<td colspan="2">Administrator is inside Admin Dashboard and accessed
into user feedback section.</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Postcondition</strong></td>
<td colspan="2">Administrator confirmed the report and updates the map
alerts and route calculation data.</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Main Flow</strong></td>
<td colspan="2"><ol type="1">
<li><p>Administrator accesses the user feedback section in the admin
dashboard</p></li>
<li><p>System displays list of user-submitted feedback/reports</p></li>
<li><p>Administrator selects a report to review</p></li>
<li><p>System displays the details of selected report</p></li>
<li><p>Administrator reviews the report and its details</p></li>
<li><p>Administrator confirms the report</p></li>
<li><p>System updates map alerts and route calculation data reflecting
the confirmed report</p></li>
<li><p>System logs the admin’s confirmation action</p></li>
<li><p>System notifies users with the confirmed report</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Alternate Scenario</strong></td>
<td colspan="2"><ol type="1">
<li><p>Administrator rejects the report</p></li>
<li><p>System fails to update the map alerts and route data</p></li>
</ol></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Author</strong></td>
<td colspan="2">YEE SI SHUN</td>
</tr>
</tbody>
</table>

![](media/image15.png){width="6.261111111111111in"
height="6.452083333333333in"}

**Figure 3.9: Administrator confirming report Sequence Diagram**

#### 3.1.1.10 Route navigation {#route-navigation .unnumbered}

**Table 3.10: Route Navigation**

<table>
<colgroup>
<col style="width: 24%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 24%" />
</colgroup>
<thead>
<tr class="header">
<th colspan="2"><strong>ID</strong></th>
<th colspan="2">REQSQ010</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td>Route navigation</td>
<td><strong>Version</strong></td>
<td>1.0</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Purpose</strong></td>
<td colspan="2">Provides live step-by-step navigation with route that
considering danger, obstacles, and constructions.</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Actor</strong></td>
<td colspan="2">User (Student / Visitor / University Staff /
Administrator)</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Precondition</strong></td>
<td colspan="2">User is on the Initial navigation page and initiates
‘Travel Mode’.</td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Postcondition</strong></td>
<td colspan="2">User receives navigation instructions and follows the
route</td>
</tr>
<tr class="even">
<td colspan="2"><strong>Main Flow</strong></td>
<td colspan="2"><ol type="1">
<li><p>User enters starting location and destination.</p></li>
<li><p>User select the desire recommendations show by system.</p></li>
<li><p>System displays the route guidance with real-time image/map of
the campus featuring an alert notification at the top.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td colspan="2"><strong>Alternate Scenario</strong></td>
<td colspan="2"><ol type="1">
<li><p>No route found</p></li>
<li><p>Error retrieving map data</p></li>
<li><p>Loss of GPS signal</p></li>
</ol></td>
</tr>
<tr class="even">
<td colspan="2"><strong>Author</strong></td>
<td colspan="2">CHANG HOE HIN</td>
</tr>
</tbody>
</table>

![](media/image16.png){width="6.260415573053368in"
height="3.3333333333333335in"}

**Figure 3.10: Route navigation Sequence Diagram**

## Performance Requirements

This section will define the quality requirements that the system must
achieve in the final product. We will be describing and defining the
desired performance and characteristics that the final system should
have good user experience, decent stability, and high efficiency. The
table below will describe all the quality requirements and its details.

**Table 3.11: Performance Requirements**

| **Requirement ID** | **Description**                                                                                                                 | **Priority** | **Author**    |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| REQ_PR0001         | The system shall display accessible route results within 2 seconds after user input.                                            | High         | Goh Chun Yong |
| REQ_PR0002         | Real-time updates (e.g., construction alerts, elevator outages) shall be reflected on the interface within 5 seconds of change. | High         | Goh Chun Yong |
| REQ_PR0003         | The system shall be available 24/7, with an uptime of at least 99.5% per month.                                                 | High         | Goh Chun Yong |
| REQ_PR0004         | Scheduled maintenance shall not exceed 2 hours per month, and users and announcements must be notified 24 hours in advance.     | Low          | Goh Chun Yong |
| REQ_PR0005         | The system shall support at least 500 concurrent users without performance degradation.                                         | High         | Goh Chun Yong |
| REQ_PR0006         | Under stress load, system response time shall not exceed 5 seconds for 95% of requests.                                         | Medium       | Goh Chun Yong |
| REQ_PR0007         | The system shall process a minimum of 100 location queries per minute without affecting system performance.                     | High         | Goh Chun Yong |
| REQ_PR0008         | The system shall support the addition of 50 events per hour without affecting system performance.                               | Low          | Goh Chun Yong |
| REQ_PR0009         | The system shall process and reflect real-time changes submitted by staff/group admins within 5 seconds.                        | High         | Goh Chun Yong |
| REQ_PR0010         | All user-facing interfaces shall synchronize with the database within 3 seconds after any user action.                          | Medium       | Goh Chun Yong |
| REQ_PR0011         | The system shall maintain a request error rate below 1% for all transactions under normal conditions.                           | High         | Goh Chun Yong |
| REQ_PR0012         | System resource usage (CPU, memory) shall remain below 80% during peak operation.                                               | Medium       | Goh Chun Yong |
| REQ_PR0013         | In the event of failure, the system shall recover and be fully operational within 30 minutes.                                   | Medium       | Goh Chun Yong |
| REQ_PR0014         | The data displayed to users shall be eventually consistent across all modules within 5 seconds of updates.                      | Medium       | Goh Chun Yong |
| REQ_PR0015         | The loading animation shall not exceed 3 seconds when initializing the app.                                                     | Low          | Goh Chun Yong |

## 3.3 Usability Requirements {#usability-requirements .unnumbered}

In this section, we will define the usability goals for the CRN
application, focusing on ease of use, accessibility, and a smooth
experience for all users.

**Table 3.12: Usability Requirement**

| **Requirement ID** | **Description**                                                                                        | **Priority** | **Author**    |
|--------------------|--------------------------------------------------------------------------------------------------------|--------------|---------------|
| REQ_UR001          | New user should be good at using the application within 10 minutes of first use.                       | High         | Chang Hoe Hin |
| REQ_UR002          | The system shall respond to end user's input within 2 seconds.                                         | High         | Chang Hoe Hin |
| REQ_UR003          | The system shall provide clear error message.                                                          | Medium       | Chang Hoe Hin |
| REQ_UR004          | After navigation end, user shall be able to rate their experience.                                     | Low          | Chang Hoe Hin |
| REQ_UR005          | The system shall have a minimum average user rating of 4.0/5.0 in usability surveys.                   | Medium       | Chang Hoe Hin |
| REQ_UR006          | The user shall have no more than 3 clicks to access the core features.                                 | High         | Chang Hoe Hin |
| REQ_UR007          | Screen transition and map loading should take not more than 3 seconds.                                 | High         | Chang Hoe Hin |
| REQ_UR008          | The system shall let end users categorize their feedback.                                              | Low          | Chang Hoe Hin |
| REQ_UR009          | When searching location, the system shall provide pre-filled suggestions to minimize user typing time. | Low          | Chang Hoe Hin |
| REQ_UR010          | The system shall provide FAQ section                                                                   | Medium       | Chang Hoe Hin |

## 3.4 Interface Requirements {#interface-requirements .unnumbered}

### 3.4.1 External Interfaces {#external-interfaces .unnumbered}

This part covers how the Campus Route Navigator connects with other
systems. It explains what kind of inputs it needs from users and what it
will show back to them during interactions.

#### 3.4.1.1 IO01 Login Page {#io01-login-page .unnumbered}

**Table 3.13: IO01 Login Page \_ REQ_IO0101**

| Requirement ID | REQ_IO0101                                    |
|----------------|-----------------------------------------------|
| Item           | Sign In Button (Input)                        |
| Description    | A button labelled \"Sign In\"                 |
| Purpose        | To submit user credentials for authentication |
| Input Format   | Button                                        |
| Valid Input    | Not Applicable                                |
| Related I/O    | REQ_IO0102 & REQ_IO0103                       |
| Author         | Goh Chun Yong                                 |

**Table 3.14: IO01 Login Page \_ REQ_IO0102**

| Requirement ID | REQ_IO0102                           |
|----------------|--------------------------------------|
| Item           | Email Address Field (Input)          |
| Description    | A text field to input user email     |
| Purpose        | To enter the email address for login |
| Input Format   | String                               |
| Valid Input    | ASCII characters (32--126)           |
| Related I/O    | None                                 |
| Author         | Goh Chun Yong                        |

**Table 3.15: IO01 Login Page \_ REQ_IO0103**

| Requirement ID | REQ_IO0103                       |
|----------------|----------------------------------|
| Item           | Password Field (Input)           |
| Description    | A text field to input password   |
| Purpose        | To authenticate user credentials |
| Input Format   | String                           |
| Valid Input    | ASCII characters (32--126)       |
| Related I/O    | None                             |
| Author         | Goh Chun Yong                    |

#### 3.4.1.2 IO02 Navigation Page {#io02-navigation-page .unnumbered}

**Table 3.16: IO02 Navigation Page \_ REQ_IO0201**

| Requirement ID | REQ_IO0201                                     |
|----------------|------------------------------------------------|
| Item           | Starting Point Input Field (Input)             |
| Description    | A text box labelled "Enter Starting Point"     |
| Purpose        | To allow users to input starting location      |
| Input Format   | String                                         |
| Valid Input    | Valid building/area names from predefined list |
| Related I/O    | None                                           |
| Author         | Tee Kah Le                                     |

**Table 3.17: IO02 Navigation Page \_ REQ_IO0202**

| Requirement ID | REQ_IO0202                                        |
|----------------|---------------------------------------------------|
| Item           | Destination Input Field (Input)                   |
| Description    | A text box labelled "Enter Destination"           |
| Purpose        | To allow users to input a desired campus location |
| Input Format   | String                                            |
| Valid Input    | Valid building/area names from predefined list    |
| Related I/O    | None                                              |
| Author         | Tee Kah Le                                        |

**Table 3.18: IO02 Navigation Page \_ REQ_IO0203**

| Requirement ID | REQ_IO0203                                     |
|----------------|------------------------------------------------|
| Item           | Destination Search Button (Input)              |
| Description    | A button labelled "Search Destination"         |
| Purpose        | To submit destination & starting point         |
| Input Format   | Not Applicable                                 |
| Valid Input    | Valid building/area names from predefined list |
| Related I/O    | REQ_IO0201 & REQ_IO0202                        |
| Author         | Tee Kah Le                                     |

**Table 3.19: IO02 Navigation Page \_ REQ_IO0204**

| Requirement ID | REQ_IO0204                                                               |
|----------------|--------------------------------------------------------------------------|
| Item           | Navigation Map (Output)                                                  |
| Description    | An embedded map displaying the path from current location to destination |
| Purpose        | To visually guide the user                                               |
| Input Format   | Not Applicable                                                           |
| Valid Input    | Not Applicable                                                           |
| Related I/O    | None                                                                     |
| Author         | Tee Kah Le                                                               |

#### 3.4.1.3 IO03 Report Obstacle Page {#io03-report-obstacle-page .unnumbered}

**Table 3.20: IO03 Report Obstacle Page \_ REQ_IO0301**

| Requirement ID | REQ_IO0301                                                                                |
|----------------|-------------------------------------------------------------------------------------------|
| Item           | Obstacle Type Dropdown (Input)                                                            |
| Description    | A dropdown menu listing obstacle types (e.g., construction, blocked path, slippery floor) |
| Purpose        | To specify the type of obstacle encountered                                               |
| Input Format   | Dropdown list                                                                             |
| Valid Input    | Predefined values                                                                         |
| Related I/O    | None                                                                                      |
| Author         | Yee Si Shun                                                                               |

**Table 3.21: IO03 Report Obstacle Page \_ REQ_IO0302**

| Requirement ID | REQ_IO0302                                           |
|----------------|------------------------------------------------------|
| Item           | Description Field (Input)                            |
| Description    | A text field for describing the obstacle             |
| Purpose        | To provide additional information about the obstacle |
| Input Format   | String                                               |
| Valid Input    | ASCII characters (32--126)                           |
| Related I/O    | None                                                 |
| Author         | Yee Si Shun                                          |

**Table 3.22: IO03 Report Obstacle Page \_ REQ_IO0303**

| Requirement ID | REQ_IO0303                               |
|----------------|------------------------------------------|
| Item           | Upload Photo Button (Input)              |
| Description    | Button to upload a photo of the obstacle |
| Purpose        | To attach visual evidence of the issue   |
| Input Format   | File Upload                              |
| Valid Input    | JPG, PNG formats only                    |
| Related I/O    | None                                     |
| Author         | Yee Si Shun                              |

**Table 3.23: IO03 Report Obstacle Page \_ REQ_IO0304**

| Requirement ID | REQ_IO0304                          |
|----------------|-------------------------------------|
| Item           | Submit Button (Input)               |
| Description    | A button labelled "Report Obstacle" |
| Purpose        | To submit the obstacle report       |
| Input Format   | Button                              |
| Valid Input    | Not Applicable                      |
| Related I/O    | None                                |
| Author         | Yee Si Shun                         |

#### 3.4.1.4 IO04 Admin Event Dashboard Page {#io04-admin-event-dashboard-page .unnumbered}

**Table 3.24: IO04 Admin Event Dashboard Page \_ REQ_IO0401**

| Requirement ID | REQ_IO0401                                            |
|----------------|-------------------------------------------------------|
| Item           | Event List (Output)                                   |
| Description    | A list of events with time, location, and description |
| Purpose        | To view all scheduled campus events                   |
| Input Format   | Not Applicable                                        |
| Valid Input    | Not Applicable                                        |
| Related I/O    | None                                                  |
| Author         | Chang Hoe Hin                                         |

**Table 3.25: IO04 Admin Event Dashboard Page \_ REQ_IO0402**

| Requirement ID | REQ_IO0402                       |
|----------------|----------------------------------|
| Item           | Create Event Button (Input)      |
| Description    | A button labelled "Create Event" |
| Purpose        | To open the event creation form  |
| Input Format   | Button                           |
| Valid Input    | Not Applicable                   |
| Related I/O    | None                             |
| Author         | Chang Hoe Hin                    |

**Table 3.25: IO04 Admin Event Dashboard Page \_ REQ_IO0403**

| Requirement ID | REQ_IO0403                                    |
|----------------|-----------------------------------------------|
| Item           | Delete Event Button (Input)                   |
| Description    | A button next to each event labelled "Delete" |
| Purpose        | To remove an existing event                   |
| Input Format   | Button                                        |
| Valid Input    | Not Applicable                                |
| Related I/O    | None                                          |
| Author         | Chang Hoe Hin                                 |

#### 3.4.1.5 IO05 Submit Feedback Page {#io05-submit-feedback-page .unnumbered}

**Table 3.26: IO05 Submit Feedback Page \_ REQ_IO0501**

| Requirement ID | REQ_IO0501                                      |
|----------------|-------------------------------------------------|
| Item           | Feedback Field (Input)                          |
| Description    | A multiline text field labelled "Your Feedback" |
| Purpose        | To collect feedback from users                  |
| Input Format   | String                                          |
| Valid Input    | ASCII characters (32--126)                      |
| Related I/O    | None                                            |
| Author         | Goh Chun Yong                                   |

**Table 3.27: IO05 Submit Feedback Page \_ REQ_IO0502**

| Requirement ID | REQ_IO0502                                   |
|----------------|----------------------------------------------|
| Item           | Rating Dropdown (Input)                      |
| Description    | A dropdown to select a rating (1 to 5 stars) |
| Purpose        | To assess user satisfaction                  |
| Input Format   | Dropdown                                     |
| Valid Input    | 1, 2, 3, 4, 5                                |
| Related I/O    | None                                         |
| Author         | Goh Chun Yong                                |

**Table 3.28: IO05 Submit Feedback Page \_ REQ_IO0503**

| Requirement ID | REQ_IO0503                          |
|----------------|-------------------------------------|
| Item           | Submit Button (Input)               |
| Description    | A button labelled "Submit Feedback" |
| Purpose        | To send feedback to the system      |
| Input Format   | Button                              |
| Valid Input    | Not Applicable                      |
| Related I/O    | None                                |
| Author         | Goh Chun Yong                       |

#### 3.4.1.6 IO06 Travel Mode Option Page {#io06-travel-mode-option-page .unnumbered}

**Table 3.29: IO06 Travel Mode Option Page \_ REQ_IO0601**

| Requirement ID | REQ_IO0601                                                       |
|----------------|------------------------------------------------------------------|
| Item           | Travel Mode Toggle (Input)                                       |
| Description    | A toggle labelled "Travel Mode"                                  |
| Purpose        | To filter navigation to wheelchair-friendly or accessible routes |
| Input Format   | Toggle switch                                                    |
| Valid Input    | Walk / Accessible / Shortest                                     |
| Related I/O    | None                                                             |
| Author         | Tee Kah Le                                                       |

**Table 3.30: IO06 Travel Mode Option Page \_ REQ_IO0602**

| Requirement ID | REQ_IO0602                                        |
|----------------|---------------------------------------------------|
| Item           | Updated Navigation Map (Output)                   |
| Description    | Map display updates based on accessibility filter |
| Purpose        | To show only accessible paths and entrances       |
| Input Format   | Not Applicable                                    |
| Valid Input    | Not Applicable                                    |
| Related I/O    | REQ_IO0601                                        |
| Author         | Tee Kah Le                                        |

#### 3.4.1.7 IO07 Navigation Map Page {#io07-navigation-map-page .unnumbered}

**Table 3.31: IO07 Navigation Map Page \_ REQ_IO0701**

| Requirement ID | REQ_IO0701                                                   |
|----------------|--------------------------------------------------------------|
| Item           | Turn-by-Turn Direction Display (Output)                      |
| Description    | Visual message showing upcoming signal (e.g., \"Turn Left\") |
| Purpose        | To guide users through the campus with real-time navigation  |
| Input Format   | Not Applicable                                               |
| Valid Input    | Not Applicable                                               |
| Related I/O    | None                                                         |
| Author         | Yee Si Shun                                                  |

**Table 3.32: IO07 Navigation Map Page \_ REQ_IO0702**

| Requirement ID | REQ_IO0702                      |
|----------------|---------------------------------|
| Item           | Travel Mode Toggle (Input)      |
| Description    | A toggle labelled "Travel Mode" |
| Purpose        | To change route mode            |
| Input Format   | Toggle switch                   |
| Valid Input    | Walk / Accessible / Shortest    |
| Related I/O    | None                            |
| Author         | Yee Si Shun                     |

**Table 3.33: IO07 Navigation Map Page \_ REQ_IO0703**

| Requirement ID | REQ_IO0703                               |
|----------------|------------------------------------------|
| Item           | Travel Time & Distance Display (Output)  |
| Description    | Displays estimated time and distance     |
| Purpose        | To inform user of current route progress |
| Input Format   | Toggle switch                            |
| Valid Input    | Not Applicable                           |
| Related I/O    | None                                     |
| Author         | Yee Si Shun                              |

#### 3.4.1.8 IO08 Navigation Map Sub Page {#io08-navigation-map-sub-page .unnumbered}

**Table 3.34: IO08 Navigation Map Sub Page \_ REQ_IO0801**

| Requirement ID | REQ_IO0801                                       |
|----------------|--------------------------------------------------|
| Item           | Destination Search Button (Input)                |
| Description    | A button to guide user back to searching routes. |
| Purpose        | To let users searching the routes                |
| Input Format   | String                                           |
| Valid Input    | Valid building/area names from predefined list   |
| Related I/O    | None                                             |
| Author         | Chang Hoe Hin                                    |

**Table 3.35: IO08 Navigation Map Sub Page \_ REQ_IO0802**

| Requirement ID | REQ_IO0802                                     |
|----------------|------------------------------------------------|
| Item           | Event Calendar Button (Output)                 |
| Description    | A button to guide user to Event Calendar Page. |
| Purpose        | To let users view event calendar.              |
| Input Format   | Button                                         |
| Valid Input    | Not Applicable                                 |
| Related I/O    | None                                           |
| Author         | Chang Hoe Hin                                  |

**Table 3.36: IO08 Navigation Map Sub Page \_ REQ_IO0803**

| Requirement ID | REQ_IO0803                                               |
|----------------|----------------------------------------------------------|
| Item           | Events Happening List (Output)                           |
| Description    | List of events occurring today with time, date, location |
| Purpose        | To help users decide what events to join on the go       |
| Input Format   | Not Applicable                                           |
| Valid Input    | Not Applicable                                           |
| Related I/O    | None                                                     |
| Author         | Chang Hoe Hin                                            |

**Table 3.37: IO08 Navigation Map Sub Page \_ REQ_IO0804**

| Requirement ID | REQ_IO0804                       |
|----------------|----------------------------------|
| Item           | Stop Button (Input)              |
| Description    | A red button labelled "Stop"     |
| Purpose        | To stop current route navigation |
| Input Format   | Button                           |
| Valid Input    | Not Applicable                   |
| Related I/O    | None                             |
| Author         | Chang Hoe Hin                    |

**Table 3.38: IO08 Navigation Map Sub Page \_ REQ_IO0805**

| Requirement ID | REQ_IO0805                              |
|----------------|-----------------------------------------|
| Item           | Continue Route Button (Input)           |
| Description    | A blue button labelled "Continue Route" |
| Purpose        | To resume paused route guidance         |
| Input Format   | Button                                  |
| Valid Input    | Not Applicable                          |
| Related I/O    | None                                    |
| Author         | Chang Hoe Hin                           |

#### 3.4.1.9 IO09 Event Calendar Page {#io09-event-calendar-page .unnumbered}

**Table 3.39: IO09 Event Calendar Page \_ REQ_IO0901**

| Requirement ID | REQ_IO0901                                 |
|----------------|--------------------------------------------|
| Item           | Calendar Widget (Input)                    |
| Description    | A calendar UI for selecting dates          |
| Purpose        | To view and filter events by selected date |
| Input Format   | Calendar Selection                         |
| Valid Input    | Date format                                |
| Related I/O    | None                                       |
| Author         | Goh Chun Yong                              |

**Table 3.40: IO09 Event Calendar Page \_ REQ_IO0902**

| Requirement ID | REQ_IO0902                                             |
|----------------|--------------------------------------------------------|
| Item           | Event Info Card (Output)                               |
| Description    | Card showing event name, time, place, and participants |
| Purpose        | To view detailed event information                     |
| Input Format   | Not Applicable                                         |
| Valid Input    | Not Applicable                                         |
| Related I/O    | None                                                   |
| Author         | Goh Chun Yong                                          |

**Table 3.41: IO09 Event Calendar Page \_ REQ_IO0903**

| Requirement ID | REQ_IO0903                        |
|----------------|-----------------------------------|
| Item           | Register Button (Input)           |
| Description    | A blue button labelled "Register" |
| Purpose        | To register for a selected event  |
| Input Format   | Button                            |
| Valid Input    | Not Applicable                    |
| Related I/O    | None                              |
| Author         | Yee Si Shun                       |

**Table 3.42: IO09 Event Calendar Page \_ REQ_IO0904**

| Requirement ID | REQ_IO0904                                 |
|----------------|--------------------------------------------|
| Item           | Delete Button (Input)                      |
| Description    | A red button labelled "Delete"             |
| Purpose        | To delete the event (for authorized users) |
| Input Format   | Button                                     |
| Valid Input    | Not Applicable                             |
| Related I/O    | None                                       |
| Author         | Yee Si Shun                                |

#### 3.4.1.10 IO10 Admin Feedback Dashboard Page {#io10-admin-feedback-dashboard-page .unnumbered}

**Table 3.43: IO10 Admin Feedback Dashboard Page \_ REQ_IO1001**

| Requirement ID | REQ_IO1001                                                                                       |
|----------------|--------------------------------------------------------------------------------------------------|
| Item           | Category Filter Dropdown (Input)                                                                 |
| Description    | A dropdown list labelled "All" with options like Obstacles Reports, Construction Reports, Others |
| Purpose        | To filter feedback reports based on category                                                     |
| Input Format   | Dropdown                                                                                         |
| Valid Input    | Obstacles Reports / Construction Reports / Others                                                |
| Related I/O    | None                                                                                             |
| Author         | Tee Kah Le                                                                                       |

**Table 3.44: IO10 Admin Feedback Dashboard Page \_ REQ_IO1002**

| Requirement ID | REQ_IO1002                                                                                             |
|----------------|--------------------------------------------------------------------------------------------------------|
| Item           | Feedback Report Card (Output)                                                                          |
| Description    | A card showing the report ID, title (e.g., Obstacles Report), content summary, username, and timestamp |
| Purpose        | To provide admins with an overview of submitted user feedback                                          |
| Input Format   | Not Applicable                                                                                         |
| Valid Input    | Not Applicable                                                                                         |
| Related I/O    | None                                                                                                   |
| Author         | Tee Kah Le                                                                                             |

**Table 3.45: IO10 Admin Feedback Dashboard Page \_ REQ_IO1003**

| Requirement ID | REQ_IO1003                                                  |
|----------------|-------------------------------------------------------------|
| Item           | Message Button (Input)                                      |
| Description    | A button labelled "Message" on each report card             |
| Purpose        | To allow the admin to respond directly to the report sender |
| Input Format   | Button                                                      |
| Valid Input    | Not Applicable                                              |
| Related I/O    | None                                                        |
| Author         | Chang Hoe Hin                                               |

**Table 3.46: IO10 Admin Feedback Dashboard Page \_ REQ_IO1004**

| Requirement ID | REQ_IO1004                                         |
|----------------|----------------------------------------------------|
| Item           | Print Report Button (Input)                        |
| Description    | A red button at the bottom labelled "Print report" |
| Purpose        | To print the current list of filtered reports      |
| Input Format   | Button                                             |
| Valid Input    | Not Applicable                                     |
| Related I/O    | None                                               |
| Author         | Chang Hoe Hin                                      |

### 3.4.2 System Interfaces {#system-interfaces .unnumbered}

The **CRN** (\"Campus Accessibility Navigation System\") will primarily
interact with users through a native mobile application designed for
both iOS and Android operating systems. This mobile application will
serve as the primary interface for accessing all features, including
navigation, facility information, and event details.

**Table 3.47: Interface Requirements**

| **Interface ID** | **System Name**                 | **Description**                                                                                                             | **Details**                                                                                | **Author**    |
|------------------|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|---------------|
| REQ_SI001        | Campus Information System (CIS) | Retrieve and synchronize data related to Facility information and Event Data.                                               | API-Driven Backend will handle data management and communication with external system      | CHANG HOE HIN |
| REQ_SI002        | Mapping Services                | Obtain base map data and potentially utilize routing algorithms.                                                            | Data Synchronization ensure data consistency of routing algorithms                         | CHANG HOE HIN |
| REQ_SI003        | Push notification Services      | Send alerts and notifications to users regarding event reminders, accessibility updates, or important campus announcements. | Communication between mobile application and the backend API will utilize secure protocols | CHANG HOE HIN |

### 3.4.3 User Interfaces {#user-interfaces .unnumbered}

The table below are the main features of each interface between the
software product and its users.

**Table 3.48: User Interfaces**

| **Module ID** | **Module Name**                  | **Description**                                                                                                                                                        | **Priority** | **Author** |
|---------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|------------|
| REQ_UI001     | Navigation Interface             | Display with accessible routes highlighted, search functional for locations, turn-by-turn navigation instructions.                                                     | High         | TEE KAH LE |
| REQ_UI002     | Facilities Information Interface | Display of facility details (e.g., building hours, accessible entrances, elevator locations, restroom accessibility), search and filtering options.                    | Medium       | TEE KAH LE |
| REQ_UI003     | Event Information Interface      | Listing of campus events with accessibility information (e.g., wheelchair access, hearing loop availability), filtering by date, category, and accessibility features. | Medium       | TEE KAH LE |
| REQ_UI004     | Administrative Interface         | Tools for administrators to manage map data, facility information, event details, and accessibility features.                                                          | High         | TEE KAH LE |
| REQ_UI005     | Reporting/Feedback Interface     | For users to report accessibility issues or provide feedback on the system                                                                                             | Low          | TEE KAH LE |

### 3.4.4 Hardware Interfaces {#hardware-interfaces .unnumbered}

**CRN** needs the mobile devices with the specification described below
so that the features work normally to user.

**Table 3.49: Hardware Interface**

| **Interface ID** | **Description**                                                                                      | **Author**    |
|------------------|------------------------------------------------------------------------------------------------------|---------------|
| REQ_HI001        | The GPS/Location should be functional from user's mobile device                                      | CHANG HOE HIN |
| REQ_HI002        | The Random Access Memory (RAM) required for the devices shall be at least 4GB                        | CHANG HOE HIN |
| REQ_HI003        | The mobile should have touchscreen features for user interaction with the map and interface elements | CHANG HOE HIN |
| REQ_HI004        | The camera of mobile device can be use for image recognition features                                | CHANG HOE HIN |

### 3.4.5 Software Interfaces {#software-interfaces .unnumbered}

**CRN** also requires other software to function properly. The
interfaces between CRN and other software are described below:

**Table 3.50: Software Interfaces**

| **ID**    | **Category**     | **Name** | **Version Number**   | **Purpose**                                         | **Reference**         |
|-----------|------------------|----------|----------------------|-----------------------------------------------------|-----------------------|
| REQ_SI001 | Operating System | Android  | Android 9.0 or later | Software platform that manages user device hardware | Google Chrome Browser |
|           |                  | iOS      | iOS 15.0 or later    |                                                     |                       |

### 3.4.6 Communications interface {#communications-interface .unnumbered}

The table below outlines the various interfaces to communications,
specifying the protocols and methods the system will use to interact
with other systems, networks, and services.

**Table 3.51: Communications interface**

| **Interface ID** | **Description**                                                                                          | **Protocols/Methods**          | **Priority** | **Author**  |
|------------------|----------------------------------------------------------------------------------------------------------|--------------------------------|--------------|-------------|
| REQ_CI001        | Communication with backend server and external services.                                                 | TCP/IP, HTTP/HTTPS             | High         | YEE SI SHUN |
| REQ_CI002        | Fetch data about facilities, events, and map information from campus systems third-party providers.      | RESTful, GraphQL               | High         | YEE SI SHUN |
| REQ_CI003        | Structuring the data exchanged over APIs.                                                                | JSON, XML                      | Medium       | YEE SI SHUN |
| REQ_CI004        | Communication with beacons or other nearby devices for indoor navigation or proximity-based information. | BLE                            | Medium       | YEE SI SHUN |
| REQ_CI005        | Deliver real-time updates about events or accessibility alerts                                           | Firebase Cloud Messaging, APNs | Low          | YEE SI SHUN |

**Table 3.52: Interface Requirement**

| **Requirement ID** | **Description**                                                                       | **Priority** | **Author** |
|--------------------|---------------------------------------------------------------------------------------|--------------|------------|
| REQ_IR001          | Users will be able to filter events by date and category.                             | Medium       | Tee Kah Le |
| REQ_IR002          | The map will show elevator location and restroom accessibility.                       | Medium       | Tee Kah Le |
| REQ_IR003          | Allows users to set their accessibility needs                                         | Medium       | Tee Kah Le |
| REQ_IR004          | Include search and filtering features, help user find specific information they need. | Medium       | Tee Kah Le |
| REQ_IR005          | The system shall provide turn-by-turn navigation instructions.                        | High         | Tee Kah Le |
| REQ_IR005          | Send notification for navigation and event reminder                                   | Medium       | Tee Kah Le |
| REQ_IR006          | At least 4GB ram required                                                             | High         | Tee Kah Le |

## 3.5 Logical database requirements {#logical-database-requirements .unnumbered}

### 3.5.1 Class Diagram {#class-diagram .unnumbered}

![A screenshot of a computer AI-generated content may be
incorrect.](media/image17.png){width="6.261111111111111in"
height="5.9215277777777775in"}

**Figure 3.23 Class Diagram**

**Table 3.53: User**

| **User**   |                                                               |                                                                                                                 |
|------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Content    |                                                               | Description                                                                                                     |
| Attributes | UserID : INT                                                  | A unique number to identify the university                                                                      |
|            | Role : string                                                 | The user\'s type (e.g., Student, Visitor, Staff, Admin).                                                        |
|            | Username : string                                             | The name used for login.                                                                                        |
|            | Password : string                                             | The user\'s password                                                                                            |
|            | UniversityID : INT                                            | Links the user to a specific university.                                                                        |
| Methods    | authenticate() : boolean                                      | Checks if the user\'s login credentials are valid. Returns true if successful, false otherwise.                 |
|            | searchLocation (locationName: string) : List\<Location\>      | Allows the user to find locations by name. Returns a list of matching locations.                                |
|            | requestRoute(origin: Location,destination : Location) : Route | Asks the system to find a route between two points, considering user preferences. Returns the calculated route. |
|            | viewEvents() : List\<Event\>                                  | Displays a list of available events.                                                                            |
|            | submitFeedback(feedback:Feedback):void                        | Allows the user to send feedback or a report to the system.                                                     |

**Table 3.54: EventManager**

| **EventManager** |                                             |                                                                                                                                |
|------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Content          |                                             | Description                                                                                                                    |
| Attributes       | EventID: INT                                | A unique number for each event.                                                                                                |
|                  | Title: String                               | the main name or headline of the event                                                                                         |
|                  | Description: String                         | detailed text field providing comprehensive information about the event\'s purpose, activities, and what attendees can expect. |
|                  | LocationID: INT                             | specific Location on campus where it is scheduled to take place.                                                               |
|                  | StartDate: Date                             | calendar date on which the event is scheduled to begin.                                                                        |
|                  | EndDate: Date                               | calendar date on which the event is scheduled to conclude. This may be the same as StartDate for single-day events.            |
|                  | StartTime: Time                             | specific time of day when the event is scheduled to commence.                                                                  |
|                  | EndTime: Time                               | specific time of day when the event is scheduled to finish.                                                                    |
|                  | Category: String                            | classifying the type of event                                                                                                  |
|                  | Organizer: String                           | indicating the name of the department, club, or individual responsible for organizing the event.                               |
|                  | ContactInfo: String                         | Contact details                                                                                                                |
|                  | IsPublic: Boolean                           | whether the event is open and visible to all users                                                                             |
| Methods          | createEvent(event: Event): boolean          | Allows administrators to add new event details.                                                                                |
|                  | editEvent(event:Event) : boolean            | Allows administrators to modify existing event details.                                                                        |
|                  | deleteEveent(eventId : INT) : boolean       | Allows administrators to remove events.                                                                                        |
|                  | getEventDetails(eventId: INT) : Event       | Retrieves detailed information for a specific event.                                                                           |
|                  | getEventsByDate(date: Date) : List\<Event\> | Retrieves all events scheduled for a particular date.                                                                          |

**Table 3.55: FeedbackManager**

| **FeedbackManager** |                                                        |                                                                                                                        |
|---------------------|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Content             |                                                        | Description                                                                                                            |
| Attributes          | FeedbackID: INT                                        | A unique integer identifier for each individual piece of feedback or report submitted by a user.                       |
|                     | UserID: INT                                            | specific feedback entry to the User who submitted it.                                                                  |
|                     | Content: String                                        | A text field containing the actual message or detailed description provided by the user in their feedback.             |
|                     | Category: String                                       | classifying the type of feedback, such as \"Obstacle Report,\" \"Suggestion,\" \"Bug Report,\" or \"General Inquiry.\" |
|                     | Rating: INT                                            | An integer value representing a numerical rating provided by the user, if applicable                                   |
|                     | Timestamp: DateTime                                    | The exact date and time when the feedback or report was submitted to the system.                                       |
|                     | LocationID: INT (if applicable)                        | specific Location on the campus if the feedback pertains to an issue or experience at a particular place.              |
|                     | RouteID: INT (if applicable)                           | specific Route if the feedback is related to a navigation experience on that route.                                    |
|                     | Status: String                                         | A text string indicating the current processing state of the feedback                                                  |
| Methods             | submitFeedback(feedback: Feedback): boolean            | Processes and stores user-submitted feedback.                                                                          |
|                     | getFeedbackReports(category: String): List\<Feedback\> | Retrieves feedback reports, optionally filtered by category.                                                           |
|                     | confirmFeedbackReport(feedbackId: INT): boolean        | Allows administrators to confirm a feedback report, potentially triggering other actions (like updating map alerts).   |

**Table 3.56: AuthenticationManager**

| **AuthenticationManager** |                                                               |                                                                                                      |
|---------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Content                   |                                                               | Description                                                                                          |
| Methods                   | authenticateUser(username : String, password : String) : User | Handles the process of verifying a user\'s login credentials. Returns the User object if successful. |
|                           | registerUser(user: User): boolean                             | Manages the creation of new user accounts. Returns true if registration is successful.               |
|                           | logoutUser(user: User) : void                                 | Handles the user logout process.                                                                     |

**Table 3.57: AlertManager**

| **AlertManager** |                                                     |                                                                                                                           |
|------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Content          |                                                     | Description                                                                                                               |
| Attributes       |  AlertID: INT                                       | unique integer number that serves as the primary identifier for each specific alert                                       |
|                  | Title: String                                       | brief headline or summary for the alert                                                                                   |
|                  | Message: String                                     | full explanation and important information regarding the alert.                                                           |
|                  | Severity: String                                    | level of impact or urgency of the alert                                                                                   |
|                  | LocationID: INT                                     | specific Location on campus that is affected by the alert.                                                                |
|                  | StartTime: DateTime                                 | ate and time when the alert officially became active or was issued.                                                       |
|                  | EndTime: DateTime                                   | exact date and time when the alert is expected to be resolved or expire.                                                  |
|                  | IsActive: Boolean                                   | whether the alert is currently active and should be displayed to users (true) or if it has expired/been resolved (false). |
|                  | AlertType: String                                   | cause of the alert                                                                                                        |
| Methods          | createAlert(alert: Alert): boolean                  | Allows administrators to create new alerts.                                                                               |
|                  | updateAlert(alert: Alert): boolean                  | allows administrators to modify existing alerts.                                                                          |
|                  | getAlertsByLocation(locationId: INT): List\<Alert\> | Retrieves active alerts associated with a specific location.                                                              |
|                  | getActiveAlerts(): List\<Alert\>                    | Retrieves all currently active alerts in the system.                                                                      |

**Table 3.58: FacilityManager**

| **FacilityManager** |                                                            |                                                                                                   |
|---------------------|------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Content             |                                                            | Description                                                                                       |
| Attributes          | FacilityID: INT                                            | primary identifier for each specific facility on campus.                                          |
|                     | Name: String                                               | name or label of the facility                                                                     |
|                     | Type: String                                               | category or kind of facility                                                                      |
|                     | LocationID: INT                                            | specific Location on campus where it is situated.                                                 |
|                     | Description: String                                        | additional information about the facility, such as its features, capacity, or specific amenities. |
|                     | Status: String                                             | current operational state of the facilit                                                          |
| Methods             | getFacilityDetails(facilityId: INT): Facility              | Retrieves detailed information for a specific facility.                                           |
|                     | getFacilitiesByLocation(locationId: INT): List\<Facility\> | Finds all facilities at a given location.                                                         |

**Table 3.59: LocationManager**

| **LocationManager** |                                                  |                                                                                             |
|---------------------|--------------------------------------------------|---------------------------------------------------------------------------------------------|
| Content             |                                                  | Description                                                                                 |
| Attributes          | LocationID: INT                                  | primary identifier for each specific location entry in the system.                          |
|                     | Name: String                                     | name for the location                                                                       |
|                     | Description: String                              | information about the location, such as its purpose, history, or points of interest.        |
|                     | Building: String                                 | identifier of the building where the location is situated                                   |
|                     | Floor: INT                                       | number indicating the floor level within a building where the location is found             |
|                     | Latitude: Double                                 | he geographical latitude coordinate of the location, representing its north-south position. |
|                     | Longitude: Double                                | The geographical longitude coordinate of the location, representing its east-west position. |
|                     | Type: String                                     | classification of what kind of location it is                                               |
|                     | AccessibilityFeatures: List\<String\>            | specific accessibility features available at the location                                   |
|                     | OpeningHours: String                             | typical hours of operation for the location                                                 |
| Methods             | getLocationDetails(locationId:INT): Location     | Retrieves detailed information for a specific location.                                     |
|                     | searchLocations(query: String): List\<Location\> | Finds locations based on a search query.                                                    |
|                     | addLocation(location: Location):boolean          | dds a new location to the system (likely for administrators).                               |
|                     | updateLocation(location: Location): boolean      | Modifies existing location information (likely for administrators).                         |

**Table 3.60: RoutePlanner**

| **RoutePlanner** |                                                                                          |                                                                                           |
|------------------|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| Content          |                                                                                          | Description                                                                               |
| Attributes       | RouteID: INT                                                                             | identifier for each specific calculated navigation route.                                 |
|                  | Origin: Location                                                                         | starting point of the calculated route.                                                   |
|                  | Destination: Location                                                                    | end point of the calculated route.                                                        |
|                  | Distance: Double                                                                         | total length of the calculated route.                                                     |
|                  | EstimatedTime: INT                                                                       | predicted duration required to travel the calculated route.                               |
|                  | RouteType: String                                                                        | type of route calculated                                                                  |
|                  | WayPoints: List\<Location\>                                                              | A list of Location objects or coordinates that define intermediate points along the route |
|                  | Instructions: List\<String\>                                                             | step-by-step navigation instructions for the user to follow along the route               |
| Methods          | calculateRoute(origin: Location, destination: Location, preferences: Preferences): Route | Computes a navigation route between two points, considering user preferences.             |
|                  | getRouteInstructions(routeId: INT): List\<String\>                                       | Overloaded method to calculate a route within a specific university.                      |
|                  | updateRouteForAlert(alert: Alert): Route                                                 | Adjusts a planned route if a new alert (e.g., an obstacle) affects it.                    |

**Table 3.61: NavigationController**

| **NavigationController** |                                                                                          |                                                                          |
|--------------------------|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Content                  |                                                                                          | Description                                                              |
| Methods                  | startNavigation(origin: Location, destination: Location, preferences: Preferences): void | Initiates the navigation process from a starting point to a destination. |
|                          | provideNavigationInstructions(routeId: INT): void                                        | Delivers turn-by-turn or step-by-step instructions to the user.          |
|                          |  handleAlert(alert: Alert): void                                                         | Manages how the navigation system responds to real-time alerts.          |
|                          | endNavigation(): void                                                                    | Ends the current navigation session.                                     |

**Table 3.62: MapDisplay**

| **MapDisplay** |                                                                                             |                                                                       |
|----------------|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| Content        |                                                                                             | Description                                                           |
| Methods        | displayMap(locations: List\<Location\>, routes: List\<Route\>, alerts: List\<Alert\>): void | Renders the campus map, showing locations, routes, and active alerts. |
|                | showRoute(route: Route): void                                                               | Highlights a specific route on the map.                               |
|                | showLocationDetails(locationId: INT): void                                                  | Displays detailed information about a specific location on the map.   |
|                | updateMapWithAlert(alert: Alert): void                                                      | Dynamically updates the map to show new or changed alert information. |

### 3.5.2 ERD {#erd .unnumbered}

![](media/image18.png){width="6.269444444444445in"
height="4.017361111111111in"}

**Figure 3.24: Entity Relationship Diagram**

The Entity-Relationship Diagram (ERD) represents the structure of
relationships between entities of CRN. The key entities include User,
Admin, Feedback, University, Location, Event, Alert, Route, Facility,
and ConfirmedReport. Content below will explain how the attributes in
the database for and what it features.

#### 3.5.1 University {#university .unnumbered}

**Table 3.63: University**

| Field Name         | Description                                           | Data Type    | Constraints                 |
|--------------------|-------------------------------------------------------|--------------|-----------------------------|
| UniversityID       | Unique identifier for the university                  | INT          | PRIMARY KEY, AUTO_INCREMENT |
| Name               | Name of the university                                | VARCHAR(255) | NOT NULL                    |
| Location           | Address or general location of the university         | VARCHAR(255) |                             |
| CampusMapData      | Path or reference to the campus map data              | TEXT         |                             |
| ContactInformation | General contact information for the university        | TEXT         |                             |
| Branding           | Information for university branding (e.g., logo path) | VARCHAR(255) |                             |

####  {#section .unnumbered}

#### 3.5.2 User {#user .unnumbered}

**Table 3.64: User**

| Field Name   | Description                            | Data Type    | Constraints                 |
|--------------|----------------------------------------|--------------|-----------------------------|
| UserID       | Unique identifier for the user         | INT          | PRIMARY KEY, AUTO_INCREMENT |
| Role         | User\'s role (Student, Visitor, Staff) | VARCHAR(50)  | NOT NULL                    |
| Username     | User\'s login username                 | VARCHAR(50)  | UNIQUE                      |
| Password     | User\'s login password (hashed)        | VARCHAR(255) | NOT NULL                    |
| Email        | User\'s email address                  | VARCHAR(100) | UNIQUE                      |
| UniversityID | Foreign key linking to the University  | INT          | FOREIGN KEY (University)    |

####  {#section-1 .unnumbered}

#### 3.5.3 Admin {#admin-1 .unnumbered}

**Table 3.65: Admin**

| Field Name | Description                             | Data Type    | Constraints                 |
|------------|-----------------------------------------|--------------|-----------------------------|
| AdminID    | Unique identifier for the administrator | INT          | PRIMARY KEY, AUTO_INCREMENT |
| UserID     | Foreign key linking to the User table   | INT          | FOREIGN KEY (User)          |
| Username   | Admin\'s login username                 | VARCHAR(50)  | UNIQUE, NOT NULL            |
| Email      | Admin\'s email address                  | VARCHAR(100) | UNIQUE, NOT NULL            |

####  {#section-2 .unnumbered}

#### 3.5.4 Location {#location .unnumbered}

**Table 3.66: Location**

| Field Name   | Description                                 | Data Type    | Constraints                 |
|--------------|---------------------------------------------|--------------|-----------------------------|
| LocationID   | Unique identifier for the location          | INT          | PRIMARY KEY, AUTO_INCREMENT |
| UniversityID | Foreign key linking to the University table | INT          | FOREIGN KEY (University)    |
| Name         | Name of the location (e.g., Building A)     | VARCHAR(255) | NOT NULL                    |
| Description  | Detailed description of the location        | TEXT         |                             |
| Coordinates  | Geographical coordinates (e.g., POINT data) | POINT        | NOT NULL                    |

#### 3.5.5 Event {#event .unnumbered}

**Table 3.67: Event**

| Field Name  | Description                               | Data Type     | Constraints                 |
|-------------|-------------------------------------------|---------------|-----------------------------|
| EventID     | Unique identifier for the event           | INT           | PRIMARY KEY, AUTO_INCREMENT |
| Name        | Name of the event                         | VARCHAR (255) | NOT NULL                    |
| Description | Detailed description of the event         | TEXT          |                             |
| DateTime    | Date and time of the event                | DATETIME      | NOT NULL                    |
| LocationID  | Foreign key linking to the Location table | INT           | FOREIGN KEY (Location)      |

####  {#section-3 .unnumbered}

#### 3.5.6 Facility {#facility .unnumbered}

**Table 3.68: Facility**

| Field Name   | Description                                                  | Data Type     | Constraints                 |
|--------------|--------------------------------------------------------------|---------------|-----------------------------|
| FacilityID   | Unique identifier for the facility                           | INT           | PRIMARY KEY, AUTO_INCREMENT |
| Name         | Name of the facility                                         | VARCHAR (255) | NOT NULL                    |
| LocationID   | Foreign key linking to the Location table                    | INT           | FOREIGN KEY (Location)      |
| Availability | Information about the facility\'s availability (e.g., hours) | TEXT          |                             |

####  {#section-4 .unnumbered}

#### 3.5.7 Alert {#alert .unnumbered}

**Table 3.69: Alert**

| Field Name  | Description                               | Data Type   | Constraints                 |
|-------------|-------------------------------------------|-------------|-----------------------------|
| AlertID     | Unique identifier for the alert           | INT         | PRIMARY KEY, AUTO_INCREMENT |
| AlertType   | Type of alert (e.g., Construction)        | VARCHAR(50) | NOT NULL                    |
| LocationID  | Foreign key linking to the Location table | INT         | FOREIGN KEY (Location)      |
| Description | Detailed description of the alert         | TEXT        | NOT NULL                    |
| StartTime   | Start time of the alert                   | DATETIME    |                             |
| EndTime     | End time of the alert                     | DATETIME    |                             |

####  {#section-5 .unnumbered}

#### 3.5.8 Route {#route .unnumbered}

**Table 3.70: Route**

| Field Name            | Description                                  | Data Type | Constraints                 |
|-----------------------|----------------------------------------------|-----------|-----------------------------|
| RouteID               | Unique identifier for the route              | INT       | PRIMARY KEY, AUTO_INCREMENT |
| OriginLocationID      | Foreign key linking to the starting Location | INT       | FOREIGN KEY (Location)      |
| DestinationLocationID | Foreign key linking to the ending Location   | INT       | FOREIGN KEY (Location)      |
| PathDetails           | Information representing the route\'s path   | TEXT      |                             |

####  {#section-6 .unnumbered}

#### 3.5.9 Feedback {#feedback .unnumbered}

**Table 3.71: Feedback**

| Field Name  | Description                                  | Data Type    | Constraints                 |
|-------------|----------------------------------------------|--------------|-----------------------------|
| FeedbackID  | Unique identifier for the feedback           | INT          | PRIMARY KEY, AUTO_INCREMENT |
| UserID      | Foreign key linking to the User table        | INT          | FOREIGN KEY (User)          |
| Category    | Category of feedback (e.g., Obstacle Report) | VARCHAR(100) | NOT NULL                    |
| Description | Detailed description of the feedback         | TEXT         | NOT NULL                    |
| DateTime    | Date and time the feedback was submitted     | DATETIME     | NOT NULL                    |
| LocationID  | Foreign key linking to the Location table    | INT          | FOREIGN KEY (Location)      |

####  {#section-7 .unnumbered}

#### 3.5.10 Confirmed Report {#confirmed-report .unnumbered}

**Table 3.72: Confirmed Report**

| Field Name | Description                                | Data Type | Constraints                    |
|------------|--------------------------------------------|-----------|--------------------------------|
| ReportID   | Unique identifier for the confirmed report | INT       | PRIMARY KEY, AUTO_INCREMENT    |
| FeedbackID | Foreign key linking to the Feedback table  | INT       | FOREIGN KEY (Feedback), UNIQUE |
| LocationID | Foreign key linking to the location table  | INT       | FOREIGN KEY (Location)         |

## 3.6 Design Constraints {#design-constraints .unnumbered}

This section outlines the design constraints and limitations that must
be considered throughout the development of the Campus Accessibility
Navigation (CRN) System. These rules and restrictions could come from
things like the hardware on mobile devices, the software systems they
run, rules and standards we need to follow, issues with the environment
or infrastructure, or policies from organizations involved. The CRN
system is specifically designed for mobile users and must operate
reliably within the constraints of real-time data processing, user
accessibility, and integration with existing university infrastructure.

**Table 3.73: Design Constraints**

| **Requirement ID** | **Description**                                                                                                                                                      | **Priority** | **Author**    |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| REQ_DC001          | The CRN system shall be designed exclusively for mobile devices and must function on both iOS and Android platforms.                                                 | High         | Goh Chun Yong |
| REQ_DC002          | The application shall rely on real-time campus infrastructure data (e.g., elevators, pathways), which may be constrained by sensor availability and network latency. | Medium       | Goh Chun Yong |
| REQ_DC003          | The system shall use the existing university authentication system for user login.                                                                                   | Medium       | Goh Chun Yong |
| REQ_DC004          | The system design must conform to the university's IT security policies and data protection regulations.                                                             | High         | Goh Chun Yong |
| REQ_DC005          | The application shall be optimized for low battery consumption, minimizing GPS polling and background tasks.                                                         | Medium       | Goh Chun Yong |
| REQ_DC006          | CRN system updates and fixes shall be distributed through the respective mobile app stores, subject to their approval processes.                                     | Low          | Goh Chun Yong |
| REQ_DC007          | Major system updates must be scheduled during semester breaks to avoid interruptions in service during academic sessions.                                            | Low          | Goh Chun Yong |
| REQ_DC008          | The system requires a stable internet connection for functionality. Offline mode will not be supported.                                                              | High         | Goh Chun Yong |

## 3.7 Software System Attributes {#software-system-attributes .unnumbered}

This part outlines the key quality features of the Campus Accessibility
Navigation (CRN) system. It mainly looks at how the system behaves
behind the scenes---things like how well it works, how secure and
dependable it is, how easy it is to use and keep up with, and whether it
functions the same way in different places. These qualities help make
sure the system lives up to what users expect and runs smoothly no
matter the situation.

### Availability

**Table 3.74: Availability**

| **Requirement ID** | **Description**                                                                            | **Priority** | **Author**    |
|--------------------|--------------------------------------------------------------------------------------------|--------------|---------------|
| REQ_SSA001         | The system shall maintain at least 99.5% uptime monthly, ensuring continuous availability. | High         | Goh Chun Yong |

### Reliability

**Table 3.75: Reliability**

| **Requirement ID** | **Description**                                                                         | **Priority** | **Author**    |
|--------------------|-----------------------------------------------------------------------------------------|--------------|---------------|
| REQ_SSA002         | The system shall function consistently under normal and expected peak usage conditions. | High         | Goh Chun Yong |

| REQ_SSA003 | All obstacles' reports shall be recorded accurately, ensuring no data loss or corruption.                       | High | Goh Chun Yong |
|------------|-----------------------------------------------------------------------------------------------------------------|------|---------------|
| REQ_SSA004 | The system shall handle a high volume of route request and concurrent users without crashing.                   | High | Goh Chun Yong |
| REQ_SSA005 | The system shall respond to user route queries within 2 seconds and reflect real-time updates within 5 seconds. | High | Goh Chun Yong |

### Security  {#security}

**Table 3.76: Security**

| **Requirement ID** | **Description**                                                                                                           | **Priority** | **Author**    |
|--------------------|---------------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| REQ_SSA006         | The system shall protect user data through secure authentication and encrypted communication.                             | High         | Goh Chun Yong |
| REQ_SSA007         | The platform shall employ encryption and access control to safeguard data.                                                | High         | Goh Chun Yong |
| REQ_SSA008         | The server API shall implement authentication checks to prevent unauthorized access.                                      | High         | Goh Chun Yong |
| REQ_SSA009         | The system shall enforce strong password policies, including a minimum length and complexity requirements.                | High         | Goh Chun Yong |
| REQ_SSA010         | The system shall conduct regular security vulnerability assessments and penetration testing.                              | Medium       | Goh Chun Yong |
| REQ_SSA011         | The platform shall have a built-in firewall to protect against unauthorized access and network attacks.                   | High         | Goh Chun Yong |
| REQ_SSA012         | The platform shall have data masking techniques in place to protect sensitive information in non-production environments. | Medium       | Goh Chun Yong |

### Maintainability

**Table 3.77: Maintainability**

| **Requirement ID** | **Description**                                                                                      | **Priority** | **Author**    |
|--------------------|------------------------------------------------------------------------------------------------------|--------------|---------------|
| REQ_SSA013         | The system shall be built with modular architecture to support easy maintenance and feature updates. | Medium       | Goh Chun Yong |
| REQ_SSA014         | The code shall be maintained and managed using a version control system.                             | High         | Goh Chun Yong |

### Portability

**Table 3.78: Portability**

| **Requirement ID** | **Description**                                                                   | **Priority** | **Author**    |
|--------------------|-----------------------------------------------------------------------------------|--------------|---------------|
| REQ_SSA015         | The system shall support iOS and Android platforms with consistent functionality. | High         | Goh Chun Yong |

## 3.8 Supporting Information {#supporting-information .unnumbered}

This section, additional information will be provided as supporting
information for our system\'s requirements. It will include information
gathered from the requirements elicitation phase.

### 3.8.1 Questionnaire {#questionnaire .unnumbered}

The questionnaire was designed to gather targeted feedback, ensuring a
clear understanding of user needs and expectations. Responses were
collected from 20 participants using online forms through various end
users (Student, Staff, Faculty, Visitor), allowing analysis of user
priorities. There's 14 questions and 2 open ended questions.

[Click here to see the form.](https://forms.gle/hf2fkF1iTNSwabhT8)

|                                                                                                                           |               |                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------|
| Question                                                                                                                  | Kano Category | Justification                                                                                                                   |
| What is your role at the university?                                                                                      | None          | Over 80% of respondents identified as Faculty and Student. Which may introduce bias toward the needs of these groups.           |
| Do you have any accessibility needs (e.g: wheelchair access)?                                                             | None          | Only 25% reported accessibility needs, so the result may introduce bias to non-accessibility groups*.*                          |
| *How important is an up-to-date campus map?*                                                                              | Dissatisfiers | 85% combined Very/Somewhat important signals up-to-date campus map is a must for end users.                                     |
| *Would missing maintenance updates affect your navigation?*                                                               | Dissatisfiers | 90% chose Significantly/Slightly, indicating maintenance updates are very much needed.                                          |
| *Should administrators validate accessibility info?*                                                                      | Dissatisfiers | 75% agree and strongly agree, therefore there's a need for admin to validate *accessibility info.*                              |
| How essential is route planning across campus for your daily navigation?                                                  | Dissatisfiers | 60% say it's useful but not critical. So, it's helpful but not essential.                                                       |
| Would you use multiple interfaces or modes (e.g: fastest route, event-free route)?                                        | Satisfiers    | 9 agree and 10 neutral. Therefore, it's a bonus feature to have.                                                                |
| How valuable are user surveys and feedback features for you to report navigation issues?                                  | Satisfiers    | 11 says useful and 8 says very valuable. Therefore, it should be included but it won't be that impressive to have this feature. |
| How important is integration with university events/facilities (e.g: closures due to events, facility used due to event)? | Satisfiers    | Only 10% say it's not important, so this feature is important for most people.                                                  |
| Would you find an event list view useful to plan your routes better?                                                      | Satisfiers    | The feedback is mixed; therefore, it can be needed or not.                                                                      |
| Would you appreciate a feature that suggests accessible routes for users with disabilities?                               | Delighters    | 45% agree and 35% neutral, so it's a good feature to have.                                                                      |
| How useful would it be if you could customize your privacy or access settings in the app?                                 | Delighters    | Majority agreed is a good feature to have.                                                                                      |
| Would you be interested in contributing updates (e.g: "path blocked due to construction") to help others?                 | Delighters    | 12 people neutral and 8 chose yes, so it's a good feature to have.                                                              |
| Would you be excited about real-time event alerts that let you avoid crowds or disruptions?                               | Delighters    | 45% says absolute while 40% neutral. So it's a bonus feature to have.                                                           |
| Are there any other features you\'d like to see in the navigation system?                                                 | None          | People have different of opinions for this, for more details please view proof of execution section.                            |
| What's your biggest frustration when navigating campus?                                                                   | None          | People have different of opinions for this, for more details please view proof of execution section.                            |

Questionnaire (Proof of Execution)

**What is your role at the university**

![Forms response chart. Question title: What is your role at the
university?. Number of responses: 28 responses.,
Picture](media/image19.png){width="6.260415573053368in"
height="2.6354166666666665in"}

**Do you have any accessibility needs (e.g: wheelchair access)?**

![Forms response chart. Question title: Do you have any accessibility
needs (e.g: wheelchair access)? . Number of responses: 28 responses.,
Picture](media/image20.png){width="5.802084426946632in"
height="2.4479166666666665in"}

**How important is it for you to have an up-to-date and accurate campus
map in the app?**

![Forms response chart. Question title: How important is it for you to
have an up-to-date and accurate campus map in the app? . Number of
responses: 28 responses.,
Picture](media/image21.png){width="6.260415573053368in"
height="2.6354166666666665in"}

**Would missing maintenance updates (e.g: blocked paths, elevator
outages) affect your campus navigation?**

![Forms response chart. Question title: Would missing maintenance
updates (e.g: blocked paths, elevator outages) affect your campus
navigation? . Number of responses: 28 responses.,
Picture](media/image22.png){width="5.960099518810149in"
height="2.6875in"}

**Should administrators validate accessibility info reported by users
before it\'s displayed?**

![Forms response chart. Question title: Should administrators validate
accessibility info reported by users before it\'s displayed? . Number of
responses: 28 responses.,
Picture](media/image23.png){width="6.260415573053368in"
height="2.6354166666666665in"}

**How essential is route planning across campus for your daily
navigation?**  
![Forms response chart. Question title: How essential is route planning
across campus for your daily navigation? . Number of responses: 28
responses., Picture](media/image24.png){width="6.260415573053368in"
height="2.6354166666666665in"}

**Would you use multiple interfaces or modes (e.g: fastest route,
event-free route)?**

![Forms response chart. Question title: Would you use multiple
interfaces or modes (e.g: fastest route, event-free route)?. Number of
responses: 28 responses.,
Picture](media/image25.png){width="6.260415573053368in"
height="2.6354166666666665in"}

**How valuable are user surveys and feedback features for you to report
navigation issues?**

1 = Not Valuable; 3 = Very Valuable

![Forms response chart. Question title: How valuable are user surveys
and feedback features for you to report navigation issues?. Number of
responses: 28 responses.,
Picture](media/image26.png){width="6.260415573053368in"
height="2.9791666666666665in"}

**How important is integration with university events/facilities (e.g:
closures due to events, facility used due to event)?**

1 = Not Important; 3 = Very Important

![Forms response chart. Question title: How important is integration
with university events/facilities (e.g: closures due to events, facility
used due to event)?. Number of responses: 28 responses.,
Picture](media/image27.png){width="6.260415573053368in"
height="3.1770833333333335in"}

**Would you find an event list view useful to plan your routes better?**

![Forms response chart. Question title: Would you find an event list
view useful to plan your routes better? . Number of responses: 28
responses., Picture](media/image28.png){width="6.260415573053368in"
height="2.6354166666666665in"}

**Would you appreciate a feature that suggests accessible routes for
users with disabilities?**

1 = Not at all;3= Yes

![Forms response chart. Question title: Would you appreciate a feature
that suggests accessible routes for users with disabilities? . Number of
responses: 28 responses.,
Picture](media/image29.png){width="5.761888670166229in"
height="2.746599956255468in"}

**How useful would it be if you could customize your privacy or access
settings in the app?**

1 = Useless;5 = Very Useful

![Forms response chart. Question title: How useful would it be if you
could customize your privacy or access settings in the app? . Number of
responses: 28 responses.,
Picture](media/image30.png){width="5.66666447944007in"
height="2.6966163604549434in"}

**Would you be interested in contributing updates (e.g: "path blocked
due to construction") to help others?**

![Forms response chart. Question title: Would you be interested in
contributing updates (e.g: "path blocked due to construction") to help
others? . Number of responses: 28 responses.,
Picture](media/image31.png){width="6.260415573053368in"
height="2.8229166666666665in"}

***Would you be excited about real-time event alerts that let you avoid
crowds or disruptions?***

![Forms response chart. Question title: Would you be excited about
real-time event alerts that let you avoid crowds or disruptions? .
Number of responses: 28 responses.,
Picture](media/image32.png){width="6.260415573053368in"
height="2.6354166666666665in"}

**Are there any other features you\'d like to see in the navigation
system?**

![image19.png, Picture, Picture](media/image33.png){width="4.34375in"
height="1.3020581802274716in"}

![image12.png, Picture,
Picture](media/image34.png){width="2.792311898512686in"
height="1.1432294400699912in"}

**What's your biggest frustration when navigating campus?**

![image26.png, Picture, Picture](media/image35.png){width="2.4375in"
height="1.25in"}

![image27.png, Picture, Picture](media/image36.png){width="2.0625in"
height="1.2708333333333333in"}

### 3.8.2 Prototyping {#prototyping .unnumbered}

[Click here to see the prototype we
did.](https://www.figma.com/design/TCdjcsfnZo6Zbta0dT9KMT/SE-assignment?node-id=20-65&t=apaAt6nWiklyywKx-1)

**Logged Out**

![Picture](media/image37.png){width="3.0208333333333335in"
height="6.0in"}

This is the first screen that greets users of the MMU application. It
prominently displays the university logo and includes a \"GET STARTED\"
button to begin the user experience. Clicking "GET STARTED" takes the
user to the login page.

**Sign-In Page**  
![Picture](media/image38.png){width="3.2395833333333335in"
height="6.5in"}

This page verifies users prior to their entry into the app\'s main
functionalities. Users input their ID and password and click the red
\"SIGN IN\" button. There's also a choice to proceed as a guest, which
may offer restricted access. A successful login directs the user to the
campus navigation system.

**Initial navigation page**

![Picture](media/image39.png){width="3.3020833333333335in"
height="6.5in"}

This page provides live navigation with danger alerts, improving campus
security. Displays a real-time image/map of the campus featuring an
alert notification at the top (e.g., \"200 m Construction ahead\"). A
red button for "Travel Mode" initiates navigation, and users can select
their starting location and endpoint at the bottom. Beneficial for
incoming students and guests who are not acquainted with the campus
design or existing challenges.

**Searching Page**

![Picture](media/image40.png){width="2.9270833333333335in"
height="5.875in"}

Allows users to look for and choose locations within the campus. Users
enter their current location and desired destination in the given search
fields. While they are typing, options such as "Faculty of Computer &
Informatics" show up underneath. Aids in simplifying campus navigation
by providing autocomplete recommendations.

Navigating Page

![Picture](media/image41.png){width="3.25in" height="6.5in"}

Gives step-by-step navigation once the route begins. Displays a map
interface with navigational instructions (e.g., "Turn Left in 200 m").
The interface still includes the red "Travel Mode" button and shows trip
details at the bottom (e.g., time, distance). Helpful for making certain
the user adheres to the right route in real-time.

**Expand (Show event information) Page**

![Picture](media/image42.png){width="3.2708333333333335in"
height="6.5in"}

Emphasizes current and incoming university activities. Shows the present
time, distance to the destination, and duration at the top. Underneath,
occasions like the \"Career Fair\" are provided along with their date,
time, and venue. Informs students about campus events while blending
academics with student life.

**Event Calendar Page**

![Picture](media/image43.png){width="3.2395833333333335in"
height="6.5in"}

Enables users to browse and sign up for events through a calendar
interface. The upper section features a calendar for viewing events
based on their dates. The bottom part provides specific event details
and offers choices to delete or sign up. Offers an efficient method for
students to organize their extracurricular activities.  
  
**Admin Dashboard**

![Picture](media/image44.png){width="3.2395833333333335in"
height="6.5in"}

Acts as the hub for administrative operations. Accesses the event
management section where administrators can alter or create events.
Accesses a page where all user-provided feedback, including hazard or
obstacle reports, can be assessed and organized. User-friendly
button-driven navigation enhances accessibility and effectiveness.

**Admin Editing Event**

![Picture](media/image45.png){width="3.09375in" height="6.15625in"}

Enables administrators to access and alter planned events. A date is
chosen through a calendar interface. The following section outlines the
current events for the chosen date, including comprehensive information
(event title, venue, schedule, interest rating, and sign-ups). Admins
are able to modify the event\'s information in the input fields. The
Delete and Save Changes buttons facilitate convenient event management.
The distinct visual hierarchy and user-friendly interface decrease
cognitive strain for administrators.

**Admin Adding Event**

![Picture](media/image46.png){width="3.0520833333333335in"
height="6.239584426946632in"}

Facilitates the formation of new events. Admins enter the event\'s name,
date, time, and venue. Buttons offered for saving the new event or
canceling the entry. Promotes effective organization and timing of
campus events through the ability to create events in real time.

**User Feedback**

![Picture](media/image47.png){width="3.3020833333333335in"
height="6.5in"}

Shows reports submitted by users regarding campus conditions. A dropdown
menu allows administrators to sort reports by category (e.g., "Obstacles
Reports", "Construction Reports", "Others"). Every feedback card
contains a report ID, category, overview, username, and time stamp.
Admins have the option to reply using the Message button or create a
Print Report. Promotes campus safety and facility oversight by
facilitating organized access to user input.

# Verification

## 4.1 Verification Approach {#verification-approach .unnumbered}

This section specifies how the Campus Accessibility Navigation System
"CRN" software will be verified.

### How {#how .unnumbered}

**Table 4.1 \*How\* Verification Table**

| Testing Type              | Description                                                                                                                                                                |
|---------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Functional Testing**    | Test each function in Section 3.1 (Functions) to ensure each function performs as expected output.                                                                         |
| **Usability Testing**     | Through users interacting with the system to detect any usability issues, and gather feedback from the user interface as described in Section 3.3(Usability requirements). |
| **Performance Testing**   | Evaluate system's performance, responsiveness, and stability under expected load conditions.                                                                               |
| **Accessibility Testing** | Verifying the system meets the accessibility requirements outlined in Section 3.3(Usability requirements)                                                                  |
| **Security Testing**      | Using potential vulnerabilities against authentication mechanisms, data privacy, and protection.                                                                           |

### Who {#who .unnumbered}

**Table 4.2 \*Who\* Verification Table**

| Name                       | Description                                                                                                                                                                                          |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Development Team (Group 3) | Will be responsible for conducting unit testing during development and initial functional and integration testing of their respective modules.                                                       |
| Quality Assurance Team     | Will be responsible for independent functional testing, usability testing, performance testing, integration testing, accessibility testing, and security testing in a dedicated testing environment. |
| Stakeholders/End Users     | Representative users from the different actor roles will participate in usability testing sessions to provide feedback on the system\'s ease of use and effectiveness.                               |

### When {#when .unnumbered}

**Table 4.3 \*When\* Verification Table**

| Timeline                                                   | Description                                                                                                                      |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **During each sprint/iteration**                           | Unit testing will be performed by developers as code is written. After the completion of significant modules.                    |
| **After the completion of significant features/modules**   | Functional and integration testing will be conducted by the development and/or QA team. Periodically throughout development      |
| **At the end of development cycles/before major releases** | Comprehensive system testing, performance testing, security testing, and accessibility testing will be performed by the QA team. |

###  {#section-8 .unnumbered}

### Where {#where .unnumbered}

1.  **Developer Workstations**:

    - Unit testing will be conducted by developers on their local
      machines.

2.  **Dedicated QA Testing Environment**:

    - Functional testing, integration testing, performance testing,
      security testing, and accessibility testing will be performed in a
      controlled environment that mimics the production environment as
      closely as possible.

3.  **Usability Labs or Representative User Locations**:

    - Usability testing sessions may take place in controlled lab
      settings or with users in their natural environment (e.g., on the
      university campus).

## Verification Criteria

This section defines the criteria against which the software will be
verified.

**Functional Testing**

- The system should correctly display events by date, time, and venue.

- Notification should trigger at scheduled time

- Admin should be able to validate reported issues and manage event data

**Usability Testing**

- New User should be able to use core features within 10 minutes of
  first use.

- All screens should be navigable with no more than 3 clicks to access
  core features.

- Error messages should guide users to resolution

- Average user rating in feedback should be at least 4 out of 5.

**Performance Testing**

- Under stress conditions, 95% of operations shall complete within 5
  seconds.

- Calendar view should load in under 3 seconds on first open.

- Notifications should be delivered within 5 seconds of their scheduled
  time.

- CRN should handle up to 500 concurrent users without degrading
  performance.

**Accessibility Testing**

- The interface shall be fully navigable using only a keyboard.

- User should be able to adjust text size.

- Alternative text must be provided for all images and icon.

**Security Testing**

- Users must be able to successfully log in with valid credentials

- The system should reject invalid credentials with an appropriate error
  message

- Sessions should automatically expire after 30 minutes of inactivity.

# Appendices

### 5.1 Assumptions and dependencies {#assumptions-and-dependencies .unnumbered}

**Assumptions:**

- **Availability and Accuracy of Campus Data:**

  - Campus information systems (for facilities and events) will provide
    reliable and up-to-date data through their APIs or other integration
    methods.

  - Data provided by these systems regarding accessibility features is
    accurate and consistently formatted.

  - Detailed digital map of the campus is available and can be
    integrated into the system.

- **User Device Capabilities:**

  - Majority of target users will have smartphones with sufficient
    processing power, storage, and connectivity (cellular or Wi-Fi) to
    run the mobile application effectively.

  - User devices have functional GPS capabilities for location services.

- **User Willingness and Ability to Use the System:**

  - Users will be willing to download and use the mobile application.

  - Basic level of digital literacy among the target user groups.

  - Users willing to provide necessary permissions (e.g., location
    access) for the application to function correctly.

- **Network Connectivity:**

  - Users generally have access to a reliable network connection (Wi-Fi
    or cellular data) on campus to utilize the real-time features of the
    application.

- **Third-Party Service Availability:**

  - Availability and stable operation of any third-party services
    integrated into the system (e.g., mapping services, push
    notification services).

- **Adherence to Accessibility Standards:**

  - Campus infrastructure (e.g., ramps, elevators, accessible restrooms)
    is maintained according to relevant accessibility standards.

**Dependencies:**

- **Integration with Campus Information Systems:** Our system ability to
  provide up-to-date information come from campus's existing data
  system.

- **Availability of Accurate Map Data:** Core functionalities of our
  system is dependent on the accuracy of digital map provided by the
  university.

- **Functionality of User Devices:** User's device hardware can impact
  the performance of the system as outdated operating system or
  graphical card can cause error running the software.

- **Network Infrastructure:** Stable internet on both user and campus is
  required as real-time features and updates of the system cannot be
  work without connection of internet.

- **Third-Party Service APIs:** The system\'s functionality depends on
  the APIs provided by external services like map service to provide
  routing.

- **User Adoption and Feedback:** Improvements of the system depends on
  the user review as their experience can reveal error in the system and
  understand what the client would like to see enhanced.

- **Maintenance and Updates:** The system needs consistency updates of
  data to ensure accuracy, maintenance requires to be schedule per week
  for compatibility and bugs free experience for users.

### 5.2 Acronyms and Abbreviations {#acronyms-and-abbreviations .unnumbered}

**Table 5.1 Acronyms and Abbreviations**

| Term/Abbreviation | Definition                                                                                                                                   |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| GUI               | Graphical User Interface: a way of arranging information on a computer screen that is easy to understand and use.                            |
| GPS               | Global Positioning System: global positioning system that can show the exact position of a person or thing by using signals from satellites. |
| Wi-Fi             | Wireless Fidelity: a system for connecting electronic equipment to the internet without using wires.                                         |
| API               | Application Programming Interface: way of communicating with a particular computer program.                                                  |
| Authentication    | Process of verifying the identity of a user or system.                                                                                       |
| Authorization     | Process of giving power to a user or system for a particular domain.                                                                         |
| Navigation System | A system that guides user to find and reach locations.                                                                                       |
| Real-time Data    | Information delivered to the destination with no delay.                                                                                      |
| Server            | Service from a computer program or device for another computer program and its client.                                                       |
| Client            | A piece of computer hardware or software that accesses a service made available by a server.                                                 |
| Prototype         | Early design product view of a software or system.                                                                                           |
| Stakeholder       | A person, group, or organization that has an interest or concern in a project or business.                                                   |
| Module            | Unit with large system for a specific function.                                                                                              |
