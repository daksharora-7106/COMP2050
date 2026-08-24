# ChargeMate Ops – Stakeholder Meeting Minutes

## Meeting Details

**Project:** ChargeMate Ops  
**Team:** Team B  
**Stakeholder Representative:** Team A  
**Purpose:** Initial requirements gathering and clarification  
**Meeting Type:** Client / Stakeholder Interview  

---

## Meeting Purpose

The purpose of this meeting is to gather additional requirements for the ChargeMate Ops system and clarify areas of the initial project brief that are currently unclear.

The discussion focuses on how operators will monitor rental stations, track individual power banks, manage faults, redistribute power banks between stations, and respond to operational issues. The meeting also aims to clarify what information needs to be exchanged between ChargeMate Ops and the customer-facing system being considered by Team A.

---

## Questions for Team A

### Station Monitoring

1. What information should operators be able to see about each rental station?

2. What different statuses should a station have, such as operational, offline, low availability, or requiring attention?

3. Should operators be able to see how many charged and available power banks are currently at each station?

4. How frequently should station information be updated?

5. What should happen if the system cannot retrieve the current status of a station?

### Power Bank Tracking

6. What information should operators be able to see about an individual power bank?

7. What statuses should a power bank have, such as available, rented, charging, faulty, missing, or unavailable?

8. Should operators be able to search for a power bank using a unique ID?

9. Should the system show the current or last known location of each power bank?

10. What should happen if different parts of the system show conflicting information about the same power bank?

### Fault Management

11. How should an operator report a faulty power bank?

12. What information should staff record when reporting a fault?

13. Should faults have different categories or priority levels?

14. Who should be allowed to mark a fault as resolved?

15. Should a faulty power bank automatically become unavailable for rental?

### Redistribution of Power Banks

16. Should ChargeMate Ops notify staff when a station is running low on available power banks?

17. Should the system recommend which station power banks should be moved from, or should staff make this decision themselves?

18. Should the system keep a record of power banks being moved between stations?

19. What should happen if the destination station is already full or unavailable?

### Alerts and Operational Problems

20. What situations should generate an alert for ChargeMate staff?

21. Should alerts have different priority levels?

22. How should unreturned power banks be handled by the operations system?

23. What should happen when a power bank is returned to an unexpected or incorrect location?

24. Should staff be able to mark an alert or issue as resolved so other operators know that it has already been handled?

### Interaction With Team A's System

25. What information does the customer-facing system need to send to ChargeMate Ops?

26. What information does ChargeMate Ops need to send back to the customer-facing system?

27. When a customer rents or returns a power bank, should ChargeMate Ops receive the update immediately?

28. If a power bank is marked as faulty by an operator, should Team A's system automatically prevent customers from renting it?

---

## Requirements Discussed

The initial discussion areas identified for ChargeMate Ops include:

- Monitoring rental station status.
- Viewing the availability of power banks at different stations.
- Tracking individual power banks and their locations.
- Recording and managing faulty power banks.
- Identifying unreturned or incorrectly returned power banks.
- Redistributing power banks between stations.
- Providing operational alerts when staff attention is required.
- Maintaining accurate and up-to-date operational information.
- Restricting operational functions to authorised staff.
- Exchanging relevant information with Team A's customer-facing system.

---

## Actions / Next Steps

- Record Team A's answers to the stakeholder questions.
- Update the initial functional and non-functional requirements based on stakeholder feedback.
- Refine the existing use case descriptions.
- Identify any new use cases discovered during the interview.
- Confirm the information that must be exchanged between Team A's system and ChargeMate Ops.
- Update the SRS with the agreed requirements.