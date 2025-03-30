# Repudiation

The example demonstrates a vulnerability that can lead to repudiation by malicious users attempting to access the services provided by a server.

## Steps to reproduce

1. Install all dependencies

   `$ npm install`

2. Run the server **insecure.ts**.

3. Pretend to be a malicous user and interact with the services by sending requests from the browser.

4. Do you think your actions can be repudiated?

## For you to do

1. Briefly explain the vulnerability.

   The vulnerability is that there is no data logging so
   there will be no record if a malicious user exploits
   aspects of the system.

2. Briefly explain why the vulnerability is addressed in **secure.ts**.

   The vulnerability is addressed by having logging so the
   date as well as requests are logged, meaning that the security
   breach can be tracked.

3. Which design pattern is used in the secure version to address the vulnerability? Briefly explain how it works?

   The middleware design pattern is being used to perform the logging operation.
