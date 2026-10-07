# Deployment

AI Diary is designed to be published automatically from GitHub to the production FTP space.

## Production flow

```text
ChatGPT / local edit
        ↓
GitHub repository
        ↓
push to main
        ↓
GitHub Actions
        ↓
FTP / FTPS
        ↓
https://emaf205.com/ideas/ai-library
```

The workflow is stored in:

```text
.github/workflows/deploy-ftp.yml
```

## One-time GitHub configuration

In the repository open:

```text
Settings
→ Secrets and variables
→ Actions
```

Create these **Repository secrets**:

- `FTP_HOST`
- `FTP_USER`
- `FTP_PASSWORD`

Then create this **Repository variable**:

- `FTP_REMOTE_DIR`

The actual password must never be committed to the repository.

## Remote directory

Set `FTP_REMOTE_DIR` to the FTP directory that corresponds to:

```text
https://emaf205.com/ideas/ai-library
```

Do not guess the path if the hosting control panel shows a specific document root.

## What is deployed

Only the public application files are packaged:

```text
index.html
manifest.webmanifest
sw.js
assets/
```

README, LICENSE, GitHub metadata and internal documentation are not uploaded to the website.

## Automatic deployment

A deployment runs when one of the public application files changes on the `main` branch.

It can also be triggered manually from:

```text
GitHub → Actions → Deploy AI Diary to FTP → Run workflow
```

## Reusing this for other EmaF205 projects

The same workflow can be copied to another static project.

Only four repository settings are required:

```text
FTP_HOST
FTP_USER
FTP_PASSWORD
FTP_REMOTE_DIR
```

Example destinations:

```text
AI Diary         → ideas/ai-library/
AI Policy Builder→ ideas/ai-policy-builder/
TORNO SUBITO     → ideas/torno-subito/
another tool     → ideas/project-name/
```

Each repository keeps its own destination directory, so projects remain isolated.

## Security

Credentials are stored in GitHub Actions Secrets and are referenced only at runtime.

Never commit FTP passwords, access tokens or private credentials to Git.


## Deploy on demand from ChatGPT

The repository includes a harmless file named:

```text
.deploy-trigger
```

The deployment workflow watches this file.

After the FTP credentials have been stored once in GitHub Actions Secrets, an authorized GitHub-connected assistant can trigger a production deployment without accessing or exposing those credentials by updating only `.deploy-trigger`.

This creates the following safe flow:

```text
request: "publish via FTP"
        ↓
update .deploy-trigger
        ↓
GitHub Actions starts
        ↓
credentials are injected privately by GitHub
        ↓
public files are uploaded to FTP
```

No FTP password is stored in the repository, commit history, README, deployment documentation or application files.
