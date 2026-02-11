# WordPress Migration Phase 4: SEO Implementation & Testing
## Sanjeevani Cos Derma - Structured Data & Search Engine Optimization

**Duration:** 5 business days (Week 6)
**Status:** Implementation Ready
**Last Updated:** February 2026

---

## Phase 4 Overview

Phase 4 optimizes the WordPress site for search engines by implementing comprehensive SEO:
- 6 JSON-LD structured data schemas
- 301 redirects from Astro URLs
- Yoast SEO per-page optimization
- Local business setup (Google My Business)
- Google Search Console configuration
- Analytics implementation

---

## Step 4.1: JSON-LD Schema Configuration (Day 1 - 2 hours)

### Access Yoast SEO Schema Settings

Admin → Yoast SEO → Appearance in Search → Schema

### Schema 1: Medical Business (Organization)

**Navigate to:** Yoast SEO → Appearance in Search → Organization

**Settings:**

```
Organization Name: Sanjeevani Cos Derma
Organization Logo: [Upload clinic logo]
Logo URL: https://sanjeevanicosderma.in/wp-content/uploads/logo.png

Organization Type: Medical Business

Contact Information:
  Telephone: +91 82962 80340
  Email: cosdermasanjeevani@gmail.com

Address:
  Street: Sunrise Complex, 1693/A/32, Dr Rajkumar Rd
  City: Bangalore
  State: Karnataka
  Postal Code: 560010
  Country: India

URL: https://sanjeevanicosderma.in
```

**Click: Save**

This generates:
```json
{
  "@type": "MedicalBusiness",
  "name": "Sanjeevani Cos Derma",
  "medicalSpecialty": ["Dermatology", "Cosmetology"],
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "Sunrise Complex, 1693/A/32, Dr Rajkumar Rd",
    "addressLocality": "Rajajinagar, Bangalore",
    "addressRegion": "Karnataka",
    "postalCode": "560010",
    "addressCountry": "IN"
  },
  "telephone": "+91 82962 80340",
  "email": "cosdermasanjeevani@gmail.com"
}
```

---

### Schema 2: Local Business

**Navigate to:** Yoast SEO → Appearance in Search → Local Business

**Settings:**

```
Business Type: Medical Practice

Business Name: Sanjeevani Cos Derma

Address:
  Street: Sunrise Complex, 1693/A/32, Dr Rajkumar Rd
  City: Bangalore (or Bengaluru)
  State: Karnataka
  Country: India
  Postal Code: 560010

Coordinates:
  Latitude: 12.9716
  Longitude: 77.5546

Phone: +91 82962 80340

Service Radius:
  Enabled: YES
  Radius: 50 km
  Location: Bangalore

Opening Hours:
  Monday: 10:30 AM - 6:30 PM
  Tuesday: 10:30 AM - 6:30 PM
  Wednesday: 10:30 AM - 6:30 PM
  Thursday: 10:30 AM - 6:30 PM
  Friday: 10:30 AM - 6:30 PM
  Saturday: 10:30 AM - 6:30 PM
  Sunday: 10:30 AM - 6:30 PM

  Special Hours:
  [Add if clinic is closed certain holidays]

Price Range: ₹ (Indian Rupees)

URL: https://sanjeevanicosderma.in
```

**Click: Save**

---

### Schema 3: Aggregate Rating

**Navigate to:** Yoast SEO → Appearance in Search → Knowledge Graph

Add this to Local Business setup:

```
Aggregate Rating:
  Enabled: YES
  Rating Value: 4.9
  Best Rating: 5
  Worst Rating: 1
  Review Count: 150+
  Base: Google Reviews / Patient Testimonials
```

Generates:
```json
{
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.9",
    "bestRating": "5",
    "worstRating": "1",
    "reviewCount": "150"
  }
}
```

---

### Schema 4: Medical Organization Services

**Using:** Yoast SEO + Schema Pro (if installed)

Or manually add via **Yoast SEO → Appearance in Search → Custom**

Add custom JSON-LD block:

