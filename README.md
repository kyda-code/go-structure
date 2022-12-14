# Golang Project Structure

The following is a folder pattern gathering from my years of experience and good practices like clean architecture.

## Authors

- [@kyda-code](https://www.github.com/kyda-code)

## Perks of Use this Structure

* Ease to maintain
* Ease to understand
* Readable for all
* Scalable for huge o small projects

## Clean Architecture

My experience with Clean Architecture begins 3 years ago, applying it in different projects from retail, fintech, and e-commerce, in this time this tool became my base for resolving problems concerned with systems architecture.

In general Clean Architecture is a software design philosophy that separates the elements of a design into ring levels. The main rule of clean architecture is that code dependencies can only move from the outer levels inward.

![Alt text](https://blog.cleancoder.com/uncle-bob/images/2012-08-13-the-clean-architecture/CleanArchitecture.jpg "Clean Architecture")

The author of this is the Uncle Bob Robert C. Martin if you need more information you can access his [blog](https://[Clean Coder Blog](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html))

## Go Folders

* /cmd => Contains all that we want to run, main application for the project
* /internal => Contains all the code you don't want others importing in their application.
* /pkg => Contains all the code that's ok to use bye external applications

  * /api => Define the configuration to run the API
  * /db => Contains the connection to database and migration logic
  * /utils => Contains utilities for the application like customExceptions, customErrors, customException, etc...
  * /services => Define each service that is used in the application
* /vendors => Contains all applications dependencies created with `go mod vendor `
* /handlers => Functions used to handle to process all request for the services
* /models => Functions that used to represent the tables of the database
* /schemas => Functions that used to represent the desired request structure

## Common Directories

* /web => Contains all application static components
* /configs => Contains the all configurations related to the application as .env, or .yml
* /scripts => Functions that used to trigger a function from another function
* /build => Contains the file to create a container for the application (docket, deb, rpm, ...)
* /tests => Collections of functions used to create different test, like a unit testing or integration testing

## Notes

You don't need to implement this structure in your projects, this can changed or updated depending of the needs of your project if you need know more about the go, always you access the official documentation [here](https://go.dev/doc/).


❤️ Happy Coding!! 😄
