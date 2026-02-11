# WordPress Migration Phase 3: Design Implementation
## Sanjeevani Cos Derma - Elementor Templates & Pages

**Duration:** 10 business days (Weeks 4-5)
**Status:** Implementation Ready
**Last Updated:** February 2026

---

## Phase 3 Overview

Phase 3 transforms WordPress content into a visually stunning site matching the Astro design:
- Homepage recreation with hero, services, testimonials, CTA
- 7 service pages with standardized layout
- Before/after gallery with filtering
- Contact form integration
- Testimonials carousel
- Header/footer design

---

## Step 3.1: Elementor Global Styles Configuration (Day 1 - 2 hours)

### Access Elementor Global Styles

Admin → Elementor → Global Settings
(Or: Appearance → Customize → Elementor)

### Color System Setup

**Brand Colors (from Astro design):**

In Elementor Color Palette:

```
Color 1 (Primary): #009fbf
Color 2 (Secondary): #0ea5e9
Color 3 (Accent/Success): #10b981
Color 4 (Warning): #f59e0b
Color 5 (Error): #ef4444
Color 6 (Dark): #1f2937
Color 7 (Light): #f3f4f6
Color 8 (Gray): #9ca3af
```

**Apply to Elements:**
- Primary CTA buttons: #009fbf
- Links: #009fbf (hover: #0ea5e9)
- Accent badges: #10b981
- Testimonial rating stars: #fbbf24 (gold)

### Typography Settings

**Font Families:**
- Display Font: Playfair Display (Google Fonts)
- Body Font: Inter (Google Fonts)
- Code Font: Courier New

**Font Sizes (Scaling Factor 1.2):**
```
H1: 48px (desktop), 36px (tablet), 28px (mobile)
H2: 40px (desktop), 32px (tablet), 24px (mobile)
H3: 33px (desktop), 27px (tablet), 20px (mobile)
H4: 28px
H5: 23px
H6: 19px
Body: 16px (desktop), 15px (tablet), 14px (mobile)
Small: 14px
```

**Line Height:**
```
Headings: 1.2
Body: 1.5
```

**Letter Spacing:**
```
Headings: 0px
Body: 0px
```

### Spacing System (8px Grid)

Create Elementor custom spacing presets:

```
Spacing 1: 8px
Spacing 2: 16px
Spacing 3: 24px
Spacing 4: 32px
Spacing 5: 40px
Spacing 6: 48px
Spacing 7: 56px
Spacing 8: 64px
```

### Button Styles

**Primary Button:**
```
Background: #009fbf
Text Color: White
Padding: 12px 32px
Border Radius: 8px
Font Weight: 600
Hover: Background #0d8fab, Shadow
Transition: all 0.3s ease
```

**Secondary Button:**
```
Background: Transparent
Border: 2px #009fbf
Text Color: #009fbf
Hover: Background #f0f9fc
```

**CTA Button:**
```
Background: #10b981
Text Color: White
Padding: 14px 40px
Border Radius: 8px
Font Weight: 700
Box Shadow: 0 4px 12px rgba(16, 185, 129, 0.3)
Hover: Transform scale(1.05)
```

---

## Step 3.2: Homepage Design with Elementor (Day 2-3 - 4 hours)

### Create Homepage Page & Template

1. **Create Homepage Page**
   - Admin → Pages → Add New
   - Title: Homepage
   - Slug: (keep as /homepage/ or use front page in settings)

2. **Edit with Elementor**
   - Click "Edit with Elementor"
   - Start blank template

### Section 1: Hero Section (40 minutes)

**Section Settings:**
```
Background: Gradient overlay
  - Gradient: Linear from #009fbf (0%) to #0ea5e9 (100%)
  - Opacity: 85%
  - Image underneath: Hero background image
Background Image: (Use Pexels medical clinic image)
Min Height: 600px (desktop), 400px (mobile)
Padding: 60px 40px (desktop), 40px 20px (mobile)
Alignment: Center
```

**Columns:** 1 Column

**Content Structure:**