```json
{
  "@context": "https://schema.org",
  "@type": "MedicalOrganization",
  "name": "Sanjeevani Cos Derma",
  "description": "Premier hair transplant and skin treatment clinic",
  "foundingDate": "2009",
  "url": "https://sanjeevanicosderma.in",
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Hair and Skin Treatments",
    "itemListElement": [
      {
        "@type": "Offer",
        "name": "FUE Hair Transplant",
        "description": "Advanced follicular unit extraction technique",
        "url": "https://sanjeevanicosderma.in/hair-transplant/",
        "price": "200000",
        "priceCurrency": "INR",
        "availability": "https://schema.org/InStock"
      },
      {
        "@type": "Offer",
        "name": "Pen-Implanter Hair Transplant",
        "description": "Most advanced hair transplant technique",
        "url": "https://sanjeevanicosderma.in/hair-transplant/",
        "price": "350000",
        "priceCurrency": "INR",
        "availability": "https://schema.org/InStock"
      },
      {
        "@type": "Offer",
        "name": "GFC Hair Treatment",
        "description": "Non-surgical hair loss treatment",
        "url": "https://sanjeevanicosderma.in/gfc-hair-treatment-bengaluru/",
        "price": "50000",
        "priceCurrency": "INR",
        "availability": "https://schema.org/InStock"
      },
      {
        "@type": "Offer",
        "name": "Skin Treatments",
        "description": "Comprehensive skin treatments including HydraFacial, chemical peels, laser therapy",
        "url": "https://sanjeevanicosderma.in/skin-treatments/",
        "price": "25000",
        "priceCurrency": "INR",
        "availability": "https://schema.org/InStock"
      }
    ]
  },
  "areaServed": {
    "@type": "City",
    "name": "Bangalore",
    "state": "Karnataka",
    "country": "India"
  }
}
```

---

### Schema 5: FAQPage Schema

**Navigate to:** Yoast SEO → Appearance in Search → FAQ

**Method 1: Manual FAQ Schema**

Create FAQ page in WordPress:
- Admin → Pages → Add New
- Title: "Frequently Asked Questions"
- Slug: faq

Edit with Elementor:
- Add FAQ accordion with questions and answers
- Yoast automatically detects and generates FAQPage schema

**Method 2: Custom Schema**

If using custom FAQ CPT, use **Schema Pro** plugin to auto-generate:

```json
{
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Is hair transplant procedure painful?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No, modern hair transplant procedures are painless. We use local anesthesia to numb the donor and recipient areas..."
      }
    },
    {
      "@type": "Question",
      "name": "How long does recovery take?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Recovery varies by technique. FUE takes 7-10 days, Pen-Implanter takes 3-5 days..."
      }
    },
    {
      "@type": "Question",
      "name": "When will I see results?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Hair growth typically begins at 3-4 months. Full results are visible at 12-14 months..."
      }
    }
  ]
}
```

---

### Schema 6: WebSite Schema

**Automatic via Yoast SEO:**

Yoast automatically generates WebSite schema including:

```json
{
  "@type": "WebSite",
  "url": "https://sanjeevanicosderma.in",
  "potentialAction": {
    "@type": "SearchAction",
    "target": {
      "@type": "EntryPoint",
      "urlTemplate": "https://sanjeevanicosderma.in/?s={search_term_string}"
    },
    "query-input": "required name=search_term_string"
  }
}
```

**Verify:** Yoast SEO → Appearance in Search → WebSite

---

### Verify All Schemas

**Google Rich Result Tester:**
1. Visit: https://search.google.com/test/rich-results
2. Enter: https://sanjeevanicosderma.in
3. Check for:
   - ✓ Organization (MedicalBusiness)
   - ✓ LocalBusiness
   - ✓ AggregateRating
   - ✓ WebSite
4. No errors should appear

**Alternative Testing:**
- https://validator.schema.org
- https://www.structured-data-linter.com

---

## Step 4.2: URL Redirects from Astro to WordPress (Day 2 - 1.5 hours)

### Create .htaccess Redirects

**Access:** Admin → Tools → File Manager
**Path:** /public_html/.htaccess

