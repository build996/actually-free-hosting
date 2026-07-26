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
| **Oracle Cloud Always Free** | Up to **4 ARM cores + 24 GB RAM**, 2 AMD micro VMs, 200 GB storage | **No** | **No** (idle instances can be reclaimed unless you upgrade to a paid account) | [Guide](https://toolfreebie.com/oracle-free-arm-vps/) |

> Oracle's ARM allowance is the single most generous free-forever compute anywhere — enough to self-host almost anything on this page.

## App / backend hosting (PaaS)

| Platform | Free tier | Sleeps? | Expires? | Guide |
|---|---|---|---|---|
| **Render** | Free web services + static sites | **Yes** — web services spin down after ~15 min idle (static sites don't) | No | [Guide](https://toolfreebie.com/render-hosting-review/) |
| **Coolify** (self-hosted) | Open-source PaaS you run on your **own** server | **No** (it's your box) | No | [Guide](https://toolfreebie.com/coolify-self-hosted-paas/) |
| **Railway** | Trial credit, then usage-based | n/a | **Yes** — the old free tier is gone; now a limited trial | [Guide](https://toolfreebie.com/railway-heroku-alternative/) |

> 💡 The killer combo: run **Coolify on an Oracle Always-Free ARM box** → your own push-to-deploy Heroku, $0/month, no sleep, no expiry.

## Frontend / static hosting

| Platform | Free tier | Sleeps? | The catch | Guide |
|---|---|---|---|---|
| **Cloudflare Pages** | Unlimited requests & bandwidth, 500 builds/mo | **No** | Most generous; build minutes are the only real cap | [Guide](https://toolfreebie.com/vercel-netlify-cloudflare/) |
| **Netlify** | 100 GB bandwidth, 300 build min/mo | **No** | Bandwidth cap on busy sites | [Guide](https://toolfreebie.com/vercel-netlify-cloudflare/) |
| **Vercel** | Hobby tier, fast global edge | **No** | **Hobby is non-commercial only** — a real gotcha for monetized sites | [Guide](https://toolfreebie.com/vercel-netlify-cloudflare/) |

## Free databases & backend

| Platform | Free tier | Sleeps? | Expires? | Guide |
|---|---|---|---|---|
| **Turso** | 9 GB across 500 SQLite DBs, 1B row reads/mo | No | No | [Guide](https://toolfreebie.com/turso-free-sqlite-database/) |
| **Supabase** | 500 MB Postgres, auth, storage | **Pauses after ~1 week inactivity** | No | [Guide](https://toolfreebie.com/supabase-vs-neon/) |
| **Neon** | Serverless Postgres, scale-to-zero | Autosuspends, resumes on query | No | [Guide](https://toolfreebie.com/supabase-vs-neon/) |
| **Upstash** | Serverless Redis / vector, pay-per-use free allowance | No (serverless) | No | [Guide](https://toolfreebie.com/upstash-serverless-redis/) |
| **PocketBase** (self-hosted) | Whole backend in one file, on your own server | **No** | No | [Guide](https://toolfreebie.com/pocketbase-free-backend/) |
| **Appwrite** | Open-source Firebase alternative, self-host or cloud free tier | No (self-host) | No | [Guide](https://toolfreebie.com/appwrite-firebase-alternative/) |

---

## The one setup that beats them all

If you want free-forever hosting with **no sleep and no expiry**, stop hunting for the perfect PaaS free tier and do this instead:

1. Spin up an **Oracle Always-Free ARM VPS** (4 cores / 24 GB — free forever).
2. Install **Coolify** on it (open-source, one command).
3. You now have your own Heroku/Vercel: push-to-deploy, auto-SSL, databases — **$0/month, forever, no cold starts.**

Full walkthrough: **[Best Free Hosting 2026](https://toolfreebie.com/best-free-hosting-2026/)**

## Contributing

Spotted a tier that changed, started sleeping, or died? PRs welcome — see [CONTRIBUTING.md](CONTRIBUTING.md). Link the provider's own docs, and keep the **Sleeps? / Expires?** columns honest.

## License

[MIT](LICENSE) — maintained by [Tool Freebie](https://toolfreebie.com).
