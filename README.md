
# 🏛️ Interactive 3D Museum Experience ✨

An immersive web-based museum experience built with Three.js, React, and Blender. Explore a beautifully crafted virtual museum environment with interactive exhibits, dynamic lighting, and engaging visual effects.

![Museum Preview](public/media/og-image.webp?raw=true "3D Museum Experience")

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build
```

## ✨ Features

- **Immersive 3D Environment**: Navigate through detailed museum halls and galleries
- **Interactive Exhibits**: Click and explore various artifacts and displays
- **Dynamic Lighting**: Realistic torch lighting and atmospheric effects
- **Custom Shaders**: Beautiful waterfall effects and fire animations
- **Responsive Design**: Optimized for desktop and mobile devices
- **Audio Integration**: Ambient sounds and interactive audio feedback
- **Performance Optimized**: Efficient 3D rendering with optimized assets

## 🛠️ Technology Stack

- **Three.js** - 3D graphics library
- **React** - UI framework
- **React Three Fiber** - React renderer for Three.js
- **@react-three/drei** - Useful helpers for R3F
- **Blender** - 3D modeling and asset creation
- **GLSL** - Custom shader development
- **WebGL** - Hardware-accelerated graphics

## 📁 Project Structure

```
src/
├── components/          # React components
├── Experience/          # 3D scene components
│   ├── World/          # 3D world elements
│   ├── components/     # 3D interactive components
│   └── shaders/        # Custom GLSL shaders
├── hooks/              # Custom React hooks
├── utils/              # Helper functions
└── assets/             # 3D models, textures, audio

public/
├── models/             # GLTF/GLB 3D models
├── textures/           # Image textures
└── audio/              # Sound effects and music
```

## 🎨 Key Components

### Waterfall Shader
A custom Three.js shader implementation featuring:
- Animated texture scrolling with mirroring
- Configurable speed and repetition
- Edge fading effects
- Color tinting and intensity control

```jsx
<WaterfallModel
  time={clock.getElapsedTime()}
  speed={0.15}
  repeatY={2.5}
  edgeFade={0.2}
  tintColor={[0.7, 0.6, 0.8]}
  tintIntensity={0.9}
/>
```

### Interactive Museum Elements
- **Torch Lighting**: Dynamic flame effects with particle systems
- **Exhibit Displays**: Interactive artifacts with information panels
- **Audio Zones**: Spatial audio for immersive soundscapes
- **Navigation System**: Smooth camera transitions and controls

## ⚡ Performance Notes

- Uses instanced rendering for repeated elements
- Optimized texture formats (WebP, KTX2)
- LOD (Level of Detail) system for complex models
- Frustum culling for off-screen objects
- Efficient state management with useRef instead of useState where possible

## 🎯 Browser Support

- Modern browsers with WebGL 2.0 support
- Chrome 56+, Firefox 51+, Safari 15+
- Mobile browsers with adequate GPU performance

## 📱 Mobile Optimization

- Touch-friendly navigation controls
- Adaptive quality settings based on device performance
- Optimized asset loading for mobile networks
- Battery-efficient rendering options

## 🔧 Configuration

The experience can be customized through various parameters:

```javascript
// Lighting configuration
const lightingConfig = {
  ambientIntensity: 0.3,
  torchIntensity: 2.0,
  shadowMapSize: 2048
};

// Performance settings
const performanceConfig = {
  pixelRatio: Math.min(window.devicePixelRatio, 2),
  antialias: true,
  shadows: true
};
```

## 🎵 Audio Features

- **Background Ambience**: Atmospheric museum sounds
- **Interactive SFX**: Footsteps, torch crackling, interaction sounds
- **Spatial Audio**: 3D positioned sound sources
- **Volume Controls**: User-adjustable audio settings

## 📋 Development Guidelines

1. **Asset Optimization**: Keep models under 5MB, optimize textures
2. **Performance First**: Profile regularly, maintain 60fps target
3. **Mobile Responsive**: Test on various device sizes and capabilities
4. **Accessibility**: Ensure keyboard navigation and screen reader support
5. **Progressive Loading**: Implement loading screens and asset streaming

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

Special thanks to the incredible 3D and web development community:

- **Three.js Team** - For the amazing 3D library
- **Blender Foundation** - For the outstanding 3D modeling software
- **PolyHaven** - High-quality HDRI and PBR materials
- **BlenderKit** - Extensive asset library
- **ambientCG** - Free PBR textures and materials
- **Sketchfab Artists** - For the beautiful 3D models used in this project

## 🔗 Resources

- [Three.js Documentation](https://threejs.org/docs/)
- [React Three Fiber](https://docs.pmnd.rs/react-three-fiber)
- [Blender Tutorials](https://www.blender.org/support/tutorials/)
- [WebGL Fundamentals](https://webglfundamentals.org/)

---

**Built with ❤️ using Three.js and React**
