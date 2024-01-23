---
description: 'Easily define and schedule cron jobs with IONOS Deploy Now directly from your GitHub repository.'
sidebar: 'docs'
prev: '/docs/visitor-statistics/'
next: '/docs/faq/'
editable: true
---

# Cron jobs

## Creating a cron job
Cron jobs can be defined directly in the `config.yaml` under `.deploy-now` in your repository. Simply add new cron jobs including a command and a schedule to the sheet. 

```
runtime:
  cron-jobs:
    - command: my-cron-job-command # the deployment is located at $HOME/htdocs/ to execute a deployed script just prefix it accordingly
      schedule: 0 5 * * * # run every day at 5:00
```

A description of the crontab syntax that is required to define schedules can be found [here](https://www.adminschoice.com/crontab-quick-reference).
