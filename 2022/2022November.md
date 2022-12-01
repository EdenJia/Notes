# 2022 November
## 01/11/2022
- Craig reviewing MR and raise changes needed, will make those changes today
- Have this afternoon off: dentist appointment
## 02/11/2022
- Catchup with Andy
    - Take up and learn more about the back-end
- Properties audit exception
    - By site code only, locale only, site code + locale but no property, propertiesauditexception delete unused constructor
## 03/11/2022
- Carry on with ticket - call with Ali where the test I’m attempting to write isn’t needed.
- Catch up with Ian
## 04/11/2022
- Carry on ticket
    - getPropertyFallbackValue() in PropertiesManagerServiceImpl.java
## 07/11/2022
- Trickle script flow task unable to view, chased Ben Ellerton on this, he confirms the task for trickle script made on thgflow but won’t be picked up until next week because of singles day on Friday and they’re going into a change freeze
- Audi unit test coverage conclusions:
    - PropertiesManagerServiceImpl.java 
        - getPropertyFallbackValue() & previewPropertyValue() -> fallback if/else statement broken toLocale(), PropertiesManagerServiceImplTest.java tests written for it don’t cover all fallbacks and since the code itself is broken it doesn’t go anywhere
        - A lot of uncovered lines are on PropertyAudit (3), RollbackData (1) and Property (3) objects initialised within the parameters of jdbcTemplate queries in methods getPropertiesFallbackValues(), getPropertiesByBulkUploadID(), getMostRecentProperties(), getRollbackProperties(), previewProperties(),  getPropertiesAudit(), getAvailableRollbacks(), 
        - MR notes:
            - Deleted unused PropertiesAuditException constructor in PropertiesAuditException.java
            - Simplified ternary if/else statements in PropertyKey.java
            - Made PropertyAuditTest.java 
            - Changed propertiesAuditException() method in PropertiesManagerControllerTest.java to throw PropertiesAuditException rather than DataRetrievalFailureException
            - PropertiesManagerServiceImplTest.java: replaced literal strings ‘sitecode’, ‘locale’ and ‘value’ with imported ConstantHelper variables, added test to check the NoChangesException was thrown on rollbackProperties() method, created 3 tests to test getPropertiesAudit() by site code and locale only, site code only and locale only.
- Early careers: resilience -> checking out resources
## 08/11/2022
- (Reviewed) properties service unit test audit MR 
    - Merging on hold until after PS migrates to GitHub 
- Retro
- Pre-DurHack chat - just for members of the hackathon to meet
    - Durhack on the 19th to 20th November (a weekend), Declan gave me the ok to go
    - Attendance & food expenses covered
        - Saturday morning train from Manchester victoria
        - Merchandise & recruitment stash
        - Learn recruitment info & pitch
        - Make a workshop: what other workshops there are
            - Docker, AWS, vue, angular, reactjs/nextjs, 
- Ask Ian to set up modular TeePee
    - Ask CTP for access to modular Teepee for git cloning
    - Attempt setting up modular Teepee
## 09/11/2022
- Fixed laptop
- Durhack preparation, creating account on corptraveller
- Sprint planning
- Call w/ Ian about modular teepee repo setup
## 10/11/2022
- Try setting up modular teepee: pre-reqs, software e.g. node, java, angular version configuration
- Call with Ian going over site details UI codebase
    - Read up on passing parent to child on angular
- Call with Ian and Sean about creating a permission ticket for adding THG core tooling to okta
- After lunch call with Ian about putting the aforementioned request access ticket in, it was closed within minutes. Then contacted core tooling team and they gave me a role to finally login to modular teepee
- Setup on properties service in GitHub, merged unit test audit branch into unofficial release branch, therefore moved that ticket to released column on the board.
## 11/11/2022
- Take on the adding put requests and functionality for updating the subset data on site details UI
    - Reading up on the site details api and the subsite DTO structure and using that to fill in the required properties for the request body.
- Catchup with Ali that was postponed from Thursday 
- Catchup with Andy
## 14/11/2022
- Carry on with my current ticket, catching up with Ian
    - How to trigger the services on app and console logs to say it’s successful or not -> plans to replace it with an error message/toaster
        - Attach change events to tabbing out/ unfocusing inputs to update the data on UI for only wide card id 4
        - Work out whether focus out event works in angular
        - Check data storage for subsite details
        - Then rig up the service put request method
        - One to subsite data, one to subsite links
            - Make logic for which input fields are which, add 1 more argument for id in handler
        - Make a success handler for the updatesubsiteconfig() for all cards.
    - (Not to do) Plans to move edit functionality from page level to card level
- Completed the new THG x Planet Earth training module I’ve been enrolled in
## 15/11/2022
- An accessibility conference on technology innovations in disability promoted by THG accessibility network
- Checked up with Ben Ellerton on trickle script request for Canterbury AU, they said if it’s necessary for Black Friday it’s going to have to go through SLT. Updated ticket with info and moved to blocked.
- Call with Ian to discuss how he will apply his changes to mine since our tickets are related.
    - subsiteLinks object building done
    - SubsiteData object building : wait until the put request endpoint updated to take the necessary data only.
    - Sending a put request on subside links api with a JSON payload returns an internal server error 500 and refreshing the site details ui shows it is changed
        - Olympus API
## 16/11/2022
- Catch up with Ali
- Attended the Takeover manager presentation with James Healy 
- Check up with Sean on Olympus thing
- Ben has noted the procedure on trickle script is taking from the wrong table. Fixed this 
## 17/11/2022
- Let Ben know this has been fixed
- See what else is on the board to pick up
- Call w/ Ian:
    - Merge edit functionality changes from Ian
    - Refactor code for new changes Sean merged in.
