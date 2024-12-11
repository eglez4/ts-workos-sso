# TypeScript Example App with SSO powered by WorkOS

An example application demonstrating to use the [WorkOS Node SDK](https://github.com/workos-inc/workos-node) to authenticate users via SSO. 

## Prerequisites

Node.js version 10+

## Node Project Setup

1. Clone the main repo and install dependencies for the app you'd like to use:
    ```bash
    # HTTPS
    git clone https://github.com/workos/typescript-example-applications.git
    ```
    or

    ```bash
    # SSH
    git clone git@github.com:workos/typescript-example-applications.git
    ```

2. Install the dependencies. 
    ```bash
    $ npm install
    ```

## Configure your environment

3. Grab your API Key and Client ID from the WorkOS Dashboard. Create a `.env`
file at the root of the project, and store these like so:
    ```
    WORKOS_API_KEY=sk_xxxxxxxxxxxxx
    WORKOS_CLIENT_ID=project_xxxxxxxxxxxx
    WORKOS_ORG_ID='org_xxxxxxxx'
    WORKOS_DIRECTORY_ID='directory_xxxxxxxx'
    ```

## SSO Setup with WorkOS

4. Follow the [SSO authentication flow instructions](https://workos.com/docs/sso/guide/introduction) to create a new SSO connection in your WorkOS dashboard.

NOTE: Make sure to create Okta Developer account and that SAML is configured. More info on this [here](https://workos.com/docs/integrations/okta-saml).

5. Add `http://localhost:8000/callback` as a Redirect URI in the Configuration section of the Dashboard.

6. Update `.env` with the Organization ID.

## Directory Setup with WorkOS

7. Follow the [Directory Sync flow instructions](https://workos.com/docs/directory-sync/quick-start/2-add-directory-sync-to-your-app) to add Directory Sync to your existing organization

NOTE: Make sure to create Okta Developer account and that SCIM is configured. More info on this [here](https://workos.com/docs/integrations/okta-scim).

8. Update `.env` with the Directory ID.

## Run the development server

```sh
npm run dev
```

## Compile TypeScript code and run the server

```sh
npm run build
npm start
```

Head to `http://localhost:8000/` to begin the login flow!


## Need help?

If you get stuck and aren't able to resolve the issue by reading our [WorkOS Node SDK documentation](https://docs.workos.com/sdk/node), API reference, or tutorials, you can reach out to us at support@workos.com and we'll lend a hand.