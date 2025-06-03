01/04/2025
- Added to CT Officially Country manager release
    - Set for release tmrw
- Big Dave feed manager secrets update
    - Got reviewed
- Call with Ian
    - Ask for review on feed manager PR
    - Ask about is he is my line manager
        - If so, talk about informal flexible working
    - Sam’s plans for the future of this team
        - cto Ali is on leave
02/04/2025
- Country manager release
- Big Dave release
- Trying to get teleport access
03/04/2025
- Big Dave release and testing
    - Bigdave does not exist in new ida-corporate, but does in ad. Had to migrate
    - Key cloak secret is using sandbox, whereas live is different
    - Prelive secret: 6hNjCL3t4h7tj4A7lUD3l0u4JEvn9sPb
    - Live secret: cd0fd01e-cb11-48c9-81ea-fb9949156d66
04/04/2025
- Release big Dave key cloak changes
    - 401 authorisation error
        - Bigdave client secret property missing in application.properties files. Released but failed to fix 401 error
    - Recreating in local is fine
07/04/2025
- Fixed big Dave key cloak
08/04/2025
- Continue redirect api 
09/04/2025
- Shadow Johnny more trees
    - Release process
        - Create feature branch, create PR to release branch, then create PR to merge into master then release to Live
        - Get write access - Ian Parkinson for all mt repos
        - Create accounts in more trees
        - Get access to Arco from Johnathan 
        - Moretrees corporate site. Brandon Ingham
        - For help: jack king (general Qs), jack Owen (code)
    - Get it running locally.
    - Go over db
- Retro + sprint planning
- Chase Ian on flexible working 
10/04/2025
- Setting up mt locally
11/04/2025
- Continue redirect api
- Contact jack king to get help on setting up transaction service.
14/04/2025
- Continue redirect api ticket
- Ask Jack Owen assistance 
15/04/2025
- Redirects: didn’t come in.
- Transaction service working. More trees local setup done.
    - Need walkthrough on adhoc task processes.
16/04/2025
- Redirects api 
- Big Dave SA PAT expiring. Need refresh
    - Dc password reset
    - Helping Kubernetes team with testing
17/04/2025
- Redirects api
- Redirect configurator with Ian
- Handover with Ian
22/04/2025
- vpn login failures company wide
- Login failing to amq gslb dashboard 
- Mt handover with Jonny
    - Meeting with Adam 1130
- Jonny: pulling customer data needed by midday and the rest of the day spent handover with me
- Ian: don’t the Redirect Configurator Okta Oauth sign in and out functionality. Will schedule a release for the changes when he’s back.
- Get activemq ui access back
    - Reset cache and it works
- Requested to be added to more trees dl
- Ryan James m.skinstore.com redirect configurator adding
    - m.skinstore.com pointed at fastly so not all redirects work. Networks team thing to do
    - Watch out for if m. Is added to ssl cert or not. If not, bother networks team
23/04/2025
- Jonny: with me, afternoon certificate issue and today that too with confluence documentation updates
- Sam away 12th may
    - Matt Gregory
- Redirect api
24/04/2025
- Meeting with Johnny and data team at 11 (jay cooke, asiam shabbir, Sarah mills, Jonny and me)
    - Sarah mills looking for solution to automate how they get their data instead of asking for Jonny to do so.
    - Ask Johnny about generating invoice
    - Build a dashboard for Sarah to access read only database: asiam shabbir
    - history: Bought mt, fe good, be spotty, did a rebuild gone live 1 year ago
- Jonny: updating confluence, admin-y bits, data meeting
- Victorious mt
    - High error rate: check error log on elastic, 
    - Victorops calls, and set to me
    - If call, pick up, acknowledge app runtime alerts, investigate
- Victorops added to mt team
25/04/2025
- Practice customer closing account
- Data for customers that opted out
- jonny: meeting with data, finding confluence database schema change
    - Tanzania
- Mt error dlq
    - Subscribed to project that no longer exists
        - Need to talk with Adam
    - Jonny wrote user flow on what could happen there
28/04/2025
- Redirect api
- Imagepullsecret not doing shit
    - Eunomia overwriting it
- For script: 
    - Kubectx gb5-st-unityv3, Kubectl get secrets-n bigdave-api —show-labels —field-selector (get a list of secrets that are dockerconfigjson managed by=helm label
- Refactor update-docker-secrets.sh script
29/04/2025
- Update docker secret
    - And drop one out
- Matt Gregory meeting
- Redirect api
30/04/2025
- Redirect api last endpoint and testing other endpoints
- Investigate bigdave site create db inserts 
    - Insert New_Site_Create_Upload, New_Site_Create (upload id), New_Site_Create_Catalogue (upload id)
    - Update New_Site_Create_Upload status
    - For social login:
        - Site table