# Office 365 Data Extensions API (Preview)

Use the Office 365 Data Extensions API to dynamically store custom data in a message, event, or contact in the signed-in user's
mailbox, or in an event in a group calendar of an organization. In the individual-user context, the user's 
account can be in Office 365 or a Microsoft account (Hotmail.com, Live.com, MSN.com, Outlook.com and Passport.com).

**Note** The Data Extensions API is currently available only in the beta endpoint for preview. If you decide to use preview services, 
plan on verifying the features in your app and accommodating possible breaking changes.


## Overview

A data extension is an OData v4 open type which contains properties that you can specify at runtime. 
You can use the Data Extensions API to _extend_ an instance of an entity type already defined in the Entity 
Data Model (EDM) - a message, event, or contact - by dynamically specifying custom properties and values in a JSON payload. This 
makes the definition of such entity types more flexible, saving you time to define new entity types just for this purpose.

A data extension is defined as an [openTypeExtension](../resources/openTypeExtension.md) object. The **ExtensionName** property is the
only pre-defined, writable property for all extensions. One way to help make sure extension names 
are unique is to use a reverse domain name system (DNS) method that is dependent on _your own domain_, for example, 
`Com.Contoso.Contact`. Do not use the Microsoft domain in an extension name.

Because an extension is an open type, you can specify additional 
data specific to an instance of an entity. For example, you can create an extension for individual business 
contacts that tracks custom data such as company name and initial referrer, and specify the data in the JSON payload as below:

```
POST https://graph.microsoft.com/beta/contoso.com/contacts('{contact_id}')/extensions
{
   @odata.type: "Microsoft.Graph.OpenTypeExtension",  
   "ExtensionName": "Com.Contoso.Customer",
   "CompanyName": "Alpine Skis",
   "InitialReferrer":  "Robin McCall"
}
```

Find out more in this section about performing CRUD operations on extensions in a message, event, or contact item.

For more information about OData open type, see OData v4 documentation on [OData.org](http://www.odata.org/documentation/).


 