# IBM Watson - Sam's Club Cognitive Shopping Assistant (orchestration engine Watson Developer Cloud services)

## Demo with automated conversation for helping a shopper find things in a store
This demo framework leverages the **Conversation**, **Text to Speech**, **Speech to Text** services. Powered by Watson, these services allow for a personalized experience in which users can engage in natural, human-like conversations with the conversation engine.  This demo has been built for Sam's Club and is using Conversations to help them find products within the store.  Example would be a customer asking Watson, "where can I find a television?" or "where can I find water?".

All of the Watson Conversations intents, entities, and dialogs are in the artifacts folder in the exported workspace JSON file.  You can import that JSON into your Watson Conversations workspace to have everything you need to run this demo in your bluemix environment!

## Recorded Demo
Every project should include a recorded demo to make it easy for others to show to their customers.  Use this recording to learn how to best pitch the Cognitive Shopping Assistant.  It's best to keep demo file size to below 100MB since that's limit for IBM Enterprise GitHub.  Otherwise, you'll have to use Git LFS (Large File Storage) and it's a bit of a pain.

## Create accounts and log in

Sign up for Bluemix at https://console.ng.bluemix.net if you haven't already, and as a C&C CTL you should have!
Login to your bluemix account and get things ready to deploy this demo from the C&C CTL Demo Collaboration Space.

## Deploy to Bluemix

1. Select the **Deploy to Bluemix** button below to fork a copy of the project code and create the services.

  [![Deploy to Bluemix](https://bluemix.net/deploy/button.png)](https://bluemix.net/deploy?repository=https://github.ibm.com/WCP-CTL/SamsClub_Cognitive_Shopping_Assistant)

2.  Once you fill in the necessary fields, click **DEPLOY** to start the deployment of the Cognitive Shopping Assistant demo app and static services used.

3.  After it's successfully deployed, do not forget to go put in the Runtime > Environment Variable to hook it up to your own Conversation Service workspace.
    A.  Go to your running app in the bluemix console.
    B.  Click on Runtime and then the Environment Variables tab.
    C.  Create a new User Defined variable with the name "CONVERSATION_WORKSPACE_ID" and the value of your Watson Conversation workspace ID.
    
4.  Also don't forget to "Connect existing" your Watson Conversation service as a "connections" to your cognitive shopping assistant demo app.  #itsTheLittleThings

## Monitor deployment

After the project has been deployed, you can setup the full DevOps Toolchain and import the source code from repository into bluemix.  This is useful if you need to change any of the underlying SOURCE CODE.  The only thing you might actually need to change in there is the logo from Sam's Club to your customer.

Change the Logo by following these steps:
1. Navigate to the static > images folder and replace the logo.jpg logo of Sam's Club with your customer logo.
2. To make it easiest, make your customer's logo file named "logo.jpg" too and just replace it.  That way you don't have to change any of the HTML code.

Once the deployment finishes, you will have an instance of the Cognitive Shopping Assistant Demo framework app in your Bluemix Dashboard.  The base code for this demo was built by Doug Ayers and he called it the Orchestration Framework.  It has Watson Speech To Text & Text To Speech already pre-built in to the web browser UI.  Works best in FireFox.

## About the services

### Answer questions with natural language using Watson Conversations service
The Watson Conversations service lets you design the way your app interacts with a user through a conversational interface. The service can track and store user profile information to learn more about users, guide them through processes based on their unique situation, or pass their information to a back-end system to help them take action and get the help they need.

The Cognitive Shopping Assistant workspace for Conversations is included in this sample app... it's located in the "artifacts" folder.  Use that JSON in your own Watson Conversation service workspace to modify.

For more information about the Conversation service, go to the [Bluemix documentation](https://www.ibm.com/watson/services/conversation/).

### Speak to the app / Watson with the Speech To Text service
The Watson Speech To Text service easily converts audio and voice into written text for quick understanding of content.  Check the box in the demo app to "use voice" and just start talking to your app.  Extra points to anyone who implements a microphone icon next to the text input field for easily enabling & disabling the mic so it doesn't always pick up what is being said!  Would make it easier to demo and explain at same time.

For more information about the Speech To Text service, go to the [Bluemix documentation](https://www.ibm.com/watson/services/speech-to-text/).

### Listen to the app / Watson with the Text to Speech service
The Watson Text to Speech service converts written text into natural-sounding audio in a variety of languages and voices.  Check the box in the demo app to "use voice" and just start talking to your app, and your apps response will talk back to you!  Make sure you have the speaker volume all the way up when delivering the demo.

For more information about the Speech To Text service, go to the [Bluemix documentation](https://www.ibm.com/watson/services/text-to-speech/).
