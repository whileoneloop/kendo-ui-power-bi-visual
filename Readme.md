# How to make use of Kendo UI components within the PowerBI sandbox

This repo uses the trial version of Kendo UI v2017.2.621 , which may be downloaded from:

    https://www.telerik.com/download-trial-file/v2/kendo-ui .

#### Please note: the Telerik Kendoui component is throwing the following exception when contained within the PowerBI 'visualsandbox':

    Uncaught TypeError: Illegal invocation
        at <anonymous>:562:21817
        at <anonymous>:562:27218
        at <anonymous>:563:18554
        at <anonymous>:563:18651
        at t.kendo.t.kendo.cultures (<anonymous>:562:21)
        at Window.<anonymous> (<anonymous>:562:59)
        at <anonymous>:841:20
        at Object.r [as injectJsCode] (visualhostcore.min.js:2)
        at i.loadWithoutResourcePackage (visualsandbox.min.js:1)
        at i.executeMessage (visualsandbox.min.js:1)

#### How to reproduce:

Start a PowerBI pro free trial if not already done:

    https://app.powerbi.com/signupredirect?pbi_source=web

Install PowerBI tools from:

https://github.com/microsoft/powerbi-visuals-tools

In this repo, install npm dependencies (jquery and its types) with:

    npm install

And then run a dev instance for PowerBI to connect to and display the visual:

    pbiviz start

... Or create and upload a package manually in your Powerbi interface with:

    pbiviz package

Login to PowerBI, enable developer custom visuals, create a new report, drag on a developer/custom visual widget.  View the console output in the browser window displaying your developer visual, the "Illegal invocation" exception should be present.

#### Other resources:

    https://github.com/microsoft/powerbi-visuals-tools
    https://github.com/Microsoft/PowerBI-visuals
    https://github.com/Microsoft/PowerBI-visuals-sampleUsingExternalLibraries