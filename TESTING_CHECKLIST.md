# WEEKEND TESTING CHECKLIST

**Goal:** Verify the dashboard works perfectly before Monday's customer demos

**Time Required:** ~2 hours total across Saturday-Sunday

---

## 📅 SATURDAY MORNING (30 minutes)

### Test 1: Basic Installation & Setup

**Objective:** Confirm the app opens and first-time setup works

- [ ] Download `sme-compliance-dashboard.html` to Desktop
- [ ] Double-click to open in browser
- [ ] Verify you see "Let's set up your first company" wizard
- [ ] Fill in test company details:
  ```
  Company Name: Test Law Firm (Pty) Ltd
  Reg Number: 2020/123456/07
  Reg Date: 2020-04-15
  Year-End: February
  Turnover: R1M - R10M (EME)
  Employees: 5
  VAT Registered: Yes
  VAT Frequency: Bi-monthly
  Provisional Taxpayer: Yes
  Company Type: Private Company (Pty) Ltd
  ```
- [ ] Click "Create Company"
- [ ] Verify dashboard loads (no errors)
- [ ] Check company name appears in header
- [ ] **PASS/FAIL:** _________

**If FAIL:** Note the error and try in different browser

---

## 📅 SATURDAY AFTERNOON (45 minutes)

### Test 2: Deadline Calculations

**Objective:** Verify all deadlines are calculated correctly

#### SARS Deadlines

- [ ] Navigate to SARS module (bottom nav)
- [ ] Verify Provisional Tax dates appear:
  ```
  Expected for Feb year-end:
  - 1st Payment: Around August 31, 2026
  - 2nd Payment: Around February 28, 2027
  ```
- [ ] Check dates are business days (not weekends)
- [ ] Verify VAT returns appear (bi-monthly, 25th of month)
- [ ] Check PAYE dates (7th of each month)
- [ ] **PASS/FAIL:** _________

#### CIPC Deadline

- [ ] Navigate to CIPC module
- [ ] Verify Annual Return date shows:
  ```
  Expected: ~30 business days after April 15
  Should be around May 27-30, 2026
  ```
- [ ] Confirm it's not a weekend
- [ ] **PASS/FAIL:** _________

#### Dashboard Summary

- [ ] Navigate back to Home/Dashboard
- [ ] Verify "This Week" section shows relevant deadlines
- [ ] Check "Next 30 Days" populates
- [ ] Confirm "Overdue" is empty (for new company)
- [ ] Check compliance score appears (should be low since nothing marked complete)
- [ ] **PASS/FAIL:** _________

---

### Test 3: Multi-Company Support

**Objective:** Verify you can manage multiple companies

- [ ] Click ➕ button (top right, in company selector)
- [ ] Setup wizard appears again
- [ ] Fill in second test company:
  ```
  Company Name: Rental Property Co (Pty) Ltd
  Reg Number: 2018/789012/07
  Reg Date: 2018-12-01
  Year-End: December
  Turnover: Under R1M
  Employees: 0
  VAT Registered: No
  Provisional Taxpayer: No
  Company Type: Private Company (Pty) Ltd
  ```
- [ ] Click "Create Company"
- [ ] Verify dropdown now shows 2 companies
- [ ] Switch between companies using dropdown
- [ ] Confirm each shows different deadlines
- [ ] Verify first company data is still intact
- [ ] **PASS/FAIL:** _________

---

## 📅 SATURDAY EVENING (30 minutes)

### Test 4: Data Persistence

**Objective:** Confirm data survives browser restart

- [ ] Note current company name in dropdown
- [ ] Note one deadline from dashboard
- [ ] **Close the browser completely** (not just the tab)
- [ ] Wait 30 seconds
- [ ] Re-open the HTML file
- [ ] Verify same company loads automatically
- [ ] Check the noted deadline still appears
- [ ] Verify both companies still in dropdown
- [ ] **PASS/FAIL:** _________

---

### Test 5: Checkbox Functionality

**Objective:** Verify marking deadlines as complete works

- [ ] Go to Dashboard (any company)
- [ ] Find a deadline in "This Week" or "Next 30 Days"
- [ ] Click the checkbox next to it
- [ ] Verify the deadline gets strikethrough
- [ ] Check compliance score increases
- [ ] Uncheck the box
- [ ] Verify strikethrough disappears
- [ ] Check score decreases back
- [ ] **PASS/FAIL:** _________

---

## 📅 SUNDAY MORNING (15 minutes)

### Test 6: POPIA Module

**Objective:** Verify POPIA checklist works

- [ ] Navigate to POPIA module (bottom nav)
- [ ] Verify score shows "0/10"
- [ ] Check 10 items appear (each with description)
- [ ] Click checkbox on first item
- [ ] Verify score updates to "1/10"
- [ ] Check 5 random items
- [ ] Verify score updates to "6/10"
- [ ] Uncheck 2 items
- [ ] Verify score updates to "4/10"
- [ ] **PASS/FAIL:** _________

---

### Test 7: Calendar Export

**Objective:** Verify export feature works

- [ ] Go to Dashboard
- [ ] Click "📤 Export to Calendar" button
- [ ] Verify `.ics` file downloads
- [ ] Check filename includes company name
- [ ] Open file in calendar app (Google/Outlook/Apple)
- [ ] Verify deadlines appear as calendar events
- [ ] Check dates match dashboard
- [ ] **PASS/FAIL:** _________

---

## 📅 SUNDAY AFTERNOON (30 minutes)

### Test 8: Mobile Responsiveness

