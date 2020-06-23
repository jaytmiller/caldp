# Wrapper scripts for processing and container

## caldp-process

This is the primary processing script which provides a clean entry
point for running the container while also capturing a combined
processing log, runtime metrics including peak memory consumption, and
also doing environment setup.

## caldp-docker-run-container

This provides a standard way of running the container including mapping in
any host directories and mapping any required ports.

## caldp-docker-run-pipeline

This provides a standard way of running the caldp-process within a container
for work outside the AWS ecosystem.

## caldp-onsite-process

Configures for running pipeline s/w onsite at STScI.  This would run inside
Docker or using a direct installation of the CAL s/w.  In this mode CRDS
runs relative to /grp/crds/cache which is assumed to be readonly and complete
so no downloads occur.

## caldp-remote-process

Configures for running pipeline s/w offsite for development or
personal use.  This would run inside Docker or using a direct
installation of the CAL s/w.  In this mode CRDS runs relative to
a dynamically downloaded demand based cache.

## caldp-s3-env

CRDS environment variables required for operating relative to AWS S3
with no server connection.

## caldp-cal-env

HST CAL s/w environment variables independent of but sometimes related
to CRDS env vars which also describe locations of reference files.