Add these redirects (keep existing WordPress rules):

```apache
# ========================================
# Astro to WordPress Redirects
# ========================================
# Permanent redirects (301) from .astro URLs to WordPress URLs

<IfModule mod_rewrite.c>
RewriteEngine On
RewriteBase /

# Remove .astro extension redirects
RewriteCond %{THE_REQUEST} ^[A-Z]{3,9}\ /([^\ ]+)\.astro [NC]
RewriteRule ^(.*)\.astro$ /$1/ [L,R=301]

# Specific service page redirects
RewriteRule ^hair-transplant\.astro$ /hair-transplant/ [R=301,L]
RewriteRule ^skin-treatments\.astro$ /skin-treatments/ [R=301,L]
RewriteRule ^acne-treatment-bengaluru\.astro$ /acne-treatment-bengaluru/ [R=301,L]
RewriteRule ^laser-hair-removal-bengaluru\.astro$ /laser-hair-removal-bengaluru/ [R=301,L]
RewriteRule ^gfc-hair-treatment-bengaluru\.astro$ /gfc-hair-treatment-bengaluru/ [R=301,L]
RewriteRule ^prp-hair-treatment-bengaluru\.astro$ /prp-hair-treatment-bengaluru/ [R=301,L]
RewriteRule ^hydrafacial-bengaluru\.astro$ /hydrafacial-bengaluru/ [R=301,L]
RewriteRule ^chemical-peel-bengaluru\.astro$ /chemical-peel-bengaluru/ [R=301,L]
RewriteRule ^cosmetic-dermatology-bengaluru\.astro$ /cosmetic-dermatology-bengaluru/ [R=301,L]

# Blog and other pages
RewriteRule ^blog\.astro$ /blog/ [R=301,L]
RewriteRule ^results\.astro$ /results/ [R=301,L]
RewriteRule ^about\.astro$ /about/ [R=301,L]
RewriteRule ^contact\.astro$ /contact/ [R=301,L]
RewriteRule ^privacy-policy\.astro$ /privacy-policy/ [R=301,L]
RewriteRule ^terms-of-service\.astro$ /terms-of-service/ [R=301,L]
RewriteRule ^accessibility\.astro$ /accessibility/ [R=301,L]

# Root redirect
RewriteRule ^index\.astro$ / [R=301,L]

</IfModule>
```

**Alternative Using Yoast SEO Redirects:**

1. Admin → Yoast SEO → Tools → Redirects
2. Click "Add redirect"
3. Create 301 redirect for each Astro URL:

   ```
   Old URL: /hair-transplant.astro
   New URL: /hair-transplant/
   Type: 301 Permanent redirect
   ```

   Repeat for all pages

4. Export redirects list for record-keeping

---

## Step 4.3: Yoast SEO Per-Page Optimization (Day 2-3 - 3 hours)

### Optimize Homepage

Admin → Pages → Edit "Homepage" → Edit with Elementor
(Or scroll down to Yoast SEO meta box)

**Yoast SEO Settings:**

```
Focus Keyphrase: "hair transplant bangalore"

Title:
"Hair Transplant in Bangalore | Pen-Implanter | FUE | Sanjeevani Cos Derma"
(60 characters - includes primary keyword twice)

Meta Description:
"Best hair transplant clinic in Bangalore with 98% success rate. Expert surgeons, natural results. Book free consultation. ₹2L+. Call +91 82962 80340"
(158 characters)

Slug: / (homepage)

Readability: Aim for green (all checks passing)

Focus on:
- Keyphrase in intro paragraph
- Keyphrase in H2/H3 headings
- Internal links with focus keyphrase as anchor
- Meta description includes call to action
```

### Optimize Hair Transplant Service Page

Admin → Pages → Edit "Hair Transplant" (service page)

**Yoast SEO Settings:**

