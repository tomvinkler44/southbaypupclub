# South Bay Pup Club: going live on Vercel

The site is plain HTML: one `index.html` plus an `images/` folder. There's no build step.

## 1. Create the Vercel project (pick one option)

### Option A: GitHub (no command line, auto-updates later)
1. On github.com, click **New repository**, name it `southbaypupclub`, and click **Create**.
2. Click **uploading an existing file**. Drag in `index.html`, `DEPLOY.md` and the `images` folder, then click **Commit changes**.
3. On vercel.com, click **Add New → Project**, pick `southbaypupclub`, and click **Import**.
4. Leave **Framework Preset** on **Other** and click **Deploy**.

### Option B: Command line (if you have Node installed)
```bash
cd southbaypupclub      # the unzipped folder
npx vercel --prod       # log in when asked and accept the defaults
```

## 2. Connect southbaypupclub.com

In the Vercel project, go to **Settings → Domains**, add `southbaypupclub.com`, and accept the `www` redirect.

- **If you switched Namecheap's nameservers to Vercel** (`ns1.vercel-dns.com` / `ns2.vercel-dns.com`): you're done. Vercel manages DNS from now on, so the A/CNAME records in Namecheap's Advanced DNS no longer matter.
- **If you kept Namecheap's own DNS** ("Namecheap BasicDNS"): use exactly two records in Advanced DNS, with nothing else for `@` or `www`:
  - A Record, Host `@`, Value `76.76.21.21`
  - CNAME Record, Host `www`, Value `cname.vercel-dns.com`

Within a few minutes to a couple of hours, the domain turns ✅ and HTTPS turns on automatically.

## 3. Activate the contact form (one time)

The form sends to vinkler@gmail.com through FormSubmit, which is free and needs no account.

1. After the site is live, submit the form once yourself.
2. FormSubmit emails you an activation link. Click it.
3. Every request after that lands in your inbox.

Check your spam folder if the activation email doesn't show up.

## 4. Editing later

- **Prices:** edit the services cards and the pricing table in `index.html`.
- **Photos:** replace the files in `images/`, keeping the same names (`park.jpg`, `portrait.jpg`, `mascot.png`).
- **Reviews:** the testimonials section is commented out in the HTML. Uncomment it once you have real client quotes.
