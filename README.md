# Angular Tech Workshop

## Learning objectives

- Be able to create a Angular Project
- Be able to create a component in Angular
- Be able to create a service in Angular
- Be able to create a module in Angular

## Prerequisites

If you have never used Angular before, run the following command in a terminal to install the Angular CLI

```bash
npm install -g @angular/cli
```

## Create new Angular Project

```bash
ng new
```

## Setup

- Fork this repo to your own github account
- Clone your forked repo
- Open the project in VSCode
- Open a terminal and run the command `npm install` to install the dependencies

## Instructions

Familiarise yourself with the existing `App` component (Take a look at the [Angular component recap](https://github.com/boolean-uk/angular-recap/blob/main/components.md) for an idea of the different parts of the component)

Implement the following requirements:

- Create a `user-list` component to display all users (This component should be a table to display all information)
- Once you click on a row in the table open a dialog or navigate to a page where the user-component will display the information
  - Ensure you pass the selected user to the component user the `@Input` signal
  - Can open a dialog OR navigate to a page (Your choice)
- Create a `user` component that will display a user's name and email address.
- Create a method in the `user-service` to retrieve all users (create your own dummy data)
- In your `user-list` component inject the service into the constructor of the component to be able to user the method
- Example of IUser interface below. (You can extend it if you want)

```ts
export interface IUser {
  id: number;
  username: string;
  emailAddress: string;
  age: number;
}
```

## Running the app

Run `ng serve` OR `ng s` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Generating a new component|module|service

- Run `ng generate component component-name` OR `ng g c component-name` to generate a new component.
- Run `ng generate module component-name` OR `ng g m module-name` to module a new component.
- Run `ng generate service component-name` OR `ng g s service-name` to service a new component.

## Help

Take a look at the [Angular recap](https://github.com/boolean-uk/angular-recap/blob/main/README.md) for examples on how we can:

- Send data into a child component from a parent component
- Send data from a child component to a parent component
