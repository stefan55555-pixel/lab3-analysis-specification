# lab3-analysis-specification
lab3-analysis &amp; specification

** Stefan Krstic — T00199336
**Date:** 19/10/26

**Stakeholders
|Stakeholder |
|---|
|Student|
|Staff|
|Superiors|
|Maintenance|
|College|


**Needs:**

- what equipment is available.
- when equipment needs to be returned.
- how much equipment is needed.
-equipment is required and when it needs upgrading.
- what equipment is available and what is unavailable.
- what equipment is present.

**Concerns:**

-Where the equipment is held.
-Whether equipment is double-booked.
-Staff
-Students accessing staff equipment.
-Time,Storage.
-Maintenance
-Budget.
-Staffing.

**Uknowns**
-How much equipment is available?
-When will maintenance be completed?
-Who has access to what?
-What style of system is currently in use or wanted?
-Candidate Requirements


*Statement:

Type: Problem / observation
-B

Type: Stakeholder need / concern
-C

Type: Candidate requirement
-D

Type: Solution idea
-E

Type: Assumption
-F







**Requirements Surgery**
*Requirement 1

-"The system shall be user-friendly."

8Problem:

"User-friendly" is subjective and cannot be measured.
It does not say who the users are or which tasks they need to do.

*Clarification question:

Which users and which tasks need to be easy, and what would "easy" look like to them?

*Missing information:

Who the users are (students, staff, technicians).
Which tasks must be easy.
A measurable target (time taken, number of steps, error rate).
Any accessibility needs.


**Requirement 2**

-"The system shall notify users about bookings."

*Problem:

It does not say who is notified, about which events, when, or how.

*Clarification question:

Which booking events (confirmation, reminder, overdue return, cancellation) need a notification, and who should receive each one?

*Missing information:

Who the "users" are.
Which events trigger a notification.
When notifications are sent.
The method of notification.

**Requirement 3**

-The system shall allow staff to create, edit and delete bookings and send reminders.

*Problem:

It combines several requirements in one sentence, so it cannot be verified as a single item.
"Staff" is unclear, and it does not say whether students can create bookings.

*Clarification question:

Which staff roles may create, edit or delete bookings, and should students be able to make their own bookings?

*Missing information:

Which staff roles have which permissions.
Whether deleted bookings should be kept as a record.
Who receives reminders and when.
Whether students book for themselves or through staff.
Improved Requirement

-Original: The system shall notify users about bookings.

-Repaired: The system shall notify the user who made a booking that it is overdue when the equipment has not been returned by the expected return date and time.

*How could we verify it?

-Create a booking, pass the expected return time without returning the equipment, and confirm the booking user is notified.

**Still unknown:**

-Notification method and timing.
-Whether staff should also be notified.
-Functional Requirements

**Five Question**

*WHO?
Technician (equipment staff).
-The technician needs to know whether equipment is available before confirming a booking.

WHAT?
-View whether an item is available for a requested date and time.

WHEN?
-Before a booking is confirmed.

WHY?
-To prevent double-booking.

HOW WILL WE KNOW?
-A booked item shows as unavailable for the booked period.

| ID | Requirement | Source | Verification |
|---|---|---|---|
| FR-01 | The system shall allow an authorised user to view equipment availability for a selected date. | Technician need (worked example); Student and Staff needs (Week 2). | Select a date with known bookings and check that the availability shown matches them. |
| FR-02 | The system shall prevent a booking from being confirmed if the equipment is already booked for any part of the requested period. | Student and Staff concern about double-booking (Week 2). | Try to book an item for an overlapping period and confirm that the booking is rejected. |
| FR-03 | The system shall record the expected return date and time for each booking. | Student need to see when equipment must be returned (Week 2). | Create a booking with a specified return date and time, then check that the system records and displays the correct details. |


**Quality requirement:** 

-security: Q
-PRRIVACY: Q
-accessibility: Q
-usability: Q
-performance: NO
-reliability: Q