- Meeting with Early careers and recruitment about the durham hackathon
    - 25 software engineering grads, 50 accelerators positions happening rn
        - No hacker rank, call with recruiter team for motivation
    - Recruitment process
        - Hackerrank, face to face over video
    - Internships & Age of hiring: 
        - No internships/placement this year - under review in the new year.
    - What do we look to hire for: software engineering, not looking for specific tech stack skills, SE principles and soft skills
- Filling in THGHourglass, could site details be added as a project on it
## 18/11/2022
- Catch up with Andy
    - Refactor projects in the hourglass
- Rewired local gitlab projects to their GitHub counterparts
- Review Craig’s sonarqube issue fixes PR
- Ian made a new ticket for me to add toasters for the site details put request handler, done the ticket and put into PR
- Write up handover notes
- Schedule automatic reply in Microsoft teams
- Test put requests and toasters in site details UI
## 19/11/2022
- Went to Victoria for 0645 train, it got cancelled and the next one after that so arrived at durham at 1030 instead of 0900 as planned
- Opening talks
- Walked around to see all the teams (had 180+) students
- Interview to push THG as a good employer and to give workshop we’re holding on graphQL later on the day more visibility
- Workshop on graphQL
- Walked around to help teams, solved a lot of git issues
- Got off work at around 1130
## 20/11/2022
- Project submissions is 1100 so arrived before to help teams with devpost problems
- Walked around the building make sure all teams are good or need any last minute help
- Then had a brief about judging criteria with other judges and helped with general judging
- Finalist presentations
- Prize giving and closing ceremony
- Catch train at 1753
## 22/11/2022
- Catch up with emails
- Check if endpoints and payload for the put requests in site details have changed and refactor the UI if so.
- Retro
- Took a look at the next sprint tickets -> Writing unit tests in modular TP, looking at what other teams did for their ui modules -> importing TestBed from core/testing
## 23/11/2022
- Looked at writing unit tests in angular and how they’re written in modular TP
- Sprint planning
- Catch up with Ali
- All hands: PEAK
## 24/11/2022
- Ben Ellerton responded, saying the Canterbury AU trickle script should get reviewed quickly after BF
- Write up travel expenses used during the weekend
- Toolbox meeting
- Took up ticket to update the component-index files for redirect engine, redirect configurator, site manager ui, site manager api
    - Call with Craig for help in snyk integration
    - Imported into snyk site manager ui successfully but the redirects configuration and redirects engine have errors
    - Redirects engine doesn’t need snyk, so changed team ownership to site builds only
    - Redirects configuration
        - live.yaml file doesn’t parse correctly -> checked the GitHub repo and it didn’t have the secrets 
        - Contacted Adam Buchan-Wyber to ask for gitlab access
## 25/11/2022
- Follow up with Adam Buchan-Wyber on the ticket
- Personal development - catching up on early careers’ handouts
## 26/11/2022
- Adam buchan-wyber responded at 10pm on Friday, attaching a screenshot of the secret being present in the secrets action section for GitHub, I checked and realised that THG-engagement has their own redirect-configurator repo set up on GitHub with secret. Redirects configurator ownership is transferred to us right?
    - Lewis Callum or Ryan Jackson
## 28/11/2022
- Since we parked redirects configuration, all the services I had to update the component-index files is finished. I made two PRs and put the ticket into review. They just need a review, freeze is still on until tomorrow so no merging needed
- Catch up with Andy - Wednesday BAU
    - Wednesday: decommission, trickle script
- Security audit on site importer ui -> Setup site import ui: bower install had a problem with installing file-saver.js as it’s not found as a remote repository, further googling showed that the file-saver.js repo is abandoned and bower is deprecated. Did the npm install of it instead and got gulp error. Did general npm install and still got an error that optional dependancy utf 8 validate couldn’t install because of a command in its setup script ’node-gyp rebuild’
## 29/11/2022
- Continue setting up site importer ui -> ask for help from Rich
    - Call with Rich, he called in Lewis Callan, and then lewis called in Ryan Jackson
    - Can’t get assets needed for site importer ui from gitlab so think changed bower.json to get from GitHub instead
-  Contacted by Scott Johnson on site configurator 
    - %%DC%%.redirects.io.thehut.local
    - %%SSH_PRIVATE_KEY%%
    - Andy’s moving those secrets over
## 30/11/2022
- Pick up site builder decommission ticket
- Site importer ui runs now, pushed the changed package manager files to my security audit branch
    - Added it to snyk and found it was a lot more work than thought
    - Call with Sean to go over what to do with it, called in Andy 
    - Give Andy the roles needed : site-importer-uploader, site-importer-widget-cloning, site-importer-display-text-uploader
    - Decided upon updating README and making sure new developers have an easier process running site importer ui
    - It was put into review and reviewed. It’s going to sit in the reviewed column until Andy gives me the go ahead
- THG hourglass: projects to add
    - Site importer api/ ui
    - Site manager ui
    - Redirects configurator/ engine
    - Sorry server
- Chased Ben Ellerton on the trickle script ticket 
    - we're doing BF follow up tasks until the end of the tighter deployment window (it ends on Tuesday) so this may have to wait until next week
- Started looking through documentation and gathering info on decommissioning old site builder with Andy 
    - 1. Part of the process is to remove nagios alerts but I did not have the role for nagios -> rich made a ticket in service desk to expedite the process
    - 2. Shutdown VM/k8 -> as old site builder is on k8 Andy says the process should be easier
    - 3. Remove DNS records for all instances of VM
        - Get access token
        - Get DNS info with access token
        - Send delete req with io_uuid key from dns info
    - 4. Submit ticket of template: request to decommission a virtual machine
