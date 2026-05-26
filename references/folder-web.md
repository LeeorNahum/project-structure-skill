# Web Folder

Use `Web/` when a larger project root contains a website, dashboard, web app, docs site, landing page, or hosted configuration surface.

Use a separate web/app repo when the web surface has its own deploy, package manager, environment contract, CI, or release cadence.

## Common Shapes

```text
Project Name/
└── Web/
    └── <canonical-web-repo>/
```

```text
<canonical-web-repo>/
├── AGENTS.md
├── README.md
├── package.json
└── src/ or app/
```

Do not force a monorepo for a single small app. Use `apps/` and `packages/` only when there are multiple deployables or shared packages that justify the split.

## Ask Before

- Creating a deployable repo or remote
- Adding root env files
- Choosing a production domain, provider, or public app name
- Moving web code under a larger product root
