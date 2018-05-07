## Run demo

```shell
# start wihh fresh data
cp db.json.dist db.json

# in one console - start JSON mock server
npm run rest-server

# in another console - start client
npm run dev

# ----
# if you want develop against GraphQL server before switching to Bridge
# (see below)
# run in another termina window:
npm run graphql-server
```

## Develop as with GraphQL server

When you are developing on the client side (and especially with React Native), it's handy just to talk to GraphQL server with standard HTTP link and then switch to Bridge Link and keep all your work done.

This example contains demostrate, how to do this with sharing all the code (and only minor configuration of apollo link).

Basically in the `App.js` comment or uncomment which link you want to use.

If you choose **Bridge**, run only `npm run rest-server`.

If you choose **HttpLink**, run (in two opened teerminals `npm run rest-server` and in the second one `npm run graphql-server`).

Basically - your app will talk to GraphQL server (that uses all your resolvers, dataloaders etc.) and this server will talk to REST API server.
