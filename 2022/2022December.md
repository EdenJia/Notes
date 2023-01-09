# 2022 December
## 01/12/2022
- Written up self assessment document
    - Call with Ian about how to fill them out
    - Send assessment to Andy by the 9th
- Chase Andy on the site importer ui ticket & site importer roles
- Add on JIRA as many issues as I can identify back to nextJS migration epic 
- Sean add to linux channel -> got nagios access
- Decommission
    - Staff tech responded: that role request is for the linux team and added that to their queue
        - chase nagios role request ticket with the linux team, don’t know how to contact them
    - Arrange a call with Craig for advice on decommissioning
- Call with Ian for setting up test on site details ui
- Ask Sean about properties service GitHub migration -> haven’t merged unit test coverage audit branch into master yet
    - Will be released after the GitHub actions pipeline is finished
## 02/12/2022
- Got on a call with Craig and finished decommissioning old site builder
- Look over self assessment before sending to Andy
- CONTACT STAFF TECH ABOUT DC ACCOUNT DETAILS NOT WORKING
- Contacted staff about troubles logging into okra
- Call with Ian on unit testing on Site details UI 
05/12/2022
- Picked up ticket about running SQL to add Cerberus Permissions to tabernus and add Site Details to Teepee Feature
    - Could not access stable tabernus, asked ctp team, they said to raise a ticket for access with the DBA team
    - Raised the ticket and pinged the DBA team, they responded and said that ticket didn’t need to be raised, I just need to be added to the windows groups that allow access. Found out the security group I needed to be added to ‘IT_development/Group_Development’
    - Followed up with DBA on who to go to to be added to the group. They told me to raise an SD+ with staff tech.
    - Raised ticket with staff tech and pinged on their teams channel. Waiting for a response now.
    - In meantime, completed as much of the ticket I will raise when finally making the changes to tabernus and Elysium. 
- Call with Ian finalising going through modular TP testing
- Did two 360 forms
## 06/12/2022
- CanterburyAU trickle script
    - Chase Ben Ellerton Canterbury AU trickle script ticket
    - Since It’s been such a long time, the auto-cleanup job has dropped the data table
    - Made redirects table and inserted data again
    - Ben Ellerton asked for rollback plan - we didn’t have one
        - He wrote a rollback trickle script and I’ll use it as a template for future rollback trickle script
        - Update sd ticket description to add rollback plan and attached rollback trickle script
- Retro 
- Released: Adding site details permission on Cerberus and site details feature on teepee
    - For gaining tabernus access, ask Andy for approval on gaining access -> got approved
    - Then will create another ticket for adding data into tabernus and Elysium -> Sam approved
    - Call with Sean to run the scripts -> done
## 07/12/2022
- Complete early careers tasks on probation prep
- Sprint planning
- Picked up and completed catch all redirect ticket with Ian
    - Redirect garden of life ru, hk. Kleanathlete de, au, jp, en. MinamiHealth en. All to everyhealth.com
- Catch up with Ali
- Picked up adding new Site Details roles to users or role group ticket
## 08/12/2022
- Completed: adding new Site Details roles to users or role group ticket
    - Asked Sam what role_names e.g. tpcms-developer, tpcms-trader will have the added permissions of site details read and write 
    - Verified SQL with lewis Callan
    - Write an SD ticket, test on stable (tell Sean so he can test changes on site details api) then on live
## 09/12/2022
- VM Patching, need access to spacewalk. Need Andy’s approval so blocked
- Reviewed: ‘search by subsite name in test server on sitebuilder’ ticket
    - Called Craig to pair program it
    - Removing theme switching on Sitebuilder, rebuilding it.
## 12/12/2022
- Merged: ‘search by subsite name in test server on sitebuilder’ ticket
- Site importer UI security audit merge
    - Had a chat w/ Andy about it -> Need to fix broken Jenkins pipeline and build a pipeline on GitHub. Added this as ticket into the backlog https://thehut.atlassian.net/browse/BGD-1377?atlOrigin=eyJpIjoiZjk0OTRlMjM3NjUxNGNlYjllNzZiZmM3ODU2MDgxODgiLCJwIjoiaiJ9 
- Finished patching big Dave on gb1, gb4 and gb5
13/12/2022
- Setting up sonarqube locally with Craig for Sitebuilder sonarqube ticket 
    - Spend afternoon working on it.
## 14/12/2022
- Carry on with site builder sonarqube ticket
    - A lot of major issues are about using nested template literals - which are used in a lot styled components. Fixing those would decrease code readability and increase bloat so I told Craig and he’s going to have a look at it.
- Power cut
- All hands
## 15/12/2022
- Put sonarqube ticket into review and it’s been merged
- Update macOS 
- End of year presentation & annual awards
- ACN update and end of year send off
- Catch up with Ali
## 16/12/2022
- Test PUT request endpoints on card content
- Test toaster pop ups
- Personal development
## 19/12/2022
- Chase up on Craig’s new service account ticket
    - Windows server Matt Samways says documentation on creating an SD account is outdated and enabling okra without 2fa needs unlikely sign off from infosec
    - ‘So at the moment this isn't something we would be doing. An investigation is underway on SAs that raise changes. I have spoken to the Admins of SDP and this investigation is currently with Nik Gupta and he is off until the 3rd Jan. ‘
- Review Craig’s tickets and release site builder with Ian - release tagged v1.2.7, but on website v1.3.0, changed package.json tag from 1.3.0 to 1.2.7
    - Site confirmation:
        - If tick labels should be linked
        - Upgrade quality of the images
    - Release notes spike ticket
        - Cannot see release notes when ran locally
        - Install and test job fails on merge request into main
## 20/12/2022
- Call w/ Ian first half of the day
    - Pick up a modular TP ticket -  to implement a feature to allow users to update a global config at the subsite level
        - Told to prioritise ticket below as this one is moving to backlog
    - Pick up other mod tp tick
        - Plan of action:
            1. (Done) Disable button fix
            2. (WIP) Figure out updating toggle
            3. Figure out persistent order when social changes 
## 21/12/22
- Released: implement social link toggle functionality
    - Call w/ Ian to fix issue
    - Found new bug with update sucess toaster message
- Fill in THG Hourglass
- Sprint planning
- Write up out of office message on Teams
- Update December notes
- Cover the prepping for early career's mid-year review drop email
- Catch up with Ali
- Chase Andy for probation review meeting