**Element 1: Hero Badge**
```
Type: Heading (small)
Text: "⭐ Bangalore's Most Trusted Hair Transplant Clinic"
Color: White
Font Size: 14px
Font Weight: 600
Background: rgba(255,255,255,0.2)
Padding: 8px 16px
Border Radius: 20px
Alignment: Center
Margin Bottom: 16px
```

**Element 2: Main Heading**
```
Type: Heading (h1)
Text: "Transform Your Hair, Restore Your Confidence"
Color: White
Font: Playfair Display
Font Size: 48px (desktop), 32px (mobile)
Font Weight: 700
Line Height: 1.2
Margin Bottom: 20px
```

**Element 3: Subheading**
```
Type: Heading (h3)
Text: "Expert hair transplant surgeons with 500+ successful cases. Natural results with FUE & Pen-Implanter techniques."
Color: rgba(255,255,255,0.95)
Font Size: 20px (desktop), 16px (mobile)
Font Weight: 400
Line Height: 1.5
Margin Bottom: 40px
```

**Element 4: Feature Checkmarks**
```
Type: Icon Box (4 columns)
Responsive: 2 columns tablet, 1 column mobile

Box 1:
  Icon: ✓ (green)
  Text: "98% Success Rate"
  Font Size: 14px

Box 2:
  Icon: ✓ (green)
  Text: "Painless Procedure"
  Font Size: 14px

Box 3:
  Icon: ✓ (green)
  Text: "Expert Surgeons"
  Font Size: 14px

Box 4:
  Icon: ✓ (green)
  Text: "Affordable Pricing"
  Font Size: 14px

Background: rgba(255,255,255,0.1)
Padding: 24px 16px
Border Radius: 8px
Text Color: White
Margin Bottom: 40px
```

**Element 5: CTA Buttons**
```
Type: Button Group (2 buttons side-by-side)
Responsive: Stack mobile

Button 1: "Book Free Consultation"
- Style: Primary (#009fbf)
- Size: Large
- URL: /contact/

Button 2: "WhatsApp Expert"
- Style: Secondary (white border)
- Size: Large
- URL: https://wa.me/918296280340?text=Hi%20I%20would%20like%20to%20book%20a%20consultation

Alignment: Center
Spacing between: 16px
```

---

### Section 2: Statistics Section (30 minutes)

**Section Settings:**
```
Background: White
Padding: 60px 40px
```

**Columns:** 4 columns (tablet: 2, mobile: 1)

**Stat Box 1:**
```
Number: "500+"
Text: "Successful Cases"
Icon: Briefcase (green)
Alignment: Center
```

**Stat Box 2:**
```
Number: "98%"
Text: "Success Rate"
Icon: Thumbs Up (green)
Alignment: Center
```

**Stat Box 3:**
```
Number: "4.9/5"
Text: "Patient Satisfaction"
Icon: Star (gold)
Alignment: Center
```

**Stat Box 4:**
```
Number: "15+ Years"
Text: "Experience"
Icon: Calendar (blue)
Alignment: Center
```

**Font Settings:**
- Number: 40px, Bold, Primary color
- Text: 16px, Medium

---

### Section 3: Featured Services Grid (45 minutes)

**Section Settings:**
```
Background: Light gray (#f9fafb)
Padding: 60px 40px
```

**Heading:**
```
Text: "Our Services"
Alignment: Center
Font: Playfair Display
Size: 40px
Margin Bottom: 20px
```

**Subheading:**
```
Text: "Comprehensive hair restoration and skin treatments"
Alignment: Center
Color: Gray
Margin Bottom: 40px
```

**Service Cards Grid: 3 columns (tablet: 2, mobile: 1)**

**Card 1: Pen-Implanter (Featured)**
```
Background: White
Border: 3px solid #009fbf (featured indicator)
Shadow: 0 4px 12px rgba(0,159,191,0.15)
Padding: 32px 24px
Border Radius: 12px
Transition: transform 0.3s

Icon: Hair icon with "Featured" badge
Title: "Pen-Implanter Hair Transplant"
Description: "Most advanced hair transplant technique with minimal pain and quick recovery. Superior graft survival rate."
Features:
  - Painless procedure
  - Fastest recovery
  - Natural results
  - 3500+ grafts capacity

Button: "Learn More" → /hair-transplant/

Hover Effect: Lift up with shadow expansion
```

