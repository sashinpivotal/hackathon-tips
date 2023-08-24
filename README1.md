
- [Overview](#overview)
- [Technical Goals](#technical-goals)
- [Notes](#notes)
- [Technical Getting Started Checklist](#technical-getting-started-checklist)
- [Project Management Getting Started Checklist](#project-management-getting-started-checklist)
- [Suggestions for Success](#suggestions-for-success)
- [Project Presentations](#project-presentations)
  - [Presentation Guidelines](#presentation-guidelines)
  - [Presentation Mechanics](#presentation-mechanics)
- [Appendix A: Notes on Teamwork](#appendix-a-notes-on-teamwork)
- [Appendix B: UI Ideas](#appendix-b-ui-ideas)
- [Appendix C: Useful links](#appendix-c-useful-links)
- [Appendix D: Financial Data](#appendix-d-financial-data)
  - [Python Projects](#python-projects)
  - [Sample REST API](#sample-rest-api)

## Overview

Your team is challenged with designing an application to manage a financial portfolio.

The portfolio may contain some or all of stocks, bonds, cash etc. 

Your task is to build the application.


## Technical Goals

You should aim to create a Portfolio Management REST API. This will be the main target for the training week where you learn about APIs.

This API should allow saving and retrieving records that describe the contents of a financial portofolio.

If/When you have made progress on the core requirements then requirements for further enhancements will be provided. This will included open-ended enhancements whereby you can make use of your particular skills and experience.

We will continue working on this project into the week where you start looking at Web front ends.

For the Front end, you can use the Technologies you have learnt about in your training. If you wish to use a specific framework or some other technology, please check with your instructor. 

The Front end should facilitate your users to (in order of priority):

* Browse a portfolio
* View the performance of the portfolio (ideally in some graphical manner)
* Add items to the portfolio
* Remove items from the portfolio

In terms of detailed requirements, your instructor will act as customer, and will tell you what they want. You can arrange meetings with them as required.


## Notes

1. There will be no authentication and a single user is assumed, i.e. there is no requirement to manage users.

2. You should use the database technology you have been using in the training for any persistent storage.

3. Make good use of git. Use branching and pull requests if you can.

4. Any documentation about how to use your REST API would be useful. Maybe Swagger if you have covered it in your training.

## Technical Getting Started Checklist

1. Create your project structure.

2. Create a bitbucket repository.

3. Add, commit, push your skeleton project to your bitbucket repository.

4. Ensure your team has access to the bitbucket repository.

5. Decide on the absolute MINIMUM fields for a first working system e.g. the first version of your model object may just be an id,  stockTicker and volume.

If you get stuck getting any of the above completed then contact your instructor for help.

## Project Management Getting Started Checklist

1. As a team decide how you will approach the work. E.g. 2 people on the backend, 1 person on UI Design Vs. Everyone on the backend  until a basic system is working. 

2. Make a task list. Ideally use a tool such as trello to keep track of tasks.

3. Some or your team may work on the DESIGN of a more fully-featured application. While some of your team work on BUILDING some small pieces as demonstration.

4. Choose the tasks required for a MINIMAL implementation first.

4. Your instructor will drop in regularly to see how you're progressing. Make a note of any questions so that you're ready to ask them then.

5. Your team should get together and decide on an initial set of data that you will store. A good team decision on this is a good path to success, however remember to STAY AGILE.
The single biggest problem teams face is starting out with a data model that is too complex.

## Suggestions for Success

1. START SMALL. Get a system working that stores a very simple object with minimal fields. You can then enhance to store more complex records.

2. Try pair programming, it can be very effective.

3. Take concious steps to keep a good energy in the team. E.g. give your team a name, systematically plan check-ins with each other.

4. Emphasise quality over quantity.


## Project Presentations

At the end of the program you will get the opportunity to present your project to your instructors and also potentially your manager and other interested stakeholders from within the firm.

The duration of your presentation will be decided by your instructor, but they are typically 20 mins for groups of 3 and sometimes up to 25 or even 30 minutes for larger groups.

### Presentation Guidelines

Here is a suggested flow. You don't have to follow this exactly, but it gives you a suggested outline:


- Tell a story!
  - Your presentation should have a beginning, a middle and an end
- Start by introducing your team
- Then introduce the project
  - What have you been learning?
  - What were you asked to do?
  - How much time have you had to work on it?
- Then explain how you approached the project
  - Did you divide roles, e.g. backend or frontend?
  - Or did you code together, e.g. pair-programming?
  - What technologies and tools did you use?
- Then show what you built
  - Start with an overview of your data model – explain your decisions
  - Then show a high-level architecture of your application
    - This could be a simple diagram in PowerPoint
  - Then give us a live demonstration of your application
- Then tell us what challenges you faced
  - Did you work well together as a team?
  - Were there any technical challenges?
  - What mistakes did you make?
  - What would you do differently?
- Then tell us what you would do next if you had more time
- And finally – thank you for listening, any questions

- Everyone is expected to speak
- Keep your cameras on throughout the presentation
- NOTE: YOU WILL BE EXPECTED TO ASK OTHER TEAMS QUESTIONS


### Presentation Mechanics

* Depending upon the size of your class, the presentations will be delivered in breakout rooms with your groups nominated lead instructor
* The lead instructor will typically have created a schedule for the presentations and will have circulated that in advance with 20-30 mins per group
* The presentation will NOT be allowed to overrun to ensure we keep to time
* The presentation schedule is sent out to wider firm staff so they know when to come if someone wants to see your presentation
* When a group says "any questions?", to avoid any unnecessary silences, the group that went before you MUST ask a question. If you are going first, then the group scheduled last must ask a question
* If your class is using virtual machines then they will continue to be available for the presentation


## Appendix A: Notes on Teamwork

It is expected that you work closely as a team during this project.

Your team should be self-organising, but should raise issues with instructors if they are potential blockers to progress. 

Your team can use a task management system such as Trello to keep track of tasks and progress. Divide the work 

Your team should keep track of all source code with git.

You may choose to create a separate bitbucket repository for each component that you tackle e.g. front-end code can be in its own repository. If you create more than one back end  application, then each can have its own bitbucket repository. To keep track of your repositories, you can use a single bitbucket 'Project' that each of your repositories is part of.

Your instructor and team members need to access all repositories, so they should be either 

a) Made public
b) Shared with your instructor and all team members.

Throughout your work, you should ensure good communication and organise regular check-ins with each other.

## Appendix B: UI Ideas

The screen below might give you some ideas about User Interfaces. You are DEFINITELY NOT expected to implement the screen below exactly as it is shown. This is JUST FOR DEMONSTRATION of the type of thing that COULD be shown.

Just to repeat.... This is NOT what is expected, it is simply here to give ideas!! In the time available, it is understood that your UI will likely be much simpler.

![Demonstration Portfolio UI](https://www.benivade.com/neueda-training/Tech2020/DemoPortfolioScreen.png)

## Appendix C: Useful links

Simple UI that reads live price data from yahoo finance and displays it in a web page: https://bitbucket.org/fcallaly/simple-price-ui

## Appendix D: Financial Data

You can get Financial data from Yahoo. 

### Python Projects

Using Python, you can access the Yahoo API using code like this:

```
import time
from datetime import datetime
import pandas as pd

dt = datetime(2023, 1, 1)
start_date = int(round(dt.timestamp()))

dt = datetime(2023, 3, 31)
end_date = int(round(dt.timestamp()))

stock = 'GOOG'

df = pd.read_csv(f"https://query1.finance.yahoo.com/v7/finance/download/{stock}?period1={start_date}&period2={end_date}&interval=1d&events=history&includeAdjustedClose=true",
    parse_dates = ['Date'], index_col='Date')

```

You could also explore the Python Library specifically designed to work with Yahoo: https://pypi.org/project/yfinance/

### Sample REST API

We have created a sample API that you can interact with to get dummy financial data.

https://c4rm9elh30.execute-api.us-east-1.amazonaws.com/default/cachedPriceData?ticker=TSLA

It's caching price data from yahoo in the background so it doesn't do excess requests to yahoo. Only a few tickers are there by default. Tickers are: C, AMZN, TSLA, FB, AAPL

