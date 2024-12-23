```markdown
# Elastic Artifact Registry 
Pre-Packaged at GitHub:

docker pull charliek17/ear:<VERSION>

Nginx based container that serves Elastic Artifacts within an airgapped envrioment. 

## Container aligns to Elastic Releases 


# Using Docker

This guide demonstrates how to create a run a Docker container to host elastic artifacts.

Currently Supports 'elastic-agent/elastic-agent' 'heartbeat/heartbeat' 'filebeat/filebeat' 'packetbeat/packetbeat' 'auditbeat/auditbeat' 'osquerybeat/osquerybeat', fleet-server/fleet-server' 'cloudbeat/cloudbeat' 'endpoint-dev/endpoint-security' 'apm-server/apm-server' 'prodfiler/pf-host-agent' 'prodfiler/pf-elastic-collector' 'prodfiler/pf-elastic-symbolizer'

## Prerequisites

Before you begin, ensure you have the following installed on your system:
- docker
- docker-compose

## Steps

# Build image on internet facing machine.

Example Build command:

''' docker build --pull --rm -f "artifact.Dockerfile" -t ear:latest "." '''

# Import image into envrioment

1. Please ensure you name your certs the following, within you certs volume:
-  els.crt 
-  els.key


Run docker compose:
'''docker compose -f "docker-compose.yaml" up -d'''

EAR should be listening on 8443


