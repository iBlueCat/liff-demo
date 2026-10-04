# LIFF Demo - Building LIFF app into LINE

Source code for LIFF v2 online course. A comprehensive demonstration of LINE Front-end Framework (LIFF) v2 features and capabilities.

## 📋 Table of Contents

- [Prerequisites](#prerequisites)
- [Features](#features)
- [Setup Instructions](#setup-instructions)
- [Project Structure](#project-structure)
- [Configuration](#configuration)
- [Deployment](#deployment)
- [Learning Resources](#learning-resources)
- [Troubleshooting](#troubleshooting)

## Prerequisites

Before getting started, you'll need:

1. **LINE Developer Account**
   - Create a provider at [LINE Developers Console](https://developers.line.biz/en/docs/liff/getting-started/#creating-a-provider-and-channel)
   - Create a channel for your LIFF app
   - Register a [LIFF app](https://developers.line.biz/en/docs/liff/registering-liff-apps/#registering-liff-app)

2. **GitHub Pages Setup**
   - Create a GitHub account (if you don't have one)
   - Enable [GitHub Pages](https://pages.github.com/) for this repository
   - Configure custom domain (optional)

3. **Tools & Software**
   - Git (for version control)
   - Text editor or IDE (VS Code recommended)
   - Modern web browser with LINE app installed

## ✨ Features

This LIFF demo includes:

- **User Authentication**
  - LIFF initialization and login flow
  - User profile retrieval (userId, displayName, email, pictureUrl)
  - Friendship status checking
  - Logout functionality

- **Messaging Features**
  - Send messages to chat
  - Share messages using Share Target Picker
  - Flex message templates
  - Text and rich message formats

- **LIFF Actions**
  - Open external URLs
  - Scan QR codes
  - Context detection (1-on-1, group, room)
  - Close LIFF window

- **Advanced Features**
  - Permanent Link creation
  - Query parameter handling
  - Deep linking
  - Universal Link support
  - Multi-environment support
  - Debug console integration (vConsole)

- **Device Information**
  - OS and language detection
  - LIFF version information
  - Access token retrieval
  - Client detection

## 🚀 Setup Instructions

### Step 1: Clone the Repository

```bash
git clone https://github.com/iBlueCat/liff-demo.git
cd liff-demo
```

### Step 2: Get Your LIFF ID

1. Go to [LINE Developers Console](https://developers.line.biz/)
2. Select your provider and channel
3. Go to LIFF app settings
4. Copy your LIFF ID

### Step 3: Configure Your LIFF ID

Edit `index.html` and update line 588:

```javascript
await liff.init({ liffId: "YOUR_LIFF_ID_HERE" })
```

Replace `YOUR_LIFF_ID_HERE` with your actual LIFF ID from step 2.

### Step 4: Deploy to GitHub Pages

```bash
git add .
git commit -m "Configure LIFF ID"
git push origin master
```

Your LIFF app will be available at: `https://yourusername.github.io/liff-demo/`

### Step 5: Register LIFF App Endpoint

1. In LINE Developers Console, go to your LIFF app settings
2. Set the Endpoint URL to your GitHub Pages URL
3. Save the changes

### Step 6: Test Your LIFF App

1. Add your LINE Bot as a friend
2. Open the LIFF app in LINE
3. Verify all features are working correctly

## 📁 Project Structure

```
liff-demo/
├── index.html           # Main LIFF demo page
├── answer.html          # Additional demo page
├── README.md            # This file
├── .gitignore           # Git ignore file
├── css/
│   └── style.css        # Styling
├── js/
│   └── vconsole.min.js  # Debug console
├── path/
│   └── index.html       # Path-based demo
└── backend/             # Backend examples (optional)
```

## ⚙️ Configuration

### LIFF ID Configuration

The main configuration needed is setting your LIFF ID in `index.html`:

```javascript
// Line 588 in index.html
await liff.init({ liffId: "YOUR_LIFF_ID" })
```

### LIFF SDK Version

Currently using LIFF SDK v2.20.5. To update, modify the script tag in `index.html`:

```html
<script src="https://static.line-scdn.net/liff/edge/versions/2.20.5/sdk.js"></script>
```

Check [LIFF SDK Release Notes](https://developers.line.biz/en/docs/liff/) for the latest version.

### Environment Variables

For production, consider using environment variables:

```javascript
const LIFF_ID = process.env.LIFF_ID || "YOUR_LIFF_ID_HERE"
await liff.init({ liffId: LIFF_ID })
```

## 🌐 Deployment

### GitHub Pages (Recommended for this project)

1. Ensure your repository is public
2. Go to repository Settings → Pages
3. Select source as main/master branch
4. Your site will be available at `https://yourusername.github.io/liff-demo/`

### Custom Domain

1. In repository Settings → Pages → Custom domain
2. Enter your domain name
3. Update DNS records as instructed

### Other Platforms

- **Vercel**: Connect GitHub repo for automatic deployment
- **Netlify**: Drag and drop or connect Git
- **AWS S3 + CloudFront**: For production applications
- **Your own server**: Upload files via FTP/SFTP

## 📚 Learning Resources

### Official LINE Documentation

- [LIFF Getting Started](https://developers.line.biz/en/docs/liff/getting-started/)
- [LIFF API Reference](https://developers.line.biz/en/docs/liff/reference/)
- [LINE Messaging API](https://developers.line.biz/en/docs/messaging-api/)
- [Flex Message Layout](https://developers.line.biz/en/docs/messaging-api/reference/#flex-message)

### Blog Posts

- [รู้จักกับ LINE Front-end Framework เวอร์ชัน 2 (LIFF v2)](https://medium.com/linedevth/85fdfb678cc6)
- [Deep Dive into LIFF & LINE Mini App](https://medium.com/linedevth/7a1de37eaeae)
- [วิธีการดึง Email ของผู้ใช้ใน LIFF v2](https://medium.com/linedevth/93ce9b944b57)
- [Share Target Picker Feature](https://medium.com/linedevth/27b480681b5b)
- [Creating Universal Links](https://medium.com/linedevth/7bf17a435339)
- [Creating Deep Links](https://medium.com/linedevth/9a130fbf53e0)
- [Automated UI Tests with Cypress.io](https://medium.com/linedevth/dccbefce7ed5)

## 📸 Screenshots

<table width="100%">
  <tr>
    <th><img src="https://user-images.githubusercontent.com/1763410/75949415-c3d9d000-5ed8-11ea-8508-606b25b062f4.png" width="100%"></th>
    <th><img src="https://user-images.githubusercontent.com/1763410/75949419-c805ed80-5ed8-11ea-9a7e-b18f8dcacdfc.png" width="100%"></th>
    <th><img src="https://user-images.githubusercontent.com/1763410/75949422-cb00de00-5ed8-11ea-9e84-d737555cfcef.png" width="100%"></th>
  </tr>
</table>

## 🎓 Course Content

This course covers:

1. **LIFF Fundamentals**
   - Setting up and initializing LIFF app
   - Getting LIFF Environment
   - Understanding LIFF context

2. **User Management**
   - Getting User Profile
   - Managing user authentication
   - Checking friendship status

3. **Messaging**
   - Sending messages to chat
   - Creating flex messages
   - Using Share Target Picker

4. **LIFF Actions**
   - Opening external browsers
   - Scanning QR codes
   - Sharing to friends or groups

5. **Advanced Topics**
   - Supporting external browsers
   - Creating permanent and deep links
   - Promoting your LIFF app
   - Debugging and caching avoidance

## 🐛 Troubleshooting

### Common Issues

#### 1. "LIFF ID is invalid"
- Verify LIFF ID is correctly configured
- Check LIFF app is enabled in LINE Developers Console
- Ensure endpoint URL is set correctly

#### 2. "User profile is not available"
- Make sure user is logged in to LINE
- Check user hasn't blocked the bot account
- Verify user granted required permissions

#### 3. "Message sending fails"
- Only available when LIFF is opened in LINE chat
- Verify bot has permission to send messages
- Check LIFF context is not "none"

#### 4. "QR Code scanning not working"
- Only works in LINE app (not web browser)
- User must have camera permissions
- Some browsers may not support this feature

#### 5. "GitHub Pages not showing latest changes"
- Clear browser cache
- Wait a few minutes for GitHub to publish changes
- Verify changes were pushed to master/main branch

### Debug Console

The app includes vConsole for debugging:

1. Open the LIFF app
2. Open developer console (F12)
3. Look for vConsole icon in the corner
4. Check logs and network requests

### Enable Debug Logging

Add to your `index.html` to see LIFF SDK logs:

```javascript
liff.init({
  liffId: "YOUR_LIFF_ID"
}).then(() => {
  console.log("LIFF initialized")
}).catch(err => {
  console.error("LIFF init error:", err)
})
```

## 📞 Support

- 📖 [LINE Developers Documentation](https://developers.line.biz/en/docs/)
- 💬 [LINE Developers Community](https://community.line.biz/)
- 🐛 [GitHub Issues](https://github.com/iBlueCat/liff-demo/issues)
- 📧 Contact: iBlueCat on GitHub

## 📝 License

This project is provided as-is for educational purposes.

## 🔄 Updates

**Last Updated**: October 4, 2024

### Recent Changes

- ✅ Updated LIFF SDK to v2.20.5
- ✅ Added comprehensive README
- ✅ Added .gitignore configuration
- ✅ Improved code documentation
- ✅ Added troubleshooting guide

### Version History

- **v2.0** (Oct 2024) - Updated to latest LIFF SDK, improved documentation
- **v1.0** (May 2020) - Initial release

## 🙏 Acknowledgments

Thanks to:
- LINE Developers team for excellent documentation
- Community members who contributed improvements
- All users testing and providing feedback

---

**Happy coding! 🚀**

If you found this project helpful, please consider giving it a ⭐ on GitHub!
