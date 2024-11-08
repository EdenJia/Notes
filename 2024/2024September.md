2/09/2024
- Release Apollo
- Releasium 
- Evaluation form with Ihor
03/09/2024
- Releasium - James & Ihor & Andy
    - GitHub login blocking creating and editing releases
    - Figure out how auth works.
    - User.jsx calls onClick() -> new window url: http://localhost8080/auth/redirect -> redirect.html returns script to call userConnect(‘500’) -> User.jsx ’s connect(code) which code=500 -> localhost:8080/auth -> requestToken in GithubService.java broken need debugging
04/09/20224
- Ask checkout for olympus event integration release 
    - No response
- Releasium
    - GitHub authentication mockoauth container doesn’t work. 
- 1-2-1 w/ Ihor 
05/09/2024
- Chase checkout
    - None of the people in the gc for olympus was in
- 3 my protein blog direct tickets made yesterday - all are done
- releasium 
- Bigdaveclientinterface SA_PASSWORD issue
06/09/2024
- Releasium
- Handover notes
- Chase up redirect tickets and olympus pals
- Bimuno redirect fix
Asdfasdfasd
- Annual leave
13/09/2023
- Catch up on emails 
- Handover notes on Monday
    - Add AL on holiday calendar
- Chase up checkout - has Oliver holden left?
    - Gareth naser
    - 1600 to 0100 for Daniel oxley
- Saw message from James mercer.
- Share grafana username w/ Harriet
    - Call to test
- Blaithin from SEO responded and confirmed bimuno redirect fix
16/09/2024
- AL
17/09/2024
- Chase checkout again - no response on Friday
    * moved on to migrating non pci apps to Rocky, we have more urgent applications to move atm
- Releasium
18/09/2024
- Releasium
- 1-2-1 with Ihor
19/09/2024
- Releasium
20/09/2024
- Releasium 
    - Call with Ihor, didn’t go with dispatch method, went with a direct REST call
23/09/2024
- Releasium
    - Problem 1: when editing existing release, platform isn’t populated with existing
    - Problem 2: can’t create a release
        - Backend error: Required Integer parameter 'platformId' is not present
        - Find where it’s set / how state is set -> tracking dispatch
24/09/2024
- Releasium
    - Figured out how to set and send correct payload to backend. Now backend is returning 500 error w/ no message. Failing to execute the insert sql
    - Finished problem 2
25/09/2024
- Releasium
    - Do problem no.1 
    - Write unit tests
    - white SOD
        - Fixed
- Sprint retro
- Sprint planning
- 1-2-1
26/09/2024
- Releasium
    - Fix source map errors - give up
    - PR check errors: 
        - runners don’t have permission for containers -> James Healy fixed
        - Test suite failed -> multiple deprecated messages where the model.spec.jsx test suite failed to run
            - Figure out running the front end tests
- Hourglass
- Training module
27/09/2024
- Releasium
    - Figure out how to run the jest tests
        - Caused by a mixture of babel 6 and 7 packages and presets clashing in package.json
        - Some dependencies e.g. parse5 are relying on newer node syntax, incompatible with node 14
            - Too many dependencies have dependencies with node 18+
            - Decided to upgrade to node 18
            - Andy helped to upgrade to node 20 partially
            - Managed to get the app running. Jest not running, missing dependencies imported in test files. Missing directories. Signs that the test dependencies have been removed from the package.json 
30/09/2024
- Releasium
    - Removed yarn run Js:test from yarn run test package.json. Merged node upgrade PR into my working branch
        - Build test job still failing. Eventually Andy said the task wasn’t needed
    - Write up local dev changes needed to run in README
    - Upgrade db schema via the upgrade.sql instructions
    - Currently being reviewed by James 