**Card 2: FUE**
```
Similar structure
Title: "FUE Hair Transplant"
Description: "Follicular Unit Extraction technique for precise, natural hairlines. Ideal for larger coverage areas."
Button: "Learn More" → /hair-transplant/
```

**Card 3: Hair Loss Treatment**
```
Similar structure
Title: "Non-Surgical Hair Loss Treatment"
Description: "GFC and PRP therapies for early hair loss. Stimulate natural hair growth without surgery."
Button: "Learn More" → /gfc-hair-treatment-bengaluru/
```

**Card 4: Skin Treatments**
```
Title: "Cosmetic & Skin Treatments"
Description: "HydraFacial, chemical peels, laser therapy, and acne treatments for healthy glowing skin."
Button: "Learn More" → /skin-treatments/
```

**Card 5: Laser Hair Removal**
```
Title: "Laser Hair Removal"
Description: "Advanced laser technology for permanent hair reduction on face and body. Painless and fast."
Button: "Learn More" → /laser-hair-removal-bengaluru/
```

**Card 6: Cosmetic Dermatology**
```
Title: "Cosmetic Dermatology"
Description: "Expert skin rejuvenation, anti-aging treatments, and specialized dermatological procedures."
Button: "Learn More" → /cosmetic-dermatology-bengaluru/
```

---

### Section 4: Why Choose Us Section (40 minutes)

**Section Settings:**
```
Background: White
Padding: 60px 40px
```

**Layout: 2 columns (desktop), 1 column (mobile)**

**Left Column: Image**
```
Image: Clinic photo or testimonial image (600x400px)
Border Radius: 12px
Shadow: 0 8px 24px rgba(0,0,0,0.1)
```

**Right Column: Content**

**Heading:**
```
Text: "Why Choose Sanjeevani Cos Derma?"
Font: Playfair Display
Size: 36px
Margin Bottom: 20px
```

**Reasons List (5 items with icons):**

1. **Expert Surgeons**
   - Icon: Award
   - "15+ years of experience with thousands of satisfied patients"

2. **Advanced Techniques**
   - Icon: Microscope
   - "Latest hair transplant and skin treatment technologies"

3. **Natural Results**
   - Icon: Smile
   - "Personalized approach for natural-looking hairlines and outcomes"

4. **Affordable Pricing**
   - Icon: CreditCard
   - "Competitive pricing with flexible payment options"

5. **Highest Success Rate**
   - Icon: Thumbs Up
   - "98% success rate with proven results across 500+ cases"

**Each Item:**
```
Background: Light (#f9fafb)
Padding: 16px 20px
Border Radius: 8px
Border Left: 4px solid #009fbf
Margin Bottom: 16px
Icon Size: 28px, color #009fbf
Font: 16px, weight 500
```

**CTA Button (below content):**
```
Text: "Book Your Consultation"
URL: /contact/
Style: Primary
Size: Large
Margin Top: 30px
```

---

### Section 5: Before/After Gallery Preview (45 minutes)

**Section Settings:**
```
Background: Gradient light
Padding: 60px 40px
```

**Heading:**
```
Text: "Real Results From Real Patients"
Alignment: Center
Font: Playfair Display
Size: 40px
Margin Bottom: 40px
```

**Gallery Grid: 3 columns (tablet: 2, mobile: 1)**

**Dynamic Gallery Loop:**
```
Use: Elementor Pro Dynamic Content
Loop: case_study posts (limit: 6)
Taxonomy filter: case_study_category
Only show: featured = true

For each case study:
  - Before image (left)
  - After image (right)
  - Slider comparison overlay
  - Case details: Technique, grafts, timeline
  - Click: Link to full case study / lightbox
```

**Gallery Item Structure:**

