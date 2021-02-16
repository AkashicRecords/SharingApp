# SharingApp
Mobile application for IOS and Android written in Meteor.js Cordova Ionic 

<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="utf-8">
		<meta http-equiv="X-UA-Compatible" content="IE=edge">
		<meta name="viewport" content="width=device-width, initial-scale=1">
	</head>
<body>
		<div class="container">
			<div class="content">
				<div class="main">
					<h1>TapShop</h1>
					<p>Buy and Sell mobile app made with Meteor, Angular and Ionic.</p>
					<hr>
					<h3>Table of Contents</h3>
					<ul class="list-unstyled">
						<li>
							<a href="#01">Getting Started</a>
						</li>
						<li>
							<a href="#02">Running the Android App</a>
						</li>
						<li>
							<a href="#03">Deploying Your App</a>
							<ul>
								<li>
									<a href="#03a">Deploy to VPS (AWS or Digital Ocean)</a>
								</li>
								<li>
									<a href="#03b">Deploy to Heroku</a>
								</li>
								<li>
									<a href="#03c">Deploying the Android App</a>
								</li>
							</ul>
						</li>
						<li>
							<a href="#04">Test Data</a>
						</li>
						<li>
							<a href="#05">Third-Party Packages</a>
						</li>
						<li>
							<a href="#06">Files and Settings</a>
								<ul>
									<li>
										<a href="#07">Product Collection Settings</a>
									</li>
									<li>
										<a href="#08">Collections</a>
									</li>
									<li>
										<a href="#09">Mobile App Settings</a>
									</li>
									<li>
										<a href="#10">Routing</a>
									</li>
									<li>
										<a href="#11">Templates and Controllers</a>
									</li>
									<li>
										<a href="#12">Methods</a>
									</li>
									<li>
										<a href="#13">Publications</a>
									</li>
									<li>
										<a href="#14">User Accounts, Oauth, and Emails</a>
									</li>
									<li>
										<a href="#15">Side Menu</a>
									</li>
									<li>
										<a href="#16">Product Listings</a>
									</li>
									<li>
										<a href="#17">Selling</a>
									</li>
									<li>
										<a href="#18">Chat</a>
									</li>
									<li>
										<a href="#19">User Rating</a>
									</li>
									<li>
										<a href="#20">User Profile</a>
									</li>
									<li>
										<a href="#21">Search</a>
									</li>
									<li>
										<a href="#22">Activity Feed</a>
									</li>
									<li>
										<a href="#23">AdMob - Android App Ads</a>
									</li>
									<li>
										<a href="#24">Push Notifications</a>
									</li>
									<li>
										<a href="#25">Integrate Image Upload with AWS S3</a>
									</li>
									<li>
										<a href="#28">Google Sign-In on Android App</a>
									</li>
								</ul>
						</li>
						<li>
							<a href="#26">Other Guides</a>
						</li>
						<li>
							<a href="#27">Changes and Bug Fixes</a>
						</li>
					</ul>
					<hr>
					<h2 id="01">Getting Started</h2>
					<p>
						<span class="bold">Step 1</span> - Install Meteor JS. Follow the installation guide on <a href="https://www.meteor.com/install">here</a>.
						<br />
						(Skip this if you already have Meteor in your system.)
					</p>
					<p>
						<span class="bold">Step 2</span> - On your terminal, go to the tapshop folder.
						<blockquote>
						 cd path-to-folder/tapshop
					 	</blockquote>
					</p>
					<p>
						<span class="bold">Step 3</span> - On the 'tapshop' folder, install the npm packages for this app.
						<blockquote>
						 meteor npm install
						</blockquote>
					</p>
					<p>
						<span class="bold">Step 4</span> - Open the <span class="bold">settings.json</span> file.
						Enter your API keys inside "".
						<br/><br/>Get your API keys here:
						<blockquote>
							<b>Google Login</b> (<a href="https://console.developers.google.com">Google Developers Console</a>)
							<br /><br />
							&emsp;- get the OAuth Client Id and Secret for Web Application.<br />
							&emsp;- configure your Google login settings as seen on this <a href="#oauth">guide</a>.
							<br /><br />
							<b>Facebook Login</b> (<a href="https://developers.facebook.com">Facebook Developers</a>)
							<br /><br />
							&emsp;- get the App Id and Secret.<br />
							&emsp;- configure your Facebook login settings as seen on this <a href="#oauth">guide</a>.
							<br /><br />
							<b>Automated Emails</b> (<a href="https://mailgun.com">Mailgun</a> or <a href="https://sendgrid.com/">Sendgrid</a>)
							<br /><br />
							Select one:<br />
							&emsp;- Sendgrid: get your API key.<br />
							&emsp;- Mailgun: get your SMTP username and password.<br />
							<br /><br />
							<b>User Location</b> (<a href="https://developer.here.com">HERE Maps</a>)
							<br /><br />
							&emsp;- get the App Id and App Code for Javascript.<br />
							<br /><br />
							<b>AdMob Ads</b>: (<a href="https://www.google.com/admob">AdMob</a>)
							<br /><br />
							&emsp;- create a banner ad for Android and get Ad Unit ID.<br />
							&emsp;- enable AdMob with this <a href="#23">guide</a>.<br />
							<br /><br />
							<b>Push Notifications</b>: (<a href="https://console.firebase.google.com">Firebase Cloud Messaging</a>)
							<br /><br />
							&emsp;- go to Project Settings, and under Cloud Messsaging tab, get your FCM Sender ID and Server Key.<br />
							&emsp;- enable Push Notification with this <a href="#24">guide</a>.<br />
							<br /><br />
						</blockquote>
					</p>
					<p>
						<span class="bold">Note:</span> The app will run without setting the API keys, but the services above will not work.
						Your API keys should be kept in settings.json file, and not on the source code for security.
					</p>
					<p>
						<span class="bold">Step 5</span> - Run the app. On terminal, run:
						<blockquote>
							meteor --settings settings.json
						</blockquote>
					</p>
					<p>
						<span class="bold">Note:</span> This command will setup the app and install all packages, before running the app.
					</p>
					<p>
						<span class="bold">Step 6</span> - When the app is already running, go to localhost:3000 on your browser.
						<br />
						<br />
						To exit the app, press ctrl + C on your terminal.
						<p>
							<span class="bold">Note:</span> If the app is running with <a href="#04">Test Data</a>,
							loading it for the first time will be slow as images will be inserted to the sample Listings on startup.
						</p>
					</p>
					<hr>
					<h2 id="02">Running the Android App</h2>
					<p>
						Make sure you have all requirements for Android app development on your computer.
						Check this <a href="http://guide.meteor.com/mobile.html#installing-prerequisites-android">guide</a> for details.
					</p>
					<p>
						If you want to enable <b>Google Sign-In</b> on Android during debug mode, please follow this <a href="#debug">guide</a> first.
					</p>
					<p>
						To test the the Android app, connect your Android device to your computer via USB, and enable debug mode.
					</p>
					<p>
						With your device connected and on debug mode, run this command on your terminal:
						<blockquote>
							meteor run android-device --settings settings.json
						</blockquote>
					</p>
					<p>
						<span class="bold">Note:</span> This app can also run as IOS app, just follow the Meteor guide above.  However, this has
						not been tested on IOS, and is currently not supported. Some adjustments on the source code may also be needed for it to
						work properly.
					</p>
					<hr>
					<h2 id="03">Deploying Your App</h2>
					<br />
					Meteor apps like TapShop can be hosted on servers that can host Node apps. This guide will show you how to deploy
					TapShop on a <span class="bold">VPS</span> like AWS and Digital Ocean, or on <span class="bold">Heroku</span>.
					So just select one and follow the guide below.
					<br />
					<br />
					Other options for hosting include <a href="https://modulus.io/meteor">Modulus.io</a> and <a href="https://www.meteor.com/hosting">Meteor Galaxy</a>.
					<br />
					<br />
					<br />
					<h3 id="03a">Deploy to VPS (AWS or Digital Ocean)</h3>
					<p>
						**Note: If you have deployed this app using <span class="bold">Mupx</span> to your server before,
						please migrate your app first as seen on this <a href="https://github.com/kadirahq/meteor-up#migrating-from-meteor-up-0x">migration guide</a>
						to use this on the same server, or go to this old <a href="#28">guide on using Mupx</a> instead.
					</p>
						<span class="bold">Step 1</span> - If you don't have a VPS yet, create a new server with Ubuntu or Debian OS.
						<p>
							If you choose to deploy using Digital Ocean, you can get $10 credit as new customer using this <a href="https://m.do.co/c/5d3c927183be">link</a>.
						</p>
						<p>
							<span class="bold">Step 2</span> - Add a deployment user on your server.
							<br />
							<br />
							Follow this <a href="https://www.digitalocean.com/community/tutorials/how-to-add-and-delete-users-on-ubuntu-16-04">Guide</a>
							by Digital Ocean on how to create a new user on Ubuntu or Debian server.
						</p>
						<p>
							After creating a new username and password, remove sudo password requirement for the username that you will use for deployment.  This will enable automated installation
							of the app and its requirements without the server asking for sudo password.
							<br />
							<br />
							<span style="font-weight: bold;">Note:</span> This will not remove the password of that username.  The server will still require the password to login.
						</p>
						<p>
							Go to sudoers file:
							<blockquote>
								sudo visudo
							</blockquote>
						</p>
						<p>
							Go to a new line in this file, and enter the following:
							<blockquote>
								Your-Username ALL=(ALL) NOPASSWD: ALL
							</blockquote>
						</p>
						<p>
							Press ctrl + X to exit, and save changes.
						</p>
					<p>
						<span class="bold">Step 3</span> - On your computer, install Mup then enter your server details
						on the <span class="bold">mup.json</span> file.
						<br />
						Visit this <a href="https://github.com/kadirahq/meteor-up#installation">link</a> for more details on Mup.
						<p>
							Install the Mupx package from npm with this command:
							<blockquote>
								npm install -g mup
							</blockquote>
						</p>
						<p>
							Create a new folder to run your deployment.  Make sure this is separate from the 'tapshop' folder.
							<blockquote>
								mkdir ~/your-folder-name
							</blockquote>
						</p>
						<p>
							Go to your new folder.  And inside the folder, run this command:
							<blockquote>
								mup init
							</blockquote>
						</p>
						<p>
							You will then find the <span class="bold">mup.js</span> file inside the folder.  Configure this file as seen in this example:
						</p>
						<p>

							<blockquote>
								&emsp;module.exports = { <br />
								&emsp;- servers: { <br />
								&emsp;&emsp;one: { <br />
								&emsp;&emsp;&emsp;host: '1.2.3.4', <span style="color: red;">//----> ip address of your server</span><br/>
								&emsp;&emsp;&emsp;username: 'your-username',  <span style="color: red;">//----> your server username</span><br />
								&emsp;&emsp;&emsp;password: 'your-password', <span style="color: red;">//----> your server password</span><br />
								&emsp;&emsp;&emsp;// pem: './path/to/pem' <span style="color: red;">//----> if you are using ssh keys on server, uncomment and place file path of your keys.</span><br />
								&emsp;&emsp;}<br />
								&emsp;},<br />
								&emsp;meteor: {<br />
								&emsp;&emsp;name: 'tapshop', <span style="color: red;">//----> your app name.</span><br />
								&emsp;&emsp;path: '/your-file-location/tapshop', <span style="color: red;">//----> file location of tapshop folder.</span><br />
								&emsp;&emsp;servers: {<br />
								&emsp;&emsp;&emsp;one: {}<br />
								&emsp;&emsp;},<br />
								&emsp;&emsp;buildOptions: {<br />
								&emsp;&emsp;&emsp;serverOnly: true<br />
								&emsp;&emsp;},<br />
								&emsp;&emsp;env: {<br />
								&emsp;&emsp;&emsp;ROOT_URL: 'http://your-domain.com', <span style="color: red;">//----> your domain name.</span><br />
								&emsp;&emsp;&emsp;MONGO_URL: 'mongodb://localhost/meteor' <br />
								&emsp;&emsp;},<br />
								&emsp;&emsp;docker:{<br />
								&emsp;&emsp;&emsp;image: 'abernix/meteord:base'<br />
								&emsp;&emsp;},<br />
								&emsp;&emsp;deployCheckWaitTime: 96,<br />
								&emsp;&emsp;enableUploadProgressBar: false<br />
								&emsp;},<br />
								&emsp;mongo: {<br />
								&emsp;&emsp;oplog: true,<br />
								&emsp;&emsp;port: 27017,<br />
								&emsp;&emsp;version: '3.4.1',<br />
								&emsp;&emsp;servers: {<br />
								&emsp;&emsp;&emsp;one: {}<br />
								&emsp;&emsp;}<br />
								&emsp;}<br />
								};<br />
							</blockquote>
						</p>
					</p>
					<p>
						<span class="bold">Step 3a (Optional)</span> - Add your SSL Certificate to your Web App for geolocation features to work on Chrome browser.
					</p>
					Place your SSL certificate files inside your deployment folder, and add settings shown in this <a href="https://github.com/kadirahq/meteor-up#ssl-support">link</a> to your <span class="bold">mup.js</span> file.
					<br />
					<br />
					If you have added an SSL Certificate, go to your tapshop folder, and run this command to redirect all traffic to your HTTPS site:
					<br />
					<br />
					<blockquote>
						meteor add force-ssl
					</blockquote>
					<br />
					<p>
						<span class="bold">Step 4</span> - Copy your <span class="bold">settings.json</span> file to your deployment folder.
					</p>
					<p>
						<span class="bold">Step 5</span> - Run Mupx deploy with the <span class="bold">settings.json</span> file.
						<br />
						<br />
						If this is your first deployment, run this command first to install all requirements on the server:
						<blockquote>
							mup setup
						</blockquote>
						<br />
						Then deploy the app with this command:
						<blockquote>
							mup deploy --settings=settings.json
						</blockquote>
					</p>
					<p>
						<span class="bold">Step 6</span> - On the browser, go to domain name, or ip address of your server to see if the app is working.
					</p>
					<p>
						<span class="bold">Note:</span> If the app is running with <a href="#04">Test Data</a>,
						loading it for the first time will be slow as images will be inserted to the sample Listings on startup.
					</p>
					<br />
					<h3 id="03b">Deploy to Heroku</h3>
					<br />
					<p>
						<span class="bold">Step 1</span> - Install and setup Heroku toolbelt.
						<p>
							Go to this <a href="https://toolbelt.heroku.com/">page</a> for details on installation for your OS.
						</p>
						<p>
							After installation, go to your terminal and login to your Heroku account with this command:
							<blockquote>
								heroku login
							</blockquote>
						</p>
						<p>
							Create a Heroku app with this command:
							<blockquote>
								heroku create Your-App-Name
							</blockquote>
						</p>
					</p>
					<p>
						<span class="bold">Step 2</span> - Go to the 'tapshop' folder and connect the files to your Heroku app.
						<blockquote>
							heroku git:remote -a Your-App-Name
						</blockquote>
					</p>
					<p>
						<span class="bold">Step 3</span> - Install Meteor buildpack to your Heroku app.
						<blockquote>
							heroku buildpacks:set https://github.com/AdmitHub/meteor-buildpack-horse.git --app Your-App-Name
						</blockquote>
					</p>
					<p>
						<span class="bold">Step 4</span> - Add MongoDB hosting via <a href="https://mlab.com/">mLab</a>.
						<blockquote>
							heroku addons:create mongolab:sandbox --app Your-App-Name
						</blockquote>
						<p>
							<span class="bold">Note:</span> The Free Sandbox plan of mLab is used for this deployment. Your settings for mLab
							can be found on the dashboard of your Heroku account.
						</p>
					</p>
					<p>
						<span class="bold">Step 5</span> - Configure your Heroku server.
					</p>
					<p>
						Set the root url of your app:
						<blockquote>
							heroku config:set ROOT_URL=https://Your-App-Name.herokuapp.com --app Your-App-Name
						</blockquote>
					</p>
					<p>
						Add your <span class="bold">settings.json</span> file.
						<br />
						<br />
						For Mac and Linux users:
						<blockquote>
							heroku config:add METEOR_SETTINGS="$(cat settings.json)" --app Your-App-Name
						</blockquote>
						<br />
						For Windows users:
						<blockquote>
							1 - Go to your Heroku account panel.<br />
							2 - Click on your app.<br />
							3 - Go to Settings tab.<br />
							4 - Click on "Reveal Config Vars"<br />
							5 - Create METEOR_SETTINGS<br />
							6 - On value, copy and paste all values inside your settings.json file.<br />
						</blockquote>
					</p>
					<p>
						<span class="bold">Step 6</span> - Deploy your app to server.
						<blockquote>
							git push heroku master
						</blockquote>
					</p>
					<p>
						<span class="bold">Step 7</span> - On the browser, go to your app url to see if the app is working.
						<blockquote>
							https://Your-App-Name.herokuapp.com
						</blockquote>
					</p>
					<p>
						<span class="bold">Note:</span> If the app is running with <a href="#04">Test Data</a>,
						loading it for the first time will be slow as images will be inserted to the sample Listings on startup.
					</p>
					<br />
					<h3 id="03c">Deploying the Android App</h3>
					<span class="bold">Note:</span> Please make sure you already have the web app running on the server before
					deploying the Android app. If you have not deployed the app on your server please follow the instructions above.
					<br />
					<br />
					Also, make sure you have all requirements for Android app development on your computer.
					Check this <a href="http://guide.meteor.com/mobile.html#installing-prerequisites-android">guide</a> for details.
					<br />
					<br />
					<p>
						<span class="bold">Step 1</span> - Build and deploy your Android app.
						<br />
						On the terminal, and on the /tapshop folder, run this command:
						<blockquote>
							meteor build /your-folder-name --mobile-settings settings.json --server=http://Your-App-Domain
						</blockquote>
						<p>This will generate the release-unsigned.apk file in this location: /your-folder-name/android/</p>
					</p>
					<p>
						<span class="bold">Step 2</span> - Sign your apk file.
						<p>
							If this is your first time to deploy this app as an apk file, you will need to create an app key.
							Follow this <a href="http://guide.meteor.com/mobile.html#submitting-android">guide</a> for more details.
						</p>
						<p>
						To generate a key, run this command with your app name:
						<blockquote>
							keytool -genkey -alias Your-App-Name -keyalg RSA -keysize 2048 -validity 10000
						</blockquote>
						<p>
							If you already have your app key, go to <span class="bold">/your-folder-name/android/</span>
							and then run the following commands:
							<blockquote>
								jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 release-unsigned.apk Your-App-Name
							</blockquote>
							<blockquote>
								$ANDROID_HOME/build-tools/23.0.2/zipalign 4 release-unsigned.apk Your-App-Name.apk
							</blockquote>
						</p>
						<p>
							<span class="bold">Step 3</span> - After signing the apk file, you can now run the apk file on your device,
							or upload to the Play Store.
						</p>
						<p>
							<span class="bold">Step 4</span> - Enable <b>Google Sign-In</b> on your Android app by following this <a href="#prod">guide</a>.
						</p>
					</p>
					<hr>
					<h3 id="04">Test Data</h3>
					<p>
						These files automatically inserts data for testing and development.  Please remove these files before deploying
						your app for production.
					</p>
					<p class="bold">tapshop/server/test_data/seed.js</p>
					<p>
						- This file inserts sample Listings and User data on startup if the app is empty.
					</p>
					<p class="bold">tapshop/server/test_data/seed_methods.js</p>
					<p>
						Listing Images
						<br/>
							- Inserts images of Listings on startup if images are empty.
							<br/>
							- Moved to <span class="bold">tapshop/server/test_data/seed.js</span> on version 18/07/2016.
							<br/>
							- For older versions this is located at <span class="bold">tapshop/client/test_data/insert_images.js</span>
					</p>
					<hr>
					<h3 id="05">Third-Party Packages</h3>
					<p>
						This app uses third-party packages to run some of its features.  The files below contain lists of Meteor packages,
						Cordova plugins, and npm packages being used.
					</p>
					<p>
						The third-party packages are not included in zip file of this app, but it will automatically be downloaded and installed by Meteor
						when your run the app.
					</p>
					<p class="bold">tapshop/.meteor/packages</p>
					<p>
						- Contains list of Meteor packages that this app is using.  You can add or remove packages by removing the package name in this list.
					</p>
					<p>
						- Other Meteor packages can be found <a href="https://atmospherejs.com/">here</a>.
					</p>
					<p class="bold">tapshop/.meteor/corodva-plugins</p>
					<p>
						- Contains list of Cordova plugins that will automatically be downloaded and installed when you run the Android app.
					</p>
					<p>
						- To learn more about adding and removing Cordova plugins, you can go to this <a href="http://guide.meteor.com/mobile.html#installing-plugins">guide</a>.
					</p>
					<p class="bold">tapshop/package.json</p>
					<p>
						- Contains npm packages that this app is using.
					</p>
					<hr>
					<h3 id="06">Files and Settings</h3>
					<br />
					<h3 id="07">1. Product Collection Settings</h3>
					<p class="bold">tapshop/server/components/products_data.js</p>
					<p>
						- The app uses this file to insert product category data on startup.  It inserts this data only if Products database is empty.
					</p>
					<p>
						- You can set your own product categories in this file, including its images. For the changes to take effect, run:
						<blockquote>
							meteor reset
						</blockquote>
						(Warning: this will erase all data in the database.)
					</p>
					<br />
					<h3 id="08">2. Collections</h3>
					<p class="bold">tapshop/lib/collections.js</p>
					<p class="bold">tapshop/lib/images.js</p>
					<p class="bold">tapshop/server/publications/</p>
					<br />
					<h3 id="09">3. Mobile App Settings</h3>
					<p class="bold">tapshop/mobile-config.js</p>
					<p class="bold">tapshop/mobile/</p>
					<br />
					<h3 id="10">4. Routing</h3>
					<p>
						<span class="bold">tapshop/client/routes.js</span>
						<br />
						- Includes settings for Loading Spinners, and pages requires user to be logged in.
					</p>
					<br />
					<h3 id="11">5. Templates and Controllers</h3>
					<p class="bold">tapshop/client/templates/</p>
					<p>
						<span class="bold">tapshop/client/templates/main/</span>
						<br />
						- Includes files for Tabs, Side Menu, Search, Activity Feed, and the Listing directive.
					</p>
					<br />
					<h3 id="12">6. Methods</h3>
					<p class="bold">tapshop/lib/methods/</p>
					<p class="bold">tapshop/server/methods/</p>
					<br />
					<h3 id="13">7. Publications</h3>
					<p class="bold">tapshop/server/publications/</p>
					<br />
					<h3 id="14">8. User Accounts, Oauth, and Emails</h3>
					<p>
						<span class="bold">tapshop/lib/config/at_config.js</span>
						<br />
						- Settings for Login and Register forms.
					</p>
					<p>
						<span class="bold">tapshop/server/components/configure_services.js</span>
						<br />
						- Settings for Oauth and smtp settings for automated emails.
					</p>
					<p>
						<span class="bold">tapshop/server/components/system_email.js</span>
						<br />
						- Message template for automated emails.
					</p>
					<p>
						<span class="bold">tapshop/server/components/user_accounts.js</span>
						<br />
						- User creation functions.
					</p>
					<p>
						<span class="bold">tapshop/client/templates/users/auth/</span>
						<br />
						- Templates and controllers for Login, Register, Forget Password, Reset Password.
					</p>
					<p>
						<span class="bold" id="oauth">Oauth Settings on Google and Facebook:</span>
					<p>
						Google Developers Console
						<br />
						<blockquote>
							Authorized Javascript Origins:  https://your-domain-name
							<br />
							<br />
							Authorized redirect URIs:  
							<br />
							&emsp;https://your-domain-name/_oauth/google
							<br />
							&emsp;https://your-domain-name/app/login
						</blockquote>
					</p>
					<p>
						Facebook Developers - App Settings
						<br />
						<blockquote>
							App Domains:  https://your-domain-name
							<br />
							<br />
							Valid Oauth URIs:
							<br />  
							&emsp;https://your-domain-name/_oauth/facebook
							<br />
							&emsp;https://your-domain-name/app/login
							<br />
							<br />
							Client Oauth Login: Yes
							<br />
							<br />
							Web Oauth Login: Yes
							<br />
							<br />
							Embedded Browser Oauth Login: Yes
						</blockquote>
					</p>
					<br />
					<h3 id="15">9. Side Menu</h3>
					<p class="bold">tapshop/client/templates/main/menu.js</p>
					<p class="bold">tapshop/client/templates/main/menu.html</p>
					<br />
					<h3 id="16">10. Product Listings</h3>
					<p>
						<span class="bold">tapshop/client/templates/shop/shop</span>
						<br />
						- Home page of this app.  Renders all product categories.
					</p>
					<p>
						<span class="bold">tapshop/client/templates/main/listings</span>
						<br />
						- Directive for 'listings' element.
					</p>
					<p>
						<span class="bold">tapshop/client/templates/shop/listings_index</span>
						<br />
						- Controller for listing index under 'Shop' tab.
					</p>
					<p>
						<span class="bold">tapshop/client/templates/shop/my_offers</span>
						<br />
						- Controller for listing index under 'Offers' tab.
						<br />
						- This page contains listings that current user has sent offers to.
					</p>
					<p>
						<span class="bold">tapshop/client/templates/product_page/product_buyer</span>
						<br />
						- Controller for product details page.
					</p>
					<br />
					<h3 id="17">11. Selling</h3>
					<p>
						<span class="bold">tapshop/client/templates/sell/sell</span>
						<br />
						- Controller for listing index under 'Sell' tab.
						<br />
						- This page contains all active posts of current user.
					</p>
					<p>
						<span class="bold">tapshop/client/templates/product_page/product_seller</span>
						<br />
						- Controller for product details page of seller.
					</p>
					<p>
						<span class="bold">tapshop/client/templates/sell/</span>
						<br />
						- Templates and controllers for creating new listing, and editing a current listing.
					</p>
					<br />
					<h3 id="18">12. Chat</h3>
					<p>
						<span class="bold">tapshop/client/templates/messages/chat_list</span>
						<br />
						- List of all users that has an active chat with the current user.
					</p>
					<p>
						<span class="bold">tapshop/client/templates/messages/chat</span>
						<br />
						- Chat and messages controller.
					</p>
					<p>
						<span class="bold">tapshop/client/templates/messages/chat_details</span>
						<br />
						- Controller for product details under 'Details' tab.
					</p>
					<br />
					<h3 id="19">13. User Rating</h3>
					<p>
						<span class="bold">tapshop/client/templates/messages/chat_details</span>
						<br />
						- Rating form loads when user leaves the chat.
						<br />
						- The form is set to load only when there are 4 messages in the chat.  You can change this setting
						in line 109.
					</p>
					<p>
						<span class="bold">tapshop/client/templates/messages/components/feedback_modal.html</span>
					</p>
					<br />
					<h3 id="20">14. User Profile</h3>
					<p>
						<span class="bold">tapshop/client/templates/users</span>
						<br />
						- Templates and controllers for User Profile, My Profile, and Profile Settings.
					</p>
					<br />
					<h3 id="21">15. Search</h3>
					<p>
						<span class="bold">tapshop/client/templates/main/search</span>
					</p>
					<p>
						<span class="bold">tapshop/client/components/search_client.js</span>
						<br />
						- Search settings on client.
					</p>
					<p>
						<span class="bold">tapshop/server/components/search_source.js</span>
						<br />
						- Search settings on Mongodb, and regex functions for basic search.
					</p>
					<br />
					<h3 id="22">15. Activity Feed</h3>
					<p>
						<span class="bold">tapshop/client/templates/main/activity_feed</span>
					</p>
					<hr />
					<h3 id="23">16. AdMob</h3>
					Enable AdMob by uncommenting the following files. Please make sure you have
					your Ad Unit Id to adId in <span class="bold">settings.json</span> file.
					<br />
					<br />
					<p>
						<span class="bold">tapshop/client/components/admob.js</span>
						<br/>
						- To enable actual ads, set <b>isTesting</b> on line 10 to <b>true</b>.
					</p>
					<hr />
					<h3 id="24">17. Push Notifications</h3>
					Enable Push Notifications by uncommenting the following files. Please make sure you have
					your Server Key and Sender ID for FCM (Firebase Cloud Messaging) in <span class="bold">settings.json</span> file.
					<br />
					<br />
					<p>
						<span class="bold">tapshop/mobile-config.js</span>
						<br />
						- Add your SENDER ID on line 14.
					</p>
					<p>
						<span class="bold">tapshop/cordova-build-override/platforms/android/res/drawable/</span>
						<br />
						- Add push notification icon image on this folder.
						<br />
						- File name should be <span class="bold">pushicon.png</span> with px dimensions of 88 x 88.
					</p>
					<hr />
					<h3 id="25">18. Integrate Image Upload with Amazon S3</h3>
					Please make sure you have set your Secret, Key, Bucket, Region, and Domain of your S3 server in <span class="bold">settings.json</span> file.
					<br />
					<br />
					<p>
						<span>For complete reference, check this <a href="https://github.com/VeliovGroup/Meteor-Files/wiki/AWS-S3-Integration">guide on Meteor-Files package with AWS S3</a>.</span>
					</p>
					<p>
						<span>Setup your AWS S3 server by following Step 1 - 4 of this <a href="https://github.com/Lepozepo/S3#create-your-amazon-s3">guide</a>.</span>
					</p>
					<p>
						<span class="bold">tapshop_files/tapshop/lib/images_s3.js</span>
						<br />
						- Uncomment this file.
						<br />
						- Enter your S3 details on <b>settings.json</b> file.
					</p>
					<p>
						<span class="bold">tapshop_files/tapshop/lib/images.js</span>
						<br />
						- Delete or disable this file.
					</p>
					<hr>
					<h3 id="28">19. Native Google Sign-In on Android App.</h3>
					<br />
					<p>
						<b id="debug">Enable Google Sign-In on Debug Mode (localhost)</b>
						<br />
						<br />
						1. Get the <b>SHA1</b> certificate of your Android debug key as seen on this <a href="https://developers.google.com/android/guides/client-auth">guide</a>.
						Enter the commands below on your terminal.
						<br/>
						<br/>
						On Linux or Mac:
							<blockquote>
								keytool -exportcert -list -v -alias androiddebugkey -keystore ~/.android/debug.keystore
							</blockquote>
						<br/>
						On Windows:
						<br/>
						<br/>
							<blockquote>
								keytool -exportcert -list -v -alias androiddebugkey -keystore %USERPROFILE%\.android\debug.keystore
							</blockquote>
						<br/>
						** If you are asked for a password, just enter "android"
						<br/>
						<br/>
						2. Go to <a href="https://console.developers.google.com">Google Developers Console</a>.
						<br/>
						<br/>
						3. Create a new Oauth Credentials for Android app.
						<br/>
						<br/>
						4. Package Name should be exactly the same as the <b>id</b> you set in <b>mobile-config.js</b> file of the app.
						<br/>
						<br/>
						5. Copy-paste the <b>SHA1</b> certificate that you got on Step 1.
						<br/>
						<br/>
						<b>Note:</b> You should have two Oauth Credentials for Android app using the same Package Name. One for Debug Mode, and another one for your live app.
					</p>
					<br />
					<p>
						<b id="prod">Enable Google Sign-In on Deployed App (Production)</b>
						<br />
						<br />
						Get the <b>SHA1</b> certificate of the key you used to sign your apk file by entering the commands below on your terminal.
						<br/>
						<br/>
						<b>Note:</b> If you don't have a key yet, please follow the <a href="#03c">Android App Deployment guide</a>.
						<br/>
						<br/>
						On Linux or Mac:
							<blockquote>
								keytool -exportcert -keystore <span style="color: red;">/your-file-path</span>/.keystore -list -v -alias <span style="color: red;">Your-App-Name</span>
							</blockquote>
						<br/>
						On Windows:
						<br/>
						<br/>
							<blockquote>
								keytool -exportcert -keystore <span style="color: red;">C:\your-file-path</span>\.keystore -list -v -alias <span style="color: red;">Your-App-Name</span>
							</blockquote>
						<br/>
						<br/>
						After getting SHA1 certificate, follow step 2 - 5 of the guide <a href="#debug">above</a>.
					</p>
					<hr>
					<h2 id="26">Other Guides</h2>
					<ul class="list-unstyled">
						<li>
							<a href="http://ionicframework.com/docs/v1/">Ionic</a>
						</li>
						<li>
							<a href="http://guide.meteor.com">Meteor</a>
						</li>
						<li>
							<a href="https://angular-meteor.com/tutorials/socially/angular1/bootstrap">Angular-Meteor</a>
						</li>
						<li>
							<a href="http://ngcordova.com/">ngCordova - Angular wrappers for Cordova.</a>
						</li>
						<li>
							<a href="https://github.com/zodern/meteor-up">Meteor-Up (Mup) - For deployment to server.</a>
						</li>
					</ul>
					<hr>
					<h2 id="27">Changes and Bug Fixes</h2>
					<br />
					<h3 class="bold">18/07/2017</h3>
					<p>
						<span>Updated the app to Meteor 1.5.1</span>
						<br />
						<span>Fixed issue of Google and Facebook sign-in going to a blank screen on latest mobile browsers.</span>
						<br />
						<span>Minor Bug Fixes.</span>
					</p>					
					<h3 class="bold">03/04/2017</h3>
					<p>
						<span>Updated the app to Meteor 1.4.3.2</span>
						<br />
						<span>Changed Google Sign-In on Android to use native sign-in process.</span>
						<br />
						<span>Perfomance Improvements.</span>
						<br />
						<span>Minor Bug Fixes.</span>
						<br />
						<span>Login and Register features no longer uses a third-party package for easy modification.</span>
						<br />
						<span>Push Notificaitons, AdMob, and System Email no longer needs to be enabled manually.</span>
					</p>
					<h3 class="bold">20/10/2016</h3>
					<p>
						<span>Updated the app to Meteor 1.4.1.2</span>
						<br />
						<span>Updated push notifications from Google Cloud Messaging to Firebase Cloud Messsaging.</span>
						<br />
						<span>Added option to use Mailgun for automated emails.</span>
						<br />
					</p>
					<h3 class="bold">27/09/2016</h3>
					<p>
					<span>Fixed issue of users cannot register without geolocation enabled.</span>
					<h3 class="bold">23/09/2016</h3>
					<p>
						<span>Added geolocation coordinates to User profile and Listings database.</span>
						<br />
						<span>Added Seller's location coordinates to Listings.</span>
						<br />
						<span>Added Distance Filter and Sort options to Listings, show distance on each Listing.</span>
						<br />
						<span>Added Distance Filter and Pagination on Search.</span>
						<br />
						<span>Ask user to enable GPS when entering the app.</span>
						<br />
						<span>Added Meteor-Toys tool, to manage Database during development.</span>
					</p>
					<h3 class="bold">15/08/2016</h3>
					<p>
						<span>Fixed error on verifying email using verfication link.</span>
						<br />
						<span>Prevent users from closing User Rating modal without clicking on any modal button.</span>
						<br />
						<span>Fixed bug which allows user to go to a deleted Product Page through Activity Feed.</span>
						<br />
						<span>Fixed bug on "Confirm Sold" button showing on Buyer when switching user account from Seller to Buyer.</span>
						<br />
						<span>Fixed bug on image upload button not working on Edit listing.</span>
						<br />
						<span>Fixed issue on app crashing due to file access permission on Android 6.0+</span>
					</p>
					<h3 class="bold">24/07/2016</h3>
					<p>
						<span>Fixed issue on slower loading speed of Listings on version 18/07/2016.</span>
					</p>
					<h3 class="bold">18/07/2016</h3>
					<p>
						<span>Fixed issue on categories not showing correctly when there are odd number of cards.</span>
						<br />
						<span>Fixed issue on images not showing on Select page when using custom categories.</span>
						<br />
						<span>Fixed issue of GPS not getting Region data on some countries.</span>
						<br />
						<span>Fixed issue on the app not loading after running 'meteor update'.</span>
						<br />
						<span>Fixed issue on image upload not working on Android 4.4.</span>
						<br />
						<span>Auto-resize of profile images for faster uploads.</span>
						<br />
						<span>Changed file upload package so uploaded images will consistently show on Android app.</span>
						<br />
						<span>Changed Test Data function.</span>
					</p>
					<br />
					<hr>
					<h2 id="03">Old Documentation</h2>
					<br />
					<h3>Native Google Sign-In on Android App.</h3>
					<br />					
					<p style="color: red;" class="bold">
						As of version 18/07/2017, the steps below are no longer needed:
					</p>
					<b>Migrating from old TapShop version (20/10/2016 and below.)</b>
					<br/>
					<br/>
					1. Install the native Google Sign-In package, by entering this command on <b>/tapshop</b> folder.
						<br>
						<br>
						<blockquote>
							meteor add hedcet:cordova-google-plus-native-sign-in
						</blockquote>
					<br/>
					<br/>
					2. Replace this file with the latest version of TapShop:
					<br/>
					<br/>
					&nbsp;&nbsp;&nbsp;<span class="bold">tapshop/server/components/user_accounts.js</span>
					<br/>
					<br/>
					<br/>
					3. On the following files, replace the following functions:
					<br/>
					<br/>
					&nbsp;&nbsp;&nbsp;<span class="bold">tapshop/server/components/configure_services.js</span>
					<br/>
					<br/>
					&nbsp;&nbsp;&nbsp;&nbsp; - Change Google configuration as seen below:
					<br/>
					<br/>
					<b>Before</b>
					<br/>
					<br/>
						<blockquote>
							Meteor.settings.google.clientId
						</blockquote>
						<br/>
						<br/>
						<b>After</b>
						<br/>
						<br/>
							<blockquote>
								Meteor.settings.<span style="color: red;">public.</span>google.clientId
							</blockquote>
					<br/>
					<br/>
					&nbsp;&nbsp;&nbsp;<span class="bold">tapshop/client/templates/users/auth/login.js</span>
					<br/>
					<br/>
					&nbsp;&nbsp;&nbsp;&nbsp; - Add <b>$ionicPopup</b> below line 17 of your existing file.
					<br/>
					<br/>
					&nbsp;&nbsp;&nbsp;&nbsp; - Replace <b>this.loginGoogle</b> function with the new version, seen on line 119 of the latest file.
					<br/>
					<br/>
					&nbsp;&nbsp;&nbsp;&nbsp; - Add <b>this.googleMerged</b> function, seen on line 101 of the latest file.
					<br/>
					<br/>
					&nbsp;&nbsp;&nbsp;&nbsp; - Since you are using the older version, remove this from the new <b>this.loginGoogle</b> function:
					<br/>
					<br/>
					<blockquote>
					&emsp;else {<br>
					&emsp;&emsp;return self.register();<br>
					&emsp;}
					</blockquote>
					<br/>
					<br/>
					<br/>
					&nbsp;&nbsp;&nbsp;<span class="bold">tapshop/client/templates/users/auth/register.js</span>
					<br/>
					<br/>
					&nbsp;&nbsp;&nbsp;&nbsp; - Add <b>$ionicPopup</b> below line 17 of your existing file.
					<br/>
					<br/>
					&nbsp;&nbsp;&nbsp;&nbsp; - Replace <b>this.loginGoogle</b> function with the new version, seen on line 199 of the latest file.
					<br/>
					<br/>
					&nbsp;&nbsp;&nbsp;&nbsp; - Add <b>this.googleMerged</b> function, seen on line 181 of the latest file.
					<br/>
					<br/>
					&nbsp;&nbsp;&nbsp;&nbsp; - Since you are using the older version, remove this from the new <b>this.loginGoogle</b> function:
					<br/>
					<br/>
					<blockquote>
					&emsp;else {<br>
					&emsp;&emsp;return self.checkUser();<br>
					&emsp;}
					</blockquote>
					<br/>
					<br/>
					<br/>
					4. On <b>settings.json</b>, move the google clientId to public, as seen below:
					<br/>
					<br/>
					<b>Before:</b>
					<br/>
					<br/>
						<blockquote>
							&emsp;{<br>
							&emsp;&emsp;"public": {<br>
							<br>
							&emsp;&emsp;&emsp; ... <br>
							<br>
							&emsp;&emsp;},<br>
							<br>
							&emsp;&emsp; ... <br>
							<br>
							&emsp;&emsp;"google": { <br>
							&emsp;&emsp;&emsp;<span style="color: red;">"clientId": "xxx",</span><br>
							&emsp;&emsp;&emsp;"secret": "xxx"<br>
							&emsp;&emsp;}, <br>
							<br>
							&emsp;&emsp;...
						</blockquote>
					<br/>
					<b>After:</b>
					<br/>
					<br/>
						<blockquote>
							&emsp;{<br>
							&emsp;&emsp;"public": {<br>
							<br>
							&emsp;&emsp;&emsp; ... <br>
							<br>
							&emsp;&emsp;&emsp;"google": { <br>
							&emsp;&emsp;&emsp;&emsp;<span style="color: red;">"clientId": "xxx"</span><br>
							&emsp;&emsp;&emsp;}<br>
							&emsp;&emsp;},<br>
							<br>
							&emsp;&emsp; ... <br>
							<br>
							&emsp;&emsp;"google": { <br>
							&emsp;&emsp;&emsp;"secret": "xxx"<br>
							&emsp;&emsp;}, <br>
							<br>
							&emsp;&emsp;...
						</blockquote>
					<hr />
					<h3 id="28">Deploy to VPS ( Old - Meteor 1.3 )</h3>
					<p>
						**Note: If you have updated your app to Meteor 1.4, please go to this <a href="#03a">guide on using the new Mup deployment script</a>.
					</p>
						<span class="bold">Step 1</span> - If you don't have a VPS yet, create a new server with Ubuntu or Debian OS.
						<p>
							If you choose to deploy using Digital Ocean, you can get $10 credit as new customer using this <a href="https://m.do.co/c/5d3c927183be">link</a>.
						</p>
						<p>
							<span class="bold">Step 2</span> - Add a deployment user on your server.
							<br />
							<br />
							Follow this <a href="https://www.digitalocean.com/community/tutorials/how-to-create-a-sudo-user-on-ubuntu-quickstart">Guide</a>
							by Digital Ocean on how to create a new user on Ubuntu or Debian server.
						</p>
						<p>
							After creating a new username and password, remove sudo password requirement for the username that you will use for deployment.  This will enable automated installation
							of the app and its requirements without the server asking for sudo password.
							<br />
							<br />
							<span style="font-weight: bold;">Note:</span> This will not remove the password of that username.  The server will still require the password to login.
						</p>
						<p>
							Go to sudoers file:
							<blockquote>
								sudo visudo
							</blockquote>
						</p>
						<p>
							Go to a new line in this file, and enter the following:
							<blockquote>
								Your-Username ALL=(ALL) NOPASSWD: ALL
							</blockquote>
						</p>
						<p>
							Press ctrl + X to exit, and save changes.
						</p>
					</p>
					<p>
						<span class="bold">Step 3</span> - On your computer, install Mupx then enter your server details
						on the <span class="bold">mup.json</span> file.
						<br />
						Visit this <a href="https://github.com/arunoda/meteor-up/tree/mupx#installation">link</a> for more details on Mupx.
						<p>
							Install the Mupx package from npm with this command:
							<blockquote>
								npm install -g mupx
							</blockquote>
						</p>
						<p>
							Create a new folder to run your deployment.  Make sure this is separate from the 'tapshop' folder.
							<blockquote>
								mkdir ~/your-folder-name
							</blockquote>
						</p>
						<p>
							Go to your new folder.  And inside the folder, run this command:
							<blockquote>
								mupx init
							</blockquote>
						</p>
						<p>
							You will then find the <span class="bold">mup.json</span> file inside the folder.  Enter your app and server
							details on this file.
						</p>
						<blockquote>
							host - Your server IP address, or full domain name.<br /><br />
							username - Your server username. (Recommended to create another username for this.)<br /><br />
							password -  Password of username you used.<br /><br />
							pem - If you use SSH key to login, enter file location here. If not, comment this part.<br /><br />
							setupMongo - Set it to true, if you want to install MongoDB on the same server.<br /><br />
							appName - Your app name.<br /><br />
							app - File location of your tapshop folder.<br /><br />
							PORT - default is 80.<br /><br />
							ROOT_URL - Your full domain name.<br /><br />
						</blockquote>
					</p>
					<p>
						<span class="bold">Step 3a (Optional)</span> - Add your SSL Certificate to your Web App for geolocation features to work on Chrome browser.
					</p>
					Place your SSL certificate files inside your deployment folder, and add settings shown in this <a href="https://github.com/arunoda/meteor-up/tree/mupx#ssl-support">link</a> to your <span class="bold">mup.json</span> file.
					<br />
					<br />
					If you have added an SSL Certificate, go to your tapshop folder, and run this command to redirect all traffic to your HTTPS site:
					<br />
					<br />
					<blockquote>
						meteor add force-ssl
					</blockquote>
					<br />
					<p>
						<span class="bold">Step 4</span> - Copy your <span class="bold">settings.json</span> file to your deployment folder.
					</p>
					<p>
						<span class="bold">Step 5</span> - Run Mupx deploy with the <span class="bold">settings.json</span> file.
						<br />
						<br />
						If this is your first deployment, run this command first to install all requirements on the server:
						<blockquote>
							mupx setup
						</blockquote>
						<br />
						Then deploy the app with this command:
						<blockquote>
							mupx deploy --settings=settings.json
						</blockquote>
					</p>
					<p>
						<span class="bold">Step 6</span> - On the browser, go to domain name, or ip address of your server to see if the app is working.
					</p>
					<p>
						<span class="bold">Note:</span> If the app is running with <a href="#04">Test Data</a>,
						loading it for the first time will be slow as images will be inserted to the sample Listings on startup.
					</p>
					<hr />
					<h3>AdMob</h3>
					<p style="color: red;" class="bold">
						As of 03/04/2017, the steps below are no longer needed:
					</p>
					<p>
						<span class="bold">tapshop/client/templates/shop/shop.js</span>
						<br />
						- Remove line 100, 106, 109, and 118.
					</p>
					<p>
						<span class="bold">tapshop/client/templates/shop/listings_index.js</span>
						<br />
						- Uncomment line 371, 378, 384 and 390.
					</p>
					<p>
						<span class="bold">tapshop/client/templates/shop/my_offers.js</span>
						<br />
						- Uncomment line 194, 200, 203, and 212.
					</p>
					<p>
						<span class="bold">tapshop/client/templates/sell/sell.js</span>
						<br />
						- Uncomment line 154, 161, 164 and 173.
					</p>
					<hr />
					<h3>Push Notifications</h3>
					<p style="color: red;" class="bold">
						As of 03/04/2017, the steps below are no longer needed:
					</p>
					<p>
						<span class="bold">tapshop/client/lib/push_notifications_client.js</span>
					</p>
					<p>
						<span class="bold">tapshop/server/components/push_notifications_server.js</span>
					</p>
					<p>
						<span class="bold">tapshop/server/methods/messages_server.js</span>
						<br />
						- Uncomment line 96.
					</p>
					<p>
						<span class="bold">tapshop/lib/methods/messages.js</span>
						<br />
						- Uncomment line 58.
					</p>					
				</div>
			</div>
		</div>
	</body>
</html>
 
