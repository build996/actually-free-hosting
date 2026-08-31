# Actually Free Hosting

A maintained list of hosting that is **actually free** — not "free trial credit" free — and, just as important, **which "free" tiers sleep, throttle, or expire on you.**

Every "free hosting" list tells you a platform has a free tier. Almost none tell you the two things that actually decide whether your project stays up:

- **Does it sleep?** (spin down after inactivity, cold-starting your users)
- **Does it expire?** (trial credit that runs out, or a tier that gets reclaimed)

This repo puts those columns front and center. Each row links to a hands-on guide with the current details.

> ⚠️ Free hosting tiers change often (Railway and Fly.io both cut their old free allowances). Numbers here stay qualitative where a provider's terms move — always confirm against the linked guide before you build.

---

## Always-free compute (VPS / servers)

| Platform | Free tier | Sleeps? | Expires? | Guide |
|---|---|---|---|---|
| **Oracle Cloud Always Free** | **2 ARM cores + 12 GB RAM** (halved from 4/24 in 2026), 2 AMD micro VMs, 200 GB storage | **No** | **No** (idle instances can be reclaimed unless you upgrade to a paid account) | [Guide](https://toolfreebie.com/oracle-free-arm-vps/) |

> Oracle's ARM allowance is the single most generous free-forever compute anywhere — enough to self-host almost anything on this page.

## App / backend hosting (PaaS)

| Platform | Free tier | Sleeps? | Expires? | Guide |
|---|---|---|---|---|
| **Render** | Free web services + static sites | **Yes** — web services spin down after ~15 min idle (static sites don't) | No | [Guide](https://toolfreebie.com/render-hosting-review/) |
| **Coolify** (self-hosted) | Open-source PaaS you run on your **own** server | **No** (it's your box) | No | [Guide](https://toolfreebie.com/coolify-self-hosted-paas/) |
| **Railway** | Trial credit, then usage-based | n/a | **Yes** — the old free tier is gone; now a limited trial | [Guide](https://toolfreebie.com/railway-heroku-alternative/) |
| **Hugging Face Spaces** | Free tier to host AI demos/apps, incl. ZeroGPU | **Yes** — free Spaces sleep after inactivity | No | [Guide](https://toolfreebie.com/hugging-face-spaces-free-gpu/) |
| **Koyeb** | Free tier **closed to new users** (2026) — see alternatives | n/a | **Yes** — free Starter gone; guide lists free hosts that don't sleep | [Guide](https://toolfreebie.com/koyeb-free-tier-alternatives/) |

> 💡 The killer combo: run **Coolify on an Oracle Always-Free ARM box** → your own push-to-deploy Heroku, $0/month, no sleep, no expiry.

## Frontend / static hosting

| Platform | Free tier | Sleeps? | The catch | Guide |
|---|---|---|---|---|
| **Cloudflare Pages** | Unlimited requests & bandwidth, 500 builds/mo | **No** | Most generous; build minutes are the only real cap | [Guide](https://toolfreebie.com/vercel-netlify-cloudflare/) |
| **Netlify** | 100 GB bandwidth, 300 build min/mo | **No** | Bandwidth cap on busy sites | [Guide](https://toolfreebie.com/vercel-netlify-cloudflare/) |
| **Vercel** | Hobby tier, fast global edge | **No** | **Hobby is non-commercial only** — a real gotcha for monetized sites | [Guide](https://toolfreebie.com/vercel-netlify-cloudflare/) |

## Traditional / PHP shared hosting

Old-school cPanel-style hosting for WordPress and PHP sites — genuinely free, no trial credit.

| Platform | Free tier | Sleeps? | The catch | Guide |
|---|---|---|---|---|
| **InfinityFree** | Free PHP + MySQL hosting, free subdomain, generous quotas | **No** | No SSH; daily-hits soft limit; upsell nags | [Guide](https://toolfreebie.com/infinityfree-free-php-hosting/) |
| **AwardSpace** | 1 GB space + PHP + 1 MySQL DB, **connect your own domain** | **No** | Small quotas; 1 website on the free tier | [Guide](https://toolfreebie.com/awardspace-free-hosting/) |

## Free databases & backend

| Platform | Free tier | Sleeps? | Expires? | Guide |
|---|---|---|---|---|
| **Turso** | 9 GB across 500 SQLite DBs, 1B row reads/mo | No | No | [Guide](https://toolfreebie.com/turso-free-sqlite-database/) |
| **Supabase** | 500 MB Postgres, auth, storage | **Pauses after ~1 week inactivity** | No | [Guide](https://toolfreebie.com/supabase-vs-neon/) |
| **Neon** | Serverless Postgres, scale-to-zero | Autosuspends, resumes on query | No | [Guide](https://toolfreebie.com/supabase-vs-neon/) |
| **Upstash** | Serverless Redis / vector, pay-per-use free allowance | No (serverless) | No | [Guide](https://toolfreebie.com/upstash-serverless-redis/) |
| **PocketBase** (self-hosted) | Whole backend in one file, on your own server | **No** | No | [Guide](https://toolfreebie.com/pocketbase-free-backend/) |
| **Appwrite** | Open-source Firebase alternative, self-host or cloud free tier | No (self-host) | No | [Guide](https://toolfreebie.com/appwrite-firebase-alternative/) |
| **Object storage (R2 / B2 / Tigris)** | Free storage + egress allowances for S3-style object storage | No | No | [Guide](https://toolfreebie.com/free-object-storage/) |
| **Vector DBs (Qdrant / Pinecone / Chroma)** | Free tiers for vector search / RAG | No | No | [Guide](https://toolfreebie.com/free-vector-database-rag/) |

---

## The one setup that beats them all

If you want free-forever hosting with **no sleep and no expiry**, stop hunting for the perfect PaaS free tier and do this instead:

1. Spin up an **Oracle Always-Free ARM VPS** (2 cores / 12 GB — free forever).
2. Install **Coolify** on it (open-source, one command).
3. You now have your own Heroku/Vercel: push-to-deploy, auto-SSL, databases — **$0/month, forever, no cold starts.**

Full walkthrough: **[Best Free Hosting 2026](https://toolfreebie.com/best-free-hosting-2026/)**

---

## Related lists

Part of a small set of measured, regularly re-checked references:

| Repo | Covers |
|---|---|
| **[awesome-free-ai-apis](https://github.com/build996/awesome-free-ai-apis)** | The AI APIs you'd run on this hosting — real limits, catches, licensing traps |
| **[free-ai-api-benchmark](https://github.com/build996/free-ai-api-benchmark)** | Measured speed and quotas for those APIs, re-run weekly |
| **[free-host-speedtest](https://github.com/build996/free-host-speedtest)** | A page for measuring free hosting speed yourself |

The same question drives all of them: **is it actually free, and does it actually work?** Free tiers collapsed across the board in 2026 — several AI APIs that were card-free last year now demand payment — so every entry gets re-checked rather than copied forward.

## Contributing

Spotted a tier that changed, started sleeping, or died? PRs welcome — see [CONTRIBUTING.md](CONTRIBUTING.md). Link the provider's own docs, and keep the **Sleeps? / Expires?** columns honest.

## License

[MIT](LICENSE) — maintained by [Tool Freebie](https://toolfreebie.com).
