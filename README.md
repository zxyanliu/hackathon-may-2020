# Docs Management VA - Microsoft Conversational AI Hackathon May 2020

## Project overview
Documentation management involves work such as periodic check of broken links in docs, and update the code links that are referenced in the docs because of changes in the samples code. We are looking for ways to automate this work flow. Instead of manually checking the changes and relies on customer reports on broken links, we look for a work flow to notify writers whenever there are changes in the samples code and which sample they need work to double check the code lines referenced in the docs. So does the broken link checks. Hence, we propose a Docs Management Virtual Assistant, which involves two skills: a code link checker skill and a broken link checker. We can use the newly-GAed [Bot Framework Composer](https://dev.botframework.com/) to add a [custom action](https://aka.ms/bf-composer-docs-custom-action) and implement this VA.

## User scenarios

### Scenario 1: Code link checker
* A sample in Bot Builder Samples' repo was updated recently. For example, [Sample #47](https://github.com/microsoft/BotBuilder-Samples/tree/master/samples/csharp_dotnetcore/47.inspection). 
* The article that references the code from [Sample #47](https://github.com/microsoft/BotBuilder-Samples/tree/master/samples/csharp_dotnetcore/47.inspection) will be identified. 
* The author/writer who writes the article will be notified by email.
* Then the author/writer can work on checking the code links. 

### Scenario 2: Broken link checker
* An aka/doc link that points to an MS document was recently removed. 
* The article/s that contains the newly broken link are identified. 
* The author/writer will be notified of this change by email. 

## Details 

|Skill|Owner|
|---|---|
|Documentation VA|---|
|Code link checker|---|
|Broken link checker|---|

## Implementation

1. Create an individual branch named "hackathon-may" based off master branch of bot-docs-pr repo.

    https://github.com/MicrosoftDocs/bot-docs-pr/tree/hackathon-may-2020

2. Fork BotBuilder-Samples repo and create an individual branch named "hackathon-may-2020". 
   
   https://github.com/zxyanliu/BotBuilder-Samples/tree/hackathon-may-2020

3. Generate a spreadsheet with the following data for each article that references a sample based on the data of the two repositories in step 1 and 2: author, docs GitHub link, referenced sample link. 

4. Call GitHub API to identify the changes in the forked branch of the BotBuilder-Samples repo (https://github.com/zxyanliu/BotBuilder-Samples/tree/hackathon-may-2020). 

5. Whenever where are changes, the author / writers will be notified by email and request them to check. 

## Demo

1. Make a change in the code in sample #47 in the forked BotBuilder-Samples' repository. 
2. The article that reference code from #47 is this article and the author is zxyanliu. 
3. The writer checks her email to read the notification. 
4. The writer creates a PR so that can view the code changes on the live side (HTML view). 
5. The writer fix the code lines, and create another PR to view the changes are updated. 

## Known issues

## Additional information
