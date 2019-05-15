## poolBlynkLink

This small NodeJS app works with [nodejs-poolController](https://github.com/tagyoureit/nodejs-poolController) to send the socket.io data to your [blink.io](https://blynk.io/) IoT project.

1. To get started created a new project with Blynk and copy the auth token to new file called `.env` in the root directory.  You also need to define the `server:port` that nodejs-poolController is running on.  In most cases this is localhost.

### Example `.env` file
```markdown
API_KEY=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
SERVER=http://localhost:3000
```
2. You will also need to review [/src/pinDefs.js](/src/pinDefs.js) as we will be reading and writing to the blynk virtual pins.  Map pins to your liking and add more as needed.  These are used to map the data between the poolController socket.io API and Blynk's widgets you add to your project.

3. Before your initial start run `npm i` to download all dependencies.

4. Start the app by running `npm start`

5. Look at [autoStart.sh](autoStart.sh) script for help on getting this node app to auto run at boot.  Adjust to your liking.

6. Add widgets to your project and link them to the appropriate vPins.  Below in the example I created.

![Example Screenshot](/screenshot1.jpeg)

7. Use the following Blynk QR code as a project template to get you started. ![Blynk QR Code](/QR_Blynk_Demo.jpeg)