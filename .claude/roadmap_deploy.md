# Roadmap: Getting herelpt.com Live

## Step 1: Push to GitHub
```bash
# Create a repo on GitHub (do this in browser or with gh CLI)
gh repo create herelpt --public --source=. --push
# Or manually:
git remote add origin https://github.com/YOUR_USERNAME/herelpt.git
git push -u origin main
```

## Step 2: Deploy to Netlify (Free)
1. Go to https://netlify.com and sign in with GitHub
2. Click "Add new site" > "Import an existing project"
3. Select the `herelpt` repo
4. Build settings: leave blank (no build command needed, it's static HTML)
5. Click "Deploy site"
6. Your site will be live at something like `herelpt.netlify.app` within 60 seconds

**Alternative: Vercel**
1. Go to https://vercel.com and sign in with GitHub
2. Import the `herelpt` repo
3. Framework: "Other"
4. Deploy — live at `herelpt.vercel.app`

## Step 3: Connect herelpt.com Domain

### Option A: Transfer domain away from Squarespace
1. Log into Squarespace > Settings > Domains > herelpt.com
2. Click "Transfer domain" or "Get transfer code"
3. Copy the EPP/auth code
4. Transfer to a cheaper registrar (Cloudflare Domains = at cost, ~$10/year, or Namecheap)
5. Wait for transfer to complete (up to 5 days)
6. Then point DNS to Netlify (see Step 4)

### Option B: Keep domain at Squarespace, just change DNS
1. Log into Squarespace > Settings > Domains > herelpt.com > DNS Settings
2. Delete the existing Squarespace records
3. Add Netlify DNS records (see Step 4)
4. This is faster but you keep paying Squarespace for the domain (~$20/year)

## Step 4: Point DNS to Netlify
In Netlify:
1. Go to Site settings > Domain management > Add custom domain
2. Type `herelpt.com`
3. Netlify will give you DNS records to add:
   - A record: `75.2.60.5` (Netlify load balancer)
   - CNAME for www: `your-site-name.netlify.app`
4. Add these records at your domain registrar (Squarespace, Cloudflare, or wherever)
5. Enable HTTPS in Netlify (automatic with Let's Encrypt)

## Step 5: Cancel Squarespace
1. Verify the new site is working at herelpt.com
2. Test all pages, forms, links
3. Go to Squarespace > Account > Billing
4. Cancel your Squarespace subscription
5. Keep the domain registered (either at Squarespace or transfer it out)

## Timeline
- Step 1-2: 10 minutes
- Step 3 (Option B): 1-2 hours for DNS propagation
- Step 3 (Option A): 1-5 days for domain transfer
- Step 4: 5 minutes + up to 48 hours DNS propagation
- Step 5: After everything is confirmed working

## Cost After Migration
- Domain registration: ~$10-20/year (Cloudflare or Squarespace)
- Hosting: $0 (Netlify free tier)
- SSL: $0 (automatic via Netlify)
- Total: ~$10-20/year vs whatever you're paying Squarespace now

## Before Going Live Checklist
- [ ] Fix remaining wrong photos (Dr. Phil headshot, verify Anna/Monica)
- [ ] Connect contact form to a backend (Netlify Forms is free, just add `netlify` attribute to the form tag)
- [ ] Test on mobile
- [ ] Test all nav links work across all pages
- [ ] Verify Google Maps embed loads
- [ ] Add real intake form PDFs to download links
- [ ] Set up Google Analytics or Plausible (optional)
- [ ] Add favicon
- [ ] Test video loads on mobile (may need fallback image)
