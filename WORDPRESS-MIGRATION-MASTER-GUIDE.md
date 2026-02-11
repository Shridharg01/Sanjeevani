# WordPress Migration Master Implementation Guide
## Sanjeevani Cos Derma - Astro to WordPress on Hostinger

**Project Duration:** 7 weeks
**Total Scope:** Complete website migration with SEO optimization
**Status:** READY FOR IMPLEMENTATION
**Last Updated:** February 2026

---

## Project Overview

This document serves as the master guide for converting Sanjeevani Cos Derma from a static Astro site to a fully-featured WordPress site hosted on Hostinger.

**Current State:**
- Astro SSG with 17 pages
- 12 blog posts
- 10 case studies
- 3 testimonials
- Comprehensive SEO (6 JSON-LD schemas)

**Target State:**
- WordPress CMS with content management
- Custom post types for case studies & testimonials
- Elementor visual builder
- Advanced SEO with Yoast
- Hostinger performance optimization
- All content preserved with 301 redirects

---

## Quick Start: What You Need

### Required Tools & Access

**For Hostinger Setup:**
1. Hostinger account (Business Plan or higher)
2. Domain: sanjeevanicosderma.in
3. Domain registrar access (for DNS migration)
4. Email account for admin notifications

**For Plugins & Licenses (Optional but Recommended):**
- Yoast SEO Premium: $179/year
- Elementor Pro: $199/year
- GeneratePress Pro: $199/year
- ACF Pro: $299/year
- WPForms Pro: $299/year
- FooGallery Pro: $149/year
- WP All Import Pro: $99/year

**Total First-Year Investment:** ~$1,400 (plugins) + ~$240/year (Hostinger)

**Free Alternatives Available:** All premium plugins have free versions that work well; upgrade as needed.

---

## Implementation Timeline

```
WEEK 1: Phase 1 - Foundation
  Mon-Wed: WordPress auto-install on Hostinger
  Wed-Thu: Install 18 core plugins
  Thu-Fri: GeneratePress theme + Elementor setup
  Deliverable: WordPress admin ready, backups created

WEEK 2-3: Phase 2 - Content Migration
  Week 2: Create custom post types, import blog posts, import case studies
  Week 3: Create testimonials, static pages, menus
  Deliverable: All content in WordPress database

WEEK 4-5: Phase 3 - Design Implementation
  Week 4: Homepage + master service page template
  Week 5: Duplicate & customize 7 service pages + gallery + contact form
  Deliverable: All pages styled and fully functional

WEEK 6: Phase 4 - SEO Implementation
  Days 1-2: Configure 6 JSON-LD schemas
  Day 3: Set up 301 redirects from Astro URLs
  Days 3-4: Yoast SEO optimization for all pages
  Day 5: Google My Business + Search Console setup
  Deliverable: Full SEO implementation, analytics active

WEEK 7: Phase 5 - Final Testing & Launch
  Days 1-2: Content and functionality verification
  Day 3: Design QA across all devices
  Day 4: Performance optimization + testing
  Day 5: Go-live preparation and DNS migration
  Deliverable: Live WordPress site, all systems green
```

---

## Detailed Phase Overview

### Phase 1: WordPress Setup & Foundation (5 days)
**Location:** `/WORDPRESS-MIGRATION-PHASE-1.md`

**What Gets Done:**
- WordPress installed on Hostinger
- 18 plugins installed and configured
- GeneratePress Pro theme activated
- Elementor Pro configured
- Performance optimization enabled (LiteSpeed, CloudFlare)
- SSL/HTTPS active
- Baseline backup created

**Key Decisions:**
- Theme: GeneratePress Pro (lightweight, SEO-friendly)
- Page Builder: Elementor Pro (recreates Astro components)
- SEO Plugin: Yoast SEO Premium
- Forms: WPForms Pro
- Gallery: FooGallery Pro
- Performance: LiteSpeed Cache + CloudFlare

**Success Criteria:**
- WordPress admin accessible
- All plugins installed and activated
- Homepage loads at https://sanjeevanicosderma.in
- PageSpeed baseline: 50-65 (before design)

**Effort:** ~8-10 hours

---

### Phase 2: Content Migration & Database (10 days)
**Location:** `/WORDPRESS-MIGRATION-PHASE-2.md`

