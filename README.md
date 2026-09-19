# Profile setup

## 1. File layout

Your `JackedUpProgrammer` repo should look like this:

```
README.md
assets/
  banner.svg
  certifications.svg
  mzansi-work.svg
  divider.svg
.github/
  workflows/
    metrics.yml
```

## 2. Turn on the GitHub stats cards

The stats cards are generated **into your own repo** on a schedule, so they
never break the way `github-readme-stats.vercel.app` does.

### Create the token

1. Go to **github.com → Settings → Developer settings → Personal access tokens → Tokens (classic)**
2. Click **Generate new token (classic)**
3. Name: `METRICS_TOKEN`
4. Expiration: `No expiration` (or 1 year, and renew)
5. Tick **only** this scope: `public_repo`
6. Generate, then copy the token

### Add it as a secret

1. Go to your `JackedUpProgrammer` repo → **Settings → Secrets and variables → Actions**
2. Click **New repository secret**
3. Name: `METRICS_TOKEN`
4. Value: paste the token
5. Save

### Run it

1. Go to the **Actions** tab in the repo
2. Select **Generate GitHub Metrics**
3. Click **Run workflow**

After about a minute, `assets/metrics.svg` and `assets/metrics-calendar.svg`
are committed to your repo and the cards appear on your profile. It then
refreshes automatically every day at 04:00 SAST.

## 3. Until the workflow runs

The section shows follower and star badges, which work immediately.
The two metrics images will show as broken until the workflow has run once.
That is expected.

## 4. Optional additions

- **LinkedIn badge** — not included, because I don't have your profile URL.
  Add it to the Contact section when ready.
- **Credly badges** — the certification graphic is custom-built. If you'd
  rather use official Microsoft badge images, grab the image URLs from your
  Credly profile and swap them into `assets/certifications.svg`.
