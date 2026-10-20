# OpenPolimi

Search course notes, transcripts, slides and assignments through an MCP connection.
Read [course availability](COURSES.md) for supported years, professors and the latest searchable lessons.

**Server:** `https://kb.openpolimi.ai/mcp`

## Get a token

1. Open [openpolimi.ai](https://openpolimi.ai).
2. Enter your `@mail.polimi.it` email address and select **Continue**.
3. Enter the emailed code in the six boxes, or paste the full code, then select **Confirm code**.
4. Select **Copy token** and save it.

The code expires after 10 minutes. Your token is shown once and has no expiration.
Keep it private. If you lose it, repeat these steps to get a new one.
Contact the maintainer to revoke a token; creating a new one does not revoke old ones.
Use this token when connecting your assistant, not an OpenAI API key.

## Claude

1. Open **Customize → Connectors → Add → Add custom connector**.
2. Name it **OpenPolimi** and enter the server URL above.
3. Select **No sign in** for OAuth. In **Request headers**, add:
   - Name: `Authorization`
   - Value: `Bearer YOUR_OPENPOLIMI_TOKEN`
4. Add the connector and enable it in the conversation.

“No sign in” disables the OAuth flow; the request header still authenticates you.
Team workspaces may require an owner to add the connector.
[Claude instructions](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp).

## ChatGPT

**The direct ChatGPT connection is not ready yet.**
This server currently accepts bearer tokens. ChatGPT's authenticated custom
MCP connection requires OAuth, which has not been configured for OpenPolimi.
Do not select anonymous access: the server will return 401.

Once OAuth is available, add a custom MCP server using the URL above, sign in,
and select OpenPolimi in a new conversation.
[ChatGPT connection guide](https://developers.openai.com/plugins/deploy/connect-chatgpt)
and [authentication requirements](https://developers.openai.com/plugins/build/auth).

## Try it

> In Software Engineering 2, year 2026-27, what did Di Nitto say about RASD qualities? Use the course notes and transcripts and cite the lesson and timestamp.

Specify the course, academic year and professor when relevant.
Answers depend on the material listed in [COURSES.md](COURSES.md).

## Updates

`COURSES.md` is generated after document synchronization from the deployed files
and index. Only availability metadata is published here. Notes, transcripts,
videos, credentials and the search database are not stored in this repository.
