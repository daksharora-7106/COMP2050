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

### UC-01 – View Station Status

**Primary Actor:** ChargeMate Operator

**Goal:**  
Allow an operator to view the current status of rental stations located throughout Harbour North Plaza.

**Preconditions:**
- The operator is authorised to access ChargeMate Ops.
- Station information is available to the system.

**Trigger:**  
The operator wants to check the current condition or availability of one or more rental stations.

**Main Flow:**
1. The operator accesses the station monitoring section of ChargeMate Ops.
2. The system retrieves information about the rental stations.
3. The system displays the available stations and their current status.
4. The operator selects a station to view more information.
5. The system displays available operational information for the selected station.
6. The operator determines whether the station is operating normally or requires attention.

**Alternative / Exception Flows:**
- If station information cannot be retrieved, the system informs the operator that the information is currently unavailable.
- If a station has an identified problem, the system indicates that the station may require staff attention.
- If the information for a station appears outdated or inconsistent, the system should make this clear to the operator.

**Postconditions:**
- The operator has viewed the available status information for the selected station.
- No station information is changed simply by viewing its status.


### UC-02 – Track a Power Bank

**Primary Actor:** ChargeMate Operator

**Goal:**  
Allow an operator to locate and view information about an individual ChargeMate power bank.

**Preconditions:**
- The operator is authorised to access ChargeMate Ops.
- The power bank is registered within the ChargeMate system.

**Trigger:**  
The operator needs to check the location or current status of a particular power bank.

**Main Flow:**
1. The operator accesses the power bank management section.
2. The operator searches for or selects a power bank.
3. The system retrieves the available information for the selected power bank.
4. The system displays the power bank's unique identifier and current status.
5. The system displays its current or most recently known location where available.
6. The operator reviews the information and determines whether further action is required.

**Alternative / Exception Flows:**
- If the power bank cannot be found, the system informs the operator.
- If the location of the power bank is unknown, the system displays the location as unavailable or unknown.
- If different parts of the system contain conflicting information about the power bank, the system should indicate that the status requires investigation.

**Postconditions:**
- The operator has viewed the available information about the selected power bank.
- The operator may decide to perform another operational action if a problem has been identified.


### UC-03 – Report and Manage a Faulty Power Bank

**Primary Actor:** ChargeMate Operator

**Goal:**  
Allow an operator to record and manage a power bank that has been identified as faulty.

**Preconditions:**
- The operator is authorised to access ChargeMate Ops.
- The power bank exists within the ChargeMate system.

**Trigger:**  
A power bank is reported or identified as faulty and requires staff attention.

**Main Flow:**
1. The operator searches for and selects the affected power bank.
2. The system displays the current information about the power bank.
3. The operator selects an option to report or record a fault.
4. The operator enters the available information about the fault.
5. The system records the fault against the selected power bank.
6. The system updates the power bank's operational status.
7. The system indicates that the power bank requires attention.
8. The operator can later review the fault and update its status after the issue has been investigated.

**Alternative / Exception Flows:**
- If the power bank cannot be identified, the operator is informed that the device could not be found.
- If required fault information has not been entered, the system asks the operator to provide the missing information.
- If the fault cannot be recorded because of a system problem, the system informs the operator and does not incorrectly mark the issue as successfully recorded.

**Postconditions:**
- The fault is recorded against the appropriate power bank.
- The power bank is identifiable as requiring attention.
- The fault remains available for staff to review until it has been appropriately resolved.


### UC-04 – Redistribute Power Banks Between Stations

**Primary Actor:** ChargeMate Operator

**Goal:**  
Allow an operator to manage the movement of power banks between rental stations when redistribution is required.

**Preconditions:**
- The operator is authorised to access ChargeMate Ops.
- The relevant stations and power banks are registered in the system.
- The power bank is available for redistribution.

**Trigger:**  
The operator identifies that power banks should be moved between stations, such as when one location has low availability while another has additional available devices.

**Main Flow:**
1. The operator reviews the status of rental stations.
2. The operator identifies a station that may require additional power banks.
3. The operator identifies another station from which suitable power banks can be moved.
4. The operator selects the relevant power bank or power banks for redistribution.
5. The system records the redistribution activity.
6. The power banks are physically moved between the relevant stations.
7. The system updates the recorded location or status of the affected power banks.
8. The operator confirms that the redistribution has been completed.

**Alternative / Exception Flows:**
- If there are no suitable power banks available for redistribution, the system informs the operator.
- If a selected power bank is faulty or otherwise unavailable, it should not be treated as normally available for redistribution.
- If the destination station cannot accept the selected power bank, the operator is informed and the redistribution is not recorded as completed.

**Postconditions:**
- Successfully redistributed power banks are associated with their new station.
- The system reflects the updated operational situation of the affected stations.

