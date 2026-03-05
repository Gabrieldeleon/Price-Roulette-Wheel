# 🎡 Prize Roulette Wheel

A modern, customizable prize roulette wheel built with React. Perfect for promotions, giveaways, contests, and interactive marketing campaigns.

![Prize Wheel Demo](https://img.shields.io/badge/React-18-blue) ![Tailwind CSS](https://img.shields.io/badge/TailwindCSS-3-38bdf8)

## ✨ Features

- 🎨 **Fully Customizable**
  - Custom colors for each prize segment (background & text)
  - Editable heading and button text
  - Custom logo support (via URL)
  
- 🎯 **Smart Prize Management**
  - Set win limits for each prize
  - Segments automatically disappear when limit is reached
  - Unlimited prizes option (set to -1)
  - Real-time win tracking

- 🎪 **Smooth Animations**
  - Realistic spinning physics with easing
  - 4-second spin duration
  - Fixed center pointer for clear results

- 📱 **Responsive Design**
  - Works on desktop and mobile
  - Modern glassmorphic UI
  - Gradient background

- ⚙️ **Easy Configuration**
  - Built-in settings panel
  - Live preview of all changes
  - Test image loading before use

## 🚀 Quick Start

### Option 1: Standalone HTML (Recommended)

1. Download or copy the component code
2. Create an `index.html` file with this structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Prize Wheel</title>
  <script crossorigin src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
  <script crossorigin src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body>
  <div id="root"></div>
  
  <script type="text/babel">
    // Paste the entire prize-wheel.jsx code here
    
    // Add this at the bottom:
    const root = ReactDOM.createRoot(document.getElementById('root'));
    root.render(<PrizeWheel />);
  </script>
</body>
</html>
```

3. Open `index.html` in your browser

### Option 2: React Project

If you have an existing React project:

```bash
# Copy prize-wheel.jsx to your components folder
# Then in your app:

import PrizeWheel from './components/prize-wheel';

function App() {
  return <PrizeWheel />;
}
```

## 🎮 How to Use

### Basic Usage

1. **Open the wheel** - Load the HTML file in your browser
2. **Click "Show Settings"** to customize
3. **Edit prizes** - Change text, colors, and win limits
4. **Customize branding** - Add your logo URL and heading
5. **Click "SPIN THE WHEEL"** to play!

### Customizing Prizes

Each prize segment has these properties:

- **Text**: The prize name/description
- **Background Color**: Segment color (color picker)
- **Text Color**: Text color for readability (color picker)
- **Max Wins**: Number of times this prize can be won
  - Set to `-1` for unlimited
  - Set to any positive number for a limit
  - Segment disappears when limit is reached

### Setting Win Limits

```
Example Configuration:
- "10% OFF" → Max Wins: 10
- "Try Again!" → Max Wins: -1 (unlimited)
- "Free T-shirt" → Max Wins: 3
- "$25 Coupon" → Max Wins: 2
```

## 🎨 Customization Guide

### Changing the Logo

1. Host your logo image online (or use a CDN URL)
2. Copy the image URL
3. In Settings → Logo URL, paste the URL
4. Click "Test Load" to verify it works
5. Logo appears as a circular badge above the wheel

### Color Schemes

The wheel comes with vibrant default colors, but you can customize each segment:
- Use the color pickers in the settings panel
- Recommended: Use contrasting colors for text visibility
- The center pointer uses gold (#FFD700) to stand out

### Responsive Behavior

- **Desktop**: 96x96 (24rem) wheel size
- **Mobile**: 80x80 (20rem) wheel size
- Text automatically scales
- Settings panel scrolls on smaller screens

## 🛠️ Technical Details

### Built With

- **React 18** - UI framework
- **Tailwind CSS** - Styling
- **Lucide React** - Icons
- **SVG** - Wheel graphics and pointer

### Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

### Dependencies (CDN)

All dependencies are loaded via CDN for the standalone version:
- React 18
- React DOM 18
- Babel Standalone (for JSX transformation)
- Tailwind CSS

## 📝 Configuration Options

### Default Prize Configuration

```javascript
[
  { text: "10% OFF", color: "#FF6B6B", textColor: "#FFFFFF", maxWins: 10, currentWins: 0 },
  { text: "Try Again!", color: "#4ECDC4", textColor: "#FFFFFF", maxWins: -1, currentWins: 0 },
  { text: "15% OFF", color: "#FFE66D", textColor: "#1A1A1A", maxWins: 5, currentWins: 0 },
  { text: "Free T-shirt", color: "#95E1D3", textColor: "#1A1A1A", maxWins: 3, currentWins: 0 },
  { text: "$25 Coupon", color: "#F38181", textColor: "#FFFFFF", maxWins: 2, currentWins: 0 },
  { text: "Try Again!", color: "#AA96DA", textColor: "#FFFFFF", maxWins: -1, currentWins: 0 }
]
```

## 🎯 Use Cases

- **E-commerce promotions** - Discount codes and coupons
- **Event marketing** - Prize giveaways at conferences
- **Social media campaigns** - Engagement and lead generation
- **Retail stores** - In-store promotions
- **Contest websites** - Online prize draws
- **Fundraising events** - Raffle alternatives

## 🔧 Troubleshooting

### Logo not loading
- Ensure the image URL is publicly accessible
- Use HTTPS URLs (not HTTP)
- Click "Test Load" to verify the URL
- Check browser console for CORS errors
- Try using Imgur, Cloudinary, or similar image hosting

### Wheel not spinning
- Check browser console for errors
- Ensure all CDN resources loaded correctly
- Try refreshing the page

### Segments not disappearing
- Verify `maxWins` is set correctly (not -1)
- Check that `currentWins` is incrementing in settings
- The segment only disappears after reaching the limit

## 📄 License

This project is open source and available for personal and commercial use.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

## 📧 Support

For questions or support, please open an issue on GitHub.

---

**Made with ❤️ for interactive promotions and giveaways**
