#                                                     Time Matters
- This is a project that intends to automate the process of booking meetings according to available time slots.

---
## What problem does Time Matter solve ?
- When a person1 wants to book a meeting with person2 he will send an email requesting for the date and time of the meeting. Person1 is not available at the requested time so he gives a date and time to person2 at which he is free. This goes on till they both find a suitable time slot at which they both are free. This is a long and cumbersome process so Time Matters solves this by showing person1 the date and time slots person2 is free so he can book his meeting immediately.

---

### Tools:
- ReactJS
- JavaScript
- Firebase

### Recommended npm Packages:
- [styled-components](https://www.npmjs.com/package/styled-components)
- [axios](https://www.npmjs.com/package/axios)
- [redux](https://www.npmjs.com/package/redux)
- [react-redux](https://www.npmjs.com/package/react-redux)
- [router](https://www.npmjs.com/package/router)
- [react-router-dom](https://www.npmjs.com/package/react-router-dom)

---

### Use case:
- User1 gets an email from User2 wanting to book a meeting
- User1 sends back a link to a site 
- User2 opens the site and sees a UI with available time slots
- User2 presses a time slot and creates a booking
- User1 gets notified about the requested booking
- User1 can approve or disapprove the booking

---

### Requirements:
- Should be able to add events in google calendar
- Should be able to send email notifications
- Should be able to show available spots
- Should check user calendar in case they book something into available spots
- User should be able to pick which times are going to be available to book, weekly, monthly or yearly (for instance Tuesdays at 3 PM is available all year, Monday at 2 PM is only available today etc)
- The user that books meeting should be able to add in details for the meeting
    - Might have options like: type of meeting [Phone, Video, Face to Face]
    - Adding in a note for what the meeting is about 
    - Name of booker, name of the company
    - Phone number and email
    - if it's a video conference an option for adding a link to the site of the meeting is required
- Main user should be able to approve or disapprove booking 

---

### Edge cases:
- User1 is in the process of booking an appointment and User2 books it before User1 finishes. So once User1 is done it is no longer available.
    - Solution: When a user presses a time slot it becomes unavailable straight away. And if they cancel or get disapproved it will become available again.
- User2 can hog available slots by opening the booking page indefinitely, making the application counter-productive. There has to be a time limit set for a single booking to take place, example: 15 mins available to book a slot after User clicks a slot to book
