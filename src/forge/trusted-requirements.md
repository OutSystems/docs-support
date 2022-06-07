---
summary: Know the set of requirements that a component shared in Forge must comply with to be considered a Trusted component.
tags: forge; forge_support; trusted
locale: en-us
guid: a5774b9a-751e-4df6-889a-9f54f363ac40
app_type: traditional web apps, mobile apps, reactive web apps
---

# Trusted components requirements

[OutSystems Forge](https://www.outsystems.com/forge/) provides a large set of reusable components that helps accelerate application delivery. These components are made available by our community users and by OutSystems.

When using Forge components, make sure they're part of the quality process already in place in your team. When searching for components in OutSystems Forge, take into consideration that some components have a curation stamp. Using the following curated components can ease your quality assurance process:

* **OutSystems Supported components** - developed, maintained, and supported by OutSystems
* **Trusted components** - developed and shared by the OutSystems Community; validated by the OutSystems Curation team to ensure these components deliver the promised functionality and are built based on best practices

![OutSystems Forge](images/trusted-components-fg.png?width=900)

This article describes the set of requirements that a component shared in Forge must comply with to be considered a **Trusted** component.

If you want to share your component with the OutSystems Community and have it trusted by the OutSystems Curation team, make sure your component complies with the requirements listed below.

## Requirements for trusted components

Trusted components must comply with quality standards within the following categories:

* Forge presence
* Installation
* Functionality
* Usability
* Implementation
    * Architecture
    * Security
    * Performance
    * Code maintainability
    * Compliance
* Support and maintenance

The following sections describe the requirements that trusted components must meet for each category.

### Forge presence

The component information in Forge must be clear and complete. For this, the component must have the following characteristics:

* Have a meaningful name, a clear description and a clear short description
* Be correctly categorized and tagged
* Have the correct application type
* Indicate the correct requirements
* Include screenshots
* New versions of the component must indicate in detail what changed and be correctly categorized and tagged

### Installation

The component must install successfully. For a component to install successfully, the following requirements must be met:

* No missing dependencies
* No dependencies to other Forge components that have been deprecated
* Documentation describing any type of additional configuration needed before using the component (for example, run Timers, Site Properties configuration, external services configuration)

### Functionality

The component must work as expected. For this, the component must have the following characteristics:

* Provide the described functional requirements, functions, and use cases
* Use functionality that's not deprecated, considering the features released by the latest OutSystems versions (for example, deprecated system actions)

### Usability

The component must be easy to use. For this, the component must include the following:

* Clear and concise documentation, describing the provided functionality
* Documentation of all actions (for example, Timers that run on publish or periodically)
* Documentation of any implementation pattern that's specific to the component’s usage (for example, the need to use Blocks/Actions/Entities in a specific order)
* Clear and helpful description for all public elements
* When possible, have an associated demo component showcasing all the provided functionality

### Implementation

Trusted components must comply with the implementation best practices described in this section. The OutSystems Curation team uses the [Architecture Dashboard](https://success.outsystems.com/Documentation/11/Managing_the_Applications_Lifecycle/Manage_technical_debt/Code_Patterns) to perform the necessary validations.

#### Architecture

Components comprising a whole application must follow the [best practices for application architecture design](https://success.outsystems.com/Documentation/Best_Practices/Architecture/Designing_the_Architecture_of_Your_OutSystems_Applications), which determines the organization of the application modules according to the layers described in the [OutSystems Architecture Canvas](https://success.outsystems.com/Documentation/Best_Practices/Architecture/Designing_the_Architecture_of_Your_OutSystems_Applications/The_Architecture_Canvas) (End-user, Core, and Foundation modules).

The component architecture must comply with the following rules:

* End-user modules/applications don’t provide services
* Foundation modules/applications don’t consume Core modules/applications
* No cyclic references between modules/applications
* Core modules don’t provide services to sublayers
* Foundation modules don’t provide services to sublayers
* Expose Public Entities as read-only

#### Security

The component must comply with the following security standards:

* Expand Inline properties in SQL Query Parameters are disabled or sanitized
* No unescaped/unencoded user inputs or screen variables (applies to Traditional Web only)
* Only enabled buttons are visible (to prevent enabling disabled buttons at runtime using development tools on a browser)
* Exposed REST services enforce SSL/TLS and require authentication
* No anonymous screens unless they are strictly necessary
* No APIs that send or collect data to external services out of the component scope
* No functionalities that can be misused with malicious intent (for example, allow the upload and execution of binary files)
* No manipulation of system tables

#### Performance

The component must comply with the following performance best practices:

* Aggregates or SQL queries Count property is never used to check if results were returned
* SQL queries Count property is always used in simplified SQL queries
* No Aggregates or SQL queries executed inside a loop
* Site Properties aren’t updated using application login
* Long-running Timers follow a wake timer pattern to process big amounts of data in chunks
* No Server Request Timeout for server actions set to more than 10s (applies only to Reactive Web and Mobile)
* Avoid server calls on client events - On Initialize, On Ready, On Render, On After Fetch (applies only to Reactive Web and Mobile)
* Only one server request - Aggregate or Server Actions - inside Client Actions (applies only to Reactive Web and Mobile)
* Correct implementation of the offline sync patterns (applies only to Mobile)
* Server data is stored in the local database asynchronously (applies only to Mobile)
* No query data passing from Preparation to Screen Actions through the ViewState (applies only to Traditional Web)
* No screen Local Variables of type Compound or Collection (applies only to Traditional Web)

#### Code maintainability

The component code must be easy to maintain. For this, the following requirements must be met:

* Preparation and Screen Actions have less than 20 nodes, otherwise have Comments describing the logic
* Server Actions and Client Actions have less than 40 nodes, otherwise have Comments describing the logic
* No disabled code
* Extension components have external libraries installed in Microsoft Visual Studio, preferably via NuGet Package Manager

#### Compliance

The component must ensure license compliance. For this, all external libraries (JavaScript libraries in modules and libraries in extensions) must be used correctly according to their license terms.

### Maintenance and support

The component must be kept up to date. For this, the component must have the following characteristics:

* Available in the latest OutSystems version
* Description and documentation must be up to date with the latest component version

The component’s owner must provide the following required support:

* Reply to any comments or questions
* Solve the reported errors
