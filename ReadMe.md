## Connecting Databricks Model Registry Webhooks to Azure Function

The guide shows how you can use Azure Function as an intermediate service to enable Databricks Model Registry to talk to CI/CD of your choice.

1. Clone this repo and deploy to Azure Function. You can Read [this tutorial](https://docs.microsoft.com/en-us/azure/azure-functions/create-first-function-vs-code-csharp?tabs=in-process) to get started with Azure Function.
2. Modify the code in `HttpExample/__init__py` to specify the trigger API call for the CI/CD of your choice.
3. Configure a webhook in databricks to trigger the HTTP URL of your function app. Please make sure that you append your function name at the end of the URL (`HttpExample` for this repo). The complete URL will look something like this: `https://{FUNCTION_APP_NAME}.net/api/HttpExample`
4. [optional] Add authentication to your Azure Function. You can follow [this guide](https://docs.microsoft.com/en-us/azure/app-service/configure-authentication-provider-aad#-configure-with-express-settings) to configure authentical for Azure Function.   
