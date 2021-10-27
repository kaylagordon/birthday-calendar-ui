### This repo is used as an assessment during the course of the Turing modules, if you are viewing this repository outside the context of an assessment, you’re in violation of the Academic Integrity policy you agreed to as a student.

## Turing Birthday Calendar - Frontend

This application was built with `create-react-app`.

### Set Up

1. Clone down this repo. (Do not Fork!)
2. `cd` into the directory.
3. On GitHub, create a new, empty, **private** repository and name it something like 'turing-birthdays-fe'.
4. Update the current remote (origin) and point it at the new URL of the repository you just created on GitHub. You can read how to do this [here](https://help.github.com/en/articles/changing-a-remotes-url) or follow the steps below:
  a. Remove the current remote repo by running `git remote rm origin`. 
  b. Add your new remote origin by running `git remote add origin git@github.com:<user_name>/<repo_name>.git`
  c. After you've made a commit, you should be able to push up to your new repo using `git push -u origin main`
5. Run `npm install` to install dependencies for the repo.
6. Run `npm start` to start up your React server.  

### Expectations

Build a React App that displays the birthdays of the Turing community!

You will have 3 hours to build this application.

![turing-bdays-screenshot](https://user-images.githubusercontent.com/51416773/132622036-217cc0ad-da6b-464a-9b8a-f4bc015dbddb.png)

While CSS is not the learning goal here, you should do your best to match the comp provided. The colors can be found in the `App.css` file.    

We do want to see good commit habits - atomic commits that log small, focused changesets. Don't worry about creating GitHub issues, though.

### Iteration 0

Pull down the [API repo](https://github.com/turingschool-examples/birthday-calendar-api). Set up instructions are in that repository's README.

Do *not* nest this inside your front-end repository.

### Iteration 1

Get all existing birthdays on page load and display them on the DOM, with each birthday appearing in the correct month. If a month does not have any birthdays in it, it should say "No birthdays this month."

Notes:  
- For now, use the months data from the `month_data.js` file. Do not fetch that data.
- Do not worry about including the delete button for each birthday at this point.

### Iteration 2

Create a controlled form component to create a birthday (look into the API documentation to see what pieces of information are expected, and what datatypes it wants each piece to be). As a user types into the input fields, the form component's state should change.  When the user clicks the `Add this birthday!` button, the application should update the App's state.  The new birthday should display with all of the existing birthdays.

Notes:  
- You can assume that the user will input correct data (i.e. a number for month and day that represent a valid date). You do not need to worry about error handling!  
- Do not worry about making the POST request to the database yet.  

### Iteration 3

Now that the functionality is there for adding a birthday, write some tests:
* Write tests covering what should be displayed on the page when the user first visits.
* Write a test that checks that when data is put into the form, the value is reflected in that form input.
* Write a test to check the user flow of adding a new birthday to the page.

Run `npm run cypress` to start up the Cypress testing server.

### Iteration 4 (extension)

When the user makes a birthday, the application should make a POST request to the API. The new birthday should still exist upon reloading the page.

Note:  
- Keep any fetch calls you write in the App component for now. If you have time to refactor your fetch calls into a separate helper file, that is fine, but it is *NOT* a requirement for this application.

### Iteration 5 (extension)

Delete a birthday when the user clicks the `X` button.  The deletion should persist upon reloading the page. You'll need to make a DELETE request for this.

### Other Extensions
* Add error handling for the form so that only valid numbers are accepted.
* Try writing out a few other tests to cover sad path testing for your network requests.
* Use a fetch to get the month data from the API, rather than using the `months_data.js` file.
* Sort the birthdays on each Month card so they appear in chronological order.
