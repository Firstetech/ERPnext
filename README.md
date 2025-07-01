# ERPNext Coolify Deployment

This repository contains a Docker Compose setup to run ERPNext using Coolify.

## Usage

1. Clone this repo
2. Import into [Coolify](https://coolify.io) as a Docker Compose app
3. Set secrets or `.env`:
    ```
    CUSTOM_IMAGE=frappe/erpnext
    CUSTOM_TAG=v15.25.0
    ```
4. Deploy

## Manual Setup

Once deployed, create the ERPNext site manually:

```bash
docker exec -it <backend-container> bash
bench new-site rayvensc.xyz --admin-password Rayvensc123@@ --mariadb-root-password Rayvensc123@@
bench --site rayvensc.xyz install-app erpnext
```
