# Invoice Studio

A responsive invoice web app with business/client details, line items, discounts, tax, multiple currencies, browser-local invoice storage, and print/PDF export.

## Run

Requires Node.js 20 or later. No dependencies or installation needed.

```sh
npm start
```

The server defaults to port 3000; set `PORT` to override it. Use Print / PDF to save a document using your browser's print dialog.

Invoices are stored only in this browser's localStorage. There is no backend database, account system, synchronization, or payment processing. Keep exported copies of important invoices. Dashboard totals use the currently selected currency and do not convert currencies.

## Publish on Render

1. Push this project to your GitHub repository.
2. Sign in at https://dashboard.render.com/ and select **New → Blueprint**.
3. Connect the repository and deploy the `render.yaml` configuration.
4. When deployment completes, open the public URL shown by Render.

Alternatively, create a Node web service with build command `node --check server.js && node --check app.js` and start command `npm start`. The application uses Render's injected `PORT`.

Browser storage is specific to the deployed URL and browser. Invoices created on another address or device will not appear automatically. This version has no accounts or cloud invoice backup.
