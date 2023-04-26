From September 2022 to April 2023 for my Senior Fall and Spring Semesters, I worked on a senior capstone project as I finished out my degree at Grand Canyon University. I set out to solve a problem I had seen in the small business website industry in Arizona where non-technical employees would spend hours of company time entering credentials and data, waiting for a report to generate, copying and pasting the needed values into a spreadsheet. In larger companies this problem could be easily solved by sitting down a developer or two and giving them a small side project of building an integration program that automatically pulls the data down from multiple REST services. However, small businesses do not have many developers at their disposal and those that they do have are busy in much more important areas. My solution to this problem was a project I called Overwatch SEO, or as it later transformed into Overwatch Rest Reader.

## Project Development
As I built out the Overwatch Rest Reader application as part of my senior capstone class, I was required to write out the specs and designs, as well as keep them updated as I moved forward with the project. This included documents such as an initial proposal, design spec, requirements document, testing plan, sprint backlog, and a traceability matrix. Along the way, I also made diagrams such as wireframes, ER diagrams, UML diagrams, sprint burn down charts, and N-Layer Architecture charts. I ran weekly sprints and continued to iterate upon my work.

One challenge of the project was that I had a lot of difficulty getting the right technology stack. The project originally started as C# terminal application, then became a .NET MAUI application (as the project needed a GUI frontend), and then an Avalonia UI application (as .NET MAUI did not work). Consequently, I learned many lessons about modularizing code so that it could be shifted when the current version of the project was not working in a way that would help the end user.

In the end, I completed the project to my original scope, as well as my expanded scope that I had added as time went on and I got a better sense for what the project needed to be.

## Current Project
The current version of Overwatch Rest Reader is hosted at this git URL: [RSoemo-GCU/Overwatch-Rest-Reader (github.com)](https://github.com/RSoemo-GCU/Overwatch-Rest-Reader)

I continue to work on the project and iterate on its design in order to better serve the users I set out to solve a problem for.

## Project Documentation
Below are some snippets from my project's documentation:

> Overwatch Rest Reader is a software technology developed to automate
> the manual collection of data from services and systems which have
> REST Service API backends. Overwatch Rest Reader speeds up the data
> collection process as an all-in-one data collection program. When a
> user starts data collection, the program begins requesting data from
> multiple services and then waits for the reports to be generated. Once
> Overwatch Rest Reader receives the reports, it will then combine the
> different data points together before displaying the data to the user.
> The user can then use this information by reading it from the program
> or they then can choose to create a CSV file of the latest data, which
> can easily be transferred into a spreadsheet program of their choice.
> 
> Overwatch Rest Reader is a general solution to the slow process of SEO
> data collection. Data points are generated over long periods of time
> with regular check-ins on different services. However, the process
> going to multiple frontends is repetitive and time wasting to SEO
> experts. With Overwatch Rest Reader, the control is given to SEO
> Experts, even those who are not technologically savvy.
> 
From Overwatch Rest Reader Project Proposal v2


![Main_Records](https://user-images.githubusercontent.com/101227901/234661321-11227809-4e2d-4d71-add8-d34c8716199d.png)
Overwatch Rest Reader Wireframe for the Records Page

![image](https://user-images.githubusercontent.com/101227901/234661437-199ca6ac-e239-4d5c-99d8-bef5dc174db6.png)

 Final Presentation

![image](https://user-images.githubusercontent.com/101227901/234661511-a8a4fd3c-65df-4a18-8508-2478656dc828.png)

Final Burn Down Chart