```
Container: Aspect ratio 1:1 (square)
Background: Before image
Overlay: Slider divider
After image: Draggable overlay
On hover:
  - Show case details
  - Show "View Details" button

Case Details Overlay:
  - Technique badge: "FUE" / "Pen-Implanter"
  - Age: "32 years"
  - Grafts: "2500"
  - Timeline: "12 months"
```

**Button Below Gallery:**
```
Text: "View All Results"
URL: /results/
Alignment: Center
Style: Secondary
Margin Top: 40px
```

---

### Section 6: Testimonials Carousel (45 minutes)

**Section Settings:**
```
Background: #f9fafb
Padding: 60px 40px
```

**Heading:**
```
Text: "Patient Testimonials"
Alignment: Center
Font: Playfair Display
Size: 40px
Margin Bottom: 40px
```

**Testimonials Carousel:**
```
Element: Elementor Pro Carousel
Loop: testimonial posts
Show: 1 slide (desktop), 1 slide (mobile)
Autoplay: Yes (5 second interval)
Navigation: Arrows + Dots
```

**Testimonial Card Layout:**

```
Background: White
Shadow: 0 4px 12px rgba(0,0,0,0.1)
Padding: 40px 32px
Border Radius: 12px
Alignment: Center

Element 1: 5-Star Rating
  Display: ★★★★★ (gold stars)
  Font: 24px
  Margin Bottom: 16px

Element 2: Testimonial Quote
  Text: testimonial_text field
  Font: 18px, italic, weight 500
  Line Height: 1.6
  Margin Bottom: 24px

Element 3: Patient Info
  Layout: Flex (avatar + text)

  Avatar: (circular, 60x60px)
    testimonial_avatar field
    Border Radius: 50%

  Text Container:
    Name: testimonial_patient_name (bold, 16px)
    Title: testimonial_patient_title (14px, gray)
    Location: testimonial_patient_location (14px, gray)
    Treatment: testimonial_treatment_type (12px, badge)
```

---

### Section 7: CTA Section (30 minutes)

**Section Settings:**
```
Background: Gradient (#009fbf to #0ea5e9)
Padding: 60px 40px
Alignment: Center
```

**Content:**

**Heading:**
```
Text: "Ready to Transform Your Hair?"
Color: White
Font: Playfair Display
Size: 40px
Margin Bottom: 16px
```

**Subheading:**
```
Text: "Get a free consultation from our expert surgeons. Natural results guaranteed."
Color: rgba(255,255,255,0.9)
Size: 18px
Margin Bottom: 40px
```

**Buttons (2 side-by-side):**

**Button 1:**
```
Text: "Book Free Consultation"
Style: White background, blue text
URL: /contact/
Size: Large
```

**Button 2:**
```
Text: "Call Now"
URL: tel:+918296280340
Style: Secondary (blue border, white text)
Size: Large
```

---

### Section 8: Footer (handled separately)

See Step 3.6: Footer Configuration

---

## Step 3.3: Service Pages Template (Day 4-5 - 5 hours)

### Create Master Service Page Template

**Create Template:**
1. Admin → Elementor → Templates
2. Click "New Template"
3. Name: "Service Page Master"
4. Type: Page
5. Edit with Elementor

### Service Page Structure

**Section 1: Hero Banner**
```
Background: Linear gradient primary to secondary
Min Height: 400px
Padding: 60px 40px

Breadcrumb:
  Home → Services → [Current Service]
  Font: 14px, gray

Heading:
  Text: [Service Title - dynamic from page title]
  Font: Playfair Display, 48px, white
  Margin: 20px 0

Subheading:
  Text: [Short description - custom per page]
  Font: 18px, white, 80% opacity
```

---

**Section 2: Service Overview**
```
Background: White
Padding: 60px 40px

3-Column Grid (tablet: 1, mobile: 1):

Column 1: Description
- Main paragraph (3-4 sentences)
- Key benefits (3-4 bullet points)

Column 2: Key Information Box
- Technique name
- Recovery time
- Success rate
- Price range (starting from)

Column 3: Quick Facts
- Grafts range (if applicable)
- Sessions needed
- Results timeline
```

