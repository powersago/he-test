# Hurricane Electric IPv6 Certification – Test Site

This repository holds the minimal static files used to satisfy the **“Enthusiast”** stage of [Hurricane Electric’s IPv6 Certification](https://ipv6.he.net/certification/).  
The site is served via **GitHub Pages** and is intentionally lightweight—just the verification file HE requests plus this README.

---

## Features

| ✨ What | ✔️ Why it matters |
|--------|------------------|
| **Native IPv6** via GitHub Pages | Lets HE verify the site over IPv6 only. |
| **Automatic HTTPS** | Free TLS certificate from Let’s Encrypt once GitHub Pages is enabled. |
| **FOSS license (GPL‑3.0)** | Fork, adapt, and share under the same terms. |

---

## Quick‑start

1. **Clone** the repo to your own GitHub account (fork or `gh repo clone`).

2. **Add the HE verification file**  
   Replace `he_verification.txt` with the file HE generated for you (e.g. `9e3c2a.txt`) and commit it to the repository root.

3. **Enable GitHub Pages**  
   - *Repo ➜ Settings ➜ Pages*  
   - **Source:** `main` branch / root (`/`).  
   - Click **Save** and note the Pages URL.

4. **Verify IPv6 reachability**

   ```bash
   curl -6 https://<username>.github.io/<repo‑name>/9e3c2a.txt
