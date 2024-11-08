01/10/2024
- Mac security update
- Releasium
    - View history button disabled intentionally for releases.
    - Dockerm cert generation:
        - Used to monitor docker containers deployed by Irene scripts but since been superseded by eunomia for Kubernetes. The data exposed by dockers used to power the dashboards in ThemisOps
- Electricity outages
02/10/2024
- Releasium
    - View history disabled - only operations in app is to insert history. Not retrieve. Except from the functions to find and retrieve history from the database in the history Repo, no other code exist to call and display that data. Needs separate ticket
    - Testing db upgrade script
    - Added enterprise as a platform
- Firefighting
    - Brought up 2 bugs in sitebuilder’s subsite details form when trying to edit details for an existing subsite
03/10/2024
- Releasium review and release
    - James review: added platforms filter, ask Andy about ‘On change it changes calendar context’ in the ticket
    - Simone review: improved error handling
- Activemq new authentication features that reqs username and password to access amq brokers.
    - Released 10th October
    - We need to:
        - If applications using TLS, regenerate certs and update in application by oct 16. Instruction here https://thehut.atlassian.net/wiki/spaces/MES/pages/5276991574/Client+SSL+TLS+creation+V2 
        - Request amq credentials. Need to submit reqs by oct 12. Instruction here https://thehut.atlassian.net/wiki/spaces/MES/pages/5282234393/New+ActiveMQ+Feature+Authorization+and+Authentication
            - Implement new authentication and authorisation by oct 18
    - Jon Clarke is pushing back: saying not enough time to make the changes
    - For our team: big Dave (has review service changes & BDCLI changes), properties services, bigdaveclientinterface, olympus. Possibly: navigation service, social login service, feed manager, country manager, 
    - Has a dedicated channel in the activeMQ announcements teams 
04/10/2024
- Releasium new changes review
07/10/2024
- Releasium
08/10/2024
- Released releasium
    - Andy review and fixes
    - Did not know to add a dropdown to filter the releases on the calendar by platform, instead of a filter in the search bar. No breaking change
    - Made a dropdown component
    - Refactored fetchAll to accept platform id
    - Yet to test
09/10/2024
- Releasium
    - API changes work
    - Working on front end changes
- Simon Harris asked if I could show off releasium’s new changes for the show and tell.  Told him it still needs some work but would be happy to do so when it is ready.
- Retro
- Sprint plan
- 1-2-1 w/ Ihor
    - Got bigdave working
10/10/2024
- Releasium
    -  Working on front end changes. Done functionally, getting styling done
- AMQ push w/ Andy
    - Ask about username in amq channel: it’s just the username you want for the application.
    - Compile applications that use AMQ
11/10/2024
- Get the credentials ticket submitted
    - Simone gave me a list of the applications, their queues and topics 
- Releasium
    - New changes demoed for Ian and Andy. Made and had the SD release ticket approved. Release tmrw
14/10/2024
- Release releasium
    - Fix bug where platform releases can’t be saved over each other
        - DB constraint change
- Ian properties manager demo w/ Ian
15/10/2024
- Help Marc with releasium
- Pick up big Dave fulfilment event driven ticket
16/10/2024
- Ping Checkout team olympus event driven release
- Continue with big Dave
    - Bdcli branch so old had to rebase it
- 1-2-1 w/ Ihor
- Amq credentials sd ticket closed. Waiting for credentials to be sent to Andy’s email
17/10/2024
- Big Dave fulfilment 
- Amq credentials update
    - Pm jurgita directly to get prioritised, otherwise, slow turnaround
    - Will discuss next sprint
- Releasium firefighting
    - moderator management support - calls with Marc Hamilton and Samantha rogulskas
    - Validation different for different platforms
        - e.g. successful enterprise release does not need a version number.
18/10/2024
- Firefighting
- BD fulfilment event integration
21/10/2024
- BD fulfilment event integration -  unit tests
    - Readied it for review and in review now with Harriet
- Worked together with Ian to run big Dave locally on his side
22/10/2024
- Harriet’s asked for other ways to test my changes. I’ll let her know the details
- Townhall
- BD fulfilment event integration released
23/10/2024
- Retro & sprint planning
- Releasium view history button
    - Rancher desktop bombs out with Kubernetes error
24/10/2024
- Releasium view history button
- Show and tell: releasium platform changes
25/10/2024
- Fixed rancher issue, new issue with running docker file popping up
    - WHY IS IT NOT RUNNING ANYMORE
28/10/2024
- Taking grandma to the GP
- Wifi black out - using hotspot
- Releasium 
    - Tried getting packages from http instead of https to avoid ssl verification issues - but build gets stuck later 
    - Tried adding certs to docker container, not accepting
29/10/2024
- Managed to get docker file running
- New team structure meeting
- Hourglass 
- Latter Half day off
    - Dentist
30/10/2024
- Releasium
- Tech townhall
- 1-2-1 w/ Ihor
31/10/2024
- Fixed releasium startup issues
- Releasium
    - Getting histories endpoint working
- Admin privileges for host files new security