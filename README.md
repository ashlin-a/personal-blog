# Ashlin Blog

This is my personal blog built with [Hugo](https://gohugo.io/) and the [Blowfish](https://blowfish.page/) theme.  
It is deployed on [Cloudflare Workers](https://developers.cloudflare.com/workers/) with automated deployments from GitHub.

Live Site: [https://blog.ashlin.dev](https://blog.ashlin.dev)

---

## Features
- **Static site generation** with Hugo  
- **Modern theme** using Blowfish  
- **Automatic deployment** via GitHub → Cloudflare Workers  
- **Custom build script** powered by Wrangler  

---

## Tech Stack
- [Hugo](https://gohugo.io/)  
- [Blowfish Theme](https://blowfish.page/)  
- [Cloudflare Workers](https://developers.cloudflare.com/workers/)  
- [Wrangler](https://developers.cloudflare.com/workers/wrangler/)  
- GitHub Actions (CI/CD)  


## Deployment Workflow
1. Push changes to the **main** branch on GitHub.  
2. GitHub triggers Cloudflare Workers via Wrangler.  
3. Wrangler runs the **build script (`build.sh`)**, which:  
   - Builds the Hugo site.  
   - Deploys the static files to Cloudflare.  
4. The site updates automatically 🎉  


## Local Development
Run the blog locally with Hugo:

```bash
# Install Hugo (extended version recommended)
brew install hugo      # macOS
sudo apt install hugo  # Ubuntu/Debian

# Clone the repository
git clone https://github.com/ashlin-a/personal-blog.git
cd personal-blog

# Start local dev server
hugo server -D
````

Then open [http://localhost:1313](http://localhost:1313).


## Manual Deployment

You can also deploy manually if needed:

```bash
# Install Wrangler
npm install -g wrangler

# Publish to Cloudflare
wrangler publish
```


## License

This repository is licensed under the **GNU General Public License v3.0 (GPL-3.0)**.

You are free to use, modify, and share the setup/config files under the terms of this license.
**Note:** The blog content itself is personal and not intended for reuse.

For full license details, see the [LICENSE](./LICENSE) file.
