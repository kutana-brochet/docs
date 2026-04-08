# K+B Office Add-ins Documentation

This repository hosts the source and build pipeline for the K+B Office Add-ins documentation, published to GitHub Pages.

## Sites

| Site | Path | Description |
|------|------|-------------|
| User Documentation | [`/user`](user/) | End-user guides covering features, configuration, and licensing |
| Developer Documentation | [`/developer`](developer/) | Developer guides covering architecture, APIs, and patterns |

## Published Docs

Once deployed, the documentation is available at:

- **Root landing page**: `https://kutana-brochet.github.io/docs/`
- **User docs**: `https://kutana-brochet.github.io/docs/user/`
- **Developer docs**: `https://kutana-brochet.github.io/docs/developer/`

## How It Works

Documentation is built using [DocFX](https://dotnet.github.io/docfx/) and deployed to GitHub Pages via the [`docs.yml`](.github/workflows/docs.yml) workflow. The workflow runs automatically on every push to `main`.

## Local Development

### Prerequisites

- [.NET SDK 8.x or later](https://dotnet.microsoft.com/download)

### Setup

```bash
# Restore the DocFX tool
dotnet tool restore

# Build the User docs
dotnet tool run docfx user/docfx.json --serve

# Build the Developer docs (in a separate terminal)
dotnet tool run docfx developer/docfx.json --serve
```

The `--serve` flag starts a local web server so you can preview the output in your browser.

## Contributing

Add or edit Markdown files under `user/` or `developer/` and open a pull request against `main`. The workflow will build and deploy the updated docs automatically when merged.
