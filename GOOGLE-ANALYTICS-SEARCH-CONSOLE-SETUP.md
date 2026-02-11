# Google Analytics & Search Console Setup Guide

This guide will walk you through setting up Google Analytics GA4 and Google Search Console for your Sanjeevani Cos Derma website.

---

## Part 1: Google Analytics GA4 Setup

### Step 1: Create Google Analytics Account

1. Go to [Google Analytics](https://analytics.google.com/)
2. Sign in with your Google account
3. Click **"Start measuring"** or **"Admin"** (bottom left)
4. Click **"Create Account"** if you don't have one

### Step 2: Set Up Property

1. **Account Name**: Enter "Sanjeevani Cos Derma"
2. Click **"Next"**
3. **Property Name**: Enter "Sanjeevani Cos Derma Website"
4. **Reporting Time Zone**: Select "(GMT+05:30) India Standard Time"
5. **Currency**: Select "Indian Rupee (₹)"
6. Click **"Next"**

### Step 3: Business Information

1. **Industry Category**: Select "Health & Fitness"
2. **Business Size**: Select your clinic size
3. Select business objectives (choose relevant ones):
   - Generate leads
   - Examine user behavior
   - Measure website conversions
4. Click **"Create"**
5. Accept Terms of Service

### Step 4: Set Up Data Stream

1. Choose **"Web"** platform
2. **Website URL**: Enter `https://sanjeevanicosderma.in`
3. **Stream Name**: Enter "Sanjeevani Website"
4. Click **"Create stream"**

### Step 5: Get Your Measurement ID

1. After creating the stream, you'll see **"Measurement ID"**
2. It looks like: `G-XXXXXXXXXX`
3. **Copy this ID** - you'll need it next

### Step 6: Add Measurement ID to Your Website

1. Open your `.env` file in the project root
2. Find the line: `PUBLIC_GA_MEASUREMENT_ID=`
3. Add your Measurement ID after the equals sign:
   ```
   PUBLIC_GA_MEASUREMENT_ID=G-XXXXXXXXXX
   ```
4. Save the file

**That's it!** Google Analytics is now configured. Data will start appearing in your GA4 dashboard within 24-48 hours.

---

## Part 2: Google Search Console Setup

### Step 1: Access Google Search Console

1. Go to [Google Search Console](https://search.google.com/search-console)
2. Sign in with the same Google account you used for Analytics
3. Click **"Add property"** or **"Start now"**

### Step 2: Choose Property Type

1. Select **"URL prefix"** (on the right side)
2. Enter your website URL: `https://sanjeevanicosderma.in`
3. Click **"Continue"**

### Step 3: Verify Ownership - HTML Tag Method

1. Google will show you several verification methods
2. Select **"HTML tag"** method
3. You'll see a meta tag that looks like:
   ```html
   <meta name="google-site-verification" content="abc123xyz456..." />
   ```
4. **Copy only the content value** (the part inside the quotes after `content=`)
   - Example: `abc123xyz456...`

### Step 4: Add Verification Code to Your Website

1. Open your `.env` file in the project root
2. Find the line: `PUBLIC_GSC_VERIFICATION=`
3. Paste your verification code after the equals sign:
   ```
   PUBLIC_GSC_VERIFICATION=abc123xyz456...
   ```
4. Save the file

### Step 5: Deploy and Verify

1. Deploy your website with the updated `.env` file
2. Wait 2-3 minutes for deployment to complete
3. Go back to Google Search Console
4. Click **"Verify"** button
5. You should see: "Ownership verified"

### Step 6: Submit Your Sitemap

1. In Google Search Console, click **"Sitemaps"** in the left menu
2. Under "Add a new sitemap", enter: `sitemap.xml`
3. Click **"Submit"**
4. Your sitemap URL will be: `https://sanjeevanicosderma.in/sitemap.xml`

✅ **Success!** Google will now start indexing your pages.

---

## Part 3: Verify Everything is Working

### Check Google Analytics

1. Go to [Google Analytics](https://analytics.google.com/)
2. Select your property
3. Go to **Reports** → **Realtime**
4. Open your website in a new tab
5. You should see yourself as an active user within 30 seconds

### Check Google Search Console

1. Go to [Google Search Console](https://search.google.com/search-console)
2. Select your property
3. Click **"URL Inspection"** at the top
4. Enter: `https://sanjeevanicosderma.in`
5. Click **"Test Live URL"**
6. If verified correctly, you'll see: "URL is on Google"

---

## Important Notes

### Analytics Data Timeline
- **Real-time data**: Appears within minutes
- **Regular reports**: Takes 24-48 hours to populate
- **Full insights**: Available after 7 days of data collection

### Search Console Timeline
- **Verification**: Immediate
- **First data**: 2-3 days after verification
- **Complete data**: 1-2 weeks for full indexing

### What to Monitor

**In Google Analytics:**
- Number of visitors
- Page views
- Most popular pages
- Traffic sources (Google, Facebook, Direct, etc.)
- User location (cities in India)
- Device types (Mobile vs Desktop)
- Conversion events (form submissions, calls)

**In Google Search Console:**
- Search queries bringing users to your site
- Click-through rates (CTR)
- Average position in search results
- Pages with indexing issues
- Mobile usability issues
- Core Web Vitals performance

---

## Setting Up Conversion Tracking (Optional but Recommended)

### Track Contact Form Submissions

Once Google Analytics is active, you can set up events to track:
- Contact form submissions
- Phone number clicks
- WhatsApp button clicks
- Appointment bookings

These insights will help you understand which pages drive the most leads.

---

## Troubleshooting

### Google Analytics not showing data?
1. Check that `PUBLIC_GA_MEASUREMENT_ID` is correctly set in `.env`
2. Clear your browser cache and reload your site
3. Check browser console for any errors (F12 → Console tab)
4. Verify the GA4 script is loaded (View Page Source → Search for "gtag")

### Google Search Console verification failed?
1. Verify `PUBLIC_GSC_VERIFICATION` is correctly set in `.env`
2. Deploy your changes and wait 2-3 minutes
3. Check the verification meta tag is in page source (View Page Source → Search for "google-site-verification")
4. Try verifying again

### Need Help?
- Google Analytics Help: https://support.google.com/analytics
- Search Console Help: https://support.google.com/webmasters
- Contact your developer for technical assistance

---

## Privacy & Compliance

Your website already includes:
- Privacy Policy page (with Google Analytics disclosure)
- Cookie consent (if needed, can be added)
- IP anonymization (automatically enabled in GA4)
- User data protection measures

Make sure to update your privacy policy if you add new tracking features.

---

## Summary

✅ **Google Analytics**: Tracks visitor behavior, traffic sources, and conversions
✅ **Google Search Console**: Monitors search performance, indexing, and technical issues
✅ **Sitemap**: Submitted for faster indexing
✅ **Structured Data**: Already configured (ratings, business info, etc.)

**Your website is now fully equipped with professional analytics and search tracking!**