```
Focus Keyphrase: "best hair transplant clinic rajajinagar bangalore"

Title:
"Best Hair Transplant Clinic in Rajajinagar | FUE | Pen-Implanter | Sanjeevani"
(66 characters)

Meta Description:
"Premier hair transplant clinic in Rajajinagar, Bangalore. FUE, Pen-Implanter techniques. 500+ cases, 98% success. Natural results. Free consultation."
(154 characters)

Keyphrase Variations:
- hair transplant bangalore
- FUE hair transplant
- pen implanter technique
- hair transplant rajajinagar
- best hair transplant surgeon

Internal Links:
- Link to GFC treatment page with "non-surgical hair loss treatment"
- Link to results page with "before after hair transplant"
- Link to testimonials with patient stories
```

### Optimize Other Service Pages

Repeat for each page (7 total):

**Acne Treatment:**
```
Keyphrase: "acne treatment bangalore"
Title: "Acne Treatment in Bangalore | Laser | Chemical Peels | Sanjeevani"
Meta: "Advanced acne treatment clinic in Bangalore using laser, chemical peels, and dermatology. Clear skin guaranteed. ₹5K+. Book online."
```

**Laser Hair Removal:**
```
Keyphrase: "laser hair removal bangalore"
Title: "Permanent Laser Hair Removal in Bangalore | Fast & Painless"
Meta: "Professional laser hair removal in Bangalore for face and body. Permanent results. Painless. Advanced technology. ₹500/session."
```

**GFC Hair Treatment:**
```
Keyphrase: "GFC hair treatment bangalore"
Title: "GFC Hair Treatment in Bangalore | Non-Surgical | Painless"
Meta: "Effective non-surgical hair loss treatment using GFC therapy. Stimulate hair growth. 6 sessions. Results in 3 months. Book now."
```

**PRP Hair Treatment:**
```
Keyphrase: "PRP hair treatment bangalore"
Title: "PRP Hair Treatment in Bangalore | Hair Loss Solution"
Meta: "PRP therapy for hair loss. Stimulates natural hair growth. 6-8 sessions. Safe and effective. Free consultation."
```

**HydraFacial:**
```
Keyphrase: "hydrafacial bangalore"
Title: "HydraFacial in Bangalore | Skin Rejuvenation | Deep Cleansing"
Meta: "Advanced HydraFacial treatment for skin rejuvenation. Removes impurities, hydrates skin. ₹3K+. Monthly maintenance recommended."
```

**Chemical Peel:**
```
Keyphrase: "chemical peel bangalore"
Title: "Chemical Peel Treatment in Bangalore | Acne Scars | Pigmentation"
Meta: "Professional chemical peel for acne scars, pigmentation, and skin renewal. Safe procedure. Visible results. Book consultation."
```

**Cosmetic Dermatology:**
```
Keyphrase: "cosmetic dermatology bangalore"
Title: "Cosmetic Dermatology in Bangalore | Skin Treatments"
Meta: "Expert cosmetic dermatology services. Anti-aging, skin rejuvenation, specialized treatments. Affordable pricing."
```

### Optimize Blog Posts

Admin → Posts → Edit [Post Title]

**For each blog post:**

```
Focus Keyphrase: [Primary keyword from blog.js SEO keywords]

Example - Post 1:
Keyphrase: "best hair transplant clinic rajajinagar bangalore"
Title: Use existing title (if already optimized)
Meta: Create 155-160 character description

Example - Post 2:
Keyphrase: "FUE hair transplant bangalore"
Title: "FUE vs Pen-Implanter: Which Hair Transplant is Best?"
Meta: "Expert comparison of FUE and Pen-Implanter techniques. Learn which method is best for your hair loss pattern and budget."
```

**For each post:**
- Ensure keyphrase appears in:
  - Title (or early in first sentence)
  - First paragraph
  - At least one H2/H3 heading
  - Meta description
- Add internal links to related service pages
- Check Yoast readability score (aim for green)

### Optimize Other Pages

**Results Gallery Page:**
```
Keyphrase: "hair transplant results before after bangalore"
Title: "Hair Transplant Results - Before & After Photos | Bangalore"
Meta: "See real hair transplant transformations. Before and after photos from 500+ successful cases in Bangalore. Proven results."
```

