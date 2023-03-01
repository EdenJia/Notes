## 01/02/23
- Most of the day spent going through release process for properties service. Released properties service with Sean
- Sprint planning
- Catch up with Ali
- Early careers L&D session
## 02/02/23
- Wellbeing campaign - about what mental and physical health services are available of us
- Shadowing Simone for site crawl and start on a site build together
- Dig deeper in what the ‘remaining’ number is - Ali thinks that may be deleted subsites 
    - Decided in sprint planning we might have to resend big dave’s db with Elysium’s to make sure inconsistencies are eradicated
## 03/02/23
- 1-2-1 with Andy
- Continue to pair with Simone on a site build
    - At a point where it’s ready to go into review- we’re just waiting to be given write access to the checkout web repo
6/02/23
- Investigated what the remaining statistic websites have in common
    - Most aren’t live in big Dave but are live in Elysium. Updated bigdave PL DB for those subsites to be live. I’ve also written a rollback sql script for them.
    - Some are in big Dave but aren’t in elysium.subsite entirely. Two of those are unused subsites that I checked with Sean and he deleted. One is Anastasia Beverly Hills NL -> in limbo as one of the services site builder uses is down.
- Made a draft PR for checkout web on the kayo body US site build
07/02/23
- Checkout pr reviewed-> put in pre-release
- Data base data management
    - Update archived and site alias in PL
## 08/02/23
- Going over SQL, testing in PL with Sean, got the service desk ticket approved 
## 09/02/23
- Action the database data changes in live big Dave with Sean
- Looking into CVE issue in properties service about insecure deserialisation introduced through
- Craig contacted me about running site importer UI
## 10/02/23
- Looking into CVE issue in properties service about and then called Ali for help - we then paired on the ticket
- Catch up with Ali
## 13/02/23
- Looking through the in review tickets: some do have reviews requesting for changes - the navigations service widget template database logging ticket does have reviews from Lewis Hill
- Shadowed Sean with Ali on implementing CRUD endpoints for site alias on big Dave
- After shadowing, had a call with Ali to fix the snyk monitor issue and found that I had to run `snyk monitor —dev` as the flag includes development only dependencies
14/02/23
- Reviewed both of Sean’s navigation service template logging PRs, one check was failing so fixed that and it’s good to merge
- Picked up a redirect for endurance sports Germany from Nick Haggis and actioned it 
- Released Sean’s site alias CRUD endpoints on big Dave
- Picked up a review for Craig on site builder - having some trouble installing a package from thg commerce called gravity icons
## 15/02/23
- Call with Craig, to help with my environment
- Update os version
- Pick up the update site importer api pipeline ticket that is moved to block after confirming the pipeline needs to be fixed first
- Picked up test and release sorry server trigger for big Dave
    - Several sorry server pipeline table values that doesn’t exist in code
    - Get request tested, post request throwing an error
- Sprint planning
- Catch up with Ali
## 16/02/23
- Carried on testing the new endpoints on big Dave
    - getSorryServerPipelineStatus (public) calls getSorryServerStatus (private) and vice versa.
    - Add create endpoint for sorry server pipeline
    - GitHub api endpoint to get all workflows
- Quick call w/ Ali after lunch to ask about debugging big dave
- Quick call with Andy about difficulties in the data being tested - found a few more issues with the sorry server changes
- Asked Craig for a call to look for the pipeline trigger web url
    - Found that site builder needs to also refactor its sorry server changes as all do to with sorry server variables has been deleted in the new changes on big Dave  in application properties files(that pointed towards gitlab)
## 17/02/23
- Have a call with Ali to release properties service with cve issue fixes
- Carry on with testing the sorry server changes on big Dave
    - Tried running the implemented get request to GitHub to retrieve the workflows,  there’s an 401 authorisation issue
    - Turns out the url for the restTemplate exchange method is triggering the error. Looked into where else the app it’s used and there is a release notes service that I’m retracing 
## 20/02/23
- Complete the new training module on THG x planet earth
- Call with Ali to test if he had access for GitHub rest api
- Asked Andy for a meeting
## 21/02/23
- Call with Andy to sort the GitHub rest api auth is sorted
    - Inserted the GitHub url into sorry server pipeline
    - The GitHub pipeline ID is several characters longer than gitlab pipeline IDs and therefore, the jdbc is throwing up about converting the varchar value to integer even though pipeline_id on big Dave DB is of type char
    - PipelineStatus has ID as float data type
- Trickle script
    - Tested on PL, the change req to create setup the trickle script to be executed is waiting for approval
- Added to a nav service release chat with two other people where lewis hill apologises for the delay in release and he’ll prioritise getting Nav service released by tomorrow
    - Need to create widget template log table in UAT Elysium_manager
## 22/02/23
- Create widget template log table on UAT Elysium_Manager
    - UAT change must be made either before 9am or after 4pm - done so and informed Lewis Callan
- Trickle script approved and executed
    - Actioned by the DBA team 
    - Documented my process
- Tried migrating last pass to 1 password
## 23/02/23
- Watch the early careers effective delegation
- Navigation service release and testing on PL and UAT: released
    - Had to change the table made in UAT
    - Ask Andy on what role is needed to delete widget templates on navigation service
- Call with Ali to ask about a jdbc error that I was getting
- Documenting trickle script process on confluence
24/02/23
- After resetting my okta password, I could login to my outlook email, the GitHub orgs but still not via VPN. Pinged staff tech, they sent me a new vpn code but I’ve got the authenticator app configured and don’t use the daily code anymore.
- Catch up with Andy
- Finished updating the redirects documentation on trickle scripts
    - Added rollback script template
- Call with Ian to go over his site details changes
## 27/02/23
- Sorted out vpn 
- Carried on working on the sorry server pipeline update request
    - The update url returns a 404 error but works when I try the url in browser - looking into fixing that next
## 28/02/23
- Retro
- THG hourglass
- Afternoon presentation by James Healy
- Sorry server pipeline put request was erroring 404 because the original endpoint was pointing towards the web url, not the api url. 