**What Gets Done:**
- Create 3 custom post types (case_study, testimonial, faq)
- Create 4 taxonomies for case studies
- Create 5 ACF field groups for custom content
- Import 12 blog posts with categories/tags
- Import 10 case studies with before/after images
- Create 3 testimonial posts
- Create 6 static pages (About, Contact, Results, Legal)
- Configure navigation menus

**Key Decisions:**
- Use WP All Import for bulk importing posts
- ACF for custom post types
- Custom Post Type UI for CPT management
- Media Folder plugin for image organization

**Success Criteria:**
- 12 blog posts visible in admin
- 10 case studies with images uploaded
- 3 testimonials created with ratings
- All static pages created
- Navigation menus configured

**Effort:** ~12-15 hours

---

### Phase 3: Design Implementation (10 days)
**Location:** `/WORDPRESS-MIGRATION-PHASE-3.md`

**What Gets Done:**
- Elementor global styles (colors, typography, spacing)
- Homepage recreation (hero, stats, services, testimonials, CTA)
- Master service page template
- 7 service pages (duplicated and customized)
- Results gallery page with filtering
- Contact page with forms
- Header/footer configuration

**Key Decisions:**
- Elementor Pro dynamic content loops
- Before/after comparison sliders
- Testimonials carousel
- Form validation and styling
- Mobile-first responsive design

**Success Criteria:**
- Homepage matches Astro design
- All 7 service pages complete
- Gallery with filtering working
- Contact form functional
- Responsive: 320px, 768px, 1024px, 1920px

**Effort:** ~15-18 hours

---

### Phase 4: SEO Implementation (5 days)
**Location:** `/WORDPRESS-MIGRATION-PHASE-4.md`

**What Gets Done:**
- Configure 6 JSON-LD structured data schemas
- Set up 301 redirects from all Astro URLs
- Yoast SEO optimization for 20+ pages
- Google My Business verification and setup
- Google Search Console configuration
- Google Analytics 4 setup with 4 conversions

**Key Decisions:**
- Yoast SEO for schema management
- .htaccess vs Yoast redirects
- Focus keyphrases per page
- Local SEO strategy for Bangalore

**Success Criteria:**
- Rich Result Tester shows no schema errors
- All old URLs redirect properly
- Google My Business verified
- GSC shows 50+ pages indexed
- GA4 tracking active with conversions

**Effort:** ~8-10 hours

---

### Phase 5: Testing & Launch (5 days)
**Location:** `/WORDPRESS-MIGRATION-PHASE-5.md`

**What Gets Done:**
- Content verification (all 12 posts, 10 cases, 3 testimonials)
- Functional testing (forms, links, buttons, filters)
- Design QA (desktop, tablet, mobile)
- Performance optimization final push
- Security verification
- Pre-launch backup
- DNS migration to Hostinger
- Go-live monitoring

**Key Decisions:**
- Test on real devices (not just browser)
- Use Google PageSpeed Insights for performance validation
- 24-hour monitoring period post-launch
- Backup plan if critical issues

**Success Criteria:**
- Zero 404 errors
- All forms working
- PageSpeed scores 75+
- Mobile responsive confirmed
- No console errors
- All SEO verified
- Site live and indexed

**Effort:** ~10-12 hours

---

## Files Included in This Package

```
/WORDPRESS-MIGRATION-PHASE-1.md (13,000 words)
  Complete WordPress setup guide for Hostinger

/WORDPRESS-MIGRATION-PHASE-2.md (12,000 words)
  Content migration and database setup

/WORDPRESS-MIGRATION-PHASE-3.md (14,000 words)
  Elementor design implementation

/WORDPRESS-MIGRATION-PHASE-4.md (13,000 words)
  SEO and search optimization

/WORDPRESS-MIGRATION-PHASE-5.md (10,000 words)
  Final testing and launch preparation

/WORDPRESS-MIGRATION-MASTER-GUIDE.md (This file)
  Quick reference and overview
```

**Total Documentation:** ~62,000 words

---

## Step-by-Step Workflow

### Before You Start

1. **Review Astro Site Content**
   - Read: src/data/blog.js (12 blog posts)
   - Read: src/data/results.js (10 case studies, 3 testimonials)
   - Read: src/layouts/Layout.astro (SEO metadata, 6 schemas)

