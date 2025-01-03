## 01/11/2024
- Releasium
- Knowledge share
- Mandatory harassment course
## 04/11/2024
- Releasium
## 05/11/2024
- Releasium
    - Call with Ian end of day on javascript issue
## 06/11/2024
- Releasium
    - Done 
- Site info api ticket
    - Endpoint we’re hitting to check for messages
## 07/11/2024
- Releasium reviewed and released
- Pick up ticket for the big Dave AMQ authentication integration
    - Asked Andy for credentials - they’ve expired
    - Asked messaging team to resend to Ian
    - Ian’s shared the bigdave ones with me
## 08/11/2024
- Carry on big Dave AMQ auth integration
    - Failed to connect with details, got error that details are invalid. The support chat for this is chockfull of errors like this so scrolling through those and seeing their solutions
## 11/11/2024
- Carry on with amq auth integration
    - Found out connecting to pl also connects st amq in bigdave
    - Found how we connect to amq in different environments is just to connect to every one of them
## 12/11/2024
- Auth integration,
    - Using every environment password as that’s needed to connect locally
        - Fixed
## 13/11/2024
- Bigdave 
    - Fixed live password not connecting to live amq
    - Update endpoint and refactor functionality and relevant unit tests.
        - Stuck on one unit test - called Ihor and didn’t have much luck with it
        - Endpoint does not return an error when site created is the same. Want to ask Kraken team about it
    - Search config is not the same for white label en-gb
        - Check channel locale
- Releasium - test and approved James’ PR
## 14/11/2024
- Continue with bigdave kraken endpoint refactor
    - Contacted Philippe and she says that endpoint’s behaviour is the same as the last one. Checked myself and yep - so unit test failing isn’t that
    - Cause was a missing hashcode and equals method in the KrakenInput model.
    - Put into review
## 15/11/2024
- Get review and release big Dave
- Chase James mercer for site info api username and password
- Staff tech ticket to resolve why I can’t change my own tickets’ status
    - Need to come back Monday as sdp staff tech member off until then
## 16/11/2024
- Let Philippa know it’s done
- Big Dave amq 
    - Asking for access to the gb5-pl ui for testing
- Try Apollo with cloud flare off
    - Update project and platform java version to 17
- Ian teach me about load tests
    - script.js needs: host variable needs specified gb1 and gb4
    - Gave me load test ltctl commands. Need to be run at project root
    - Post response to Black Friday 2024 channel report targeted peak traffic
## 17/11/2024
- Amy big Dave ticket
    - Access to st broker ui
- Ali contacted me on Stephen lewis’ behalf to gain access to create releases on releasium
- Call with Ian about endurance checkout Artemis styling issue
    - Contacted mike collins, he says Simone should be back tmr
## 18/11/2024
- Contact Simone and set up some time for her to debrief me on what to do.
    - Unable to replicate locally - pulling through Artemis but checkout has data mocked is separate to live / Artemis
        - mock data is not Artemis styles.
    - Check with checkout if other new sites pulling Artemis is ok unlike endurasports
    - Charlotte Whelan to ask about Artemis: what other conditions will alternate logo be called in.
    - Font size should be 14px but now too big 18px (body text, large device on Artemis)
    - Only a small test number of sites have light theme calc logic
    - Asking write access to checkout-web from Oliver holden
- Sprint + retro
- Submit annual leave from Ihor
## 19/11/2024
- Continue with endurance checkout fix
## 20/11/2024
- Endura 
## 21/11/2024
- Continue chasing endurance 
## 22/11/2024
- Continue chasing endurance 
- Renewed GitHub token for sa bigdave
- Call with Ian 
## 25/11/2024
- Big Dave AMQ
- Quickly ask for endura sports updates
    - No response
## 26/11/2024
- Oliver holden says it’s on gb1 999 and to test I’ll need to apply checkout settings - no clue what those are
    - Simone is offline and until the 29th
- Broker url changed
## 27/11/2024
- Test the endurance sports - released on gb1 999 but unable to hit, only gb4 endpoints.
    - Didn’t release to gb4 did so, logo pulled in is fine but font size is still too big
- Continue with AMQ
- Call with Ian
## 28/11/2024
- Look at checkout fontSize override since it’s not working
- Town hall
- Setup new mod tp
    - Ask Ali / CTP
## 29/11/2024
- Setup mod tp - ask ctp
    - Tried methods Ian has forwarded to me
- Simone checkout: meeting and fix
    - Needs testing on a list of other checkout sites
- Hourglass