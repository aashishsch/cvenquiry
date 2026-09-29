CV WEBSITE WITH ENQUIRY FORM (n8n demo)

FILES
index.html  The whole page (HTML, CSS and JavaScript in one file).
profile.jpg The round headshot shown at the top. Keep it in the same folder as index.html.

WHERE TO PASTE THE WEBHOOK URL
Open index.html in Notepad or VS Code. Near the bottom, in the script, find this line:
  const WEBHOOK_URL = "PASTE_YOUR_N8N_WEBHOOK_URL_HERE";
Replace the text between the quotes with your n8n webhook URL.
Test URL (contains /webhook-test/) works only while "Listen for test event" is on in n8n.
Production URL (contains /webhook/) works after the workflow is published.

IPINFO.IO (LOCATION AND COUNTRY FLAG)
When the form opens, the page calls the ipinfo.io API (https://ipinfo.io/json) to find the visitor's city and country, then shows the flag and country code.
Optional: sign up free at ipinfo.io and put your token in the line const IPINFO_TOKEN = "..." for higher limits.
If ipinfo.io is blocked or offline, the form quietly defaults to India (+91).

HOW TO TEST LOCALLY
1. Double-click index.html to open it in your browser.
2. Press F12 and open the Console tab.
3. Click "Connect with me", fill the form and click Submit.
4. The Console shows the JSON object that is sent to n8n. Check the execution in n8n.

MAKE IT YOURS
Name, title and credentials: edit the text inside the header block near the top of the body.
Photo: replace profile.jpg with your own photo (square works best) using the same file name.
Text: edit the Profile, Core Competencies, Automation Toolkit, Experience and Engagements sections. Each chip is one line like: span class="chip" with your skill inside.
Colours: change the values at the top of the style block (--accent and --accent2).

HOSTING
Upload both files to a GitHub repository and turn on GitHub Pages in the repository settings.
