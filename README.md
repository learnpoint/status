## `status.json`

`fullyOperational`: This property indicates if Learnpoint is up and running. Set to false if there are any problems.

`notFullyOperationalMessage`: Use this property to display a message when Learnpoint is not fully operational. (When Learnpoint is fully operational, this message is ignored.)

`messages`: This is the list of messages you can choose from by setting the `notFullyOperationalMessage` property.



## `incidents.json`

`date`: Represents the date of the incident.

`major`: Set to true if the incident was major. If major, then the incident day in the calendar will be red, otherwise it will be orange.

`minutes`: Duration of the incident, expressed in minutes. The duration will be counted directly towards the uptime for the month.

`title`: Title of the incident.

`decscription`: Description of the incident.

<img src="incident.jpg" width="640px">



## How to: Set status

Modify `status.json` and commit to the main branch.



## How to: Add an incident

Modify `incidents.json` and commit to the main branch.



## Deploy time

When you've commited `status.json` or `incidents.json` it'll take ~60 seconds for the files to be deployed. Once the files are deployed, your commited changes should be visible on [https://learnpoint.se/status/](https://learnpoint.se/status/) — the json files are fetched from that page with `cache: no-store`.

However, the server (github pages) always responds with a `max-age` of 10 minutes. If the client browser doesn't respect `no-store`, it might take up to ~11 minutes for your commited changes to be visible.



## How to: Preview changes before commit

Navigate to `index.html` in a browser using a static web server.
