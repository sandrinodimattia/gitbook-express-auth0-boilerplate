# GitBook - Auth0 boilerplate

This boilerplate will allow you to setup kickass internal documentation in no time. The book will be built and hosted in a small Express application which uses `passport-auth0` for authentication.

Demo: http://gitbook-boilerplate-demo.herokuapp.com/

More info: http://sandrinodimattia.net/better-internal-documentation-with-gitbook-express-and-auth0/

## Configuration

 1. Create an [Auth0](https://auth0.com) account
 2. Create a new application in Auth0
 3. Set the **Allowed Callback URLs** to http://localhost:4001/login/callback (or change this to your actual domain)
 4. Update the settings in the **config.json** file (or use environment variables)
 5. Update the title/links/... of your book in **content/book.json**

### Settings

 - `SESSION_SECRET`: The secret used to protect your session, please change this to something else.
 - `AUTH0_DOMAIN`: Your Auth0 Domain
 - `AUTH0_CONNECTION`: The connection to use by default (optional). Not setting this will show the Auth0 login page and allow you to choose a connection.
 - `AUTH0_CLIENT_ID`: Your Auth0 Client ID
 - `AUTH0_CLIENT_SECRET`: Your Auth0 Client Secret

## Usage

 - `npm run serve:book`: Host the book without authentication (useful for when you're writing content)
 - `npm run serve:dev`: Host the book with authentication
 - `npm run serve:prod`: Host the book with authentication (production)

## Deployment

When you deploy this application and run `npm install` it will also automatically build the book. This means you'll only need to execute the following after deploying your code somewhere (eg: Heroku, Azure Web Apps, ...):

```
npm install
npm run serve:prod
```