**Contact Page:**
```
Keyphrase: "hair transplant consultation bangalore"
Title: "Hair Transplant Free Consultation | Contact Sanjeevani"
Meta: "Book your free hair transplant consultation in Bangalore. Call +91 82962 80340 or fill form. Expert doctors. Same-day appointment."
```

**About Page:**
```
Keyphrase: "hair transplant clinic bangalore"
Title: "About Sanjeevani Cos Derma | Hair Transplant Clinic"
Meta: "Learn about Sanjeevani Cos Derma clinic in Bangalore. 15+ years experience, expert surgeons, 500+ cases, 98% success rate."
```

---

## Step 4.4: Local SEO - Google My Business Setup (Day 3 - 1.5 hours)

### Claim/Create GMB Listing

1. **Visit:** https://www.google.com/business
2. **Sign in** with Google account
3. **Search** for your business: "Sanjeevani Cos Derma, Bangalore"
4. If not found, click **"Create business"**

### Complete GMB Profile

**Business Information:**

```
Business Name: Sanjeevani Cos Derma
Category: Medical Practice / Hair Transplant Clinic / Dermatology
Address: Sunrise Complex, 1693/A/32, Dr Rajkumar Road, Rajajinagar, Bangalore 560010, Karnataka
Phone: +91 82962 80340
Website: https://sanjeevanicosderma.in
```

**Service Categories:** (Select all applicable)
- Hair transplant
- Dermatology
- Cosmetic surgery clinic
- Medical clinic
- Skin care clinic

**Service Area:** (if applicable)
- Cities served: Bangalore, Bengaluru and surrounding metro area
- Service radius: 50 km

**Opening Hours:**
```
Monday: 10:30 AM - 6:30 PM
Tuesday: 10:30 AM - 6:30 PM
Wednesday: 10:30 AM - 6:30 PM
Thursday: 10:30 AM - 6:30 PM
Friday: 10:30 AM - 6:30 PM
Saturday: 10:30 AM - 6:30 PM
Sunday: 10:30 AM - 6:30 PM
Holiday Hours: (Add any special closures)
```

**Attributes:** (Optional but recommended)
- Women-led: (if applicable)
- LGBTQ-friendly: YES
- Wheelchair accessible: (if applicable)

**Photos:** (Add minimum 5 photos)
1. Clinic exterior / storefront
2. Clinic interior / reception
3. Treatment room
4. Doctor/staff photo
5. Before/After case study (if available)
6. Service/procedure photo

**Description:**
```
Sanjeevani Cos Derma is Bangalore's premier hair transplant and skin treatment clinic.
With 15+ years of experience and 500+ successful cases, we offer:

- Hair Transplant (FUE & Pen-Implanter techniques)
- Hair Loss Treatment (GFC, PRP therapy)
- Skin Treatments (Laser, HydraFacial, Chemical Peels)
- Cosmetic Dermatology

98% success rate. Expert surgeons. Natural results. Free consultation.

Located in Rajajinagar, Bangalore.
```

**Business Links:**
- Website
- Social media profiles (Facebook, Instagram)

**Verification:**
- Verify by postcard (if available in your region)
- Or verify by phone/email
- Wait for verification (typically 7-14 days)

---

### Add Reviews Request Link

Once verified, share GMB review link with patients:

**Copy from:** GMB Dashboard → Customer Reviews → Share button

**Add to:**
- Thank you email after consultation
- Contact page
- Footer of website
- WhatsApp follow-up messages

---

## Step 4.5: Google Search Console Setup (Day 4 - 2 hours)

### Add & Verify Domain

1. **Visit:** https://search.google.com/search-console
2. **Click:** "Start now"
3. **Choose verification method:**

**Option A: Domain Property** (Recommended)
- Verify via DNS TXT record
- hPanel → Domains → DNS Zone
- Add Google's TXT record
- Verify in GSC (may take 24-48 hours)

**Option B: URL Prefix**
- Add: https://sanjeevanicosderma.in
- Verify via HTML file upload
- Or via Google Site Kit plugin

### Configure Search Console

**After verification, complete:**

