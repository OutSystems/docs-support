---
platform-version: o11
summary: Recomended actions for the error "The attribute has recursive references, which are not supported by OutSystems. Please deselect it before proceeding." in Integration Builder.
tags: ide usage, reactive web apps, tutorials for beginners, error handling, sap odata integrations
locale: en-us
guid: 81e9c04e-3962-4cdd-af49-b53826872f0a
app_type: traditional web apps, mobile apps, reactive web apps
figma:
audience:
  - backend developers
  - full stack developers
  - platform administrators
outsystems-tools:
  - integration builder
  - service studio
coverage-type:
  - unblock
---

# OS-INBL-GEN-00110


## Error message

`The attribute <EntityName>.<AttributeName> has recursive references, which are not supported by OutSystems. Please deselect it before proceeding.`


## Cause

In Integration Builder 1.38.0, a breaking change was introduced to SAP OData integrations: nested attributes of the "object" type stopped being ignored for **Create** actions.

Before this change, if an entity `MyEntity` had an attribute `A1` of the `object` type, and `A1` had an attribute `A1_1` also of the object type, then the `CreateMyEntity` action, generated by Integration Builder, would have an input structure that contained `A1`, but not `A1_1`. 
After this change, the `CreateMyEntity` action generated by Integration Builder would have an input structure that contained `A1`, and `A1_1`.

Continuing the previous example, if `MyEntity`'s `A2` attribute contained an `A2_2` attribute, which had the type `array of MyEntity`, then the `A2_2` attribute wouldn't be selectable in Integration Builder.This is because it would lead to recursive structures, which aren't supported.
When publishing an existing integration where `A2` was selected without unselecting `A2`, this error message is displayed.


## Impact

Integration Builder can't save or publish an integration.


## Recommended action

1. Navigate to the **Add Entities** step of the SAP OData integration wizard. At **Add Entities** click the **Next** button. Integration Builder will automatically unselect the attributes that would create recursive structures.
1. If your business requirements aren't attainable without selecting an attribute that would create recursive structures, the recommended path is to consume the OData service through an extension, created in Integration Studio.
