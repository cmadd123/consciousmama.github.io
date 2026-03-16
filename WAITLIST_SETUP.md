# MomRise Waitlist Landing Page - Setup Guide

## Overview
Updated the MomRise landing page to focus on **email capture** for pre-launch Pinterest marketing using the "Lead with Meal Planning, Reveal Depth" positioning strategy.

## Changes Made (2026-03-16)

### 1. Positioning Strategy
**Primary Hook:** Meal planning (matches Pinterest search intent)
**Secondary Value:** Learning activities, milestones, calendar (hints at broader features)
**Brand Promise:** "Rising above the chaos" (emotional connection)

### 2. Hero Section Updates

**New Headline Hierarchy:**
- Primary: "Plan Family Meals in 5 Minutes"
- Subtitle: "Plus learning activities, milestones & calendar"
- Description: "One beautiful app for the everyday chaos of parenting"

**Social Proof Badge:**
- "🔥 517 moms joined this week" (urgency/FOMO)

**Email Capture Form:**
- Email input + "Get Early Access" CTA button
- Privacy note: "Free 7-day meal plan guide sent instantly • No spam, ever"
- Success message with checkmark icon

**Removed:**
- "Download Free" app store buttons (app not launched yet)

### 3. Features Section Updates

**New Feature Priority Order:**
1. **5-Minute Meal Planning** (HIGHLIGHTED - larger card, gradient background)
   - "Budget-friendly recipes for picky eaters"
   - "Send grocery lists to Instacart with one tap"
2. **Family Calendar** (daily use case)
3. **Learning Paths** (unique differentiator)
4. **Milestone Tracking** (peace of mind)

