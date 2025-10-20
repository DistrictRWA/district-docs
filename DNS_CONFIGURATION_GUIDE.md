# DNS Configuration Guide for docs.district.capital

## Overview

You need to point `docs.district.capital` to GitBook's hosting servers so your documentation is accessible at your custom domain.

## Step 1: Get GitBook's DNS Information

First, you need to get the exact DNS records from GitBook:

1. Go to https://gitbook.com
2. Open your District documentation space
3. Click on **Settings** (gear icon)
4. Go to **"Domain & URLs"** or **"Custom Domain"**
5. Click **"Add a custom domain"**
6. Enter: `docs.district.capital`
7. GitBook will show you the DNS records to add

## Step 2: Identify Your DNS Provider

Where is `district.capital` hosted? Common providers:

- **Cloudflare** (most common)
- **GoDaddy**
- **Namecheap**
- **Route 53 (AWS)**
- **Google Domains**
- **Other**

## Step 3: Add DNS Records

### Option A: CNAME Record (Recommended by GitBook)

**Record Type:** CNAME  
**Name/Host:** `docs` (or `docs.district.capital`)  
**Value/Points to:** `hosting.gitbook.io` (or the value GitBook provides)  
**TTL:** 3600 (or Auto)

### Option B: A Record (If CNAME doesn't work)

GitBook will provide specific IP addresses if needed.

---

## DNS Configuration by Provider

### If Using Cloudflare

1. Log in to https://dash.cloudflare.com
2. Select `district.capital` domain
3. Click **DNS** in the left menu
4. Click **Add record**
5. Configure:
   - **Type:** CNAME
   - **Name:** docs
   - **Target:** hosting.gitbook.io (or GitBook's provided value)
   - **Proxy status:** DNS only (gray cloud) ⚠️ Important!
   - **TTL:** Auto
6. Click **Save**

**Important for Cloudflare:**
- Turn OFF the orange cloud (proxy)
- Use "DNS only" mode (gray cloud)
- Otherwise SSL verification may fail

### If Using GoDaddy

1. Log in to https://account.godaddy.com
2. Go to **My Products** → **DNS**
3. Find `district.capital` and click **DNS**
4. Scroll to **Records** section
5. Click **Add** → **CNAME**
6. Configure:
   - **Host:** docs
   - **Points to:** hosting.gitbook.io
   - **TTL:** 1 Hour
7. Click **Save**

### If Using Namecheap

1. Log in to https://namecheap.com
2. Go to **Domain List**
3. Click **Manage** next to `district.capital`
4. Go to **Advanced DNS** tab
5. Click **Add New Record**
6. Configure:
   - **Type:** CNAME Record
   - **Host:** docs
   - **Value:** hosting.gitbook.io
   - **TTL:** Automatic
7. Click the green checkmark to save

### If Using AWS Route 53

1. Log in to AWS Console
2. Go to **Route 53** → **Hosted Zones**
3. Select `district.capital`
4. Click **Create Record**
5. Configure:
   - **Record name:** docs
   - **Record type:** CNAME
   - **Value:** hosting.gitbook.io
   - **TTL:** 300
   - **Routing policy:** Simple routing
6. Click **Create records**

### If Using Google Domains

1. Log in to https://domains.google.com
2. Select `district.capital`
3. Click **DNS** in the left menu
4. Scroll to **Custom resource records**
5. Add new record:
   - **Name:** docs
   - **Type:** CNAME
   - **TTL:** 1H
   - **Data:** hosting.gitbook.io
6. Click **Add**

---

## Step 4: Verify DNS Configuration

After adding the DNS record, verify it's working:

### Method 1: Online DNS Checker
- Go to https://dnschecker.org
- Enter: `docs.district.capital`
- Select: CNAME
- Click **Search**
- Wait for propagation (green checkmarks)

### Method 2: Command Line (Mac/Linux)

```bash
# Check CNAME record
dig docs.district.capital CNAME

# Or use nslookup
nslookup docs.district.capital
```

You should see `hosting.gitbook.io` (or GitBook's provided value) in the results.

---

## Step 5: Complete GitBook Setup

1. Go back to GitBook
2. In the custom domain settings
3. Click **Verify** or **Check DNS**
4. GitBook will verify the DNS records
5. Once verified, GitBook will provision SSL certificate (automatic)
6. Wait 5-15 minutes for SSL setup

---

## Troubleshooting

### DNS Not Propagating

**Issue:** DNS changes not showing up

**Solutions:**
- Wait 5-60 minutes (DNS propagation time)
- Clear your DNS cache:
  ```bash
  # Mac
  sudo dscacheutil -flushcache; sudo killall -HUP mDNSResponder
  
  # Windows
  ipconfig /flushdns
  ```
- Check multiple DNS checkers
- Verify you saved the record correctly

### Cloudflare Proxy Issues

**Issue:** SSL certificate won't verify

**Solution:**
- In Cloudflare DNS settings
- Click the orange cloud next to `docs` record
- Change to gray cloud (DNS only)
- Wait a few minutes and try again

### Wrong DNS Value

**Issue:** GitBook says DNS not configured

**Solution:**
- Double-check the CNAME value
- GitBook might provide a custom value like:
  - `hosting.gitbook.io`
  - `custom.gitbook.io`
  - Or a specific subdomain
- Use the EXACT value GitBook provides

### SSL Certificate Pending

**Issue:** Domain verified but SSL pending

**Solution:**
- This is normal - wait 5-15 minutes
- GitBook automatically provisions Let's Encrypt SSL
- Don't make DNS changes during this time
- Refresh the GitBook page to check status

---

## Expected Timeline

1. **Add DNS record:** 2 minutes
2. **DNS propagation:** 5-60 minutes (usually 10-15 minutes)
3. **GitBook verification:** Instant (once DNS propagates)
4. **SSL certificate:** 5-15 minutes (automatic)
5. **Total time:** 15-90 minutes typically

---

## Quick Reference

### What You Need

| Setting | Value |
|---------|-------|
| Record Type | CNAME |
| Name/Host | `docs` |
| Value/Target | `hosting.gitbook.io` (or GitBook's value) |
| TTL | 3600 or Auto |
| Proxy (Cloudflare) | OFF (gray cloud) |

### Verification Commands

```bash
# Check CNAME
dig docs.district.capital CNAME

# Check if site is accessible
curl -I https://docs.district.capital

# Check SSL certificate
openssl s_client -connect docs.district.capital:443 -servername docs.district.capital
```

---

## After DNS is Configured

Once everything is set up:

1. ✅ `docs.district.capital` will load your GitBook
2. ✅ SSL certificate will be active (https://)
3. ✅ Updates from GitHub will auto-deploy
4. ✅ Your documentation is live!

---

## Need Help?

**Can't find your DNS provider?**
- Check your domain registrar (where you bought district.capital)
- Check your email for domain-related messages
- Look for nameserver information

**Still having issues?**
- Share which DNS provider you're using
- Share the error message from GitBook
- Check if district.capital is using custom nameservers

**Common DNS Providers:**
- Cloudflare: https://dash.cloudflare.com
- GoDaddy: https://dcc.godaddy.com/manage/dns
- Namecheap: https://ap.www.namecheap.com/domains/list
- Google Domains: https://domains.google.com

---

## What's Your DNS Provider?

Let me know which provider you're using and I can give you specific step-by-step instructions!
