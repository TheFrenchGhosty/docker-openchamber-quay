# docker-openchamber-quay

An [OpenChamber](https://github.com/openchamber/openchamber) image, on Quay.

[Quay page](https://quay.io/repository/thefrenchghosty/openchamber)

## Tags

- `latest` tracks the latest OpenChamber release, installed from the `@openchamber/web` npm package.
- `edge` is built from the latest source (upstream `main` branch), compiled in-image.


## Usage

- Download (or copy the content of) the `docker-compose.yml`.
- Set `OPENCHAMBER_UI_PASSWORD` in it - the container binds `0.0.0.0`, so UI authentication is required.
- Create the folders OpenChamber needs with the right permissions (Docker would create them as root otherwise): `mkdir -p data/openchamber data/opencode/share data/opencode/state data/opencode/config data/ssh workspaces && chown -R 1000:1000 data workspaces`
- `docker compose up -d`
- The UI is available at `http://127.0.0.1:3000`.
