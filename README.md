This image is designed to have all the tools necessary to help perform Deployments to GCP and G Suite.

It is based off the [google/cloud-sdk:latest](https://hub.docker.com/r/google/cloud-sdk/) Docker image, then adds:

* Node.JS 8
* clasp
* jq

No authentication has been setup in this image, so you will need to setup auth with the various components when using.

In general, here's what needs to happen:

* For clasp, save contents of a clasprc file to `~/.clasprc.json`
* For gcloud, save contents of GCP Service Account to the image (anywhere really), then run `gcloud auth activate-service-account --key-file <key file path>`