---

**Section 3: Technique Comparison** (if applicable)

For hair transplant pages (FUE, Pen-Implanter):

```
Background: Light gray (#f9fafb)
Padding: 60px 40px

Heading: "Comparison: [Technique 1] vs [Technique 2]"

Table Layout:
  Columns: Technique 1 | Comparison Factor | Technique 2
  Rows: Pain Level, Recovery Time, Cost, Graft Survival, Success Rate, etc.

  Styling:
  - Header background: Primary color (#009fbf)
  - Header text: White
  - Alternating row backgrounds: White and light gray
  - Winner highlights: Green checkmark
```

---

**Section 4: Before & After Gallery**
```
Background: White
Padding: 60px 40px

Heading: "Patient Results"

Gallery Grid: 3 columns (tablet: 2, mobile: 1)

Dynamic Loop Filter:
- Show: case_study posts by technique
- Filter buttons: [All] [FUE] [Pen-Implanter] [Other]
- Each item: Before/after comparison slider
- On click: Lightbox

Layout:
- Before image (left 50%)
- After image (right 50%)
- Draggable slider divider
- On hover: Show case details (age, grafts, timeline)
```

---

**Section 5: Benefits Section**
```
Background: White
Padding: 60px 40px

Heading: "Benefits of [Service Name]"

Icon Grid: 6 boxes (desktop), 3 (tablet), 1 (mobile)

Each Box:
- Icon (32px, primary color)
- Title (16px, bold)
- Description (14px, gray)
- Background: Light gray (#f9fafb)
- Padding: 24px 20px
- Border radius: 8px
- Hover: Lift effect + shadow

Benefits Examples (for Hair Transplant):
- Permanent solution
- Natural-looking results
- Minimal scarring
- Quick recovery
- Affordable cost
- High success rate
```

---

**Section 6: Pricing Table** (if pricing available)

```
Background: Light gray (#f9fafb)
Padding: 60px 40px

Heading: "Transparent Pricing"

Table: 4 columns (responsive)
Columns: Plan | Grafts | Timeline | Price | Action

Row 1 (recommended):
- Basic Plan
- 1500-2000 grafts
- 10-12 months
- ₹From 2,00,000
- Button: "Choose Plan"

Row 2:
- Standard Plan
- 2000-3000 grafts
- 11-13 months
- ₹From 3,50,000
- Badge: "Most Popular"

Row 3:
- Premium Plan
- 3000-4000 grafts
- 12-14 months
- ₹From 5,00,000
- Button: "Choose Plan"

Table Styling:
- Header: Primary color background, white text
- Recommended row: Light green background
- Price: 28px, bold, primary color
- Buttons: CTA style
```

---

**Section 7: FAQ Accordion**
```
Background: White
Padding: 60px 40px

Heading: "Frequently Asked Questions"

Accordion: 6-8 items
Loop: faq posts related to service
Or: Manually create FAQ items

Each Item:
- Question (clickable)
- Answer (expandable)
- Icon: + (closed) / - (open)
- Color: Primary on active

Example FAQs:
1. Is the procedure painful?
2. How long is recovery?
3. When will I see results?
4. Are results permanent?
5. Can I return to work immediately?
6. Is financing available?
```

---

**Section 8: Testimonials** (service-specific)

```
Background: Light gray (#f9fafb)
Padding: 60px 40px

Heading: "What Our Patients Say"

Carousel: 3 testimonials
Filter: testimonials for this service
Layout: Quote + patient info + rating

Styling:
- White cards
- Shadow on hover
- 5-star rating display
- Patient name/location/title
```

---

**Section 9: Call-to-Action**
```
Background: Gradient (primary to secondary)
Padding: 60px 40px
Alignment: Center

Heading: "Ready to Get Started?"
Color: White
Font: 36px

Subheading: "Book your free consultation today"
Color: White 80% opacity

Button: "Schedule Consultation"
URL: /contact/
Size: Large
Margin Top: 24px
```

---

## Step 3.4: Duplicate Service Page Template (Day 5 - 3 hours)

