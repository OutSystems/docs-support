---
summary: <place summary here>
---

# Newtonsoft.Json version error after upgrading to OutSystems 10

## Symptoms

After upgrading to OutSystems 10, when you try to deploy one of your modules or applications you get a compilation error with a message similar to:

`Internal Error: Compilation Error`

`bin\OutSystems.RESTService.Runtime.dll: error CS1705: Assembly 'OutSystems.RESTService.Runtime, Version=10.0.200.0, Culture=neutral, PublicKeyToken=null' uses '**Newtonsoft.Json, Version=8.0.0.0**, Culture=neutral, PublicKeyToken=30ad4fe6b2a6aeed' which **has a higher version than referenced assembly 'Newtonsoft.Json, Version=4.5.0.0**, Culture=neutral, PublicKeyToken=30ad4fe6b2a6aeed'`
`bin\Newtonsoft.Json.dll: (Location of symbol related to previous error)`

## Cause

This is a side effect caused by a [breaking change](https://success.outsystems.com/Support/Release_Notes/Platform_Server/10.0/OutSystems_Platform_side_effects_and_breaking_changes) (#11) introduced on OutSystems 10, where we've changed the Newtonsoft.Json library from 4.5.0.0 to 8.0.0.0.

If you followed all the the OutSystems 10 installation checklist (`.NET` / `Java`) instructions, selecting the upgrade use case, you should not experience the issue mentioned above. One of the mandatory steps includes a full factory republish. This will refresh all references between producers and consumers, thus removing any references to the previous Newtonsoft.Json library and resolving the conflict.

## Resolution

Perform a [full factory republish](https://success.outsystems.com/Documentation/Unlisted/Technical_Communication/Deleted_Development_FAQs/How_to_republish_your_factory).
