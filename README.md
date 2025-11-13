# Ad Approval Portal Template

Template repository for Static Shift client ad approval portals.

## Setup Instructions

### For New Client:

1. **Use this template** (click green button)
2. Name repo: `ads-approval-[client-name-lowercase]`
3. Edit `index.html` and update CONFIG section:
   - SHEET_ID
   - API_KEY  
   - APPS_SCRIPT_URL
4. Enable GitHub Pages: Settings → Pages → Source: main branch
5. Portal will be live at: `https://[username].github.io/[repo-name]/`

## Configuration Values Needed

- **SHEET_ID**: From Google Sheet URL
- **API_KEY**: From Google Cloud Console
- **APPS_SCRIPT_URL**: From Apps Script deployment

## Support

Contact: operations@staticshift.com.au
```

4. Commit changes

#### Step 2.3.4: Mark as Template Repository
1. Go to: Settings (repo settings)
2. Scroll to: **Template repository**
3. Check: ✓ Template repository
4. Save

**✅ Template Setup Complete!**

---

## 3. New Client Onboarding

**⏱️ Time Required:** 11 minutes per client  
**Prerequisites:** Templates created (Section 2)

### 3.1 Pre-Setup Information Gathering

Before starting, collect from the client:

- [ ] Business name (exact as appears on Facebook)
- [ ] Website URL
- [ ] Landing page URL (destination for ads)
- [ ] Facebook Page profile image (or get from their page)
- [ ] Client contact email
- [ ] Initial batch of ad creative assets

**Template Document:**

Create a Google Doc template called "Client Onboarding Checklist" with this:
```
CLIENT: _____________________
SETUP DATE: _____________________
POINT OF CONTACT: _____________________

INFORMATION COLLECTED:
□ Business Name: _____________________
□ Website URL: _____________________
□ Landing Page URL: _____________________
□ Profile Image: _____________________
□ Client Email: _____________________

PORTAL DETAILS (Fill during setup):
□ Sheet ID: _____________________
□ Apps Script URL: _____________________
□ GitHub Repo: _____________________
□ Portal URL: _____________________

COMPLETION:
□ Portal tested and working
□ Sheet shared with client (Viewer access)
□ Welcome email sent
□ Quick start guide attached
```

### 3.2 Duplicate Template Sheet

#### Step 3.2.1: Make Copy
**⏱️ 1 minute**

1. Open: `[TEMPLATE] Meta Ads Tracking Sheet - Static Shift`
2. File → Make a copy
3. Name: `Meta Ads Tracking Sheet - [Client Name]`
   - Example: `Meta Ads Tracking Sheet - HRAO`
   - Example: `Meta Ads Tracking Sheet - Food Effects`
4. Click: **Make a copy**
5. New sheet opens automatically

#### Step 3.2.2: Update Client Info
**⏱️ 2 minutes**

1. Go to: **Client Info** tab
2. Click on Row 2
3. Update each cell:

| Column | Value | Example |
|--------|-------|---------|
| A | Client ID | CLI-003 |
| B | Business Name | HR Advice Online |
| C | Website URL | https://hradviceonline.com.au |
| D | Destination URL | https://hradviceonline.com.au/consultation |
| E | Profile Image URL | *(see below for getting this)* |

**Getting Profile Image URL:**

**Option 1: If client provides image:**
1. Upload to your Google Drive
2. Right-click → Get link → Anyone with link can view
3. Copy the link:  
   `https://drive.google.com/file/d/ABC123XYZ/view`
4. Convert to direct URL:  
   `https://lh3.googleusercontent.com/d/ABC123XYZ`
5. Paste in Column E

**Option 2: From Facebook Page:**
1. Go to client's Facebook Page
2. Right-click their profile image → Copy image address
3. Paste directly into Column E

#### Step 3.2.3: Get Sheet ID
**⏱️ 30 seconds**

1. Look at the browser URL bar
2. Copy the Sheet ID:
```
   https://docs.google.com/spreadsheets/d/[THIS_IS_THE_SHEET_ID]/edit
```
3. Save it in your onboarding checklist
4. Example: `1OQxNLz4IuwsVOSVBTOyvZK-a_9mog81Cns5XGZYBFXU`

### 3.3 Deploy Apps Script

#### Step 3.3.1: Open Apps Script
**⏱️ 30 seconds**

1. In the new client sheet: Extensions → Apps Script
2. 🎉 **Code is already there!** (from template)
3. Verify you see the script code

#### Step 3.3.2: Create New Deployment
**⏱️ 1 minute**

1. Click: Deploy → **New deployment**
2. Click the gear icon ⚙️ next to "Select type"
3. Select: **Web app**
4. Settings:
   - Description: `Ad approval webhook for [Client Name]`
   - Execute as: **Me ([your-email@staticshift.com.au])**
   - Who has access: **Anyone**
5. Click: **Deploy**

#### Step 3.3.3: Authorize (First Time Only)
**⏱️ 1 minute (first client), 0 minutes (subsequent clients)**

**First client setup only:**
1. Click: **Authorize access**
2. Choose your Google account
3. Click: **Advanced**
4. Click: **Go to Ad Approval Handler (unsafe)**
5. Click: **Allow**

**Subsequent clients:**
- No authorization needed! ✨

#### Step 3.3.4: Copy Web App URL
**⏱️ 15 seconds**

1. After deployment, a dialog appears with the Web App URL
2. Copy the entire URL:
```
   https://script.google.com/macros/s/AKfycby.../exec
