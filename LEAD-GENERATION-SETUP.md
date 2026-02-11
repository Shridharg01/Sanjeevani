# 📞 Lead Generation Form Setup Guide

## 🎯 Overview
This guide shows you how to set up and optimize lead generation forms for maximum conversions from Bangalore patients.

---

## 📋 Current Lead Generation Setup

### **1. Main Contact Form**
**Location:** `src/pages/contact.astro`

**Current Features:**
✅ Name, Phone, Email fields
✅ Service selection dropdown
✅ Preferred time selection
✅ Message field
✅ WhatsApp integration
✅ Automatic form submission to WhatsApp

### **2. Quick Action Buttons**
**Locations:** Throughout the website

**Current Features:**
✅ "Book Free Consultation" buttons
✅ "WhatsApp Expert" buttons
✅ "Call Now" buttons
✅ Direct phone number links

---

## 🚀 Enhanced Lead Generation Setup

### **Step 1: Add Location-Specific Fields**

Add this to your contact form in `src/pages/contact.astro`:

```html
<!-- Add after the email field -->
<div class="form-group">
  <select id="location" name="location" required>
    <option value="">Select Your Area in Bangalore</option>
    <option value="electronic-city">Electronic City</option>
    <option value="whitefield">Whitefield</option>
    <option value="marathahalli">Marathahalli</option>
    <option value="koramangala">Koramangala</option>
    <option value="indiranagar">Indiranagar</option>
    <option value="hsr-layout">HSR Layout</option>
    <option value="btm-layout">BTM Layout</option>
    <option value="jayanagar">Jayanagar</option>
    <option value="rajajinagar">Rajajinagar</option>
    <option value="malleswaram">Malleswaram</option>
    <option value="yeshwanthpur">Yeshwanthpur</option>
    <option value="vijayanagar">Vijayanagar</option>
    <option value="basaveshwaranagar">Basaveshwaranagar</option>
    <option value="peenya">Peenya</option>
    <option value="hebbal">Hebbal</option>
    <option value="other">Other Bangalore Area</option>
  </select>
</div>

<!-- Add after service selection -->
<div class="form-group">
  <select id="budget" name="budget">
    <option value="">Budget Range (Optional)</option>
    <option value="under-50k">Under ₹50,000</option>
    <option value="50k-1lakh">₹50,000 - ₹1,00,000</option>
    <option value="1lakh-2lakh">₹1,00,000 - ₹2,00,000</option>
    <option value="above-2lakh">Above ₹2,00,000</option>
    <option value="discuss">Prefer to Discuss</option>
  </select>
</div>

<!-- Add urgency field -->
<div class="form-group">
  <select id="urgency" name="urgency">
    <option value="">When are you planning the procedure?</option>
    <option value="immediately">Within 1 month</option>
    <option value="soon">Within 3 months</option>
    <option value="planning">Within 6 months</option>
    <option value="researching">Just researching</option>
  </select>
</div>
```

### **Step 2: Enhanced WhatsApp Message Template**

Update the WhatsApp message in the contact form script:

```javascript
const whatsappMessage = `🏥 *New Consultation Request - Sanjeevani Cos Derma*

👤 *Patient Details:*
Name: ${name}
Phone: ${phone}
Email: ${email}
Location: ${location}

🏥 *Treatment Interest:*
Service: ${service}
Budget Range: ${budget}
Timeline: ${urgency}
Preferred Time: ${time}

📝 *Additional Information:*
${message}

📍 *Patient Location:* ${location}, Bangalore
⏰ *Inquiry Time:* ${new Date().toLocaleString('en-IN', {timeZone: 'Asia/Kolkata'})}

Please confirm appointment availability. Thank you!`;
```

### **Step 3: Add Lead Scoring System**

Add this lead scoring logic to prioritize high-quality leads:

