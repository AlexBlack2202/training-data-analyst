# training-data-analyst
Labs and demos for courses for GCP Training (http://cloud.google.com/training).

Task 3. Build and deploy the backend component

Navigate to the folder containing the code required to build and deploy the backend.

cd ../../../../backend

Copied!

Create the .env file. As mentioned earlier, this file contains project specific infromation so that the application's backend component can communicate with the Cloud Spanner instance.

In the cloud shell enter the following command to invoke the Nano text editor and create a new .env file.

nano .env

Copied!

Paste the code block listed below.

PROJECTID = qwiklabs-xxxx

INSTANCE = alexblack-instance

DATABASE = alexblack-db

JWT_KEY = xxx ( replace by jwt key)

EXPIRE_IN = 30d

Copied!

Press Ctrl+X to exit Nano, Y to confirm the update, and press Enter to save your changes.

Before you proceed further you must install updated components for npm so that the backend can be properly compiled. npm is a package manager for JavaScript. npm is the default package manager for the JavaScript runtime environment Node.js.

nvm install node

Copied!

npm install npm -g

npm install --loglevel=error

Copied!

Next build the backend application using a reference dockerfile that exists in the repository folder.

docker build -t gcr.io/qwiklabs-gcp-04-790ef0394039/omega-trade/backend:v1 -f dockerfile.prod .

Copied!

Note: You may safely ignore any npm notice... messages that appear during the build process
