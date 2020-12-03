# LifTOvers

## Iteration 03

* Start date: Nov 14, 2019
* End date:  Dec 01, 2019

### Changes from Our `product.md`

Changes we have made during our development process:
1. User ability to search lifts by location, and see nearby lifts: <br> 
We removed this feature because after discussing with the partner, we realized that they wanted our app to be more admin-focused. Having the ability for volunteers to search by location would add a tremendous amount of work to our team without significant benefit to the users. Our implemented solution is that volunteers get notifications for lifts that are near their listed postal code.
2. General features: <br> 
We added the ability to export information from the application as per the partners’ requests. They wanted to be able to have an easily accessible way to aggregate the data that would be in the application. For example, they wanted a way to export the data for donor information.
3. Blacklist: <br> 
We originally planned for admin to be able to blacklist volunteers that didn’t show up or didn’t deliver the food to the proper destination. However, instead of a blacklist, we’ve decided to implement a delete feature instead. We believe this is a more natural method to achieve the same goal as blacklisting.
4. Front-end design changes: <br>
   During the development process, we found out that some of the views we have designed in deliverable 1 are not practical to use for our target users, so we made a few changes to the front-end design.  
    * Volunteer profile view:
        The most information that a volunteer need is information about the lift requests that are currently available to them, so we made that information easier to access. The picture of the volunteer is not needed for the management, so we delete that too.
        - Original Design:
        ![Alt text](https://github.com/csc301-fall-2019/team-project-liftovers/blob/master/deliverables/d3/userview.png "Dashboard Statistics")
        - Move the information and functions to other views, no longer shows the volunteer’s profile picture. (in-progress lifts, completed lifts, edit information). The profile picture was nice to have but not necessary for any workflow of the volunteer.
        - The information of In-progress and completed lift requests now is no two spread views:
        ![Alt text](https://github.com/csc301-fall-2019/team-project-liftovers/blob/master/deliverables/d3/user_in_progress.png "Dashboard Statistics")
        ![Alt text](https://github.com/csc301-fall-2019/team-project-liftovers/blob/master/deliverables/d3/user_completed.png "Dashboard Statistics")
        - The volunteer's basic information shows in the “Settings” view, edit information function also merged into this view: 
        ![Alt text](https://github.com/csc301-fall-2019/team-project-liftovers/blob/master/deliverables/d3/user_settings.png "Dashboard Statistics")
    * Admin profile view:
        In the Original design, the manage function is attached to the main dashboard of the admin users, and we believe that it is very inconvenient for the admin user. Admin should have the ability to access the information of all the lift requests and volunteers and the ability to manage them. Also, the admin users do not need the picture of the lift request for the lift management, so we remove the functions of adding/viewing the photos of both lift requests and volunteers.
        - Original design:
        ![Alt text](https://github.com/csc301-fall-2019/team-project-liftovers/blob/master/deliverables/d3/adminview.png "Dashboard Statistics")
        - Move the information and functions to other views (all volunteers, lift statistics, all lift requests, edit information, basic admin information, delete volunteers and lift requests).
        - The lift statistics information now shows on the main dashboard:
        ![Alt text](https://github.com/csc301-fall-2019/team-project-liftovers/blob/master/deliverables/d3/dashboard.png "Dashboard Statistics")
        - The information of all lift requests and the function of delete lift requests are on the "Lift" view. Admin can access this view by click on the "Lift" tab on the navigation bar：
        ![Alt text](https://github.com/csc301-fall-2019/team-project-liftovers/blob/master/deliverables/d3/lifts.png "Dashboard Statistics")
        - The information of all volunteers and the function of delete volunteers are on a new "Volunteer" view. Admin can access this view by click on the "Volunteer" tab on the navigation bar：
        ![Alt text](https://github.com/csc301-fall-2019/team-project-liftovers/blob/master/deliverables/d3/volunteers.png "Dashboard Statistics")
        - The admin's basic information shows in the "Settings" view and editing information function also merged into this view：
        ![Alt text](https://github.com/csc301-fall-2019/team-project-liftovers/blob/master/deliverables/d3/settings.png "Dashboard Statistics")
    * Change the design of the lift request view:
        - No longer shows the picture of each lift request. The above section has shown the new designs of lift request views for volunteers and admins. 
        - Original design:
        ![Alt text](https://github.com/csc301-fall-2019/team-project-liftovers/blob/master/deliverables/d3/requestsview.png "Dashboard Statistics")
    * Remove the veiw that shows the detial information of a single lift request
        - Detail information is not needed for an admin to manage the lift request nor for a volunteer to accept a lift request, so we remove this view.
        - Original design:
        ![Alt text](https://github.com/csc301-fall-2019/team-project-liftovers/blob/master/deliverables/d3/singlerequestview.png "Dashboard Statistics")


### Handoff plan

We will be having a handoff meeting with the liftovers. In this meeting, we will discuss everything liftovers needs to use the application in their daily workflow. The workflow includes giving them the code (either as a .zip or access to our development repository to fork), the Heroku account, the database account, as well as the Twilio account. We also will hand liftovers our Trello board, so they can see the features that we have implemented in a list. We will guide them through the process of white-listing Twilio phone numbers, if needed (although they probably already know how to do this since they had a twilio system in place before we began working on the project).<br><br> 
As all the accounts were our own, we will create new accounts specifically for liftovers before the handoff and set up the application to use those accounts instead. Liftovers has a technically proficient staff member with the web application development industry experience, so the minimum explanation is needed on our part for tools like Node, Heroku, etc... We will load the database with the correct sample data provided by the partner. We believe they have full capabilities to further modify and maintain our project. <br><br>
The provided README in the codebase to setup/use our application will be available should they want to have a comprehensive view of our application features. Most of our work in making it easy for them to maintain the code was done while we were developing the application itself (making code extensible and readable), so we will not need to do additional steps for the handoff step.