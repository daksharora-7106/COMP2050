# COMP2050
# ChargeMate Ops – Initial System Requirements Analysis

## Project Overview

ChargeMate Ops is a proposed operator-facing software system designed to support the management of ChargeMate's portable phone-charging power bank service at Harbour North Plaza. The shopping centre contains a variety of facilities, including a supermarket, food court, cinema, medical centre, library branch and bus interchange. As these areas experience different levels of activity throughout the day, ChargeMate requires an effective way for staff to monitor and manage the distribution and condition of power banks and rental stations across the centre.

The purpose of ChargeMate Ops is to provide staff with a centralised view of the power bank network and reduce reliance on manual processes such as sticky notes, repeated physical checks or staff members remembering unresolved issues. The system should provide operators with enough information to understand the current state of the service and determine when action may be required. This is particularly important because demand may vary depending on location, time of day and events occurring within Harbour North Plaza.

## System Scope

ChargeMate Ops will focus specifically on the operational and staff-facing aspects of the ChargeMate service. The system should allow authorised staff to monitor rental stations and the power banks associated with them. Staff should be able to determine whether stations are operating normally and identify stations or individual power banks that may require attention.

The system may also support staff in tracking the movement and status of power banks throughout the shopping centre. For example, an operator may need to identify whether a power bank is currently available, rented, returned, charging, reported as faulty or otherwise unavailable. Having this information available through one system would allow staff to respond more efficiently when problems occur.

Another important aspect of the system is the management of faults and unusual situations. Power banks may be returned to unexpected locations, reported as faulty, remain unreturned for an extended period or have conflicting status information within different parts of the service. Rental stations themselves may also experience problems that are not immediately visible to customers. ChargeMate Ops should therefore provide operators with a way to identify, record and follow up on these situations.

## Initial Functional Requirements

Based on the initial project brief, several potential functional requirements have been identified. These requirements will need to be discussed and refined through stakeholder interviews before being considered final.

The system should allow authorised operators to view the current status of ChargeMate rental stations located throughout Harbour North Plaza. Information displayed may include the operational state of a station, the number of power banks currently available and whether the station requires staff attention.

Operators should also be able to view information about individual power banks. This could include a unique device identifier, its current location and its current operational status. The system should support the reporting and management of faulty power banks so that damaged or unreliable devices are not treated as normally available devices.

ChargeMate Ops should support the redistribution of power banks between stations. Demand is likely to vary throughout the shopping centre. For example, stations near the food court may experience greater demand around lunchtime, while stations near the cinema may experience greater demand during the evening. Operators may therefore need to identify stations with low availability and move available power banks from another location.

The system may provide alerts when situations require staff attention. Possible examples include a station becoming unavailable, a station running low on charged power banks, a device being reported as faulty or a power bank remaining unreturned beyond an expected period. The exact conditions that generate alerts and their priority will need to be confirmed with the stakeholders.

## Non-Functional Considerations

ChargeMate Ops should be reliable because staff may depend on the information displayed by the system when making operational decisions. Information about stations and power banks should therefore be kept sufficiently current so that operators are not regularly acting on outdated information.

Usability will also be important. Staff should be able to quickly identify problems and determine which stations or devices require attention without needing extensive technical knowledge. Information should be presented clearly, particularly when several stations are operating simultaneously across Harbour North Plaza.

Security and access control should also be considered because ChargeMate Ops is intended for operational staff rather than customers. Access to operational information and management functions should be restricted to authorised users. Further stakeholder consultation will be required to determine whether different staff roles require different levels of access.

## Interaction With the Customer-Facing System

ChargeMate Ops will operate alongside the customer-facing ChargeMate system being specified by Team A. Some information will likely need to be exchanged between the two systems. For example, customer rental and return activities may affect the operational status and location of power banks displayed within ChargeMate Ops.

However, the exact information exchanged between the systems has not yet been established. This should be investigated during stakeholder interviews with Team A to ensure that both systems use consistent information and clearly defined responsibilities.