```javascript
function calculateLeadScore(formData) {
  let score = 0;
  
  // Location scoring (closer = higher score)
  const highValueAreas = ['electronic-city', 'whitefield', 'koramangala', 'indiranagar'];
  if (highValueAreas.includes(formData.location)) score += 20;
  
  // Budget scoring
  const budgetScores = {
    'above-2lakh': 30,
    '1lakh-2lakh': 25,
    '50k-1lakh': 20,
    'under-50k': 15,
    'discuss': 10
  };
  score += budgetScores[formData.budget] || 0;
  
  // Urgency scoring
  const urgencyScores = {
    'immediately': 30,
    'soon': 25,
    'planning': 15,
    'researching': 5
  };
  score += urgencyScores[formData.urgency] || 0;
  
  // Service type scoring
  const serviceScores = {
    'hair-transplant': 25,
    'pen-implanter': 30,
    'fue': 25,
    'gfc': 15,
    'skin-treatment': 10
  };
  score += serviceScores[formData.service] || 0;
  
  return score;
}
```

---

## 📊 Lead Generation Optimization Strategies

### **1. Multiple Entry Points**

#### **Homepage CTAs:**
- Hero section: "Book Free Consultation"
- Services section: Service-specific CTAs
- Testimonials: "Share Your Experience"
- Footer: Contact information

#### **Service Page CTAs:**
- Top of page: "Get Cost Estimate"
- Middle of page: "Book Free Assessment"
- Bottom of page: "Schedule Consultation"

#### **Blog Post CTAs:**
- Within content: "Learn More About [Service]"
- End of post: "Book Free Consultation"
- Sidebar: "Get Expert Advice"

### **2. Exit-Intent Popups**

Add this exit-intent popup code:

```html
<!-- Add to Layout.astro before closing body tag -->
<div id="exitIntentPopup" class="exit-popup" style="display: none;">
  <div class="popup-content">
    <button class="close-popup">&times;</button>
    <h3>Wait! Don't Miss Your Free Consultation</h3>
    <p>Get expert advice on hair transplant options in Bangalore</p>
    <div class="popup-actions">
      <a href="https://wa.me/918296280340" class="btn btn-whatsapp">WhatsApp Now</a>
      <a href="/contact" class="btn btn-primary">Book Consultation</a>
    </div>
  </div>
</div>

<script>
let exitIntentShown = false;
document.addEventListener('mouseleave', function(e) {
  if (e.clientY <= 0 && !exitIntentShown) {
    document.getElementById('exitIntentPopup').style.display = 'flex';
    exitIntentShown = true;
  }
});

document.querySelector('.close-popup').addEventListener('click', function() {
  document.getElementById('exitIntentPopup').style.display = 'none';
});
</script>
```

### **3. Floating WhatsApp Button**

Add this floating WhatsApp button:

```html
<!-- Add to Layout.astro -->
<div class="floating-whatsapp">
  <a href="https://wa.me/918296280340" target="_blank" rel="noopener">
    <svg width="24" height="24" fill="currentColor" viewBox="0 0 24 24">
      <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893A11.821 11.821 0 0020.465 3.63"/>
    </svg>
    <span>Chat with Expert</span>
  </a>
</div>

<style>
.floating-whatsapp {
  position: fixed;
  bottom: 20px;
  right: 20px;
  z-index: 1000;
}

.floating-whatsapp a {
  display: flex;
  align-items: center;
  gap: 8px;
  background: #25D366;
  color: white;
  padding: 12px 16px;
  border-radius: 50px;
  text-decoration: none;
  box-shadow: 0 4px 12px rgba(37, 211, 102, 0.4);
  transition: all 0.3s ease;
  animation: pulse 2s infinite;
}

.floating-whatsapp a:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(37, 211, 102, 0.6);
}

@keyframes pulse {
  0% { box-shadow: 0 4px 12px rgba(37, 211, 102, 0.4); }
  50% { box-shadow: 0 4px 12px rgba(37, 211, 102, 0.8); }
  100% { box-shadow: 0 4px 12px rgba(37, 211, 102, 0.4); }
}

@media (max-width: 768px) {
  .floating-whatsapp a span {
    display: none;
  }
  .floating-whatsapp a {
    width: 56px;
    height: 56px;
    border-radius: 50%;
    justify-content: center;
  }
}
</style>
```

---

## 📈 Lead Tracking & Analytics

### **1. Google Analytics Setup**

