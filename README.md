Simple chat app using android studio java and socket.io

To use simply clone this repo and then run the backend file using npm start. And then run the test file in android studio.

Also if you want to use the code in your own project:
* First install node.js and then use npm i express socket.io nodemon
* Then add backend/ndex.js code to your file
* Then run index.js file using npm start
* Open Android studio and then open a new project add MainActivity.java and activity_main.xml and MessageAddapter.java to your files
* To work properly you have to add the followings to your gradle and manifest:
** In build.gradle add:
implementation("io.socket:socket.io-client:2.0.0") {
    exclude(group = "org.json", module = "json")
}
** In gradle.properties add:
android.nonFinalResIds=false
** In manifest add:
<uses-permission android:name="android.permission.INTERNET" />
** In manifest add:
<application
…
android:usesCleartextTraffic="true"
…
</application>

