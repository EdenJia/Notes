# 2023 January
## 03/01/23
- Preparing new objectives for H1 2023 for 1-2-1 w/ Andy
- Bug: Updating subsite links doesn’t work - my protein still works
- Do 360 forms
- Looked into persisting social link order when changed on site details ui
    - Ask Ian if he’s talked to Sean about it yet.
04/01/23
- Migrate from docker desktop to pod man as its access is being blocked soon
- Sprint planning
- Picked up ticket to fix when site details social media link does not have any active
    - Will fix toaster message for toggle
## 05/01/23
- Continue ticket to fix when site details social media link does not have any active
    - Ian called saying he has fixed it already
- Will fix toaster message for toggle
- Catch up with Ali
- Investigate bug when you add inactive social link url toaster message is NaN
    - Adding logic to to prevent users from sending off a put request if there is no value for the url in the corresponding social media
    - Change error toaster to error message and highlight input with red border
    - No ticket for that
## 06/01/23
- Continue with implementing a red border on the social media url input field
    - Done so, call with Ian to do so
    - Discovered a bug,
- 1-2-1 w/ Andy
- Presentation with Sam
- Call with Ian to pair program and update each other on our progress on both ends
    - He has implemented social media url put requests on his end, and suggested I implement validation on it as well. Continue that today
## 09/01/23
- Call with Ian to fix errors, then merge into his branch
- Will be off Tuesday, Wednesday and Thursday 
## 13/01/23
- Call w/ Ian for more changes
    - When toggling error, focus on input as well
    - Bug - toggling active with updated url 
        - Make url update before comma separated list
        - Make a global value that stores input value of url and toggle checked value of every social media
            - Already exists, this.socialMediaProviders.object.url and .status
        - Refactor social media url to update that ^ global variable with new string url, then check if that social media has it’s toggle on or not, if not then send update. If not, do nothing
        - Refactor social link toggle to update that ^ global variable with new checked value. Then check if that social media has a url that’s different from passed down url, if yes then send update for url and then send update for active
    - Resolve inaccurate branch name and ticket -> bgd-1427
    - Rxjs observable, subscribe, pipe
## 16/01/23
- Asked Sean if I could pick up some navigation service tickets, he said there was a pre-requisite ticket for it that needed to be done and we could pair on it when he gets navigation service to run
- In meantime, picked up ticket to check if Apollo nagios alerts have been directed to our team. Couldn’t find the Apollo service on nagios so I asked Andy about it and he confirmed it doesn’t exist there and said he’ll look on grafana.
- Attending first wellbeing meeting from L&D early careers
- Shadowed Sean at the end of the day to test his changes to navigation service
## 17/01/23
- Shadowed Sean on his ticket to implement an endpoint to navigation service to retrieve widget template logs and testing it
- Retro
- Put properties service release branch into a pr to merge into master
## 18/01/23
- Continued shadowing Sean, where he finished testing the newly added endpoint in navigation service 
- Sprint planning
- Started on software pre-requisites for checkout environment setup
    - Installed software pre-requisites e.g. tomcat 8, maven
## 19/01/23
- Call with Simone to go over installing everything else
- Continued working with Simone, then more members of the checkout team were added to the call.
## 20/01/23
- Attended growth mindset L&D session
- Catch up with Andy
- Catch up with Ian on site details
- Catch up with Ali
- Checkout environment
    - Reinstall maven via ibrew instead of brew
## 23/01/23
- Andrea from checkout team was in meetings all day so no progress made - tried on my own and encountered the same difficulties
- Call with Ali to help with running tests
- Updated macOS version and fixing issues that caused
## 24/01/23
- Picked up ticket to confirm site builder metrics
    - Figured out it was because the query for new_subsite_create_upload table instead of 
- Checkout environment
    - If running acceptance test, must run mock adapter before
    - If running web, everything else must be running before 
## 26/01/23
- Finished setting up checkout
- Continue on ticket to confirm site metrics accuracy. Could I arrange a call with you today Andy - I’ve got a few questions need clarification on before I implement the possible solution to this.
    - Are all subsets in the Elysium.Subsite table created through site builder
## 30/01/23
- Decided to pick up the properties service security hub fix ticket, couldn’t access our organisation’s snyk page, asked Sean and he said he had similar issues with permissions and directed me to contact staff tech - have done so - they didn’t respond but at the daily catch up Samantha and Chris let me know I had to sign in via okta
- Reviewed Craig’s code to fix a dropdown issue
## 31/01/23
- Got properties service running and tested. Created a PR for those changes and just waiting for approval to merge. Then will go through the release process
- Fill in THG hourglass since it’s the last day of the month
- Have a call with Andy 
    - Make metric representation more explicit, find out what remaining means and change it to be more representative
    - Found that in big Dave’s New subside site configuration inputs table has an archived field that is NULL for all entries. Performed an inner join with archived subsets with an inner join on matching site ID and subsite codes and have found more entries that are on ‘remaining’. 
- We have retro
- Ask Simone if I can shadow her for the next site crawl
    - Need PCI training for site crawl stuff
    - But can shadow her on site builds
        - Also set up site build file templates