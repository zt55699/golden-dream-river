# 金梦河家庭探险指南 (River of Golden Dreams Family Guide)

一个为家庭和宠物量身定制的惠斯勒金梦河划桨指南网站。

A comprehensive paddling guide website for families and pets exploring Whistler's River of Golden Dreams.

## 🌟 Features / 功能特色

### 🚣‍♀️ Interactive Route Map / 交互式路线地图
- **Terrain view** showing natural landscape and topography
- **Precise GPS waypoints** following the actual waterway through wetlands
- **Animated canoe** moving along the route to show direction
- **Clickable markers** with detailed start/end point information
- **User location tracking** with real-time GPS positioning

### 🌤️ Live Weather Forecast / 实时天气预报
- **Environment Canada integration** for accurate local weather
- **4-day forecast** with proper Chinese weekday names
- **Dynamic weather icons** matching current conditions
- **Chinese translations** for all weather conditions
- **High/low temperature display** with day and night temperatures
- **Retry logic** for reliable weather data fetching

### 👨‍👩‍👧‍👦 Family-Focused Content / 家庭专属内容
- **Safety tips** for paddling with young children (3+ years)
- **Pet-friendly guidance** for bringing dogs on the water
- **Equipment recommendations** and rental considerations
- **Logistics planning** for multi-vehicle shuttle setup
- **Interactive preparation checklist** with click-to-check items

### 🎨 User Experience / 用户体验
- **Fully responsive design** for mobile and desktop
- **Bilingual content** (Chinese and English)
- **Image lightbox** for detailed map viewing
- **Modern UI** with Tailwind CSS styling
- **Accessibility features** including proper alt text and ARIA labels

## 🛠️ Technical Stack / 技术栈

- **Frontend**: Pure HTML5, CSS3, JavaScript (ES6+)
- **Styling**: Tailwind CSS via CDN
- **Maps**: Google Maps JavaScript API with Geometry library
- **Weather**: Environment Canada API via CORS proxy
- **Fonts**: Inter + Noto Sans SC for bilingual typography
- **Deployment**: GitHub Pages compatible (static site)

## 🚀 Quick Start / 快速开始

1. **Clone the repository / 克隆仓库**
   ```bash
   git clone https://github.com/zt55699/golden-dream-river.git
   cd golden-dream-river
   ```

2. **Serve locally / 本地运行**
   ```bash
   # Using Python
   python3 -m http.server 8000
   
   # Using Node.js
   npx serve .
   
   # Using any static file server
   ```

3. **Open in browser / 在浏览器中打开**
   ```
   http://localhost:8000
   ```

## 🌍 Live Demo / 在线演示

Visit the live site: [https://zt55699.github.io/golden-dream-river/](https://zt55699.github.io/golden-dream-river/)

## 📱 API Integrations / API 集成

### Google Maps API
- **Maps JavaScript API**: Interactive mapping and route display
- **Geometry Library**: Canoe direction calculation and smooth animation
- **Places API**: Location markers and info windows

### Environment Canada Weather
- **CORS Proxy**: `api.allorigins.win` for cross-origin requests
- **Retry Logic**: 3 attempts with exponential backoff for reliability
- **Data Parsing**: Custom HTML parsing for forecast extraction

## 🎯 Route Information / 路线信息

**Start Point / 起点**: Rainbow Park (Alta Lake)
- GPS: `50.1199914, -122.9833144`
- Address: 5778 Alta Lake Rd, Whistler, BC

**End Point / 终点**: Meadow Park Sports Centre
- GPS: `50.1441348, -122.9599503`
- Address: 8625 BC-99, Whistler, BC

**Total Distance / 总距离**: ~7 km
**Estimated Time / 预计时间**: 2-3 hours
**Difficulty / 难度**: Easy (suitable for families)

## 🔧 Configuration / 配置

### Google Maps API Key
The current API key is restricted to the GitHub Pages domain. For local development or custom deployment:

1. Create a Google Cloud Project
2. Enable Maps JavaScript API and Geometry Library
3. Create an API key with domain restrictions
4. Replace the key in `index.html`:
   ```html
   <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&libraries=geometry&callback=initMap"></script>
   ```

### Weather Data Source
Weather data is fetched from Environment Canada with automatic retry logic. No API key required.

## 🎨 Customization / 自定义

### Weather Conditions
Add new weather translations in the `weatherTranslations` object:
```javascript
const weatherTranslations = {
    'Your Condition': '您的天气状况',
    // ...
};
```

### Route Points
Update GPS coordinates in the `routePoints` array for different routes:
```javascript
const routePoints = [
    { lat: 50.1199914, lng: -122.9833144 }, // Start
    // ... your waypoints
    { lat: 50.1441348, lng: -122.9599503 }  // End
];
```

### Animation Speed
Adjust canoe animation speed:
```javascript
progress += 0.002; // Lower = slower, higher = faster
```

## 📄 License / 许可证

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing / 贡献

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📞 Contact / 联系方式

For questions about the River of Golden Dreams route, please contact local Whistler tourism or recreation authorities.

For technical issues with this website, please open an issue on GitHub.

---

**Disclaimer**: Weather conditions and water levels can change rapidly. Always check current conditions and safety advisories before starting your paddling adventure.

**免责声明**: 天气条件和水位可能快速变化。在开始划桨探险之前，请务必检查当前状况和安全建议。