2. **Prepare Assets**
   - Download all images from Pexels (blog featured images)
   - Save before/after images (case studies)
   - Download patient avatars (testimonials) if available

3. **Get Hostinger Setup**
   - Create Hostinger account (Business Plan)
   - Point domain to Hostinger nameservers
   - Wait for DNS propagation (up to 48 hours)

4. **Organize Documentation**
   - Print or bookmark all 5 phase documents
   - Create checklist spreadsheet for tracking
   - Designate backup person for redundancy

### Day 1-5: Phase 1 Execution

**Follow:** `/WORDPRESS-MIGRATION-PHASE-1.md`

**Time Estimate:** 8-10 hours

```
Monday:
  - Complete Step 1.1: WordPress auto-install (0.5 hrs)
  - Complete Step 1.2: Hostinger performance (0.75 hrs)
  - Complete Step 1.3: Database config (0.5 hrs)

Tuesday:
  - Complete Step 1.4: SSL & security (0.75 hrs)
  - Complete Step 1.5: CloudFlare (0.5 hrs)
  - Start Step 1.6: Install plugins (begin first batch)

Wednesday:
  - Continue Step 1.6: Install all 18 plugins (2 hrs)
  - Complete Step 1.7: GeneratePress setup (1.5 hrs)

Thursday:
  - Complete Step 1.8: Elementor Pro setup (1.5 hrs)
  - Complete Step 1.9: WordPress settings (1 hr)

Friday:
  - Complete Step 1.10: Backup & verification (1 hr)
  - Test: WordPress admin accessible ✓
  - Test: All plugins active ✓
  - Test: Homepage loads ✓
  - Create baseline backup ✓
```

**After Phase 1 Complete:**
- [ ] WordPress fully functional
- [ ] All plugins installed
- [ ] Hostinger optimized
- [ ] Baseline backup created
- [ ] Ready for Phase 2

---

### Day 6-16: Phase 2 Execution

**Follow:** `/WORDPRESS-MIGRATION-PHASE-2.md`

**Time Estimate:** 12-15 hours

```
Week 2 - Days 1-4:
  - Complete Step 2.1: Create custom post types (2 hrs)
  - Complete Step 2.2: ACF field groups (2 hrs)
  - Complete Step 2.3: Blog import preparation (1.5 hrs)
  - Complete Step 2.4: Import 12 blog posts (2 hrs)

Week 2 - Days 5:
  - Complete Step 2.5: Create testimonials (1 hr)
  - Create backup at end of week

Week 3 - Days 1-3:
  - Complete Step 2.4: Import case studies (2.5 hrs)
  - Complete Step 2.6: Create static pages (1.5 hrs)
  - Complete Step 2.7: Menu setup (0.75 hrs)
  - Complete Step 2.8: Widget areas (0.5 hrs)

Week 3 - Days 4-5:
  - Verification & testing (1.5 hrs)
  - Content quality check
  - Create backup before Phase 3
```

**After Phase 2 Complete:**
- [ ] 12 blog posts in WordPress
- [ ] 10 case studies with images
- [ ] 3 testimonials created
- [ ] 6 static pages created
- [ ] Menus configured
- [ ] All content verified

---

### Day 17-27: Phase 3 Execution

**Follow:** `/WORDPRESS-MIGRATION-PHASE-3.md`

**Time Estimate:** 15-18 hours

```
Week 4 - Days 1-3:
  - Complete Step 3.1: Elementor global styles (1.5 hrs)
  - Complete Step 3.2: Homepage design (3 hrs)

Week 4 - Days 4-5:
  - Complete Step 3.3: Service page template (2 hrs)
  - Complete Step 3.4: 7 service pages (2.5 hrs)
  - Create backup

Week 5 - Days 1-3:
  - Complete Step 3.5: Results gallery page (1.5 hrs)
  - Complete Step 3.6: Contact form page (1 hr)
  - Complete Step 3.7: Header & navigation (1 hr)

Week 5 - Days 4-5:
  - Complete Step 3.8: Footer (1 hr)
  - Responsive design testing (2 hrs)
  - Create backup before Phase 4
```

**After Phase 3 Complete:**
- [ ] Homepage matches design
- [ ] All 7 service pages live
- [ ] Gallery with filtering working
- [ ] Contact form functional
- [ ] Header/footer configured
- [ ] Responsive design verified

