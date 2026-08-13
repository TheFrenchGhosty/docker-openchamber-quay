# docker-openchamber-quay

An [OpenChamber](https://github.com/openchamber/openchamber) image, on Quay.

[Quay page](https://quay.io/repository/thefrenchghosty/openchamber)

## Tags

- `latest` tracks the latest OpenChamber release, installed from the `@openchamber/web` npm package.
- `edge` is built from the latest source (upstream `main` branch), compiled in-image.

Both tags are rebuilt every 3 hours.

## Usage

- Download (or copy the content of) the `docker-compose.yml`.
- Set `OPENCHAMBER_UI_PASSWORD` in it - the container binds `0.0.0.0`, so UI authentication is required.
- `docker compose up -d`
- The UI is available at `http://127.0.0.1:3000`.

---

Image structure based on upstream's [Dockerfile](https://github.com/openchamber/openchamber); packaging repo modeled on [docker-priviblur-quay](https://github.com/PussTheCat-org/docker-priviblur-quay).