ChargeMate Ops will not be responsible for implementing the customer rental application, payment process, customer account management or kiosk rental journey. These functions are outside the scope of this project and belong to Team A's customer-facing system.

## Further Requirements Investigation

The requirements described above represent an initial interpretation of the ChargeMate Ops project brief and should not yet be treated as the complete set of system requirements. Further requirements will be identified and existing requirements refined through consultation with the stakeholder representatives.

Future discussions should investigate areas such as staff roles and permissions, how frequently station information should be updated, what conditions should generate alerts, how faults should be recorded and resolved, how unreturned power banks should be handled, and what information needs to be exchanged with the customer-facing system.

These stakeholder discussions will allow the team to convert the initial ideas presented in the project brief into clear, testable and agreed software requirements for the final Software Requirements Specification.

## Use Case Descriptions

The following use cases describe some of the main interactions between ChargeMate staff and the ChargeMate Ops system. These are initial use cases based on the provided project brief and may be updated or expanded after further stakeholder discussions with Team A.

## Use Case Descriptions

---

### UC-01 – View Station Status

**Goal:**  
Allow a ChargeMate operator to view the current operational status of rental stations across Harbour North Plaza.

**Preconditions:**  
- The operator has access to ChargeMate Ops.
- The rental stations are registered in the system.
- Station information is available to ChargeMate Ops.

**Success End Condition:**  
The operator successfully views the current status and relevant information for a selected rental station.

**Failed End Condition:**  
The operator is unable to retrieve the station information or the system cannot provide a reliable status.

**Primary Actor:**  
ChargeMate Operator

**Secondary Actors:**  
- Rental Station System
- Customer-Facing ChargeMate System

**Trigger:**  
The operator wants to check whether a rental station is operating correctly or requires staff attention.

#### Description / Main Success Scenario

| Step | Action |
|---|---|
| 1 | The operator opens the station monitoring section in ChargeMate Ops. |
| 2 | The system retrieves the latest available information about the rental stations. |
| 3 | The system displays the list of rental stations and their current status. |
| 4 | The operator selects a station to view more details. |
| 5 | The system displays information such as station status, power bank availability and any identified issues. |
| 6 | The operator reviews the information and determines whether the station requires attention. |

#### Alternative Flows

| Step | Action |
|---|---|
| 2A | If the system cannot retrieve station information, it informs the operator that the data is currently unavailable. |
| 3A | If a station has an identified fault or operational issue, the system clearly marks the station as requiring attention. |
| 5A | If the information appears outdated or inconsistent, the system indicates this to the operator. |

---

### UC-02 – Track a Power Bank

**Goal:**  
Allow a ChargeMate operator to locate and view the current information associated with an individual power bank.

**Preconditions:**  
- The operator has access to ChargeMate Ops.
- The power bank is registered in the system.
- The power bank has a unique identifier.

**Success End Condition:**  
The operator successfully views the available status and location information for the selected power bank.

**Failed End Condition:**  
The requested power bank cannot be found or reliable information about the device cannot be retrieved.

**Primary Actor:**  
ChargeMate Operator

**Secondary Actors:**  
- Rental Station System
- Customer-Facing ChargeMate System

**Trigger:**  
The operator needs to locate a particular power bank or check its current status.

#### Description / Main Success Scenario

| Step | Action |
|---|---|
| 1 | The operator opens the power bank management section. |
| 2 | The operator searches for or selects a power bank using its unique identifier. |
| 3 | The system retrieves the available information for the selected power bank. |
| 4 | The system displays the power bank's identifier, current status and location information. |
| 5 | The operator reviews the information. |
| 6 | The operator determines whether any further operational action is required. |

#### Alternative Flows

| Step | Action |
|---|---|
| 2A | If the operator enters an invalid or unknown power bank identifier, the system informs them that the device could not be found. |
| 3A | If the location of the power bank is unavailable, the system displays the location as unknown or unavailable. |
| 4A | If conflicting information exists for the power bank, the system indicates that the status requires investigation. |

