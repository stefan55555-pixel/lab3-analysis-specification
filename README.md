# lab3-analysis-specification
lab3-analysis &amp; specification

Student: Stefan Krstic — T00199336
Date: 19/10/26

Stakeholders
Stakeholder
Student
Staff
Superiors
Maintenance
College
Key Needs and Concerns
Student

Needs:

See what equipment is available.
See when equipment needs to be returned.

Concerns:

Where the equipment is held.
Whether equipment is double-booked.
Staff

Needs:

See what equipment is available and what is unavailable.
See what equipment is present.

Concerns:

Students accessing staff equipment.
Whether equipment is double-booked.
Superiors

Needs:

Know how much equipment is needed.
Know when equipment is required and when it needs upgrading.

Concerns:

Time.
Storage.
Maintenance

Needs:

Know who is responsible for looking after the equipment.
Know whether maintenance is automatic or manual.
College

Needs:

A timeline.
Know what is needed.

Concerns:

Budget.
Staffing.
Unknowns
How much equipment is available?
When will maintenance be completed?
Who has access to what?
What style of system is currently in use or wanted?
Candidate Requirements
A

Statement: "People are sometimes unsure whether a camera is available."

Type: Problem / observation

Reason: Describes a current difficulty, not what the system must do.

B

Statement: "Technicians need to know what equipment is due back."

Type: Stakeholder need / concern

Reason: States what a stakeholder needs, without saying how.

C

Statement: "The system shall record the expected return date for each booking."

Type: Candidate requirement

Reason: Uses "shall", describes system behaviour and can be verified.

D

Statement: "The college should build a mobile app."

Type: Solution idea

Reason: Decides the technology before the problem is understood.

E

Statement: "We assume all users will have a college login."

Type: Assumption

Reason: Not confirmed by any stakeholder, so it needs checking.

F

Statement: "A lecturer wants reliable availability information before promising equipment."

Type: Stakeholder need / concern

Reason: Describes what a stakeholder wants and why.

Requirements Surgery
Requirement 1

"The system shall be user-friendly."

Problem:

"User-friendly" is subjective and cannot be measured.
It does not say who the users are or which tasks they need to do.

Clarification question:

Which users and which tasks need to be easy, and what would "easy" look like to them?

Missing information:

Who the users are (students, staff, technicians).
Which tasks must be easy.
A measurable target (time taken, number of steps, error rate).
Any accessibility needs.
Requirement 2

"The system shall notify users about bookings."

Problem:

It does not say who is notified, about which events, when, or how.

Clarification question:

Which booking events (confirmation, reminder, overdue return, cancellation) need a notification, and who should receive each one?

Missing information:

Who the "users" are.
Which events trigger a notification.
When notifications are sent.
The method of notification.
Requirement 3

"The system shall allow staff to create, edit and delete bookings and send reminders."

Problem:

It combines several requirements in one sentence, so it cannot be verified as a single item.
"Staff" is unclear, and it does not say whether students can create bookings.

Clarification question:

Which staff roles may create, edit or delete bookings, and should students be able to make their own bookings?

Missing information:

Which staff roles have which permissions.
Whether deleted bookings should be kept as a record.
Who receives reminders and when.
Whether students book for themselves or through staff.
Improved Requirement

Original: The system shall notify users about bookings.

Repaired: The system shall notify the user who made a booking that it is overdue when the equipment has not been returned by the expected return date and time.

How could we verify it?

Create a booking, pass the expected return time without returning the equipment, and confirm the booking user is notified.

Still unknown:

Notification method and timing.
Whether staff should also be notified.
Functional Requirements
Five Questions

"The technician needs to know whether equipment is available before confirming a booking."

WHO?

Technician (equipment staff).

WHAT?

View whether an item is available for a requested date and time.

WHEN?

Before a booking is confirmed.

WHY?

To prevent double-booking.

HOW WILL WE KNOW?

A booked item shows as unavailable for the booked period.
FR-01

Requirement: The system shall allow an authorised user to view equipment availability for a selected date.

Source: Technician need (worked example); Student and Staff needs (Week 2).

How could we verify it?

Select a date with known bookings and check the availability shown matches them.
FR-02

Requirement: The system shall prevent a booking from being confirmed if the equipment is already booked for any part of the requested period.

Source: Student and Staff concern about double-booking (Week 2).

How could we verify it?

Try to book an item for an overlapping period and confirm the booking is rejected.
FR-03

Requirement: The system shall record the expected return date and time for each booking.

Source: Student need to see when equipment must be returned (Week 2).

How could we verify it?

Create a booking and confirm the return date and time are stored and can be viewed.
FR-04

Requirement: The system shall allow an authorised user to view all equipment that is currently booked out and its expected return date.

Source: Staff need to see what equipment is present (Week 2).

How could we verify it?

Book out an item and confirm it appears in the list with its return date.
Review
"Authorised user" is not yet defined (FR-01, FR-04).
FR-02 assumes partial overlaps are not allowed.
FR-03 does not cover late returns.
Equipment categories are not yet known.
Quality Requirements
NFR-01

Quality requirement: The system shall restrict booking actions to authorised users, who must sign in before using it.

Why does it matter?

Staff are concerned about students accessing staff equipment.

How could it be checked?

Attempt a booking without signing in, and as a user without permission, and confirm both are refused.

Unknown:

What "authorised" means for each stakeholder (Who has access to what?).
Project Application

Chosen requirement: Student need to see when equipment needs to be returned.

Step 1 — Source:

Student (Week 2 stakeholder needs).

Step 2 — Examine the requirement:

Type: stakeholder need, which can become a functional requirement (see FR-03).
Unclear: how and how far ahead the student is told.

Step 3 — Question:

When borrowing equipment, how and when would you like to be told about the return date?

Step 4 — Verification:

Create a booking, then confirm the student can see the return date and time for it.

Step 5 — Unknowns:

How students should be reminded of return dates (Students, Equipment staff).
Standard loan periods for different equipment (Equipment staff, College).
