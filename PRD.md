# All Things College

## Core Functionalities

### User Profile

- There are two types of profiles
    - Student Profile
        - Sign-up using **college email id**
        - Extra Data Fields
            - Room Number
            - Hostel
    - Alumni Profile
        - Sign-up using **personal email id**, still have to provide **college email id** (though not used for verification)
        - Extra Data Fields
            - Company Name
- Data Fields
    - Name
    - Phone Number (optional)
    - Batch (k20)
    - Branch (CSE)
    - Degree (BTech)
- Name, Phone Number, Room Number are to be provided by the **user**
- Hostel, Batch, Branch and Degree **options** are to be provided by the **config** (which will be pushed to the database by the script)
- There will be a boolean **is_alumni** which will differentiate alumnis from students.

### Groups

- Two types of groups are supported
    - System Generated 
    - User Generated
- Groups are verifiable, and System Generated groups will be verified by default
- Admin of User Generated groups will be the creator of the group
- System Generated Groups Hierarchy: College -> Degree -> Branch -> Batch
- Group Sections
    - Chat
    - Events
    - Posts
- Every year, following will happen to the System Generated Groups
    - There will be two **College admin level buttons**
        - Refresh Hostel Button
        - Refresh Classes Button
    - Refreshment will be queued for 7 days, for which students will get the warning in chat to backup any resource of the original group they want to.
    - Refresh Hostel Button
        - Members will be removed from the group
        - A popup will appear after this, to select new hostel
        - Resources will stay in the group
        - Group chat (along with media) will be cleared for privacy reasons
    - Refresh Classes Button
        - Members will be removed from the group
        - Members will be added to the new class, automatically by the system
        - Resources will stay in the group
        - Group chat (along with media) will be cleared for privacy reasons
- Groups can make posts and events
    - public, which can be seen by members and subscribers
    - private , which can be seen by members with authorized roles (which by default will be everyone)

#### Group Chat

- Chat will be like discord, each group chat could have multiple channels known as **topics**
- Topics will be visible by the roles mentioned during the Topic creation
- Potential User Interface
    - Each group chat will have a topic selection dropdown at the top
- Users can tag others with roles, to send notifications (given, user has not suppressed notifications)
- Chat attachments will be supported, with embedded view/play option for supported media
- People in the specific topic, will be visible to others
- Chat reply chaining
- Chat Reactions

#### Group Posts

- Rich Markdown editor
- Tag based classification
- Reddit like nested comment section
- Like, Dislike 
- Admin can mark posts as important, by starring it

#### Group Events

- Group Events will have the following
    - Event Description
    - Event Title
    - An option to register for the event, which is enabled by Custom Google Form Like Implementation. 
        - It's benefit is we can reuse the User's profile data, rather than collecting it again and again
        - A participant can register another user as his/her team-mate by using their profile email
- We will have a way to show matchups for elimination, round-robin and score-based systems. 
- We will have leaderboards
- The event organizer will have access to analytics associated with the form entries
- The event organizer must be a group admin

#### Group Staff Directory

- Staff can be a teacher, accounts department official, hostel warden, auto wala, etc
- Each staff will have a profile
    - Name
    - Contact Number
    - Rating
    - Position
- Addition/Updation
    - Profile addition and updation will require verification by a group admin
    - Users can give staff rating

#### College Marketplace

- Users can sell items to their college mates
- Items will comprise of
    - Title
    - Description
    - Media
    - Price
- This will only act as a listing, and any transactions should be made by the users on a personal basis. We should display appropriate warning.
- Marketplace will have an **option to host auctions**
- User can mark an item as sold

### Direct Messaging

- Users can DM other users from their profile
- Specifics are similar to group messaging

### Global Search

- A sophisticated global search for various entitites would be implemented to make them easy to find. 
- Full text search and tags will be used.

#### Alumni Features

- They will be automatically added to a alumni group
- And there will be two channels
    - Only Alumni Channel
    - Alumni-Student combined Channel
- Alumni will be allowed to join/create only those groups which allow alumnis.
- Students will automatically be promoted to alumnis, after their end date
- There will be company specific roles assigned to each alumni

**Note**: We will try to support draft functionality for all forms of the app


