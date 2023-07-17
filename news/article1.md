# Software Quality and Testing - Quality Plan

Module Code: CS2QT19

Assignment report Title: Quality Plan

Student Numbers: 29012845, 29011382, 29020320

Date: 18/2/22

Actual hrs spent for the assignment: 14

Assignment evaluation (3 key points):
1. We got to explore a quality plan on our own
2. We enjoyed working together to come up with other ideas
3. We found researching interesting

## Contents

- [Software Quality and Testing - Quality Plan](#software-quality-and-testing---quality-plan)
  - [Contents](#contents)
  - [Product introduction](#product-introduction)
    - [Product Overview](#product-overview)
    - [Product Audience](#product-audience)
  - [Product plans](#product-plans)
  - [Process descriptions](#process-descriptions)
    - [Event Scheduling](#event-scheduling)
    - [Creating Groups](#creating-groups)
    - [Accessing users’ data](#accessing-users-data)
    - [Notifications/Mailing List](#notificationsmailing-list)
    - [Budget tools](#budget-tools)
    - [Checklists](#checklists)
  - [Quality goals](#quality-goals)
    - [Client-Server Response Time](#client-server-response-time)
    - [Intuitive Design](#intuitive-design)
    - [Database Quality](#database-quality)
    - [Encryption](#encryption)
    - [Defects](#defects)
    - [Training](#training)
  - [Risks and risk management](#risks-and-risk-management)
  - [References](#references)

## Product introduction

This Software Quality Assurance Plan will outline the details of how the project should be completed to ensure high-quality software is produced.

### Product Overview

The product is an Event Management Assistant. It will be capable of assisting event managers in the planning phase of events, such as concerts, business meetings and more.

- Checklists to ensure that important things are noted down, so that they can be done on time or when needed.
- Scheduling assistant to ensure that meetings and events are planned accordingly when people are free.
- Budget tools allow users to plan and manage spending.
- Mailing lists allow users to send emails to multiple other users.
- Planners can also amend the event after being set up to account for changes in venue and staff.
- Each user should be able to see where they are assigned and at what times.
- Create new roles and teams when needed to allow for versatility in the user’s business strategies and models and allow them to encompass all the teams needed for the events they may plan. Templates will be provided for standard use cases.

The product will be a web-app, that users can log onto to see their scheduled events and information about that event to help it run as smoothly as possible.

Event managers/coordinators will be able to input details of an event and assign workers to each part of the event so that everyone involved knows what they are doing and where they will be.

Workers will be able to log onto the system to see their assigned team, posts, and what they will be doing. For example, a security guard can be assigned to a "Security" group. They can log onto the service via a desktop or mobile browser. They will be presented with information on where they will be stationed, how long for, and any other information a security guard can do.

### Product Audience

This product is aimed towards small and large-scale businesses alike, to help event managers coordinate events with ease and security.

- Project managers will be able to perform the tasks specified in this document.
- Workers will be able to see their schedule for the events.
- Stakeholders will be able to collaborate with us in testing to ensure that the product’s aligned with their needs and allow for criticism with real-world users.

## Product plans

To ensure quality, we will adopt an agile approach, using the V-Model, to complete the product. This will allow room for testing during development to reduce the impact of bugs that may be hidden until late testing.

The order in which the project will be completed is as follows:

1. The back end, to ensure that all required functionality is encompassed in the database and server side. Development of the mass email-systems will occur here.
2. The front-end. Once all functionality is implemented into the database, the front-end developers will be able to generate a user-interface which will allow the users to see all the information they need when using the service.
   - This includes UI for the Scheduling Assistant, Mailing List, Budgeting Tools, Groups and Checklist.
3. Logic for all systems that can be processed on the front end.
4. The interface between the front-end and the database, connecting the two together. This is to ensure that the front-end and the database can remain separate from each other so that testing can be done on both the front-end and database without interference from the other, ensuring that each works correctly on their own.
   - Making sure that the scheduling aligns with all parties involved and provides warnings if not.
   - Converting checklists into data that can be stored on a database.
   - Processing requests to send to the server for mailing.
   - Processing budget used.
   - Processing new groups into a format that can be stored in the database.

Testing will be completed in-between each step to ensure that each part functions as intended before linking them together with the interface layer. If bugs are found, they can be fixed at each step. This will reduce the risk of there being system-breaking bugs in each section which will increase the overall quality of the product.

We have chosen to complete the product this way so that each system can remain independent from the others, allowing for easy adaptation of each underlying system and process with minimal change of it affecting the other. The interface to link the front- and back-end systems, where any needed conversion between data can take place, for example, date-time formatting, converting SQL returns to readable text, and validating user inputs. It will also allow for different front ends can be created in the future if demand for desktop/mobile versions of the product are requested.

## Process descriptions

In this project, there many different processes which must occur. These are the following:

### Event Scheduling

Event scheduling is the process by which an event manager will pick a date and time for the event. The name for the event will also be entered, along with the location it is taking place in, much like a regular online calendar. Events can overlap to account for the company having multiple events in one day, however, the planner should receive a warning if the date and time overlap with an event already on the schedule.

When a date and time is input into the software, a new record should be entered into the database with its own unique ID which can be generated when a new record is entered.

### Creating Groups

A group is a collection of employees/members that are will be assigned to the same team, like security, or sound. The groups will be stored in a new table that will link the two created event using a linking table. Each group can have its own ID.

Groups may also be templated and linked to the event via a foreign key, as it is likely a company's security team will change from event-to-event.

Groups must have at least one person in them. Members can be assigned to a group from the group menu. The data stored about that member will be their ID, name, location they will be working at the event, their working times, and an additional section for notes. This notes section can be used to provide additional information about the job. All fields will be required, except the notes section.

### Accessing users’ data

As the nature of the project is to plan events, it would make sense for the people involved to be able to see their role within the event.

Users should be able to log into the webapp using a username and password. As they are employees, they should have limited access to event details and should only be able to see the information the event planner has put next to their name. This includes:

- Event date, time, and location.
- Employees scheduled shift and timings.
- Additional notes left by the event planner.

If there are any changes that need to be made to the event, then the event planner can login at any time and adjust the plan. Each field (location, date, time, group information, etc.) can be edited by the event planner and saved at any time.

### Notifications/Mailing List

Following along from the last process, everyone who is affected by a change that was made to the event should be notified via email about the changes that have been made.

Planners can also send emails to everyone involved in the event using a mailing list to notify users of additional changes, not covered by the automated system.

For example, if an event venue was changed, all employees should be notified of this so that there is no confusion. Similarly, if the location of security guard was changed, the guard and their superior should be notified of this change.

To decrease the number of emails sent out, they should be combined into one email which is sent out at the end of the working day. This preference can be toggled off and notifications can be sent as soon as one is made.

### Budget tools

Budget tools can be used in the planning of events to manage and allocate their finances to different events, whether they are external events and must be paid for in advance or whether they are internal events that need equipment to be bought.

Planners can view their budget and see what they have already spent and on what so they can find out how much money they have for other things. This can all be displayed in a spreadsheet-like table. The planner can also filter this table and order it so they can view the information they would find most helpful.
* Order from most expensive to least expensive.
* Only show costs of over a certain amount of money.
* Etc.

### Checklists

Checklists can be used to write down important tasks that need to be done or notable events that need to be planned in the coming weeks.

Users can set a list of items in their checklist and assign groups/people to that item. For example, the design group will be able to see all checklist items related to designing. They will be able to mark them as completed when they are done.

## Quality goals

To achieve a high-quality system, we must achieve the following:

### Client-Server Response Time

The communication between the server, which houses the database (and the client) must be as fast as possible so ensure that the users are not waiting for the information they requested for too long. An acceptable range for response time is between 500ms and 2000ms to send the requested data over the Internet.

This can be achieved by optimising the interface between the client and the server and optimising the SQL instructions used to get the information.

### Intuitive Design

It is important that the UI is intuitive and consistent. To ensure this, we will make sure to assess the UI with in-house, stakeholder and external testers to get a wide range of feedback for a UI design that is both intuitive and functional. We can measure the results by asking participants to rate the software in categories:

- Aesthetics.
- Functionality.
- Intuitiveness.

We can also take inspiration from other, similar applications, like Zoho Backstage.

### Database Quality

The database part of the project will be its backbone. To ensure the database works correctly, we will employ a model such that it is in at least the 3rd Normal Form. This is so that the database is consistent with industry standards. Putting the database into the 3rd Normal Form will also allow us to adapt the database more easily for future updates and improvements and reduce the amount of storage required and the efficiency of the database.

### Encryption

An Event Management Product will hold lots of sensitive information about the companies that employ our system. To ensure security, we will use an encryption to help and keep our customers' information secure. To do this, we will use an implementation of Triple DES to keep the information secure.

### Defects
Ensure that there are less errors in code, which may lead to faults and failures, thus reducing the reliability of the code. Make sure there are less than 5% of errors. This can be achieved by static and dynamic testing. Make sure that more than 95% of available errors are checked for.

### Training
Ensure that the employees are trained in using the system, so that they know how to use it and that they don’t run into problems while using it. Make sure at least 80% of users are trained to reduce time spent from users being unsure how to use the system and requiring assistance.

## Risks and risk management

<table>
  <tr>
    <th style="width: 35%%">Risk</th>
    <th style="width: 15%">Probability</th>
    <th style="width: 15%">Impact</th>
    <th style="width: 35%">Mitigation Plan</th>
  </tr>
  <tr>
    <td>Lots of different businesses have different business models and structures, so it is likely that our system may not be adequate for all use cases. </td>
    <td>Medium</td>
    <td>High</td>
    <td> To mitigate this, we will keep the design of groups as open as possible so that they can be used in a wide range of situations. </td>
  </tr>
  <tr>
    <td>The stakeholders could change their mind on some elements of the system and how they want it to work. </td>
    <td>High</td>
    <td>High</td>
    <td>We will complete the project using the V-model agile approach. This is so that if the stakeholders change their mind about a certain process, we can make those changes easily. </td>
  </tr>
  <tr>
    <td>Some parts of the product may take longer to produce compared to others.</td>
    <td>High</td>
    <td>High</td>
    <td>We will work on various parts at separate times. The details of which can be seen in the Project Plan section. This will minimise the risk of sections being incomplete before testing and all resources can be put into each section to complete each one as quickly as possible. </td>
  </tr>
  <tr>
    <td>Not enough resources.</td>
    <td>Medium</td>
    <td>High</td>
    <td>Holiday/Sick days have been accounted for in the plan to allow for staff to be absent and allow the product to be completed on time.</td>
  </tr>
  <tr>
    <td>Unexpected errors may show during late testing.</td>
    <td>High</td>
    <td>High</td>
    <td>A plan is in place to ensure that the product is completed on time and is as bug-free as possible. The use of an agile approach allows us to fix errors as they are found and test accordingly.</td>
  </tr>
  <tr>
    <td>Potential loss of data when transferring between client and server.</td>
    <td>Low</td>
    <td>High</td>
    <td>We can employ a TCP text transfer protocol to ensure that the data is checked when being transferred to the database</td>
  </tr>
  <tr>
    <td>Potential rubbish data.</td>
    <td>Low</td>
    <td>High</td>
    <td>We will make copies of the database to ensure that if a mistake happens, it can be rolled back to a pervious state. Also, if two people are making changes to the same listing at the same time, it could cause corruption or data being overwritten. In which case, the user that logged on last will be told that someone is already editing that document and will have to wait until the other user logs off before continuing.</td>
  </tr>
  <tr>
    <td>Mailing Lists being sent to the wrong people</td>
    <td>Low</td>
    <td>High</td>
    <td>This would happen if a user’s email address is input incorrectly. This could be because someone entered the wrong employees email address because they have similar names. To mitigate this, the employee's email address will be collected from the employee database to minimise the risk of human error. </td>
  </tr>
  <tr>
    <td>Version Control errors when committing</td>
    <td>Medium</td>
    <td>High</td>
    <td>We will be using a Git system to help with version control. This will allow us to keep track of users work and monitor progress of employees. If errors are made, we can use the Git system to recover the lost work. The Git system will also be backed up daily in case someone overrides another's work, and it is unable to be retrieved through Git. </td>
  </tr>
  <tr>
    <td>Breakdown in communication as employees can’t keep track of who has done what.</td>
    <td>Low</td>
    <td>Medium</td>
    <td>Have scrum meetings for review of performance. </td>
  </tr>
  <tr>
    <td>Staffing issues & Lack of motivation as staff can’t do work properly because of being unmotivated or tired.</td>
    <td>Low</td>
    <td>Low</td>
    <td>Improvements in skill set and projects in a portfolio. Review of performance and improvements. </td>
  </tr>
</table>

## References

Zoho. (2019). Online Event Management Software | Zoho Backstage. [online]
Available at: https://www.zoho.com/backstage/ [Accessed 12 Feb. 2022].

Sample Test Plan - OrangeHRM Live Project Training Test Plan (a Real Sample). (n.d.). [online] 
Available at: https://www.softwaretestinghelp.com/wp-content/qa/uploads/2014/02/Live_Project_Test_Plan_SoftwareTestingHelp.pdf [Accessed 13 Feb. 2022].


CQI | IRCA. (2020). Setting and applying SMART objectives. [online] Available at: https://www.quality.org/knowledge/applying-smart-objectives#:~:text=All%20quality%20objectives%20should%20be [Accessed 17 Feb. 2022].

Simplicable. (2018). 26 Examples of Quality Goals Simplicable [online]
Available at: https://simplicable.com/new/quality-goals [Accessed 18th Feb. 2022].

Hello!