---

### Day 28-33: Phase 4 Execution

**Follow:** `/WORDPRESS-MIGRATION-PHASE-4.md`

**Time Estimate:** 8-10 hours

```
Day 1-2:
  - Complete Step 4.1: JSON-LD schemas (2 hrs)
  - Verify with Rich Result Tester

Day 2-3:
  - Complete Step 4.2: URL redirects (1.5 hrs)
  - Test redirects

Day 3-4:
  - Complete Step 4.3: Yoast SEO per-page (2 hrs)

Day 4-5:
  - Complete Step 4.4: Google My Business (1 hr)
  - Complete Step 4.5: Search Console (1.5 hrs)
  - Complete Step 4.6: Analytics setup (1 hr)

Day 5:
  - Complete Step 4.7: SEO audit (1.5 hrs)
  - Create backup before Phase 5
```

**After Phase 4 Complete:**
- [ ] 6 schemas configured and verified
- [ ] All redirects working (test 10 URLs)
- [ ] 20+ pages Yoast optimized
- [ ] Google My Business verified
- [ ] GSC domain verified, sitemap submitted
- [ ] GA4 tracking active

---

### Day 34-39: Phase 5 Execution

**Follow:** `/WORDPRESS-MIGRATION-PHASE-5.md`

**Time Estimate:** 10-12 hours

```
Day 1-2 (Content & Functional Testing):
  - Step 5.1: Content verification (2 hrs)
  - Step 5.2: Functional testing (2 hrs)

Day 3 (Design QA):
  - Step 5.3: Desktop testing (1 hr)
  - Tablet testing (1 hr)
  - Mobile testing (real devices) (1.5 hrs)

Day 4 (Performance Optimization):
  - Step 5.4: Image optimization (2 hrs)
  - Cache optimization (1 hr)
  - Core Web Vitals check (1 hr)

Day 5 (Launch Preparation):
  - Step 5.5: Final pre-launch checklist (2 hrs)
  - Step 5.6: Backup & DNS migration (1 hr)
  - Execute DNS migration
  - Monitor 24 hours
```

**After Phase 5 Complete - Go-Live!**
- [ ] All content verified
- [ ] All functions tested
- [ ] Design QA passed
- [ ] Performance optimized (75+)
- [ ] SEO complete
- [ ] Analytics active
- [ ] Site indexed by Google
- [ ] Support plan in place

---

## Key Decision Points

### Plugin Choices

**Free vs Premium:**
- Free versions adequate for most needs
- Premium versions recommended for:
  - Yoast SEO: Better schema management
  - Elementor Pro: Dynamic content loops (essential)
  - GeneratePress Pro: Advanced styling
  - ACF Pro: Better field groups

**Recommendation:** Start with free versions, upgrade to Pro as needed

---

### Theme Choice: GeneratePress

**Why GeneratePress?**
- Lightweight (highest PageSpeed scores)
- Excellent Hostinger compatibility
- Built-in SEO features
- Great mobile responsiveness
- Easy customization

**Alternatives:**
- Astra Pro (similar features)
- OceanWP (good for medical)
- Hello Elementor (minimal)

---

### Page Builder: Elementor Pro

**Why Elementor Pro?**
- Dynamic content loops (pull from CPTs)
- Responsive breakpoints
- Advanced animations
- Template inheritance
- Global styling

**Alternatives:**
- Divi Builder
- Beaver Builder
- Gutenberg block editor (free, but limited)

---

### Form Solution: WPForms

**Why WPForms?**
- Easy to use (drag-drop)
- Excellent for contact forms
- Conditional logic available
- Anti-spam built-in
- Email notifications

**Free version sufficient for:**
- Contact form
- Appointment form
- Newsletter signup

---

## Hosting Performance Optimization

### Hostinger Advantages

```
✓ Auto-install WordPress in 1 click
✓ LiteSpeed server (70% faster than Apache)
✓ Free SSL certificate (auto-renewing)
✓ CloudFlare CDN integration
✓ Automatic daily backups
✓ One-click WordPress updates
✓ Built-in caching
✓ Excellent support
```

### Performance Targets

