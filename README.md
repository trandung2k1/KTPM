# Cypress code-first sample project

This project is using a code-first workflow. This is the approach you should use if you want your test cases to be automatically created in TestRail and not worry about mapping them manually. Using this approach, you don't need to do any modifications to the way you usually write your automated test cases. You can see sample tests in the `cypress/e2e/todo_app` folder.

## How to use the project

Before executing the script, replace the placeholders in `trcli-config.yml` with your TestRail instance details.

Notice the `-y` option on the script below. This will allow all test entities to be automatically created.

````sh
# Install python
https://www.python.org/downloads/

```sh
# Install TR CLI
pip install trcli

# Install test project
npm install

# Run tests
npx cypress run --reporter junit --reporter-options "mochaFile=reports/junit-[hash].xml"

# Merge reports
junitparser merge --glob "reports/junit-*" "reports/junit-report.xml"

# Upload test results
trcli -y -h https://trandungksnb00.testrail.io --project "TRCLI Test" --username trandungksnb00@gmail.com --password Tranvandung2001@  parse_junit --title "Automated Tests Run" -f "reports/junit-report.xml"
````

```js
npx cypress open
```

## Email

```js
trandungksnb00@gmail.com
```

## Password

```js
Tranvandung2001@
```
