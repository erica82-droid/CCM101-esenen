# Research: Multi-Tier Architecture

## What is a Two-Tier Architecture?

A Two-Tier Architecture is a software architecture that separates an application into two main parts: the Web/Application Tier and the Database Tier. These two tiers communicate with each other to process user requests and manage data.

## The Web/Application Tier

The Web/Application Tier handles the application's user interface and business logic. It receives HTTP requests from users' browsers, processes user actions, and communicates with the database to retrieve or save information. It then sends the appropriate response back to the user.

## The Database Tier

The Database Tier is responsible for storing, managing, and retrieving persistent data. This includes user accounts, login credentials, product information, orders, and other application data. It processes database queries from the Web/Application Tier and ensures that information can be stored and accessed when needed.

## Why Separate Them?

Separating the web server and database into two different containers improves security, makes maintenance easier, and allows each tier to be managed independently. It also allows the web application and database to use separate resources, so increasing the workload of one tier does not necessarily affect the other. Compared with placing both in a single container, this approach provides better isolation, flexibility, and scalability.