### Create 7 Service Pages

Use Elementor template inheritance to speed up page creation:

**Service Pages to Create:**

1. **Hair Transplant** (/hair-transplant/)
   - Hero: FUE, Pen-Implanter, and Grafts information
   - Techniques: FUE vs Pen-Implanter comparison
   - Pricing: Include graft counts and costs
   - Testimonials: Hair transplant specific

2. **Skin Treatments** (/skin-treatments/)
   - Services: List all skin treatments offered
   - Benefits: Skin health, rejuvenation focus
   - No graft information (not applicable)
   - Testimonials: Skin treatment specific

3. **Acne Treatment** (/acne-treatment-bengaluru/)
   - Hero: Acne solution focus
   - Techniques: Laser, chemical peels, treatments
   - Before/After: Skin acne cases
   - FAQ: Common acne questions

4. **Laser Hair Removal** (/laser-hair-removal-bengaluru/)
   - Hero: Permanent hair reduction
   - Techniques: Laser technology, results
   - Benefits: Fast, painless, permanent
   - FAQ: Hair removal process questions

5. **GFC Hair Treatment** (/gfc-hair-treatment-bengaluru/)
   - Hero: Non-surgical option
   - Technique: GFC therapy explanation
   - Sessions: Number of sessions needed
   - Results: Timeline and expectations

6. **PRP Hair Treatment** (/prp-hair-treatment-bengaluru/)
   - Similar to GFC
   - Sessions-based approach
   - Non-invasive focus

7. **HydraFacial** (/hydrafacial-bengaluru/)
   - Hero: Skin rejuvenation
   - Technique: HydraFacial technology
   - Sessions: Routine-based
   - Before/After: Skin transformation

**For each page:**

1. Create WordPress page with title and slug
2. Edit with Elementor
3. Use "Add Template" → Select master service template
4. Customize:
   - Hero heading and description
   - Before/after images specific to service
   - Testimonials filtered by treatment type
   - Pricing (if applicable)
   - Service-specific FAQs
5. Publish and verify

---

## Step 3.5: Results Gallery Page (Day 6 - 2 hours)

### Create Results/Gallery Page

Admin → Pages → Add New
- Title: Results Gallery
- Slug: results

**Edit with Elementor:**

**Section 1: Hero**
```
Background: Gradient
Heading: "Real Patient Results"
Subheading: "See the transformation with our proven techniques"
```

**Section 2: Gallery with Filters**

**Heading:**
```
Text: "Browse Our Case Studies"
Center aligned, 36px
```

**Filter Buttons:**
```
Layout: Button Group (horizontal)
Buttons:
  - All (shows all 10 case studies)
  - FUE (shows FUE cases)
  - Pen-Implanter (shows Pen-Implanter cases)
  - GFC (shows GFC cases)
  - Skin (shows skin treatment cases)

Interaction: Click filter → Gallery updates (Elementor dynamic)
```

**Gallery Grid:**
```
Columns: 3 (tablet: 2, mobile: 1)
Dynamic Loop: case_study posts
Sort: By featured first, then by date

Each Item (Before/After Card):
- Aspect ratio: 4:3
- Before image on left 50%
- After image on right 50%
- Draggable comparison slider
- On hover: Show case details
- On click: Expand to lightbox with details

Lightbox Content:
- Full case images (large)
- Technique badge
- Patient age
- Number of grafts
- Timeline to results
- Full case description
- Related case studies (next/prev navigation)
```

**Section 3: Statistics**
```
Background: Primary color
Color: White
Padding: 40px

4-Column Grid:

Column 1:
Number: 500+
Text: Successful Cases

Column 2:
Number: 98%
Text: Success Rate

Column 3:
Number: 4.9/5
Text: Patient Satisfaction

Column 4:
Number: 15+
Text: Years Experience
```

**Section 4: CTA**
```
Heading: "Ready to See Your Transformation?"
Button: "Book Consultation"
URL: /contact/
```

---

## Step 3.6: Contact Form Page (Day 6 - 1.5 hours)

### Create Contact Page

