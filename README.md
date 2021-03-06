# discordjs-heroku-template

## Setup Development Environment

1. Setup Discord Dev Application
   1. Create a Discord Account if you dont have one.
   2. Create a new Discord Application
      1. <https://discord.com/developers/applications>
   3. Setup Environment Variables in your local repository
      1. Copy `.env.template` and name the copy just `.env`
      2. Open `.env` and fill in the DISCORD_TOKEN of your Discord Dev Application (can be found in the discord developer portal)
   3. Create a discord server for testing your bot during development
   4. Invite bot the bot to the test server
2. Install dependencies by calling `npm install` in your terminal
3. Start bot by caling `npm start`
4. Test the bot in your test server by writing `!ping`, the bot should respond with `!pong`.

## Setup Production Environment

1. Setup Discord Prod Application
   1. Create a Discord Account if you dont have one.
   2. Create a new Discord Application
      1. <https://discord.com/developers/applications>
2. Setup Heroku
   1. Create Heroku account
   2. Connect your github account to your heroku account
   3. Create a new Heroku App
   4. Select "Github" as the deployment method
   5. Connect your Heroku App to your Github repo
   6. Enable Automatic Deploys
   7. Setup Environment Variables
      1. Go to the Settings tab
      2. Click "reveal config vars"
      3. Add the key DISCORD_TOKEN with the value being the Token for the Production Application.
         1. The token can be found in the discord developer portal.
      5. Add the kay DEPLOY_ENVIRONMENT with the value `"production"`
   8. Setup worker dyno
      1. Go to the Overview tab
      2. Click "Configure Dynos"
      3. Enable "worker" dyno
      4. Disable "web" dyno
3. Commit your code and any changes to github
4. Your bot is now live and can be invited to any server

## Env

```ts
/**
 * The secret token provided by discord for accessing the bot api.
 * @see https://discord.com/developers/applications
 */
DISCORD_TOKEN: string;

/**
 * The deployment environment is either "development" or "production".
 * This can be used to control log levels, debug features, as well as the database instance that will be used.
 */
DEPLOY_ENVIRONMENT: "development" | "production";
```

## Invite bot

`https://discord.com/oauth2/authorize?client_id=<APPLICATION_CLIENT_ID>&scope=bot`