**Option A: Use Actual Phone**
- [ ] Open HTML file on your phone
- [ ] Check all 5 bottom nav buttons work
- [ ] Verify company dropdown works
- [ ] Test setup wizard on mobile
- [ ] Check checkboxes are clickable (not too small)

**Option B: Use Chrome DevTools**
- [ ] Open dashboard in Chrome
- [ ] Press F12 (open DevTools)
- [ ] Click device toolbar icon (or Ctrl+Shift+M)
- [ ] Select "iPhone 12 Pro" from device list
- [ ] Test navigation
- [ ] Test form inputs
- [ ] Test checkboxes

- [ ] **PASS/FAIL:** _________

---

### Test 9: Print Report

**Objective:** Verify print layout is clean

- [ ] Go to Dashboard
- [ ] Click "🖨️ Print Report" button
- [ ] Check print preview:
  - [ ] Navigation buttons hidden
  - [ ] Company selector hidden
  - [ ] Export buttons hidden
  - [ ] Content is clean and readable
  - [ ] All deadlines visible
- [ ] **PASS/FAIL:** _________

---

### Test 10: Company Deletion

**Objective:** Verify delete function works safely

- [ ] Select the "Rental Property Co" (second test company)
- [ ] Click 🗑️ button (delete)
- [ ] Verify confirmation dialog appears
- [ ] Click Cancel - confirm nothing deleted
- [ ] Click 🗑️ again
- [ ] Click OK to confirm
- [ ] Verify company is deleted
- [ ] Check dropdown only shows first company now
- [ ] Verify first company data still intact
- [ ] **PASS/FAIL:** _________

---

## 📅 SUNDAY EVENING (20 minutes)

### Test 11: Browser Compatibility

**Objective:** Verify works in multiple browsers

**Test in Chrome:**
- [ ] Open dashboard
- [ ] Navigate to all 5 modules
- [ ] Mark deadline complete
- [ ] Export calendar
- [ ] **PASS/FAIL:** _________

**Test in Safari (Mac) or Edge (Windows):**
- [ ] Open same HTML file
- [ ] Data still there (same LocalStorage)
- [ ] All functions work
- [ ] **PASS/FAIL:** _________

**Test on Mobile Browser:**
- [ ] Open on phone's Safari/Chrome
- [ ] Check navigation works
- [ ] Verify readable on small screen
- [ ] **PASS/FAIL:** _________

---

### Test 12: Customer Demo Dry Run

**Objective:** Practice Monday's demo flow

- [ ] **Close all browser tabs**
- [ ] Open dashboard in fresh browser
- [ ] Time yourself: Set up new company from scratch
  - Target: Under 3 minutes
  - Actual time: _________ minutes
- [ ] Navigate through all modules as if showing customer
- [ ] Practice explaining:
  - [ ] "This is your compliance dashboard"
  - [ ] "We calculate SARS deadlines automatically"
  - [ ] "CIPC accounts for business days"
  - [ ] "Track POPIA compliance"
  - [ ] "Manage multiple companies"
  - [ ] "Export to your calendar"
- [ ] End with pricing: "R199/month, want to start today?"
- [ ] **PASS/FAIL:** _________

---

## 🐛 BUGS FOUND LOG

**If any test fails, record here:**

| Test # | Issue Description | Browser | Severity (High/Med/Low) | Fixed? |
|--------|------------------|---------|-------------------------|---------|
| Example: Test 2 | VAT dates showing weekend | Chrome | High | Yes |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |

---

## ✅ FINAL PRE-DEMO CHECKLIST (Sunday Night)

- [ ] All 12 tests passed (or bugs fixed)
- [ ] Dashboard works on laptop
- [ ] Dashboard works on phone
- [ ] Can set up company in under 3 minutes
- [ ] Deadlines calculate correctly
- [ ] Multi-company switching works
- [ ] Export function works
- [ ] Practiced demo script
- [ ] Screenshots saved (for backup/marketing)
- [ ] HTML file copied to safe location (not Downloads)
- [ ] Laptop charged
- [ ] Phone charged
- [ ] Customer details ready (if received)

---

## 📊 TEST RESULTS SUMMARY

**Total Tests:** 12  
**Passed:** _________  
**Failed:** _________  
**Bugs Fixed:** _________  
**Bugs Remaining:** _________  

**Ready for Monday demo?** YES / NO

**If NO, what needs fixing?**
_______________________________________________
_______________________________________________
_______________________________________________

---

## 🚀 MONDAY MORNING (Pre-Demo)

### 30 Minutes Before First Meeting

- [ ] Open dashboard in fresh browser window
- [ ] Have customer details ready to input (if received)
- [ ] Close all distracting tabs/apps
- [ ] Turn off notifications
- [ ] Have pricing sheet visible
- [ ] Test screen sharing (if virtual demo)
- [ ] Take 3 deep breaths

**You've tested everything. It works. You're ready.** 💪

---

## 📝 CUSTOMER DEMO DATA (Optional)

If customers send their details before demo, prepare here:

**Customer 1: __________________**
- Reg Date: _______________
- Year-End: _______________
- Employees: _______________
- VAT: Yes / No
- Provisional: Yes / No

**Customer 2: __________________**
- Reg Date: _______________
- Year-End: _______________
- Employees: _______________
- VAT: Yes / No
- Provisional: Yes / No

**Customer 3: __________________**
- Reg Date: _______________
- Year-End: _______________
- Employees: _______________
- VAT: Yes / No
- Provisional: Yes / No

**Customer 4: __________________**
- Reg Date: _______________
- Year-End: _______________
- Employees: _______________
- VAT: Yes / No
- Provisional: Yes / No

---

**Testing complete. Dashboard ready. Let's sell.** 🎯
