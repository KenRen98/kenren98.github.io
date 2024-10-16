---
title: Event Posting and Management Platform
date: 2023-07-15 15:37:45
tags: 
  - REST API
  - ExpressJS
  - nodeJS
  - VUE
  - AWS
  - Docker
  - MicroServices
  - Redis
  - Cognito
  - S3
  - EC2
  - Lambda
cover_detail: /2023/07/15/event-posting-and-management-platform/EvtGo.png
cover_index: /2023/07/15/event-posting-and-management-platform/450.png
---
## Introduction

The Event Posting and Management Platform is an innovative startup project designed to revolutionize the way individuals and organizations plan and manage events. From selecting venues to hiring temporary staff, selling tickets, and coordinating with suppliers, this platform offers a comprehensive solution for all event-related needs.

**Website: https://old.evtgo.com/**

Note: UI/UX is done by contractors, but prototyping and coding are done by me.

![GUI](Prototyping.jpg)
(Above Prototype is designed by me)  

![GUI](UI-1.png)
![GUI](UI-2.png)
(Detailed design by third party)  

## Features

### Event Planning Tools
- **Venue Selection:** Browse and rent the perfect place for your event.
- **Supplier Coordination:** Find and collaborate with suppliers for catering, decorations, and more.
- **Equipment Rental:** Rent necessary equipment such as sound systems, lighting, and furniture.
- **Staffing Solutions:** Hire temporary staff for event support.
- **Ticketing System:** Manage ticket sales and distribution seamlessly.
- **Collaborative Planning:** Share and coordinate plans with team members or clients.

## Technology Stack

### Backend
- **ExpressJS and REST API:** Powering the server-side logic and providing a robust API for client interaction.
- **Mongoose and MongoDB:** Serving as the primary database for storing event details, user information, and more.
- **Redis:** Utilized as a caching solution for frequently requested content, enhancing performance.
- **InfluxDB:** Used as data logging micro service, trade off little accuracy to eliminate blocking and complex batching 

### User Management
- **Cognito:** Managing user authentication, authorization, and profile handling. (Removed in later version)
- **Decoupled DB:** For User Store and other regional data for best performance while maintain user data consistency

### Hosting and Deployment
- **EC2:** Hosting the application on Amazon's Elastic Compute Cloud (EC2) for scalable and reliable performance.
- **S3:** Leveraging Amazon S3 as an economical Content Delivery Network (CDN) solution.
- **Docker:** Implementing containerization for consistent development, testing, and deployment through CI/CD pipelines.
- **Lambda:** Utilizing AWS Lambda for serverless computing, enabling efficient scaling and cost optimization.

## Future Expectation
The app is expected to use the user generated data to train AI and perform Interest based recommendation on events and ads, and provide events planning AI for faster planning and suitable options and solutions.

## Conclusion

The Event Posting and Management Platform is a comprehensive solution that simplifies the complex process of event planning. By integrating cutting-edge technologies and providing user-friendly tools, it offers a one-stop solution for event organizers, suppliers, and attendees. Explore the platform and transform the way you plan and execute events.