#### 1. Verify Property Owners
- Admin → Google Site Kit → Settings
- Connect to GSC
- Confirm ownership

#### 2. Submit Sitemap

- Yoast auto-generates XML sitemap
- URL: https://sanjeevanicosderma.in/sitemap.xml

GSC:
- Sitemaps → Add a new sitemap
- Enter: sitemap.xml
- Submit

#### 3. Submit Homepage & Key Pages

GSC:
- URL Inspection tool
- Enter: https://sanjeevanicosderma.in
- Click "Request indexing"

Repeat for:
- /hair-transplant/
- /skin-treatments/
- /results/
- /blog/
- /contact/

#### 4. Monitor Coverage Report

GSC:
- Coverage tab
- Check for "Valid" pages (green checkmark)
- Fix any "Error" or "Valid with warning" pages

#### 5. Check Mobile Usability

GSC:
- Mobile Usability report
- Should show "No issues" or low issue count
- Fix any issues (small touch targets, etc.)

#### 6. Monitor Indexing

GSC:
- Pages Index Coverage → Monitor trends
- Track newly indexed pages (should increase over time)

---

## Step 4.6: Analytics Setup (Day 4 - 1.5 hours)

### Google Analytics 4 Configuration

1. **Create GA4 Property** (if not already created)
   - Visit: https://analytics.google.com
   - Click "Create"
   - Property name: "Sanjeevani Cos Derma"
   - Timezone: Asia/Kolkata
   - Currency: INR

2. **Create Web Data Stream**
   - Platform: Web
   - Website URL: https://sanjeevanicosderma.in
   - Stream name: "Website"
   - Copy Measurement ID: G-XXXXXXXXXX

### Connect Google Analytics to WordPress

**Via Google Site Kit:**

1. Admin → Google Site Kit → Settings
2. Connect Google Analytics
3. Select property: "Sanjeevani Cos Derma"
4. Enable auto-insertion of GA code

**Or Manual GA4 Code:**

1. Install plugin: "MonsterInsights"
2. Activate
3. MonsterInsights → Settings
4. Connect to Google Analytics
5. Select property
6. Enable tracking

### Configure GA4 Conversions

**Conversion 1: Contact Form Submission**
- Event name: form_submission
- Trigger: WPForms form submit
- Mark as: Conversion

**Conversion 2: Phone Click**
- Event name: phone_click
- Trigger: Click tel: link
- Mark as: Conversion

**Conversion 3: WhatsApp Click**
- Event name: whatsapp_click
- Trigger: Click WhatsApp button
- Mark as: Conversion

**Conversion 4: Schedule Consultation**
- Event name: schedule_consultation
- Trigger: CTA button click
- Mark as: Conversion

**In GA4:**
GA4 → Admin → Events → Mark as conversion

---

## Step 4.7: SEO Audit & Verification (Day 5 - 2 hours)

### Comprehensive SEO Checklist

**On-Page SEO:**
- [ ] All pages have unique titles (50-60 characters)
- [ ] All pages have meta descriptions (155-160 characters)
- [ ] Focus keyphrases set in Yoast for 20+ pages
- [ ] H1 tags present on all pages (one per page)
- [ ] H2/H3 hierarchy logical
- [ ] Images have alt text (for accessibility and SEO)
- [ ] Internal linking 15-20 links per main page
- [ ] External links (at least 5 per long-form page)

