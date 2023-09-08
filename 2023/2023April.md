## 28/04/23
- THG hourglass
- Talk to Craig about the trigger sorry server error. 
- Continue nav service ticket
    - Getting to publish events to local activemq, discovered the endpoint for localhost exists in the application-dev.properties file, so it’s already getting published there but I’m not seeing it
    - Get access to PL broker
- Added another throw clause so when a sorry server status isn’t found, big Dave throws a 404 instead of a 500.
- Call with Simone on the rendering reports testbox error
    - Testbox api code we’re pinging on big dave seems to be deprecated and moved to the site-builds-testbox repo