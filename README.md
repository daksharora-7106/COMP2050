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