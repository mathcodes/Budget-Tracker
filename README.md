# Unit 18 Budget Tracker

Add functionality to our existing Budget Tracker application to allow for offline access and functionality.

The user will be able to add expenses and deposits to their budget with or without a connection. When entering transactions offline, they should populate the total when brought back online.

Offline Functionality:

  * Enter deposits offline

  * Enter expenses offline

When brought back online:

  * Offline entries should be added to tracker.

## User Story
AS AN avid traveller
I WANT to be able to track my withdrawals and deposits with or without a data/internet connection
SO THAT my account balance is accurate when I am traveling

## Business Context

Giving users a fast and easy way to track their money is important, but allowing them to access that information anytime is even more important. Having offline functionality is paramount to our applications success.

## Additional Notes
I told you during the homework introduction that the application's online and offline behavior should be indistinguishable. After further study of the solution, this turned out to be infeasible. So the actual user story is a bit weaker:

> The user loads the page (while online) and starts adding transactions. They may go offline one or more times during this process. If a transaction is added while offline, the table and chart still update. As soon as the connection is back online, any pending transactions are posted to the server (and will be visible the next time the page is loaded).

There are no requirements for what happens to any remaining pending transactions if the page is closed while still offline.

The solution includes a service worker to cache files and API requests, as well as a `manifest.json` for PWA capability, but these don't contribute to the required functionality (presumably they were included to confuse me). So it turns out that, in fact, you don't even need service workers for this assignment, only IndexedDB. If you examine 26-Stu-Mini-Project from unit 17, you should find it readily adaptable.

## Acceptance Criteria
GIVEN a user is on Budget App without an internet connection
WHEN the user inputs a withdrawal or deposit
THEN that will be shown on the page, and added to their transaction history when their connection is back online.

- - -

## Commit Early and Often

* One of the most important skills to master as a web developer is version control. Building the habit of committing via Git is important for two reasons:

1. Your commit history is a signal to employers that you are actively working on projects and learning new skills

2. Your commit history allows you to revert your code base in the event that you need to return to a previous state

* Follow these guidelines for committing:

  * Make single purpose commits for related changes to ensure a clean, manageable history. If you are fixing two issues, make two commits

  * Write descriptive, meaningful commit messages so that you and anyone else looking at your repository can easily understand its history

  * Don't commit half done work, for the sake of your collaborators (and your future self!)

  * Test your application before you commit to ensure functionality at every step in the development process

* We would like you to have well over 200 commits by graduation, so commit early and often!

## Submission on BCS

* You are required to submit the following:

  * the URL to the deployed application

  * the URL to the Github repository

