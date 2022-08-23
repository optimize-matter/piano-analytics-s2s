# Piano Analytics S2S using sGTM

> Disclaimer : this repository is expected to be used by power user of both sGTM and GTM.
>
> Moreso, the templates and their content will be in English as per specified by the partner.

## Summary

### Content

This repo contains 3 templates :
- A Client template "Piano Analytics S2S - Client.tpl" , to be used in sGTM for S2S or Hybrid tracking.
- A Server Tag template "Piano Analytics S2S - Collection API.tpl" , to be used in sGTM for sending data to your Piano Analytics property.
- A Front Tag template "Piano Analytics S2S - Transporteur.tpl" , to be used in GTM for sending front data to your sGTM.

### Usage

Download and import the templates in the appriorate container.
It is intended to be used **as is**.

Ideally, the front tag should have all the data required by Piano, and the server tag should only copy data received.
Event data are parsed and isolated to ease the use of specific variables.

More details below for specific tracking

##### S2S tracking

For S2S tracking, you should aim to have a POST request fulfilling every specified conditions stated in the official documentation [here](https://developers.atinternet-solutions.com/piano-analytics/).

If needs be, should you send a GET request, the front tag and the "mirror" const in the client code part might help you with properly formatting your hit.

> As specified in the template (in French), the path is "/pa" and is hardcoded.

##### Hybrid tracking
Use the front tag to send already formatted data.

You should only populate the values required in the front tag.

If your front tag is sending a "site id", it will use this value. Else, you should specify it in the server tag.

## What's next

Minor improvements might be made here, though we expect our templates to be available in the gallery soon.
