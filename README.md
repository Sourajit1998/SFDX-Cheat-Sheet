# SFDX Cli Cheat Sheet

## Apex Commands
<hr>
### Creates an Apex Class
`sfdx force:apex:class:create -n <Class Name> -d <OUTPUTDIR>`

### Creates an Apex Trigger
`sfdx force:apex:trigger:create -n TRIGGERNAME -d <OUTPUTDIR> -s <sObject> -e <TRIGGEREVENTS>`

### Executes one or more lines of anonymous Apex Code, or executes the code in a local file
`sfdx force:apex:execute -u <user-email-id@example.com> -f <APEXCODEFILE>`

### Fetches the last Debug Log
`sfdx force:apex:log:get -u <user-email-id@example.com> -c -n <Number of Logs> -i <LOGID>`

### Displays a list of debug Log IDs, along with General Information
`sfdx force:apex:log:list -u <user-email-id@example.com>`

## Authentication Commands
<hr>
### List Auth Connection Information
`sfdx force:auth:list`

### Log Out of all connected Orgs
`sfdx force:auth:logout -a --noprompt`

### Log Out a user
`sfdx force:auth:logout -u <user-email-id@example.com>`

### Connect Salesforce DX to an Org (e.g. DevHub, Sandbox, Production)
`sfdx force:auth:web:login -d -r <Login URL> -a <Org Alias>`

## Config Commands
<hr>
### Gets the Salesforce CLI Configuration values
`sfdx force:config:get`

### Lists the Configuration variables
`sfdx force:config:list`

### Set a Scratch Org as the Default
`sfdx force:config:set defaultusername=<user-email-id@example.com>`

## Org Commands
<hr>
### Create a Scratch Org
`sfdx force:org:create -s -f <pathTo/project-scratch-def.json> -u <user-email-id@example.com> -a <Project Name>`

### Marks a Scratch Org for Deletion
`sfdx force:org:delete -u <user-email-id@example.com> --noprompt`

### Gets the description for the Current or Target Org
`sfdx force:org:display --json -u <user-email-id@example.com>`

### View a list all of the Orgs
`sfdx force:org:list -all`

### List all Orgs except inactive/expired Orgs
`sfdx force:org:list --clean --noprompt`

### Open a org in your browser
`sfdx force:org:open -u <user-email-id@example.com>`

## Project Commands
<hr>
### Create a blank project
`sfdx force:project:create -d <OUTPUTDIR> -n <Project Name>`

### Create project with manifest
`sfdx force:project:create -d <OUTPUTDIR> -x -n <Project Name>`

## Schema Commands
<hr>
### Displays the metadata for a standard or custom object
`sfdx force:schema:sobject:describe -u <user-email-id@example.com> -s <Object API Name>`

### Lists all Objects of a specified sObject category
`sfdx force:schema:sobject:list -u <user-email-id@example.com> -c <sObject Type Category>`
* c = all, custom, or standard

## Source Commmands
<hr>
### Converts Source-Formatted files into Metadata that you can deploy using Metadata API
`sfdx force:source:convert -r <ROOTDIR> -d <OUTPUTDIR> -x <MANIFEST> -m <METADATA>`
* m comma-separated list of names of metadata components to delete from your project and your org

### Deletes Source Files from your Project and from a Non-Source-Tracked Org
`sfdx force:source:delete -u <user-email-id@example.com> --noprompt  -m <METADATA>`

### Deploy source to an Org
`sfdx force:source:deploy -p <SOURCEPATH> -m <METADATA> -u <user-email-id@example.com>`

### Cancels an Asynchronous Source Deployment
`sfdx force:source:deploy:cancel -u <user-email-id@example.com>`

### Opens the specified Lightning Page in Lightning App Builder
`sfdx force:source:open -u <user-email-id@example.com> -f <SOURCEFILE>`

### Pull changes Source from the Scratch Org to your Project to keep them in Sync
`sfdx force:source:pull -u <user-email-id@example.com> -f`

### Pushes changes Source from your Project to a Scratch Org to keep them in Sync
`sfdx force:source:push -u <user-email-id@example.com> -f`

### RetrievesMetadata in Source format from an Org to your local Salesforce DX Project
`sfdx force:source:retrieve -u <user-email-id@example.com> -m <METADATA> -x <MANIFEST> -p <SOURCEPATH>`

### Lists changes that have been made locally, in a Scratch Org, or Both
`sfdx force:source:status -u <user-email-id@example.com> -a`

## User Commands
<hr>
### Creates a user for a Scratch Org
`sfdx force:user:create -u <user-email-id@example.com> -a <Set Alias>`

### Displays information about a user of a Scratch Org
`sfdx force:user:display -u <user-email-id@example.com>`

### Lists all users of a Scratch Org
`sfdx force:user:list -u <user-email-id@example.com>`

### Generates a password for Scratch Org users
`sfdx force:user:password:generate -u <user-email-id@example.com>`

### Assigns a named permission set to one or more users of an Org
`sfdx force:user:permset:assign -u <user-email-id@example.com> -n <PERMSETNAME>`

## Visualforce Commands
<hr>
### Creates a Visualforce Component
`sfdx force:visualforce:component:create -d <OUTPUTDIR> -n <Component Name> -l <Label>`

### Creates a Visualforce Page
`sfdx force:visualforce:page:create -d <OUTPUTDIR> -n <Component Name> -l <Label>`

## Upadte Commands
### Update sfdx
`sfdx update`

# References
* [Salesforce CLI Command Reference](https://developer.salesforce.com/docs/atlas.en-us.sfdx_cli_reference.meta/sfdx_cli_reference/cli_reference.htm)