**Technical SEO:**
- [ ] XML sitemap generated and submitted
- [ ] robots.txt properly configured
- [ ] 404 errors handled with custom page
- [ ] SSL/HTTPS active (green lock icon)
- [ ] No mixed content (all https://)
- [ ] Mobile responsive (tested on device)
- [ ] Core Web Vitals optimized:
  - [ ] LCP < 2.5s
  - [ ] FID < 100ms
  - [ ] CLS < 0.1

**Structured Data:**
- [ ] 6 JSON-LD schemas implemented
- [ ] Rich Result Tester shows no errors
- [ ] FAQPage schema generating rich results
- [ ] LocalBusiness with rating displaying

**Local SEO:**
- [ ] Google My Business verified
- [ ] All business info complete
- [ ] 5+ photos uploaded
- [ ] Opening hours correct
- [ ] Service areas defined
- [ ] Review link shared

**Search Console:**
- [ ] Domain verified
- [ ] Sitemap submitted
- [ ] 20+ pages indexed
- [ ] No critical errors
- [ ] Mobile usability good
- [ ] Core Web Vitals passing

---

### Performance Testing

**Tool 1: Google PageSpeed Insights**

Visit each page:
- Homepage: https://pagespeed.web.dev/?url=https://sanjeevanicosderma.in
- Hair Transplant: https://pagespeed.web.dev/?url=https://sanjeevanicosderma.in/hair-transplant/
- Results page, Contact page, etc.

**Target Scores (minimum):**
- Mobile: 70+
- Desktop: 80+

**Tool 2: GTmetrix**

Visit: https://gtmetrix.com

**Tool 3: SEMrush/Ahrefs**

(If using paid SEO tools, run audit)

---

### Backlink & Keyword Research (Optional)

**Check competitor backlinks:**
- Google "best hair transplant clinic bangalore"
- Note: Competitor domains linking
- Reach out for content collaboration

**Monitor rankings:**
- Track 10-15 primary keywords in Excel
- Check monthly rankings in Google
- Target: Reach page 1 for 5+ keywords within 6 months

---

## Phase 4 Verification Checklist

**By end of Phase 4:**

- [ ] All 6 JSON-LD schemas configured and validated
- [ ] 301 redirects working for all Astro URLs
- [ ] Yoast SEO optimized for:
  - [ ] Homepage
  - [ ] 7 service pages
  - [ ] Blog posts (12)
  - [ ] Results page
  - [ ] Contact page
  - [ ] About page

- [ ] Google My Business:
  - [ ] Verified and published
  - [ ] All business info complete
  - [ ] 5+ photos uploaded
  - [ ] Review link working

- [ ] Google Search Console:
  - [ ] Domain verified
  - [ ] Sitemap indexed (shows 50+ URLs)
  - [ ] 30+ pages indexed
  - [ ] Coverage report: Mostly valid
  - [ ] Mobile usability: No issues (or minimal)
  - [ ] Core Web Vitals: Good (green)

- [ ] Google Analytics:
  - [ ] GA4 tracking active
  - [ ] 4 conversions set up
  - [ ] Data flowing (10+ sessions/day minimum)

- [ ] Performance:
  - [ ] PageSpeed scores 70+ mobile, 80+ desktop
  - [ ] Core Web Vitals: LCP <2.5s, FID <100ms, CLS <0.1
  - [ ] No JavaScript errors in console

- [ ] SEO Audit:
  - [ ] No broken internal links
  - [ ] All images have alt text
  - [ ] No duplicate content
  - [ ] Proper URL structure
  - [ ] Mobile responsive confirmed

---

## Phase 4 Deliverables

**Schemas Configured:**
- Medical Business schema
- Local Business schema
- Aggregate Rating schema
- Medical Organization schema with services
- FAQPage schema
- WebSite schema

**SEO Optimization:**
- 20+ pages optimized with Yoast
- 300+ keyphrases and variations tracked
- Meta descriptions written for all pages
- Internal linking structure created
- Images optimized with alt text

**Local Presence:**
- Google My Business verified
- Local schema active
- Service areas defined
- Business hours specified
- Contact info verified

**Search Engine Visibility:**
- Google Search Console verified
- 50+ URLs indexed
- Sitemap submitted
- Mobile usability checked
- Core Web Vitals optimized

**Analytics:**
- Google Analytics GA4 tracking
- 4 key conversions set up
- Dashboard configured

---

## Next Steps: Phase 5

Phase 5 focuses on final testing and launch preparation:
1. Content verification
2. Functionality testing (all forms, links, buttons)
3. Design QA (all breakpoints, all devices)
4. Performance optimization final push
5. Go-live checklist and DNS migration

**Phase 5 Duration:** 5 business days (Week 7)

---

**Phase 4 Status: READY FOR IMPLEMENTATION**

