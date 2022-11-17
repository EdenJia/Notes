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
