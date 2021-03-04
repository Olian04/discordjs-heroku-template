# discordjs-heroku-template

Step 1: Create discord developer account
Step 2: Create application
Step 3: Setup env
Step 4: Invite bot

## Env

```ts
/**
 * The secret token provided by discord for accessing the bot api.
 * @see https://discord.com/developers/applications
 */
DISCORD_TOKEN: string;

/**
 * The deployment enviorment is either "development" or "production".
 * This controls log levels, debug features, as well as the database instance that will be used.
 */
DEPLOY_ENVIRONMENT: "development" | "production";
```

## Invite bot

<https://discord.com/oauth2/authorize?client_id=<YOUR_CLIENT_ID>&scope=bot>
