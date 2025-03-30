# Privilege Escalation

The example demonstrates a privilege escalation vulnerability and how to exploit it.

## Steps to reproduce

1. Install all dependencies

   `$ npm install`

2. Start the **insecure.ts** server

   `$ npx ts-node insecure.ts`

3. In the browser, send a GET request

   ```
       http://localhost:3000/send-form
   ```

4. Try different UserIds and see which one gives you authorized access to change the role of that user.

## For you to do

Answer the following:

1. Briefly explain the potential vulnerabilities in **insecure.ts**

   The insecure code makes no attempt to check the
   priviledge of the user in the current user session.

2. Briefly explain how a malicious attacker can exploit them.

   A malicious attacker could change the role of the user
   without any kind of authentication. So change an admin to a user.

3. Briefly explain the defensive techniques used in **secure.ts** to prevent the privilege escalation vulnerability?

   secure.ts has authentification to check if the user in the session has priviledges or not.
