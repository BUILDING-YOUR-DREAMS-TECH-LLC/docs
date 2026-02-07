---
title: "Web Chat Widget (Embed)"
---

## Objective

Install the chat widget on your website to start conversations with agents.

## Requirements

- An agent with Web Chat channel enabled.
- Access to the HTML of your site.

## Step by step (embed)

1. Get your tenantId and agentId.
2. Insert the snippet before </body> on your site:

```html
<script>
  (function() {
    window.HeliosChat = {
      tenantId: 'YOUR_TENANT_ID',
      agentId: 'YOUR_AGENT_ID',
      apiUrl: 'https://app.heliosvisionai.com'
    };
    var script = document.createElement('script');
    script.src = 'https://app.heliosvisionai.com/widget/helios-chat.js';
    script.async = true;
    document.body.appendChild(script);
  })();
</script>
```

3. Save changes and reload the site.

## Notes

- The agent must have Web Chat enabled in Agents.
- If you change the agentId, new conversations will use the new agent.

## Suggested illustrations

### Embed Snippet
![Embed Snippet](../../images/helios/en/web-chat/web-chat-embed-snippet.png)