```
PageSpeed Insights:
  Mobile: 75+ (starting target)
  Desktop: 85+ (starting target)

Core Web Vitals:
  LCP: < 2.5 seconds
  FID: < 100ms
  CLS: < 0.1

Load Time:
  First page: < 3 seconds
  Cached page: < 1 second
```

---

## SEO Strategy

### Keyword Targets

**Primary Keywords:**
- hair transplant bangalore
- best hair transplant clinic bangalore
- FUE hair transplant bangalore
- hair transplant rajajinagar

**Location Keywords:**
- bangalore, bengaluru, rajajinagar, malleswaram, whitefield
- +30 more city/locality combinations

**Service Keywords:**
- laser hair removal bangalore
- hydrafacial bangalore
- chemical peel bangalore
- skin treatments bangalore
- etc. (8 service pages)

**Long-tail Keywords:**
- "best hair transplant surgeon in rajajinagar bangalore"
- "affordable hair transplant in bangalore"
- "hair transplant cost in bangalore"
- "painless hair transplant bangalore"

### Target Rankings (6 months)

```
By Month 3:
  5+ keywords on page 1
  15+ keywords on pages 1-3

By Month 6:
  15+ keywords on page 1
  50+ keywords on pages 1-3

By Month 12:
  30+ keywords on page 1
  100+ keywords on pages 1-3
```

---

## Content Strategy

### Blog Post Plan (Post-Launch)

**Month 1-3 (Maintenance):**
- Add 1-2 new blog posts per month
- Topics: Hair loss prevention, treatment recovery, patient stories
- SEO: Target long-tail keywords

**Month 4-6:**
- Add 2-3 new blog posts per month
- Topics: Seasonal tips, comparative guides, patient testimonials
- SEO: Target service-specific keywords

**Ongoing:**
- Update existing posts with latest info
- Add new case studies monthly
- Encourage patient testimonials (reviews)
- Monitor keyword trends and adjust

---

## Maintenance Schedule

### Weekly
- [ ] Check WordPress error logs
- [ ] Monitor analytics for anomalies
- [ ] Quick site load test

### Monthly
- [ ] WordPress core update
- [ ] Plugin updates
- [ ] Theme update (if available)
- [ ] Security scan (Wordfence)
- [ ] Backup verification

### Quarterly
- [ ] Comprehensive SEO audit
- [ ] Performance review
- [ ] Keyword ranking check
- [ ] Competitor analysis
- [ ] Blog content plan update

### Annually
- [ ] Major performance optimization
- [ ] Design refresh (if needed)
- [ ] Plugin audit (remove unused)
- [ ] Security audit
- [ ] Strategy review

---

## Troubleshooting Quick Guide

### Common Issues & Solutions

**Issue: Forms not working**
```
Check: WPForms plugin activated
Check: Email addresses configured
Check: SMTP settings if using advanced features
Solution: Test with simple form first
```

**Issue: Images not displaying**
```
Check: File uploads enabled in WordPress settings
Check: Media folder permissions (755)
Check: Disk space available
Solution: Re-upload via media library
```

**Issue: PageSpeed scores low**
```
Check: EWWW bulk optimization completed
Check: LiteSpeed cache active
Check: Large unoptimized images
Solution: Optimize images, clear caches
```

**Issue: Pages not indexed by Google**
```
Check: Robots.txt allows indexing
Check: No noindex meta tags
Check: Sitemap submitted to GSC
Solution: Submit pages manually in GSC
```

**Issue: Redirects not working**
```
Check: .htaccess syntax correct
Check: Redirect plugin enabled
Check: Old URL still accessible
Solution: Test with browser, clear cache
```

---

## Success Metrics Dashboard

### Track These Numbers

**Traffic:**
```
Week 1: 0-100 sessions (brand search)
Month 1: 200-500 sessions
Month 3: 500-1000 sessions
Month 6: 1000-2000 sessions
```

**Rankings:**
```
Week 4: Track 10 primary keywords
Month 1: Monitor for improvements
Month 3: 5+ keywords on page 1
Month 6: 15+ keywords on page 1
```

**Conversions:**
```
Week 1: 5-10 form submissions
Month 1: 20-30 submissions
Month 3: 50-100 submissions
Month 6: 100-200 submissions
```

**Performance:**
```
Launch: PageSpeed 80+
Month 1: Maintain 80+
Month 6: Maintain 80+ (or improve)
```

