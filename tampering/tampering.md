# Tampering

This example demonstrates tampering through script injection.

## Steps to reproduce

1. Install all dependencies

   `npm install`

2. Start the **insecure.ts** server

   `npx ts-node insecure.ts`

3. In the browser, type a potentially malicious script in the name field of the form

   ```
       <script> document.body.innerHTML = "<a href='https://google.com'> Gotcha </a>"</script>
   ```

4. Do you see the potentially malicious hyperlink being injected into the form?

## For you to do

Answer the following:

1. Briefly explain the potential vulnerabilities in **insecure.ts**

   The vulnerability in insecure is that there is not name sanitization,
   so script code can just be injected directly into the code.

2. Briefly explain how a malicious attacker can exploit them.

   They can exploit this by injecting code into the server and getting access
   to things they shouldn't have access to tamper with.

3. Briefly explain why **secure.ts** does not have the same vulnerabilties?

   secure does not have the same vulnerability because it sanitizes it's data.
   So code cannot be injected.
