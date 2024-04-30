## 01/03/2024
- Continue decommissioning site importer VM
    - Chris foley from Networks team doesn’t own thehut.local and after reviewing GB1/4 LBs, he’s unable to find anything for the below hosts and IPs. redirected me to linux team. I’ve created and SD ticket and pinged them
- Chased nav service
    - Emmanuel said will look at some point. Asked for a specific date, no response
## 04/03/2024
- Chase nav service
- Chase linux
    - Deleted dns records, created the final decommission vm ticket and pinged linux team
## 05/03/2024
- Chase nav service
- Expiring BD TOKEN - New Longer Coverage in 7 days
    - Released big Dave with the token no longer set as strings
    - https://thehut.atlassian.net/browse/BGD-2113
## 06/03/2024
- 1-2-1 w/ Andy
- Chase nav service
    - Asked to remove comments, got the approval.
- Ticket set up another for Ian okta big Dave SA
- Ticket to consolidate PATs to one secret for bdsa
- Ticket to backfill missing sorry server data in BD
    - Caused by site builds team triggering sorry server release directly via repository than through sitebuilder 
## 07/03/2024
- Chase for Release date on nav service
    - Monday
- Firefighting 
    - 302 temporary redirect on your Coca Cola, investigated and resolved with Ian 
## 08/03/2024
- Reviewed two PR
- Tracking down the error on sitebuilder’s Celio IN
## 11/03/2024
- Nav service release
- Simone event client
- 1-2-1 w/ Andy
## 12/03/2024
- Nav service: Evgeny asked to review PR as well
- Redirect ticket on two broken redirects on protexin
## 13/03/2024
- 1-2-1 w/ Andy
    - Need to add filter for released tickets missing description with Andy / someone with admin access
- Retro
- Navigation service release
    - Asked to run end to end tests. Several tests failed for another change that has nothing to do with my work. Let the team know, they’re looking at that now
- Writing sprint ticket descriptions
- Sprint planning
## 14/03/2024
- Navigation service released
- Released Big Dave for changes to remove nav service subsite endpoint setup
- Protexin broken redirects
    - Reporter sent a screenshot of their redirect not working, they used a different source url where it’s a ? Instead of %3F. 
    - Found out it was a case of using an illegal character as the source url. Fixed this by changing in the DB those encoded characters to their original ?, tested on my end and asked for her to test on hers.
## 15/03/2024
- Keep an eye on the broken protexin links tickets
- Add to BDSA okta Ihor’s phone number
## 18/03/2024
- Protexin redirects: response from yuliya, Gemma has left the business so she’s taking over. Caught her up and put the ticket to done
    - Gemma’s messages on that ticket were deleted, so Yuliya misunderstood what was happening on the ticket. I had to explain again what happened.
- Reviewed Ali’s stock owner PR
- Trying to get site info api to run
## 19/03/2024
- Site info api meeting with Ali to write POA, where we define, split up tasks and created several child tickets on the prototype site info api ticket.
- Rest of the day worked on implementing site metadata entity and hooking it up
## 20/03/2024
- Implement sitecreatedCMSSetup for site info API
## 21/03/2024
- Site reader api
## 22/03/2024
- Site reader api
    - Finished implementing all assigned entities
## 25/03/2024
- Site reader api review
    - Merged into main, put tickets into done
- Planned site info api tickets next sprint
    - Used the confluence doc site info api write up and made changes
## 26/03/2024
- Retro 
- Added a ticket into next sprint
- PR review for Simone
## 27/03/2024
- Update OS
- Sprint planning
- As a developer, I have created a new display to handle multiple  Stock Owners assignment  
28/03/2024
- As a developer, I have created a new display to handle multiple  Stock Owners assignment  
    - Ali asked me to also remove the create stock owner component 
        - Done