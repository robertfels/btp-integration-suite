<!-- loiob583b7a62f3c4cfdb50a499250c25c15 -->

# Updating the Connection Request Credentials for an Approved Request

There can be instances where you have to update the credentials once the connection request is approved by the API business hub enterprise admin.



<a name="loiob583b7a62f3c4cfdb50a499250c25c15__prereq_unb_5nc_tpb"/>

## Prerequisites

To update the API portal access credentials, you must first generate it. To generate the credentials from the API Portal, you must have the *APIPortal. Administrator* role assigned to you.

1.  Log in to the Integration Suite.

2.  Choose the navigation icon on the left and choose *Settings* \> *APIs*.

3.  Choose the *Connection* tab.

4.  Choose *Regenerate Credentials* and *Copy* the API portal access credentials.


> ### Note:  
> The client credentials get generated for *APIPortal .Service.CatalogIntegration* role.



<a name="loiob583b7a62f3c4cfdb50a499250c25c15__context_xmh_dsd_tpb"/>

## Context

To establish the connection between the API portal and the API business hub enterprise, the client Id and client secret created for the API Portal is shared during the connection request process.

If you encounter one of the following situations after the connection request has already been approved by the API business hub enterprise admin, you have to update the credentials:

-   The service instance, or the service key gets deleted after the connection between the API portal and the API business hub enterprise was established. In this case, the credentials you were using before the service instance or the service key got deleted becomes invalid.

-   Similarly, if the destination that fetches the API content from the API Portal workspace gets deleted, the credentials you were using before the destination got deleted becomes invalid.




<a name="loiob583b7a62f3c4cfdb50a499250c25c15__steps_ymh_dsd_tpb"/>

## Procedure

1.  Log on to the *API Business Hub Enterprise*.

2.  Navigate to the *Manage* tab and choose *Establish API Portal Connectivity with API Business Hub Enterprise* tile.

3.  Go to the *Actions* column and select the approved connection request that you want to edit and choose *Re-establish Connection*.

4.  On the *Submit Connection Request* page, enter the *Client ID* and *Client Secret* that you copied earlier from the API Portal.

    Sample credentials:

    ```
    {
      "url": "https://<application name>.cfapps.sap.hana.ondemand.com",
      "tokenUrl": "https://<name>.authentication.sap.hana.ondemand.com/oauth/token",
      "clientId": "sb-apiaccessxxxxxxxx!xxxx|api-portal-xsuaa!bxxxx",
      "clientSecret": "xxxxxxxxxxxxxxxxxxxxxxx="
    }
    ```

5.  Choose *Save*.




<a name="loiob583b7a62f3c4cfdb50a499250c25c15__result_yk3_ng1_x4b"/>

## Results

You’ve updated the Integration Suite API portal access credentials successfully.