Admin → Pages → Add New
- Title: Contact Us
- Slug: contact

**Edit with Elementor:**

**Section 1: Hero**
```
Background: Gradient
Heading: "Get in Touch"
Subheading: "Book your free consultation or ask questions"
```

**Section 2: Contact Form & Info**

**2-Column Layout (tablet: 1, mobile: 1):**

**Left Column: Contact Form**

Using WPForms plugin:

1. Admin → WPForms → Add New
2. Form Name: "Contact Form"
3. Fields:
   ```
   - Name (required, single line text)
   - Email (required, email)
   - Phone (required, phone number)
   - Treatment Interest (required, dropdown)
     Options: Hair Transplant, Hair Loss Treatment, Skin Treatment, Other
   - Message (required, textarea)
   - GDPR Consent (required, checkbox)
     Label: "I agree to the privacy policy and terms of service"
   - Submit Button: "Send Message"
   ```
4. Notifications:
   - Send email to admin
   - Send confirmation to user
5. Confirmation: Display message "Thank you! We'll contact you within 24 hours."

**Place Form in Elementor:**
- Add form via Elementor WPForms widget
- Form style: Default
- Styling: Match site colors

**Right Column: Contact Information**

```
Background: Light gray (#f9fafb)
Padding: 32px 24px
Border Radius: 12px

Contact Details:

Address Section:
Icon: Location pin (primary color)
Heading: "Visit Us"
Text:
  Sanjeevani Cos Derma
  Sunrise Complex, 1693/A/32
  Dr Rajkumar Road, Prakash Nagar
  Rajajinagar, Bangalore 560010
  India

Phone Section:
Icon: Phone (primary color)
Heading: "Call Us"
Text: +91 82962 80340
Link: tel:+918296280340

Email Section:
Icon: Envelope (primary color)
Heading: "Email Us"
Text: cosdermasanjeevani@gmail.com
Link: mailto:cosdermasanjeevani@gmail.com

Hours Section:
Icon: Clock (primary color)
Heading: "Hours"
Text:
  Monday - Sunday
  10:30 AM - 6:30 PM
  (Every Day)

WhatsApp Button:
Icon: WhatsApp (green)
Text: "Chat on WhatsApp"
URL: https://wa.me/918296280340?text=Hi%20I%20would%20like%20to%20book%20a%20consultation
Styling: Green background, white text
```

---

**Section 3: Google Map**

```
Element: Elementor Google Map widget
Location: Rajajinagar, Bangalore
Coordinates: 12.9716, 77.5546
Zoom: 15
Marker: Clinic location
Height: 400px
```

---

**Section 4: Appointment Booking** (Optional - Phase 4)

If using Calendly or Acuity Scheduling:

```
Heading: "Quick Appointment Booking"
Subheading: "Schedule directly with our team"
Embedded calendar widget
Height: 600px
```

---

## Step 3.7: Header & Navigation Setup (Day 7 - 1.5 hours)

### GeneratePress Header Configuration

Admin → GeneratePress → Settings → Header

**Logo Setup:**
```
Logo: Upload clinic logo
Logo Width: 200px
Logo Height: Auto
Logo on mobile: Display
```

**Navigation Menu:**
- Primary Menu: Main Menu (created in Phase 2)
- Location: Header

**Header Layout:**
```
Left: Logo
Center: Menu
Right: CTA Button + Contact Info
```

**Header Style:**
```
Background: White
Text Color: #1F2937 (dark gray)
Link Color: #009fbf (primary)
Link Hover: Underline + color change
Shadow: Subtle (0 1px 3px rgba(0,0,0,0.1))
Sticky: YES (sticky on scroll)
Transparent on: Front page only
```

**Mobile Menu (Hamburger):**
```
Breakpoint: 768px
Icon: Hamburger menu
Slide direction: From right
Background: White overlay
Animation: Smooth slide-in
```

---

## Step 3.8: Footer Configuration (Day 7 - 1.5 hours)

### GeneratePress Footer Setup

Admin → Appearance → Widgets

**Footer Widget Areas: 3 columns (if supported)**

