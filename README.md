# 🤯 OMG MCP WTF: Three Ways MCP Servers Can Change Your Life

Repository to store all assets for the **🤯 OMG MCP WTF: Three Ways MCP Servers Can Change Your Life** session, first delivered as part of [DynamicsMinds](https://www.dynamicsminds.com/) 2026.

## Abstract

The adoption of the Model Context Protocol (MCP) standard by Microsoft heralds an important moment in the generative AI journey, as work is done to better facilitate agent to agent communication, and unlock the full capabilities of solutions such as Microsoft Dataverse, Dynamics 365 Customer Service, and more. With access to just a single (or indeed multiple) MCP server, complex, multi-turn actions can be accomplished in a pinch. But are the promises as real and as easy to work with as claimed? How can a functional user start to integrate these experiences into their day to day workflows?

In this session, join Joe and Daniel, as they demystify the buzz around MCP servers, and present 3 practical, day-to-day scenarios where using MCP servers obliterates any previous process, in terms of speed and efficiency. You’ll gain a thorough understanding of how to get going with MCP Servers, and walk away with insights and inspiration on how to use them yourself. This session is perfect for the MCP curious, who may not be strong as a developer, but is keen to see how MCP servers can be used in an easy way.

## Instructions

### Pre-Requisites
- Access to a Dataverse environment (can be trial)
- Power Platform CLI installed and authenticated
- Python 3 installed with `PowerPlatform.Dataverse` package (`pip install PowerPlatform.Dataverse`)
- GitHub Copilot
- (Optional) Visual Studio Code with Python and C# extensions

### Configuration
- Clone this repository
- Create a `.env` file in the root with the following content (replace values as needed):
```
DATAVERSE_URL=<YOUR DATAVERSE URL>
TENANT_ID=<YOUR TENANT ID>
MCP_CLIENT_ID=<YOUR MCP CLIENT ID>
SOLUTION_NAME=<YOUR SOLUTION NAME>
PUBLISHER_PREFIX=<YOUR PUBLISHER PREFIX>
PAC_AUTH_PROFILE=<YOUR PAC AUTH PROFILE>
```
- This configures the connection to the Dataverse environment, as well as solution and publisher naming conventions. The `PAC_AUTH_PROFILE` should match the name of an authenticated profile in your Power Platform CLI (`pac auth list` to check).
- The `SOLUTION_NAME` and `PUBLISHER_PREFIX` values will be used throughout the repo for naming the solution, tables, and plugins, so you can change them if you want to use different names (just be sure to update the values in the `.env` file and adjust any references in the code accordingly).
- `MCP_CLIENT_ID` is the client ID of a registered Azure AD application with permissions to access the Dataverse environment. You can create your own app registration in Azure AD and grant it the necessary API permissions (Dynamics CRM API with delegated permissions), then update the `.env` file with your app's client ID.

### Executing the Demo

The repository contains an [LLD-AIHotTakes.md](LLD-AIHotTakes.md) file which provides a detailed walkthrough of the solution architecture, components, and code for the "AI Hot Takes" solution. This can be referenced in a chat session. Begin by asking the agent to setup your Dataverse environment:

```
Connect to Dataverse and validate the connection
```

Next, you can request it to create the solution and necessary tables, by referencing the LLD-AIHotTakes.md file:

```
Now proceed to create a solution for my AI "Hot Takes" solution, as described in the LLD.
```

From there, the agent can guide you through the process of building out the solution, including creating tables, forms, views, and plugins, as well as demonstrating how to use the MCP server to interact with the data in Dataverse. You can ask the agent to perform specific tasks, such as:

- Create a new table for "Topics" with columns for "Name", "Description", and "Sentiment Score"
- Create a form for the "Topics" table that includes the "Name", "Description", and "Sentiment Score" fields
- Create a new environment and deploy the solution to it
- Generate documentation for the current solution as a markdown file.
- And much more!

## Disclaimer

All instructions are correct as of the time of writing. However, Microsoft frequently updates its products and services, which may result in steps no longer working as expected. In case of any discrepancies, please raise an issue on the GitHub repository. We will do our best to address any issues, but please note we cannot provide any immediate support.

## License

This repository is licensed under the GPL-3.0 license. You are free to use, modify, and distribute these lab steps as you see fit, as long as you comply with the terms of the GPL-3.0 license.