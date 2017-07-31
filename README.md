# form-demo-app
Web application that serves and processes GET and POST forms

## Project Members

[Jonathan Pool](https://github.com/jrpool)

## modules

```
app.js
```

## Discussion

### General

This application demonstrates the use of the [`express` package][exp] to create an application that serves and processes GET and POST forms

The demonstration takes the form of a website that serves the requested form and, on its submission, returns a JSON string containing the submitted parameters and their values.

The application fulfills the requirements of the “Posting Data To The Server With A Form” module in Phase 2 of the [Learners Guild][lg] curriculum.

## Installation and Setup

0. These instructions presuppose that (1) [npm][npm] is installed.

1. Your copy of this project will be located in its own directory, inside some other directory that you may choose or create. For example, to create that parent directory inside your own home directory’s `Documents` subdirectory and call it `projects`, you can execute:

    `mkdir ~/Documents/projects`

Make that parent directory your working directory, by executing, for example:

    `cd ~/Documents/projects`

2. Clone this project’s repository into it, thereby creating the project directory, named `form-demo-api`, by executing:

    `git clone https://github.com/jrpool/form-demo-app.git json-api-promise`

2. Make the project directory your working directory by executing:

    `cd form-demo-app`

3. Install required dependencies (you can see them listed in `package.json`) by executing:

    `npm i`

## Usage and Examples

To start the application, execute `npm start` (or, if under Windows, `npm run startwin`).

To request a form while the application is running, use a web browser to request either of these URLs:

`http://localhost:3000/form-get`
`http://localhost:3000/form-post`

Complete the form that is served and submit it.

The response to your submission will be an application/JSON document containing a JSON string representing an object with 2 properties: `body-params` and `query-params`. The former will be empty if you submitted the GET form, and the latter will be empty if you submitted the POST form. The non-empty property’s value will be an object with a property for each field in the form you submitted.

To stop the application, send a SIGINT signal to its process, by entering the keypress CONTROL-C in the terminal window.

To perform linting, execute `npm run lint`.

[exp]: https://www.npmjs.com/package/express
[lg]: https://www.learnersguild.org
