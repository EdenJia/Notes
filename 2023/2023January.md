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