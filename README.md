Ghost Inspector Extension for Visual Studio Team Services
-------------
With this plugin you can add a build step to your VSTS project that executes a Ghost Inspector test suite. If the test suite is successful, your pipeline will continue to the next step in your pipeline; however, if it fails (or times out), the build will be marked as failed.

## Installation
This plugin can be installed from within the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=ghost-inspector.ghost-inspector-vsts-extension).

## Prerequisites
* **API Key** - This is a unique, private key provided with your account which allows you to access the API. You can find it in your Ghost Inspector account settings at https://app.ghostinspector.com/account.
* **Suite ID** - The ID of the Ghost Inpsector suite that you would like to execute.
 
## Usage
1. Install the extension from [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=ghost-inspector.ghost-inspector-vsts-extension).
1. Open your project within VSTS and navigate to **Builds**. 
2. In the **Tasks** section, click the ```+``` icon to add a new task.
3. To find the extension in the list quickly, type `Ghost` and select **Add**.
4. Click on the new task and fill in the required fields for **Suite ID** and **API Key**.
4. If you would like to run your Ghost Inspector tests on a URL other than their default setting (such as a local build instance of your application using a tunnel), enter the start URL in the ```Start URL``` field.
5. If you would like to pass other custom parameters or variables to your suite run, specify them in the ```Additional Parameters``` field.
6. Save and queue your project.

# Development
The extension is written in TypeScript. Between changes, you can simply run the tests with:

```
./bin/test.sh
```

## Support
Please report any issues [on Github](https://github.com/ghost-inspector/ghost-inspector-vsts-extension/issues) or [through support](https://ghostinspector.com/support/).

## Change Log
2018-Feb-021: Initial release