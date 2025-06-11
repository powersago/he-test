# Hurricane Electric IPv6 Certification – Test Site

This repository contains the minimal static files I’m using to satisfy the **“Enthusiast”** stage of [Hurricane Electric’s IPv6 Certification](https://ipv6.he.net/certification/).  
The site is served via **GitHub Pages** and is deliberately lightweight—just the verification file HE asks for and this README.

---

## Features

| ✨ What | ✔️ Why it matters |
|--------|------------------|
| **Native IPv6** via GitHub Pages | Lets HE verify the site over IPv6 only. |
| **Custom domain** support through `CNAME` | Clean “www.example.com” URL instead of `<username>.github.io`. |
| **Automatic HTTPS** | Free TLS certificate from Let’s Encrypt once GitHub Pages is enabled. |
| **FOSS license (GPL‑3.0)** | Feel free to fork, adapt, and share under the same terms. |

---

## Quick‑start

1. **Clone** the repo to your own GitHub account (fork or `gh repo clone`).

2. **Add the HE verification file**  
   Replace `he_verification.txt` with the file HE generated for you (e.g. `9e3c2a.txt`) and commit it to the repository root.

3. **Enable GitHub Pages**  
   - *Repo ➜ Settings ➜ Pages*  
   - **Source:** `main` branch / root (`/`).  
   - Click **Save** and note the Pages URL.

4. **Use a custom domain (optional but recommended)**  
   - Create a `CNAME` file (no extension) in the repo containing your domain, e.g. `www.example.com`.  
   - Add the required **AAAA** (and optional **A**) records at your DNS provider **or** create a proxied **CNAME** via Cloudflare.

5. **Verify IPv6 reachability**

   ```bash
   dig AAAA www.example.com +short      # should return GitHub Pages IPv6 blocks
   curl -6 http://www.example.com/9e3c2a.txt
