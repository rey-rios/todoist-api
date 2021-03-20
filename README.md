# todoist api
Newman API Automation Testing repo for `https://api.todoist.com/`

## Requirements
1. Nodejs installed
2. Newman installed

## Installation

1. Clone repository using git bash to your desired location:
</br> `git clone https://github.com/rey-rios/todoist-api.git`

2. Open the cloned project using Visual Studio Code (VSCode)

3. In VSCode's terminal run the following command:
</br> `npm install`

## Running the tests
Execute below command in VSCode's terminal to run all the **Tasks tests**:
</br>`npx newman run ./YOUR_APP/tests/backEnd/collections/tasks.json -e ./YOUR_APP/tests/backEnd/envVariables/env.json -r htmlextra --reporter-htmlextra-export ./YOUR_APP/tests/backEnd/reports/report.html --env-var token="{your_todoist_token}"` \*
</br></br>
Execute below command in VSCode's terminal to run all the **Create Tasks Data Driven tests**:
</br>`npx newman run ./YOUR_APP/tests/backEnd/collections/create_Tasks_DDT.json -e ./YOUR_APP/tests/backEnd/envVariables/env.json -r htmlextra --reporter-htmlextra-export ./YOUR_APP/tests/backEnd/reports/report.html -d ./YOUR_APP/tests/backEnd/data/tasks.csv --env-var token="{your_todoist_token}"` \*

</br>*\*Replace `{your_todoist_token}` with a valid todoist-api Auth token.*
</br>*HTML report will be published in below path*:
</br>`YOUR_APP/tests/backEnd/reports/report.html`
