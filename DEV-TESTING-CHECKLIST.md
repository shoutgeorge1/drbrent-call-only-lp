# Dr. Brent Moelleken Landing Page - Dev Testing Checklist

**Live URL:** https://drbrent-call-only-lp-v4pp.vercel.app/  
**Repository:** https://github.com/shoutgeorge1/drbrent-call-only-lp

## Overview
This is a phone-only landing page for Dr. Brent Moelleken. All conversions are tracked through phone call clicks. Please thoroughly test all functionality before deployment.

---

## Critical Functionality Tests

### ✅ Phone Number Links
- [ ] **Sticky Call Bar** (top of page) - Verify `tel:+13109191060` link works
- [ ] **Hero CTA Button** - Verify `tel:+13109191060` link works
- [ ] **Beverly Hills Location** - Verify `tel:+13109191060` link works
- [ ] **Santa Barbara Location** - Verify `tel:+18059792535` link works
- [ ] **Bottom CTA Button** - Verify `tel:+13109191060` link works
- [ ] All phone links trigger phone dialer on mobile devices
- [ ] All phone links are clickable and properly formatted

### ✅ Call Tracking (GTM)
- [ ] Verify GTM tracking script is firing on all call link clicks
- [ ] Check browser console for any JavaScript errors
- [ ] Verify `dataLayer.push` events are firing with correct data:
  - Event: `call_click`
  - Phone number captured correctly
  - Link text captured correctly
  - Link location captured correctly

### ✅ Visual/Design Checks
- [ ] Logo positioning - Should NOT cover doctor's face in hero image
- [ ] Hero image displays correctly (Brent-Moelleken-Team.jpg)
- [ ] Team section image is properly contained in gradient box (not overpowering)
- [ ] All images load correctly (no broken images)
- [ ] Text is readable and properly formatted
- [ ] Colors match brand guidelines (accent blue: #1e73be)
- [ ] Spacing and padding look consistent

### ✅ Responsive Design
- [ ] **Mobile (320px - 767px)**
  - [ ] Sticky call bar displays correctly
  - [ ] Logo scales appropriately
  - [ ] Hero section text is readable
  - [ ] CTA buttons are full-width and tappable
  - [ ] All sections stack vertically
  - [ ] Images scale properly
  - [ ] No horizontal scrolling

- [ ] **Tablet (768px - 1023px)**
  - [ ] Two-column layouts display correctly
  - [ ] Images and text are balanced
  - [ ] CTA buttons are appropriately sized

- [ ] **Desktop (1024px+)**
  - [ ] Full layout displays correctly
  - [ ] Max-width containers are centered
  - [ ] All hover states work (buttons, links)

### ✅ Performance
- [ ] Page loads quickly (< 3 seconds)
- [ ] Images are optimized and load efficiently
- [ ] No console errors or warnings
- [ ] Lighthouse score: 90+ for Performance, Accessibility, Best Practices, SEO

### ✅ Accessibility
- [ ] All images have proper alt text
- [ ] Phone links have proper aria-labels
- [ ] Color contrast meets WCAG AA standards
- [ ] Keyboard navigation works (Tab through all links)
- [ ] Focus states are visible on all interactive elements

### ✅ Cross-Browser Testing
- [ ] Chrome (latest)
- [ ] Safari (latest)
- [ ] Firefox (latest)
- [ ] Edge (latest)
- [ ] Mobile Safari (iOS)
- [ ] Chrome Mobile (Android)

### ✅ SEO/Meta Tags
- [ ] Title tag is present and correct
- [ ] Meta description is present
- [ ] All heading tags are properly structured (h1, h2, h3)
- [ ] Semantic HTML is used correctly

---

## Specific Issues to Verify Fixed

1. **Logo Position** - Logo should be positioned below the doctor's face, not covering it
2. **Team Image** - Should be contained in a subtle gradient box, not overpowering
3. **Mobile Layout** - All elements should be properly sized and spaced on mobile devices
4. **Call Tracking** - All phone number clicks must fire GTM events

---

## Testing Instructions

1. **Desktop Testing:**
   - Open the live URL in multiple browsers
   - Test all phone links (they should open phone dialer or show phone number)
   - Verify hover states on buttons
   - Check responsive design using browser dev tools

2. **Mobile Testing:**
   - Test on actual devices (iOS and Android)
   - Verify all phone links trigger native phone dialer
   - Check touch targets are large enough (minimum 44x44px)
   - Test sticky call bar functionality

3. **Tracking Verification:**
   - Open browser console (F12)
   - Click each phone link
   - Verify `dataLayer.push` events appear in console
   - Check GTM Preview mode to confirm events are firing

4. **Performance Testing:**
   - Run Google PageSpeed Insights
   - Run Lighthouse audit
   - Check network tab for slow-loading resources

---

## Known Requirements

- **Phone Numbers:**
  - Beverly Hills: 310.919.1060
  - Santa Barbara: 805.979.2535

- **Tracking:**
  - All call clicks must fire GTM events
  - Event name: `call_click`
  - Must capture: phone_number, link_text, link_location

- **Design:**
  - Logo should not cover doctor's face
  - Team image should be subtle and contained
  - Mobile-first responsive design

---

## Sign-Off

Once all items are checked and verified, please confirm:
- [ ] All functionality works correctly
- [ ] No console errors
- [ ] Tracking is firing properly
- [ ] Mobile experience is optimal
- [ ] Ready for production deployment

**Tested by:** _______________  
**Date:** _______________  
**Status:** ☐ Ready for Production | ☐ Needs Fixes

---

## Notes for Dev Team

- This is a phone-only landing page - there are no forms
- All conversions are tracked through phone call clicks
- Focus on ensuring all phone links work and tracking fires correctly
- Pay special attention to mobile experience as most traffic will be mobile
- If you find any issues, please document them clearly with screenshots