---

## Post-Launch Support

### First 30 Days (Critical)

**Daily:**
- Check error logs
- Verify forms working
- Monitor Google Search Console

**Weekly:**
- Performance check (PageSpeed)
- Analytics review
- Ranking check for 5 primary keywords
- Backup verification

### First 6 Months

**Ongoing:**
- Monthly analytics review
- Quarterly SEO audit
- Regular content updates
- Monitor performance trends

### Support Contacts

- **Hostinger:** https://support.hostinger.com
- **WordPress:** https://wordpress.org/support
- **Yoast:** https://yoast.com/help
- **Elementor:** https://elementor.com/help

---

## Investment Summary

### One-Time Costs
```
Hostinger Business Plan setup: $50-100
Premium plugins (optional): $1,400
Professional optimization: $500-2000
Total: $1,950-3,500
```

### Ongoing Monthly Costs
```
Hostinger hosting: $20-30/month
Premium plugin subscriptions: ~$40/month (if annual)
Maintenance & updates: $0 (DIY) or $100-200/month (managed)
Total: $20-30/month (DIY)
```

### Year 1 Cost
```
Hosting: ~$300
Plugins: ~$500 (if purchased monthly)
Maintenance: $0 (DIY)
Total: ~$800-1,300
```

### ROI Estimate
```
Assuming 100 consultations at ₹50,000 average value:
  Revenue: ₹50 Lakhs
  Investment: ~₹10,000-35,000
  ROI: 1,400% - 5,000%
```

---

## Final Checklist Before Starting

```
Pre-Implementation Checklist:

PREPARATION:
  ✓ All 5 phase documents reviewed and printed
  ✓ Astro site content backed up
  ✓ Images downloaded locally
  ✓ Hostinger account created
  ✓ Domain nameservers noted
  ✓ Team trained on process

RESOURCES:
  ✓ Estimated time: 40-50 hours
  ✓ Team assigned (1-2 people)
  ✓ Support contact documented
  ✓ Backup person identified

TOOLS:
  ✓ FTP client installed (for file access)
  ✓ Browser DevTools ready
  ✓ Testing checklist printed
  ✓ Staging environment ready (if available)

COMMUNICATION:
  ✓ Stakeholders informed of timeline
  ✓ Support team on standby (Week 7)
  ✓ Launch announcement prepared
  ✓ Redirect strategy communicated
```

---

## Getting Started

### Next Steps

1. **Read Phase 1 completely** - `/WORDPRESS-MIGRATION-PHASE-1.md`
2. **Get Hostinger setup** - Create account, point domain
3. **Gather assets** - Download images, prepare content
4. **Begin Phase 1** - Follow step-by-step guide
5. **Create checklist** - Track progress through all 5 phases

### Expected Timeline

- Phase 1: Days 1-5 (8-10 hours)
- Phase 2: Days 6-16 (12-15 hours)
- Phase 3: Days 17-27 (15-18 hours)
- Phase 4: Days 28-33 (8-10 hours)
- Phase 5: Days 34-39 (10-12 hours)

**Total: 7 weeks | 53-65 hours of work**

---

## Support & Questions

This comprehensive guide covers:
- 62,000+ words of detailed instructions
- 5 complete phase implementations
- 100+ detailed screenshots descriptions
- Troubleshooting guide
- Success metrics and monitoring
- Post-launch support plan

**For detailed information on any phase, refer to the specific phase document.**

---

## License & Usage

These migration guides are created specifically for Sanjeevani Cos Derma's WordPress migration project.

**Confidential Information Included:**
- Business name and location
- Phone numbers and email
- SEO strategy and keywords
- Custom plugin configurations

**Do not share publicly.**

---

**READY TO PROCEED WITH PHASE 1**

---

For questions about specific phases, refer to:
- Phase 1 Details: `/WORDPRESS-MIGRATION-PHASE-1.md`
- Phase 2 Details: `/WORDPRESS-MIGRATION-PHASE-2.md`
- Phase 3 Details: `/WORDPRESS-MIGRATION-PHASE-3.md`
- Phase 4 Details: `/WORDPRESS-MIGRATION-PHASE-4.md`
- Phase 5 Details: `/WORDPRESS-MIGRATION-PHASE-5.md`

