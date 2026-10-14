Set up gmail-mcp, a local Gmail MCP server for Claude Code, on this computer. Do as much as you can yourself and ask me only for the things you cannot do.

<context>
gmail-mcp is a private MCP server that runs on my machine and lets Claude Code search, read, write, file and change settings in several Gmail accounts. It uses my own Google Cloud OAuth client; nothing is hosted. Every change waits for my approval in Claude Code's prompt. I received the gmail-mcp folder from its author; it is not downloaded from anywhere. The folder's README and its Google Cloud setup guide describe everything; read them first and follow them. Where they and this prompt disagree, the folder wins.

What gmail-mcp needs:
- Claude Code.
- Node.js 26 or later.
- My own Google Cloud project with a Desktop OAuth client (free). I create it in my browser, following the folder's guide.
- A system keyring for refresh tokens, or the file mode the README describes on systems without one.
</context>

<steps>
1. Ask me where the gmail-mcp folder is. Confirm it contains the server, the skill and the Google Cloud setup guide.
2. Check Node.js and whether a keyring is available. Tell me which token store will be used.
3. Install dependencies and run the project's checks. Stop if tests fail.
4. Walk me through the Google Cloud guide one step at a time. I do the clicks. When I have downloaded the client file, tell me where to put it and set its permissions as the README says. Do not open or print the client file.
5. Register the server with Claude Code at user scope and install the skill, as the README describes. Show me each command before you run it.
6. After I reconnect the server, ask me which Gmail account to log in first. Start the login and give me the link; I open it in the browser profile that is signed in to that account. Then check the login status.
7. Ask me what the account is for and save that purpose (this needs my approval in the prompt).
8. Test: search that account for mail from the last day and show me only the count. Then draft one short email to that same account and send it only after I approve it in the prompt.
9. Report what you installed, which account is logged in with what purpose, and the test results.
</steps>

<rules>
- Never read, print or copy the OAuth client file or any token.
- Never send, delete or change anything except the one test email I approve.
- Never set the auto-approve option.
- If a step fails twice, stop and tell me what you saw instead of trying other routes.
</rules>
