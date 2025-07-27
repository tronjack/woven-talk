# WovenTalk - WebRTC SIP Client

A browser-based SIP phone for voice/video calls using WebRTC.
Built with SIP.js. Includes demo contact list and chat UI.

By Jordan Oamelda

Deployment Instructions
To deploy WovenTalk and start using it as a WebRTC SIP softphone, follow these steps:

1. Prepare a Secure Web Server
WovenTalk requires HTTPS to work correctly in modern browsers due to WebRTC security policies.

You can use any web server that supports HTTPS, such as:

Apache or Nginx with SSL certificates (Let’s Encrypt is free)

Static site hosting platforms with HTTPS support (e.g., GitHub Pages, Netlify, Vercel)

2. Upload Project Files
Upload the index.html file to your web server’s public directory.

Ensure it is accessible via an HTTPS URL.

3. Configure Your SIP Server
Your SIP server must support WebSocket Secure (WSS) on port 7443 or the port your SIP provider specifies.

Make sure your SIP credentials (username, password, domain) are valid and allow WebSocket connections.

The SIP URI entered in the app must follow the format:
sip:<extension>@<your_sip_domain>

4. Access the Application
Open a modern browser (Chrome, Firefox, Edge) and navigate to the URL where you hosted index.html.

You should see the WovenTalk interface.

5. Enter Your SIP Credentials
Fill in the following fields:

SIP URI: Your full SIP URI, e.g., sip:8000@domain.com

Username: Your SIP username (often the extension number)

Password: Your SIP password

Destination: The SIP address you want to call, e.g., 9001@domain.com

6. Make a Call
Click Call to register and start the call.

Click Hang Up to terminate the session.

Notes
Make sure your network and SIP provider allow SIP over WSS.

For NAT traversal, STUN servers are preconfigured, but TURN may be needed in restrictive networks.

If calls fail, check browser console logs for errors and verify SIP server compatibility.


