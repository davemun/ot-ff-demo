# Demo app for Firefox Screensharing Extension v2

## View the OpenTok screensharing repo
You can view the documentation and code here: [OpenTok Screensharing](https://github.com/opentok/screensharing-extensions)

## View the sample deployment
Navigate to the [live deployment](https://ot-ff-demo.herokapp.com).

## How to develop and start this locally
`npm install`

`npm start`
This builds a Firefox extension in the [build-extension](./build-extension) folder.

## Configure this sample repo for your own application
Edit `gDomains` in [index.js](./build-extension/index.js#L4) to contain your application URL.

Edit `id` in [package.json](./build-extension/package.json#L2) to be a unique string - this will be used to identify your own extension that you will use in your deployment.

`npm run build` to build the extension.

Publish the resulting `xpi` file (which is output into [build-extension](./build-extension)) to the [Firefox submissions page](https://addons.mozilla.org/en-US/developers/addon/submit/) to be signed and be universally accessible to your users.

In the install parameters of [index.ejs](./views/index.ejs#L11-12), edit the `href` and `hash` properties to contain the link and hash to your newly published extension.
