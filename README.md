# N Gauge (`ngauge`)

A homelab-scale PaaS based on [Railpack](https://github.com/railwayapp/railpack). 

## Goals

- **Easy to setup**: provide a simple solution to deploy small services to bare-metal servers.
- **Easy to use**: users should be able to link a repo/branch, set your variables, attach a volume, and hit deploy. Focus on homelabbers.
- **Runs well on cheap hardware**: `nguage` should be resource efficient and run well on cheap hardware.

## Features 

- **Github triggered deploys**: changes can be triggered by pushes to a specified GitHub repo and branch.
- **No config deploys**: railpack will automatically build your images for you from source code.
- **Persistent data**: simple persistence of data via docker volumes.
- **Automated data backups**: simple data backups (basically just `tar czf` your volume folder)
- **Automated HTTP/TCP reverse proxying**: automatically assign a port to your service for HTTP and TCP services and provide a domain.  
- **Automatic SSL**: automated SSL certificates via letsencrypt when psosible (this is annoying on-prem without `DNS-01` challenges).
- **Observability**: export metrics via a prometheus endpoint and support log drains via loki.

and a whole bunch of other stuff.