**Area 1: Clinic Information**
```
Title: "Sanjeevani Cos Derma"

Content Widget:
Clinic name
Address
Phone
Email
Social media icons
```

**Area 2: Quick Links**
```
Title: "Quick Links"
Menu: Footer Menu (created in Phase 2)
```

**Area 3: Business Hours**
```
Title: "Hours"
Content:
Monday - Sunday
10:30 AM - 6:30 PM

Closed: Holidays

Book Online: [Button]
```

**Bottom Footer:**
```
Left: Copyright text
Center: Privacy Policy | Terms | Accessibility
Right: Social icons

Styling:
Background: #1F2937 (dark gray)
Text Color: White
Link Color: #009fbf
Link Hover: Underline
Padding: 40px 20px
```

---

## Phase 3 Verification Checklist

**By end of Phase 3:**

- [ ] Elementor Global Settings configured
- [ ] Color palette set (#009fbf, #0ea5e9, #10b981, etc.)
- [ ] Typography configured (Playfair Display, Inter)
- [ ] Spacing system defined (8px grid)

- [ ] Homepage complete:
  - [ ] Hero section with statistics
  - [ ] Services grid (6 services)
  - [ ] Why Choose Us section
  - [ ] Before/After gallery preview
  - [ ] Testimonials carousel
  - [ ] CTA sections

- [ ] Service pages created (7 total):
  - [ ] Hair Transplant
  - [ ] Skin Treatments
  - [ ] Acne Treatment
  - [ ] Laser Hair Removal
  - [ ] GFC Hair Treatment
  - [ ] PRP Hair Treatment
  - [ ] HydraFacial
  - Each with: Hero, comparison, gallery, FAQ, CTA

- [ ] Results Gallery page:
  - [ ] Filter buttons working (by technique)
  - [ ] Before/After sliders displaying
  - [ ] 10 case studies visible
  - [ ] Statistics section
  - [ ] Lightbox functionality

- [ ] Contact page:
  - [ ] WPForms contact form functional
  - [ ] Validation working
  - [ ] Contact information displayed
  - [ ] Google Map embedded
  - [ ] WhatsApp button

- [ ] Header & Footer:
  - [ ] Navigation menu displaying correctly
  - [ ] Mobile menu (hamburger) working
  - [ ] Footer widgets populated
  - [ ] Social media links visible
  - [ ] Business hours displayed

- [ ] Responsive Design:
  - [ ] All pages tested on mobile (320px+)
  - [ ] Tablet layout (768px+) correct
  - [ ] Desktop layout (1024px+) correct
  - [ ] Images responsive
  - [ ] No horizontal scrolling

- [ ] Visual Design:
  - [ ] Color scheme consistent
  - [ ] Typography hierarchy clear
  - [ ] Spacing consistent (8px grid)
  - [ ] Buttons styled with hover effects
  - [ ] Cards have subtle shadows
  - [ ] Animations smooth and subtle

---

## Phase 3 Deliverables

**Pages Created:**
- Homepage (complete with all sections)
- 7 Service pages (with standardized template)
- Results Gallery page
- Contact page
- About page (basic)
- Blog page (auto-generated by WordPress)

**Design Elements:**
- Global Elementor styles and color palette
- Button components (primary, secondary, CTA)
- Card components with shadows and hover effects
- Icon boxes and grid layouts
- Forms styled and functional
- Gallery with filtering and lightbox
- Testimonials carousel

**Functionality:**
- Dynamic loops pulling from custom post types
- Before/After comparison sliders
- Filter buttons for case studies
- Contact form validation
- Responsive navigation
- Sticky header
- Mobile hamburger menu

---

## Next Steps: Phase 4

Phase 4 focuses on SEO and final optimization:
1. Configure JSON-LD schemas (6 types)
2. Set up redirects from Astro URLs
3. Yoast SEO optimization per page
4. Google My Business setup
5. Google Search Console configuration
6. Analytics implementation

**Phase 4 Duration:** 5 business days (Week 6)

---

**Phase 3 Status: READY FOR IMPLEMENTATION**

