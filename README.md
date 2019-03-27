# TheBench
Created by Daniel Campbell

![Initial Screen](UI%20Showcase%20Images/Initial.png)

The Bench is a family-oriented chore management application. It features multiple key concepts of Android and Java development, such as databases, layouts, menus, adapters, recycler views, and many other crucial elements of a complex application. The purpose of this document is to make record of the many features, processes, and designs of this application, as well as the process taken for it’s creation. This document will provide insight on any errors we may have made throughout the development process, and on how we chose to implement the features asked of us at the very start of this project. 

The Java libraries used for this project are the following:
CircleImageView 2.2.0 by Hdodenhof, 
RecyclerItemClickSupport 1.0.1 by Rohit, and 
Joda-Time 2.9.9 by Joda-Time




Software Requirements

Functional Requirements:

Creating a Chore:
-The system must allow parent users to create chores
-The system must allow users to assign a deadline to a chore
-System is able to have chores assigned to a specific person
-The system must allow points to be assigned to the chore
-The system must allow multiple resources to be specified within the chore
-The system shall support the creation of multiple chores per user, per week

Household & User Profiles:
-The system must allow the initial user to set the household name
-The system must allow the admin users to alter the household name after creation
-System will ask the initial user to create a password for their admin account when creating a household, to restrict certain chores on the app
-The system will allow the initial user to create multiple user profiles for a new Household while in the Household creation screen.
-System shall allow users to switch between profiles
-The system must ensure that admin users authenticate on login with their previously set password
-The system must allow admin users to delete other users
-The system must allow admin users to create new admin user accounts
-The system must allow admin users to create new basic user accounts
-The system shall allow admin users to change their account password once they are logged in

Modifying & Removing a Chore:
-System shall allow the user to add, or remove any resources in a chore
-The system shall allow admin users to mark a chore as complete
-The system will allow admin users to modify the date and time of a chore
-The system will allow admin users to modify the points rewarded at the end of a chore
-The system will allow admin users to postpone a chores due-date
-The system will allow an admin to re-assign a chore to a different user
-The system must allow the admin user to delete a chore

User Experience:
-The system shall allow the user to switch between profiles
-The system shall allow the user to filter chores that are assigned to them
-The system shall allow users to view previously completed chores, as well as who completed the chores
-The system will display completed chores in a separate list.
-The system will allow a user to choose their avatar.
-The system will allow a user to see their points, as well as the points of every other user in the household.


Non-Functional Requirements:
-System shall allow user to access any use case within five interactions with the interface
-The system must support at least the latest version of Android
-The system shall be properly configured and compatible with any phone screen size up to 7”(diagonally measured). 
-The system must support an unlimited amount of users and chores
-The system shall be compatible with the latest version of SQLite for its backend



Use Cases:

Switching Users:
Actors - All Users (Parents and Children)
Goals - Switch profile to see assigned chores
Preconditions - User is on any page of the app, with a household and more than one profile already created
Summary - When a user would like to go on their personal profile to see their assigned chores
Related use cases - 
Steps
Actor Actions
System Responses
1. User clicks menu icon on the top left of app
2. Navigation bar slides in
3. User selects the profile they would like to switch to by choosing the icon
4a. Screen customizes for the specified user




4b. Navigation bar slides out
Create Chore:
Actors - Parent users
Goals - To create a chore that is assigned to a specific person, with an optional deadline date
Preconditions - Must be switched to a parent profile
Summary - When a parent user would like to create a chore, he or she must enter the chore details, who the chore is assigned to, and the optional deadline date (option for recurring)
Related use cases - 
Steps:
Actor Actions = (A)
System Responses = (S)
1(A). Click on the “create chore” button
2(S). Create chore screen opens
3a(A). Enter chore name
3b(A). Enter chore description
4(A). Click the “User Responsible” textbox
5(S). A dialog with a list of users appears
6(A). Select the assigned user from the list 
7(S). The selected user is displayed as the assigned user
8(A). Enter a deadline date
9(S). The deadline date is displayed
10(A). Enter the amount of points
11(S). Display the number of points assigned
12(A). Click the “save” checkmark
13(S). The chore is saved and the user is returned to the chores screen


Create User (Admin):
Actors - Admin Users
Goals - To add a admin new user to the household.
Preconditions - The actor must be logged into to an admin account. The user must be choosing to create an admin account, rather than a standard user account.
Summary - When creating a new user account, the admin user creating the account must fill in and select details such as; the name of the new user, the option to create an admin account instead of a user account, and the new admin users password.
Related Use Cases - Specialization of: Create Admin User
Steps:
Actor Actions = (A)
System Responses = (S)
1(A). Clicks menu icon on the top left of app
2(S). Navigation drawer slides out
3(A). Selects the “plus” icon at the bottom of the navigation drawer.
4a(S). Navigation drawer slides in
4b(S). Create user page takes over screen.
5a(A). Select the ‘New User Name’ field
5b(A). Type new users name
6(A). Enable “Admin” switch
7(S). System prompts for new users admin/login password.
8a(A). Select new prompt text field
8b(A). Type new users password
9(A). Click ‘OK’ checkmark
10(S). System closes create user page and switches back to people page.