---

### UC-03 – Report and Manage a Faulty Power Bank

**Goal:**  
Allow a ChargeMate operator to record, manage and resolve a fault associated with a power bank.

**Preconditions:**  
- The operator has access to ChargeMate Ops.
- The affected power bank is registered in the system.
- The operator has permission to record faults.

**Success End Condition:**  
The fault is successfully recorded against the correct power bank and the device is marked as requiring attention or unavailable.

**Failed End Condition:**  
The fault is not recorded successfully, or the operator cannot identify the affected power bank.

**Primary Actor:**  
ChargeMate Operator

**Secondary Actors:**  
- Rental Station System
- Customer-Facing ChargeMate System
- Maintenance Staff, if applicable

**Trigger:**  
A power bank is reported or identified as faulty.

#### Description / Main Success Scenario

| Step | Action |
|---|---|
| 1 | The operator searches for and selects the affected power bank. |
| 2 | The system displays the current information for the selected power bank. |
| 3 | The operator selects the option to report a fault. |
| 4 | The operator enters details about the fault. |
| 5 | The system validates the entered information. |
| 6 | The system records the fault against the selected power bank. |
| 7 | The system updates the power bank status to indicate that it requires attention or is unavailable. |
| 8 | The operator later reviews the fault after the issue has been investigated. |
| 9 | Once resolved, the operator updates the fault status. |

#### Alternative Flows

| Step | Action |
|---|---|
| 1A | If the power bank cannot be found, the system informs the operator and the fault cannot be recorded against that device. |
| 4A | If required fault information is missing, the system asks the operator to provide the missing details. |
| 6A | If the system cannot save the fault, the operator is informed that the fault was not successfully recorded. |
| 9A | If the issue has not been resolved, the fault remains active and the power bank continues to be marked as requiring attention. |

### UC-04 – Redistribute Power Banks Between Stations

**Goal:**  
Allow a ChargeMate operator to manage the movement of power banks between rental stations to maintain suitable availability across Harbour North Plaza.

**Preconditions:**  
- The operator has access to ChargeMate Ops.
- The source and destination stations are registered in the system.
- The selected power banks are available for redistribution.
- The destination station has capacity to accept additional power banks.

**Success End Condition:**  
The selected power banks are successfully moved and the system reflects their updated location and status.

**Failed End Condition:**  
The redistribution cannot be completed because the selected power banks are unavailable, the destination station cannot accept them, or the system cannot update the movement.

**Primary Actor:**  
ChargeMate Operator

**Secondary Actors:**  
- Rental Station System
- Other ChargeMate Staff responsible for physically moving the devices

**Trigger:**  
The operator identifies that one station requires additional available power banks while another station has devices that can be redistributed.

#### Description / Main Success Scenario

| Step | Action |
|---|---|
| 1 | The operator reviews the current status and availability of rental stations. |
| 2 | The operator identifies a station with low power bank availability. |
| 3 | The operator identifies another station with suitable power banks available for redistribution. |
| 4 | The operator selects the power bank or power banks to be moved. |
| 5 | The system records the planned redistribution. |
| 6 | The selected power banks are physically moved from the source station to the destination station. |
| 7 | The operator confirms that the redistribution has been completed. |
| 8 | The system updates the recorded location and status of the affected power banks. |
| 9 | The system displays the updated availability of both stations. |

#### Alternative Flows

| Step | Action |
|---|---|
| 3A | If no suitable power banks are available for redistribution, the system informs the operator. |
| 4A | If a selected power bank is faulty or unavailable, the system prevents it from being treated as available for redistribution. |
| 5A | If the destination station is full or unavailable, the redistribution cannot proceed and the operator is informed. |
| 7A | If the physical movement is not completed, the operator does not confirm the redistribution and the system should not record it as successfully completed. |
| 8A | If the system cannot update the new location, it informs the operator that the redistribution record may require further attention. |