# How to set webhook system

Webhooks let your server send logs and updates to external services like Discord. For multimedia (images, videos, audio), use an external uploader service due to API and permission constraints on FiveM and Discord.

## External uploader integration (multimedia)
If you need to send images or videos along with your logs, integrate with a trusted external uploader service. This approach enables secure and efficient media uploads and links, and works seamlessly with Banshy Store assets.

Typical steps:
1. Create an account on your chosen uploader service.
2. Generate an API token on their platform.
3. Add the token to your asset configuration (for example, `Config.Webhook` or a dedicated `uploader.token` field depending on the script).
4. Use the provided endpoint from the service to upload media and include the returned URL in your webhook payloads.

> Note: Do not hardcode tokens in public repositories. Use environment variables or a secure secrets store.

## Discord webhooks (logs only)
Discord webhooks are ideal for sending text-based logs such as:
- Server events
- Player joins, bans, purchases, or other activities
- System updates and notifications for specific assets

Discord webhooks no longer support hosting images, videos, or audio files directly. For media, use an external uploader and include the media URL in your Discord webhook payload.

### Create a Discord webhook
1. In your Discord server, right-click the target channel > Edit Channel > Integrations > Webhooks.
2. Create a new webhook and copy the webhook URL.
3. Store this URL in your server configuration (for example, `Config.WebhookUrl`).

### Example JSON payload
Send a POST request with a JSON body like the following:

```json
{
  "username": "Banshy Logger",
  "avatar_url": "https://example.com/logo.png",
  "content": "Server started successfully.",
  "embeds": [
    {
      "title": "Player Purchase",
      "description": "Player JohnDoe purchased item: Deluxe Burger",
      "color": 5814783,
      "fields": [
        { "name": "Player ID", "value": "123", "inline": true },
        { "name": "Price", "value": "$25", "inline": true }
      ],
      "image": { "url": "https://media-uploader.example.com/uploads/abc123.jpg" },
      "timestamp": "2024-01-01T12:00:00Z"
    }
  ]
}
```

### curl example
```bash
curl -H "Content-Type: application/json" -X POST \
  -d @payload.json \
  "https://discord.com/api/webhooks/WEBHOOK_ID/WEBHOOK_TOKEN"
```

## Configuration tips
- Keep tokens and webhook URLs out of your repo. Use environment variables or a server-side secrets file.
- Rate-limit your webhook sends to avoid hitting provider limits.
- Implement retries with backoff for transient failures (HTTP 429/5xx).
- Log failures locally for troubleshooting.

## Media
- Video: [Placeholder – creating a Discord webhook, sending a test payload]
- Screenshots: [Placeholder – Discord Integrations screen, example payload JSON]


