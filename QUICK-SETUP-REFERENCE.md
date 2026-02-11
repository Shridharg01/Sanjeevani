# Quick Setup Reference - Google Analytics & Search Console

## What You Need to Do

### 1. Get Your Google Analytics Measurement ID

1. Go to https://analytics.google.com/
2. Create account → Create property
3. Add web stream with URL: `https://sanjeevanicosderma.in`
4. Copy your **Measurement ID** (looks like `G-XXXXXXXXXX`)

### 2. Get Your Google Search Console Verification Code

1. Go to https://search.google.com/search-console
2. Add property: `https://sanjeevanicosderma.in`
3. Choose "HTML tag" verification method
4. Copy the **verification code** (the content value from the meta tag)

### 3. Add to Your .env File

Open `.env` file and add:

```env
PUBLIC_GA_MEASUREMENT_ID=G-XXXXXXXXXX
PUBLIC_GSC_VERIFICATION=your_verification_code_here
```

### 4. Deploy Your Website

After updating the `.env` file, deploy your website. The tracking will be active immediately.

### 5. Complete Search Console Verification

1. Wait 2-3 minutes after deployment
2. Go back to Google Search Console
3. Click "Verify" button
4. Submit sitemap: `sitemap.xml`

---

## What's Already Done

✅ Google Analytics GA4 tracking code is installed
✅ Google Search Console verification meta tag is configured
✅ Both will activate automatically when you add your IDs
✅ Sitemap.xml is ready at `/sitemap.xml`
✅ All structured data includes 4.9/5 rating

---

## Need Detailed Instructions?

See the complete guide: `GOOGLE-ANALYTICS-SEARCH-CONSOLE-SETUP.md`

---

## Verification

**Test Google Analytics:**
- Visit your site → Check "Realtime" report in GA4
- You should see yourself as an active user

**Test Search Console:**
- Go to "URL Inspection"
- Test your homepage URL
- Should show "URL is on Google" after verification
