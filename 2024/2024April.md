## 02/04/2024
- Call with Harriet, introduced to sitebuilder:
    - Data inconsistency in metrics page
    - ‘Site build record is now at -467 ????
- Handle multiple stock owner assignment: a lot more than you think
    - Create custom dropdown that allows multiple selection
        - Maybe just a handle click that updates a stockowner list 
## 03/04/2024
- Continue handle multiple stock owner assignment: 
    - Create custom table component that allows reordering of elements
- Q2 meeting
- Team bonding
- Create access request ticket to strongDM
## 04/04/2024
- Tech townhall
- Chase sd ticket
    - Waiting for Andrew appointment
- Continue with handling multiple stock owner assignment for sitebuilder
- Reviewed the view details PR by Ihor
- Call with Ihor about logging in to big Dave SA GitHub
- Call with Ian about sitebuilder 2 
## 05/04/2024
- Chase Andy for approval
- Continue with handling multiple stock owner assignment for sitebuilder
    - Found blockers existing in sitebuilder and big Dave 
## 08/04/2024
- Chase strongDM access request
- Continue with handling multiple stock owner assignment for sitebuilder
## 09/04/2024
- Call with Ali to generate a new bd token
- Continue with making custom draggable table component
    - Package installation errors
    - Rows are draggable, 
## 10/04/2024
- Chase strongDm access
    - Kinga
- Continue with making custom draggable table component
    - Making rows deletable
    - trouble running sitebuilder but realised big Dave timed out
- Retro 
## 11/04/2024
- Planning
- Got too focused into draggable table
- strongDM still not account
    - Kinga 
## 12/04/2024
- Got strongDM installed using thg.com
- Contact Ian with draggable component
    - Got draggable working: had to contact Craig to ask about strict mode
    - Now rows keep their order if using test data created on component, but go back to their original order if using passed on data.
        - Key is probably useEffect, so experimenting with that.
    - Reworked how the passed on data is used 
    - Quick call with Craig, asking about using his existing table body component because then the styling would be easy to copy over
## 15/04/2024
- Continue with draggable component
    - Had some calls with Ali when testing those changes.
    - Styling and functionality is done, PR check tasks failing and fixing that.
        - Commit lint keeps failing so I removed that from the install and test
## 16/04/2024
- Draggable component review
- Pick up ticket to remove SLS subsite setup in BD 
    - Released big Dave
## 17/04/2024
- Release sitebuilder
- 1-2-1 w/ Andy
    - Put dentist appointment on ADP
    - Driving test July 5th
## 18/04/2024
- Quick call with Harriet and Ali to fix running big Dave
- See where I can help out on the board with reviews and pick up tickets
    - A ticket on bigdave in reviewed is being blocked by a ticket in the next sprint that’s to create display allows request main product types in a site build
## 19/04/2024
- Continue with product types display.
    - Called Ali for more details
    - Business unit and legal entities endpoint dying at one point and preventing the subsite details page from loading on franked subsites 
## 22/04/2024
- Continue with product types display
    - Made a PR for it
    - Stuck on e2e tests: Ian helped and I intercepted the product-types endpoint in cypress tests - subsiteDetails passes on local but fails on the PR check
## 23/04/2024
- Keep debugging e2e test on sitebuilder
    - Passed, needed a cache dump
    - Releasing now, but failing to push docker image
- 1-2-1 w/ Ihor
- Retro 
## 24/04/2024
- Released sitebuilder and big Dave with Ali
- Culture amp survey results
- Sprint planning
- THG status
- Pick up ticket on test server entity creation
## 25/04/2024
- Firefighting
    - Protexin pets us yuliya encoded url
    - Creed: Danielle McCulloch wants to insert redirect. Asked her for the error before inserting those redirects for her. Holding them hostage because otherwise more likely to get ignored.
- Sitebuilder product types bug that Ali and me are struggling to recreate on local as saving subsite details have 504 conflict error with product pricing
- Show and tell
## 26/04/2024
- Finished fixing the product types bug
- Firefighting redirects
- Tried helping with Simone’s SDM access, but it was fixed by Ali in a separate call with her.
## 29/04/2024
- Continue on test server entity creation
## 30/04/2024
- Hourglass
- 1-2-1 w/ Ihor
- Released Test server entity for site info api
- Pick up ticket on test server event in big Dave 