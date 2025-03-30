# Spoofing

This example demonstrates spoofind through two ways -- Stealing cookies programmatically and cross site request forgery (CSRF).

## Steps to reproduce the vulnerability

1. Install dependencies

   `$ npx install`

2. Start the **insecure.ts** server

   `npx ts-node insecure.ts`

3. Start the malicious server **mal.ts**

   `npx ts-node mal.ts`

4. Open **http://localhost:8000** in a browser, type a name and Submit.

5. Open the **Application** tab in the Browser's inspect pane. Find the **Cookies** under **Storage**. You should see a **connect.sid** cookie being set.

6. Open the HTML file **mal-steal-cookie.html** file in the same browser (different tab). Open inspect and view the console.

7. Click the link in the HTML file. Do you see the cookie being stolen in the console?

8. Open the HTML file **mal-csrf.html** file in the same browser (different tab). What do you see if the user has not logged out of **insecure.ts**? What do you see if the user has logged out?

## For you to answer

1. Briefly explain the spoofing vulnerability in **insecure.ts**.

   The session cookie is configured insecurely. on line 26 of insecure the "secret" is just hard coded.

2. Briefly explain different ways in which vulnerability can be exploited.

   The vulnerability can be exploited by the hacker taking the cookie and impersonating the session thus impersonating the user. They could also gain access to the admin account and get sensative information.

3. Briefly explain why **secure.ts** does not have the spoofing vulnerability in **insecure.ts**.

   The "secret" is not hardcoded, everytime the server is started the secret is changed making it more secure everytime we want to use the site.
