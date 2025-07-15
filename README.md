# Neuton Browser

A modern, privacy-focused web browser built with Electron that blocks ads, tracking scripts, and enhances your online privacy.

## Features

### 🔒 Privacy Protection
- **Ad Blocking**: Automatically blocks advertisements and ad networks
- **Tracking Protection**: Blocks tracking scripts, pixels, and analytics
- **Cookie Control**: Blocks third-party cookies and tracking cookies
- **Fingerprinting Protection**: Prevents browser fingerprinting attempts
- **Enhanced Security Headers**: Adds security headers to protect against common attacks

### 🛡️ Security Features
- **Do Not Track**: Automatically sends DNT headers
- **Secure Browsing**: Enhanced security headers and protections
- **Session Isolation**: Each tab runs in its own isolated context
- **No Data Collection**: The browser doesn't collect or store your browsing data

### 🎨 Modern Interface
- **Dark Theme**: Beautiful dark interface that's easy on the eyes
- **Tab Management**: Multiple tabs with easy switching and closing
- **Search Integration**: Built-in search with multiple search engines
- **Quick Links**: Easy access to popular websites
- **Responsive Design**: Works well on different screen sizes

### ⚙️ Customizable Settings
- **Privacy Controls**: Toggle ad blocking, tracking protection, and cookie blocking
- **Search Engine Selection**: Choose your preferred search engine
- **Keyboard Shortcuts**: Full keyboard navigation support

## Installation

### Prerequisites
- Node.js (version 16 or higher)
- npm or yarn

### Steps

1. **Clone or download the project**
   ```bash
   git clone <repository-url>
   cd neuton-browser
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Run the browser**
   ```bash
   npm start
   ```

### Building for Distribution

To create distributable packages:

```bash
npm run build
```

This will create platform-specific packages in the `dist` folder.

## Usage

### Basic Navigation
- **Address Bar**: Type URLs or search terms directly
- **Navigation Buttons**: Use back, forward, and reload buttons
- **Tabs**: Click tabs to switch between pages, or use Ctrl+T for new tabs

### Privacy Features
- **Automatic Blocking**: Ads and trackers are blocked automatically
- **Privacy Stats**: View blocked content statistics on the welcome page
- **Settings**: Access privacy settings via the settings button (gear icon)

### Keyboard Shortcuts
- `Ctrl+T` (or `Cmd+T` on Mac): New tab
- `Ctrl+W` (or `Cmd+W` on Mac): Close current tab
- `Ctrl+R` (or `Cmd+R` on Mac): Reload page
- `Ctrl+L` (or `Cmd+L` on Mac): Focus address bar

### Search Engines
The browser supports multiple search engines:
- **DuckDuckGo** (default) - Privacy-focused search
- **Google** - Traditional search
- **Bing** - Microsoft's search engine

## Privacy Features Explained

### What Gets Blocked
1. **Advertisement Networks**: Google AdSense, Facebook Ads, Amazon Ads, etc.
2. **Tracking Scripts**: Google Analytics, Facebook Pixel, etc.
3. **Analytics Services**: Various website analytics and tracking services
4. **Third-party Cookies**: Cookies from domains other than the current site
5. **Fingerprinting Attempts**: Scripts that try to identify your browser uniquely

### How It Works
- **Network Level**: Requests to known tracking domains are blocked before they reach the server
- **Script Level**: JavaScript tracking code is prevented from executing
- **Header Level**: Privacy-enhancing headers are added to all requests
- **Storage Level**: Tracking attempts via localStorage and sessionStorage are blocked

## Technical Details

### Architecture
- **Electron**: Cross-platform desktop application framework
- **WebView**: Chromium-based web rendering engine
- **Node.js**: Backend functionality and system integration

### Security Model
- **Context Isolation**: Renderer process is isolated from main process
- **Sandboxing**: Web content runs in a sandboxed environment
- **No Node Integration**: Web pages cannot access Node.js APIs

### Privacy Implementation
- **Request Filtering**: Network requests are filtered at the session level
- **Script Injection**: Privacy scripts are injected into web pages
- **Header Modification**: Request and response headers are modified for privacy

## Development

### Project Structure
```
neuton-browser/
├── src/
│   ├── main.js              # Main Electron process
│   ├── preload.js           # Preload script for security
│   └── renderer/
│       ├── index.html       # Main browser interface
│       ├── styles.css       # Styling
│       └── renderer.js      # Browser logic
├── assets/                  # Icons and assets
├── package.json            # Dependencies and scripts
└── README.md              # This file
```

### Development Commands
```bash
npm start          # Run in development mode
npm run dev        # Run with development flags
npm run build      # Build for distribution
npm run dist       # Create distributable packages
```

## Contributing

Contributions are welcome! Please feel free to submit issues and pull requests.

### Areas for Improvement
- Additional ad-blocking rules
- More privacy features
- Performance optimizations
- UI/UX enhancements
- Platform-specific features

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Disclaimer

This browser is designed to enhance privacy but cannot guarantee complete anonymity. Always use additional privacy tools (VPNs, etc.) for maximum protection.

## Support

If you encounter any issues or have questions:
1. Check the existing issues on GitHub
2. Create a new issue with detailed information
3. Include your operating system and browser version

---

**Neuton Browser** - Browse the web with confidence and privacy. 