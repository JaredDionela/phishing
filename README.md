# Microsoft Account Password Change - GoPhish Landing Page

This is a Microsoft Account-themed landing page designed for use with GoPhish phishing simulation campaigns.

## GoPhish Integration

### Setup Instructions

1. **Upload to GoPhish Templates**:
   - Copy the content of `index.html` 
   - In GoPhish admin panel, go to "Landing Pages"
   - Create a new landing page and paste the HTML content
   - GoPhish will automatically replace `{{.URL}}` with your server URL

2. **Template Variables**:
   - `{{.URL}}` - Your GoPhish server URL (automatically replaced)
   - `{{.RID}}` - Recipient ID for tracking (can be added if needed)
   - `{{.FirstName}}`, `{{.LastName}}`, `{{.Email}}` - User data from campaign

3. **Tracking Features**:
   - **Page Visit Tracking**: Automatically tracks when someone visits the page
   - **Form Submission Tracking**: Captures credentials when form is submitted
   - **Redirect**: Redirects to legitimate Microsoft login after data capture

### Analytics Tracked

- Email addresses entered
- Current passwords
- New passwords
- Form submission timestamps
- User interactions

### Security Notes

⚠️ **Important**: This template is designed for authorized security awareness training and penetration testing only. Ensure you have proper authorization before use.

## Hosting Options

### Option 1: GoPhish Built-in Hosting (Recommended for Testing)
- Use GoPhish's built-in web server
- Template will be served directly from GoPhish

### Option 2: Vercel Hosting + GoPhish Integration
- Host on Vercel for professional deployment
- Modify the GoPhish script URL to point to your GoPhish server
- Update CORS settings in GoPhish if needed

#### Vercel Deployment Steps:
1. Push your code to GitHub (already done!)
2. Go to https://vercel.com and sign up/login
3. Click "New Project"
4. Import your GitHub repository: `JaredDionela/phishing`
5. Deploy with default settings
6. Your site will be live at: `https://your-project-name.vercel.app`

### Option 3: InfinityFree Hosting
- Alternative free hosting option
- Upload files manually to htdocs folder

## File Structure

```
├── index.html          # Main landing page
├── phishing.html       # Backup copy
└── README.md          # This file
```

## Customization

To customize for your organization:

1. Update the Microsoft logo URL if needed
2. Modify redirect URL in JavaScript
3. Adjust styling to match target organization
4. Add additional form fields if required

## Testing

Before launching a campaign:

1. Test the landing page locally
2. Verify GoPhish tracking is working
3. Check redirect functionality
4. Ensure mobile responsiveness