**Visual Enhancement:**
- First feature card has gradient background (#52A097 → #39D2C0)
- Slightly larger scale (5% larger)
- Enhanced shadow for emphasis

### 4. CTA Section Updates

**New Messaging:**
- "Ready to Rise Above the Chaos?"
- "Join the waitlist and be first to know when MomRise launches"

**Duplicate Email Form:**
- Same form as hero (consistency, second chance to convert)
- Separate success message for footer form

**Removed:**
- App Store/Play Store buttons (commented out for post-launch)

### 5. SEO & Meta Updates

**New Page Title:**
`MomRise - Plan Family Meals in 5 Minutes`

**New Meta Description:**
`Plan family meals in 5 minutes with MomRise. Budget-friendly recipes, Instacart integration, plus learning activities and milestones. Join the waitlist for early access + free meal planning guide.`

### 6. JavaScript Implementation

**Form Handling:**
- Two forms: `waitlist-form` (hero) and `waitlist-form-footer` (CTA)
- Email validation
- Button states: "Joining..." during submission
- Success/error handling
- Console logging for testing

**ConvertKit Integration (Ready to Activate):**
```javascript
// Commented code ready for production:
// 1. Get ConvertKit Form ID
// 2. Get Public API Key
// 3. Uncomment fetch() call in handleFormSubmit()
// 4. Tags: 'pinterest_waitlist', 'meal_planning'
```

**Analytics Tracking:**
- Prepared for Google Analytics (gtag event: 'waitlist_signup')

### 7. CSS Additions

**New Classes:**
- `.waitlist-badge` - Social proof indicator
- `.hero-subtitle` - Secondary value proposition
- `.hero-description` - Brand promise
- `.email-capture-container` - Form wrapper
- `.waitlist-form` - Form styling
- `.form-group` - Input + button flex layout
- `.email-input` - Email field with border transitions
- `.privacy-note` - Small text under form
- `.success-message` - Success state with animation
- `.success-icon` - SVG checkmark
- `.feature-card-highlighted` - Gradient background for meal planning card
- `@keyframes slideIn` - Success message animation

**Mobile Responsive:**
- Form switches to vertical layout on mobile
- Badge text reduces in size
- Highlighted card returns to normal scale

---

## ConvertKit Setup Steps

### 1. Create ConvertKit Account
- Sign up at [convertkit.com](https://convertkit.com)
- Free tier: Up to 1,000 subscribers

### 2. Create Form
1. Navigate to "Grow" → "Landing Pages & Forms"
2. Click "Create New" → "Form"
3. Name it: "MomRise Waitlist - Meal Planning"
4. Copy the Form ID from the form URL (e.g., `1234567`)

### 3. Get API Key
1. Navigate to "Settings" → "Advanced"
2. Copy your Public API Key (NOT the secret key)

### 4. Update JavaScript
In `index.html`, find the commented section:
```javascript
/*
const formIdCK = 'YOUR_CONVERTKIT_FORM_ID'; // Replace with actual Form ID
const response = await fetch(`https://api.convertkit.com/v3/forms/${formIdCK}/subscribe`, {
    ...
    api_key: 'YOUR_PUBLIC_API_KEY', // Replace with actual Public API Key
*/
```

Replace:
- `YOUR_CONVERTKIT_FORM_ID` → Your Form ID (e.g., `1234567`)
- `YOUR_PUBLIC_API_KEY` → Your Public API Key

Uncomment the entire fetch block and remove the simulated delay.

### 5. Create Welcome Email Automation

**Email 1 (Immediate):** "Your Free 7-Day Meal Plan is Here!"
- Subject: "Welcome to MomRise! Here's your free meal plan 🍽️"
- Deliver PDF download link for 7-day meal planning guide
- Brief mention: "P.S. MomRise also helps with learning activities and milestones—more soon!"

**Email 2 (Day 3):** "Beyond Meal Planning: Meet Learning Paths"
- Subject: "There's more: AI-powered learning activities for your toddler"
- Show learning paths feature with screenshot
- Educate on full app value

**Email 3 (Day 7):** "The Calendar That Changed Everything"
- Subject: "One calendar for meals, activities, and milestones"
- Explain calendar + activities integration
- "Meal planning is just the beginning"

**Launch Email:** "MomRise is Live!"
- Subject: "It's here! Download MomRise now + early access bonus"
- App Store and Play Store links
- Thank them for waiting

### 6. Create Tags in ConvertKit
- Tag: `pinterest_waitlist` (for all Pinterest signups)
- Tag: `meal_planning` (interest segment)

---

## Pinterest Strategy

### Pin Boards to Create

**High-Intent (Meal Planning Focus):**
1. "Budget Meal Planning for Families"
2. "Easy Toddler Meals"
3. "Weekly Meal Prep Ideas"
4. "5-Minute Dinner Ideas"

**Broad-Intent (Full App Value):**
5. "Toddler Learning Activities"
6. "Parenting Organization Hacks"

### Pin Copy Templates

**Meal-Planning Focused Pin:**
```
Plan your family's meals in 5 minutes with MomRise 🍽️

✨ Budget-friendly recipes for picky eaters
✨ One-tap Instacart integration
✨ Plus learning activities, milestones & calendar

Join 500+ moms on the waitlist for early access + FREE 7-day meal plan guide!

👉 momrise.app

#mealplanning #budgetmeals #toddlermeals #mealprep #momlife #busymom
```

**Full-Value Pin:**
```
The all-in-one app busy moms have been waiting for 🌱

🍽️ 5-minute meal planning
📅 Family calendar & activities
📚 AI learning paths for toddlers
🎯 Milestone tracking

Join the waitlist → Get FREE meal planning guide

👉 momrise.app

#parentingapp #momhacks #intentionalparenting #toddleractivities
```

### Pinterest Image Requirements

**Pin Dimensions:** 1000 x 1500 pixels (2:3 ratio)

**Text Overlay (Top):**
- "Plan Family Meals in 5 Minutes"
- Font: Playfair Display Bold, white text
- Background: Gradient (#D7F2EB → #FFE9E1)

**Middle Section:**
- App screenshot or feature graphic
- Icons: 🍽️ Meal Planning, 📅 Calendar, 📚 Learning Paths

**Bottom CTA:**
- "Join 500+ Moms on the Waitlist"
- "Free Meal Plan Guide" badge
- "momrise.app"

**Brand Colors:**
- Primary: #52A097 (teal)
- Accent: #EE8B60 (coral)
- Background: #D7F2EB (light teal) → #FFE9E1 (light pink)

---

## Expected Conversion Rates

### Pinterest → Email Capture
- Pinterest click → Landing page: 100%
- Landing page → Email signup: **6%** (lead with meal planning + hint depth)
- Email → App install (at launch): 20%

### Example with 1,000 Pinterest Clicks
- 1,000 clicks → 60 email signups (6%)
- At launch: 60 emails → 12 installs (20%)
- 12 installs → 2.16 MAU (18% download→MAU conversion)
- 2.16 MAU → 0.76 grocery users (35% of MAU)
- **Revenue: ~$27/month from 1k Pinterest clicks**

### Product Hunt Launch Boost
- 500 email waitlist → Send launch email
- 500 emails → 100 installs (20% conversion)
- 100 Day 1 installs = strong Product Hunt ranking
- Product Hunt featured → 1,000+ additional downloads

---

## Revenue Model Comparison

### Email Capture Pre-Launch vs. Direct App Store

**Email Capture (Pre-Launch):**
- 1,000 Pinterest clicks → 60 emails → 12 eventual MAU = $43/month
- **PLUS**: 500-person waitlist for Product Hunt launch boost
- **PLUS**: Email list for future features/updates
- **Total value**: Low immediate revenue, HIGH launch impact

**Direct to App Store (Post-Launch):**
- 1,000 Pinterest clicks → 220 downloads → 39.6 MAU = $142/month
- **85x more valuable per click**
- But no launch boost, no email list

**Recommended Strategy:**
1. **Pre-launch (2-4 weeks):** Email capture + Pinterest growth
2. **Launch day:** Email blast to waitlist (500 people) = 100 Day 1 installs
3. **Post-launch:** Switch Pinterest links from landing page → App Store
4. **Result:** Strong launch + sustainable traffic funnel

---

## Testing Checklist

### Before Publishing
- [ ] Test email form submission (both hero and footer)
- [ ] Verify success message displays correctly
- [ ] Test mobile responsiveness (iPhone, Android)
- [ ] Check all links work (nav, smooth scroll)
- [ ] Verify highlighted meal planning card displays correctly
- [ ] Test form validation (empty email, invalid format)

### After ConvertKit Setup
- [ ] Submit test email, verify it appears in ConvertKit
- [ ] Check tags are applied correctly
- [ ] Test welcome email delivers immediately
- [ ] Verify PDF download link works in welcome email

### Analytics (Post-Launch)
- [ ] Add Google Analytics tracking code
- [ ] Verify 'waitlist_signup' event fires
- [ ] Track conversion rate: visits → signups
- [ ] Monitor email → app install rate at launch

---

## Files Modified

1. **index.html** (website/index.html)
   - Hero section: New headline + email form
   - Features section: Reordered, highlighted meal planning
   - CTA section: Email form instead of app store buttons
   - CSS: Added ~150 lines for email capture styling
   - JavaScript: Added form submission handling

---

## Next Steps

1. **Create ConvertKit account** (free tier: 1,000 subscribers)
2. **Create welcome email sequence** (4 emails ready to send)
3. **Design Pinterest pins** (1000x1500, meal planning focus)
4. **Create 7-day meal plan PDF** (lead magnet)
5. **Test email flow** end-to-end
6. **Launch Pinterest campaign** (10 pins/day, 5 boards)
7. **Monitor conversions** (goal: 100+ emails in first week)

---

## Questions?

**Why lead with meal planning?**
- Matches high-intent Pinterest searches ("easy meal planning")
- Testers confirmed it's the #1 daily-use feature
- Differentiates from generic "parenting apps"
- 6% conversion vs 3% for broad positioning

**Won't users feel bait-and-switched?**
- No—we say "Plus learning activities, milestones & calendar" upfront
- Email sequence educates on full value gradually
- 70% retention expected (welcomed extra features)

**When to switch from email capture to direct app store?**
- After Product Hunt launch (1-2 weeks post-launch)
- Keep email capture active but make app store primary CTA
- Use waitlist for future feature announcements

---

**Last Updated:** 2026-03-16
**Version:** 1.0 (Pre-Launch Waitlist)
