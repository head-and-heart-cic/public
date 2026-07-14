# Build It Yourself? Part 1: A Proportionate Architecture
**Date:** 14/07/2026

## Introduction

Most smaller nonprofit organisations don't have dedicated data and software experts, so they find ways of using standard tools like Word, Excel and SharePoint to manage their data securely and effectively.  The big headache comes when they are answerable to an external regulator, and their work needs to be **demonstrably** secure and effective.

The standard way to handle this would be to bring everything together into a central managed system like Microsoft's Dynamics 365.  But that's expensive, and setting up and maintaining such a system requires a level of technical expertise between application user and software developer.

This series of articles will document my experience as I explore an alternative path to the same space between software user and software developer.  Instead of starting with a full enterprise system like Dynamics 365 and configuring it to meet the needs of the organisation, I'll start with the core of such a system (Microsoft's open-source Common Data Model for Nonprofits) and use Microsoft's no-code development tools to configure it into a central system capable of demonstrably complying with the demands of an external regulator.

## Two core problems of centralising data

- **Flexibility**
  
  Data design decisions affect people who haven't been hired yet, working in departments that don't exist yet, doing work that no one has thought of yet.  
  
  When data repositories are distributed among different teams, each team can adjust their working practices as they go with little impact on the rest of the organisation, but once you move to a shared database, even the smallest change has to be carefully managed because it can have unintended consequences across the organisation. 

  The most robust way of dealing with this in a shared data resource is to produce models that are ruthlessly accurate and comprehensive, but designing and building a data schema capable of adapting to the changing needs of an organisation is a highly skilled, specialist job.

- **Security**
  
  You can easily restrict access to individual files, folders and specialist systems to the people who need them, but an accurate and comprehensive database brings everything to the same place. So, if there is any sensitive data, every interaction needs to be monitored and managed to protect it.

There's no perfect solution to these problems, but for any organisation there are proportionate solutions that resolve them well enough.  The option I want to outline here is aimed at nonprofit organisations without permanent specialist database and development experts, but with staff who are in a position to take on technically challenging commitments.

## The opportunity

There is a reoccurring theme of shared responsibility in the Microsoft ecosystem, resources where Microsoft's staff look after the specialist work, leaving their customers free to focus on tailoring the tools to their own circumstances.  The two of interest here are the Common Data Model for Nonprofits (CDM-NP) and Model-driven Power Apps, when combined with role-based security you get a powerful trio.  CDM-NP provides you with a pool of potential features to include in your application, Model-driven Power Apps provide you with the tools to bring those features to the surface, and role-based security gives you the tools to control who can see and do what in your model.

As it happens, this is exactly the strategy the Microsoft uses for their flagship suite of enterprise applications, Dynamics 365.  They are Model-driven Power Apps, built on the more corporate Common Data Model and governed by role-based security.  The difference is that whereas Microsoft does this to free up their technical staff from dealing with standard features to focus on developing advanced features, I am suggesting that you don't need to worry about developing advanced features if the basic features you can surface from CDM-NP will meet your needs.

- **The Common Data Model for Nonprofits**
  
  The core idea for this approach is that the Common Data Model for Nonprofits is literally a model, in exactly the same way as a toy can be a model of a train, and an architect's doll's house can be a model of a building. When you populate the schema it looks like a collection of spreadsheets, but every table represents an entity, some identifiable thing that you could refer to when describing your organisation, and the columns of the tables represent the defining attributes of those entities.
  
  When Microsoft built CDM-NP they put together the framework needed to model a complex international nonprofit organisation, but you don't have to use the whole thing, you can pick out just those parts that are relevant for your organisation.  And that is how you protect yourself from the problem of flexibility: when you choose which parts of the model to use you end up with a solid model of your own organisation that is naturally extendable, and no matter how your organisation changes in the future, you are unlikely to change in ways that are not already covered by part of CDM-NP. 

- **Role-based security**
  
  The problem of flexibility is a practical problem, and using CDM-NP as a capability pool is an imperfect but proportionate solution, the problem of security is a governance issue and that does demand a full solution.  This is where role-based security comes in.
  
  Role-based security is your organisation's working policies expressed as access rules.  For example, in a sales context, sales staff might be allowed to see and change the records for their own sales and see selected information about the sales of other people in their team, while a manager could be given access to see and change the sales records for everyone that reports to them, but no one else.
  
  With suitably configured role-based security anyone interacting with the model can only see and change the parts of the model they need to see and change.

- **Model-driven Power Apps**
  
  Once you have selected the entities from CDM-NP you want to use, applied role-based security to them, and populated them with your organisation's data, you will have a fully functioning model of your organisation.  
  
  At that point, if you understand the model, then you can just about operate it by looking at the entities directly as if they were tables in a spreadsheet. But, because each table you look at will only show you a small amount of the model taken out of context, unless you can picture the wider context yourself or the task is very straightforward, that won't be a practical option.
  
  Model-driven Power Apps are a no-code and low-code development environment which gives you the tools to build visual interfaces for interacting with your model that shape themselves to its logic and that respect the role-based security rules you build into your model. 

Maintaining your records in a secure, rigorous model also opens up the options of using Power Automate and deploying AI agents with Copilot Studio, but for now I am exploring the options for maintaining a compliant bespoke information system with minimal in-house technical expertise, and for that purpose Model-driven Power Apps are probably going to be sufficient.

## The next step

This is an established methodology at an industrial level, with full time developers, the question I want to explore next is if Microsoft's shared responsibility policies are enough to make this approach feasible for a small nonprofit organisation with self-taught IT champions.  To find out the details needed to answer that my next step will be to build a proof-of-concept app based on a couple of CDM-NP entities, and see exactly what it involves and what relevant training materials are available to learn the requisite skills.

Patrick Killeen  
Head and Heart CIC  
patrick@headandheart.info  
www.headandheart.info

This work is released under the MIT Licence and is available at  
https://github.com/head-and-heart-cic/public/blob/main/in-practice/260714_build_it_yourself_part_1_a_proportionate_architecture/README.md