Add enhanced tracking to your forms:

```javascript
// Add to contact form submission
gtag('event', 'form_submit', {
  'event_category': 'Lead Generation',
  'event_label': 'Contact Form',
  'value': calculateLeadScore(formData)
});

// Track WhatsApp clicks
document.querySelectorAll('a[href*="wa.me"]').forEach(link => {
  link.addEventListener('click', function() {
    gtag('event', 'whatsapp_click', {
      'event_category': 'Lead Generation',
      'event_label': 'WhatsApp Button'
    });
  });
});

// Track phone clicks
document.querySelectorAll('a[href^="tel:"]').forEach(link => {
  link.addEventListener('click', function() {
    gtag('event', 'phone_click', {
      'event_category': 'Lead Generation',
      'event_label': 'Phone Number'
    });
  });
});
```

### **2. Lead Quality Scoring**

Implement this lead scoring system:

```javascript
const leadQualityIndicators = {
  // High-quality indicators
  highQuality: [
    'immediate timeline',
    'high budget range',
    'specific service interest',
    'detailed message',
    'premium location'
  ],
  
  // Medium-quality indicators
  mediumQuality: [
    'planning timeline',
    'medium budget',
    'general inquiry',
    'standard location'
  ],
  
  // Low-quality indicators
  lowQuality: [
    'just researching',
    'no budget specified',
    'very brief message',
    'far location'
  ]
};
```

### **3. Automated Follow-up System**

Set up automated responses based on lead quality:

```javascript
function setupAutomatedFollowup(leadData) {
  const score = calculateLeadScore(leadData);
  
  if (score >= 80) {
    // High-priority lead - immediate response
    scheduleFollowup('immediate', leadData);
  } else if (score >= 50) {
    // Medium-priority lead - 2-hour response
    scheduleFollowup('2hours', leadData);
  } else {
    // Low-priority lead - 24-hour response
    scheduleFollowup('24hours', leadData);
  }
}
```

---

## 🎯 Conversion Optimization Tips

### **1. Form Optimization:**
- Keep forms short (max 6 fields)
- Use progressive disclosure
- Add trust indicators
- Include social proof
- Use action-oriented CTAs

### **2. Page Speed Optimization:**
- Optimize images
- Minimize JavaScript
- Use CDN for assets
- Enable compression

### **3. Mobile Optimization:**
- Responsive design
- Touch-friendly buttons
- Easy form filling
- Quick loading

### **4. Trust Building:**
- Display certifications
- Show patient testimonials
- Include doctor credentials
- Add security badges

---

## 📞 Lead Response Templates

### **High-Priority Lead Response:**
```
Hi [Name],

Thank you for your interest in hair transplant at Sanjeevani Cos Derma!

I see you're from [Location] and interested in [Service]. We have immediate availability for consultation.

Can we schedule your free consultation for:
- Tomorrow at [Time]
- [Alternative Time]

Our Rajajinagar clinic is easily accessible from [Location] via metro/bus.

Best regards,
Sanjeevani Cos Derma Team
📞 +91 82962 80340
```

### **Medium-Priority Lead Response:**
```
Hi [Name],

Thank you for reaching out to Sanjeevani Cos Derma!

Based on your inquiry about [Service], I'd like to schedule a free consultation to discuss your options and provide a personalized treatment plan.

Available slots this week:
- [Date/Time options]

We're conveniently located in Rajajinagar with easy access from [Location].

Looking forward to helping you achieve your hair goals!

Best regards,
Sanjeevani Cos Derma Team
```

---

## 📊 Success Metrics to Track

### **Lead Generation KPIs:**
- Form submission rate
- WhatsApp inquiry rate
- Phone call volume
- Appointment booking rate
- Lead-to-patient conversion rate

### **Quality Metrics:**
- Average lead score
- Response time
- Follow-up completion rate
- Patient satisfaction scores

### **Source Tracking:**
- Organic search leads
- Social media leads
- Direct website leads
- Referral leads

---

**Remember: The key to successful lead generation is providing immediate value and making it easy for potential patients to take the next step. Focus on building trust and addressing their specific concerns about hair transplant in Bangalore.**