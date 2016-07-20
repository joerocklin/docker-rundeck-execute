Rundeck Execute
===============

I needed a simple way to kick off a rundeck job and monitor the output from a seperate CI tool. For various reasons,
this was the best means to the end - at least for now.

It's based on Alpine Linux and is pretty tiny, only pulling in curl to do the rundeck interaction. All behavior is
based on environment variables.

Environment Variables
---------------------

 * `RUNDECK_URL` _required_ - The base URL on which all Rundeck URLs are built. This _should only_ include the portion of the URL
   prior to the `/api` path.
 * `RUNDECK_TOKEN` _required_ - The token to use to authenticate to Rundeck
 * `RUNDECK_JOB_ID` _required_ - The Rundeck Job ID to execute
 * `RUNDECK_JOB_OPTIONS` _optional_ - JSON formatted options to pass to the rundeck execute call
