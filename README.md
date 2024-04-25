# Scheduled ping to FAIR Data Point Index

## Set up
Actions -> New workflow -> Skip this and set up a workflow yourself

Change name from main.yml to ping.yml

Copy the contents of https://github.com/dwijnbergen/scheduled_ping_FDP-Index/blob/main/.github/workflows/ping.yml

Replace the https://patient-registries.fdps.ejprd.semlab-leiden.nl/ URL with your FAIR Data Point URL

Commit changes -> commit changes

## Use
The workflow will run automatically once a week.

The workflow can also be started manually:

Actions -> ping every week -> Run workflow -> Run workflow

## Limitations
Since GitHub actions cost resources, there are some limitations to the scheduled workflow.

See: https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#schedule

For example, it only works on the main branch, and the schedule is disabled after 60 days of repository inactivity
