# Scheduled ping to VP FAIR Data Point Index

This workflow regularly runs the following command in order to ping the VP FAIR Data Point Index:

```
curl -X POST -H "Content-Type: application/json" -d '{"clientUrl": "URL_HERE"}' https://index.vp.ejprarediseases.org/
```

Where URL_HERE is replaced by a FAIR Data Point URL.

## GitHub workflow Set up
Actions -> New workflow -> click "Skip this and set up a workflow yourself"

Change the file name from main.yml to ping.yml

Copy the contents of https://github.com/dwijnbergen/scheduled_ping_FDP-Index/blob/main/.github/workflows/ping.yml

Replace the https://patient-registries.fdps.ejprd.semlab-leiden.nl/ URL with the URL of your FAIR Data Point

Commit changes -> commit changes

## GitHub workflow Use
The workflow will run automatically once a week, and on changes in the repository.

The workflow can also be started manually:

Actions -> Ping Fair Data Point Index -> Run workflow -> Run workflow

## GitHub workflow Limitations
Since GitHub actions cost resources, there are some limitations to the scheduled workflow.

See: https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#schedule

For example, it only works on the main branch, and the schedule is disabled after 60 days of repository inactivity.

## Alternatives to GitHub workflow
- Set up a cron job on a linux server to perform the ping command
- Integrate the command with the software that publishes the FAIR Data Point documents
- Run the command manually
