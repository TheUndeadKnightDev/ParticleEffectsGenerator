# Particles - Particle Effects Generator

Create stunning particle effects with an interactive, real-time canvas. Perfect for games, websites, or just for fun.

## Features

✨ **6 Presets** — Explosion, fireworks, rain, snow, confetti, smoke  
🎨 **Full Customization** — Adjust count, speed, size, color, lifetime  
🖱️ **Click to Create** — Click anywhere on canvas to generate effects  
⚙️ **Gravity Toggle** — Add or remove gravity simulation  
📥 **Download** — Save particle frames as PNG  
⚡ **Real-time** — 60 FPS particle simulation  
🎯 **Clean UI** — Dark theme, responsive controls  

## Installation

```bash
git clone https://github.com/TheUndeadKnightDev/particle-effects.git
cd particle-effects
# Open index.html in browser
```

Or deploy to GitHub Pages.

## How to Use

### Create Particles

1. **Click on canvas** — Creates particle effect at click location
2. **Choose preset** — Select from Explosion, Fireworks, Rain, etc.
3. **Customize** — Adjust settings on the right panel
4. **Watch** — Real-time animation updates

### Presets Included

- **Explosion** — Fast burst outward, orange, high gravity
- **Fireworks** — Yellow burst, disappears quickly
- **Rain** — Blue particles falling down
- **Snow** — White particles drifting gently
- **Confetti** — Colorful particles scattered
- **Smoke** — Gray particles rising gently

### Customize Settings

- **Particle Count** — 10-500 particles per click (default: 50)
- **Speed** — 0.5-10 (how fast particles move)
- **Size** — 1-20 (pixel size)
- **Color** — Pick any color with color picker
- **Lifetime** — 0.5-5 seconds (how long particles live)
- **Gravity** — Toggle gravity simulation on/off

### Download

Click **Download** to save the current canvas as PNG image.

---

## How It Works

### Particle System

Each particle has:
- Position (x, y)
- Velocity (vx, vy)
- Lifetime counter
- Size and color
- Optional gravity

### Animation Loop

1. Update particle positions
2. Apply velocity
3. Apply gravity (if enabled)
4. Fade out as lifetime decreases
5. Remove when lifetime reaches 0
6. Redraw all particles

### Physics

- **Velocity** — Particles move in direction set at creation
- **Gravity** — Optional downward acceleration (0.2 per frame)
- **Decay** — Opacity fades based on lifetime
- **Spread** — Initial velocity angles vary by preset

---

## Project Structure

```
particle-effects/
├── index.html        # Single-file application (~500 lines)
└── README.md         # This file
```

---

## Tips & Tricks

💡 **Rapid Clicking** — Click multiple times quickly for layered effects  
💡 **Drag to Draw** — Click and drag for particle trails  
💡 **Low Count** — Use 10-20 for subtle effects  
💡 **High Count** — Use 300+ for dramatic effects  
💡 **Long Lifetime** — 4-5 seconds for lingering effects  
💡 **No Gravity** — Better for floating particles  
💡 **Gravity On** — Better for falling effects  

---

## Customization Ideas

### Add New Presets

Edit the `presets` object in JavaScript:

```javascript
meteor: {
    count: 40,
    speed: 8,
    size: 3,
    color: '#ff3300',
    lifetime: 2.5,
    gravity: true,
    spread: Math.PI * 0.3
}
```

Then add button:
```html
<button class="preset-btn" onclick="loadPreset('meteor')">Meteor</button>
```

### Adjust Physics

Change gravity value (default 0.2):
```javascript
if (settings.gravity) {
    this.vy += 0.2;  // Change this value
}
```

### Change Colors

Use gradient or patterns instead of solid colors:
```javascript
ctx.fillStyle = this.color;  // Already supports gradients
```

---

## Browser Support

Works in all modern browsers:
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

---

## Use Cases

🎮 **Games** — Background effects, explosions, power-ups  
🌐 **Websites** — Loading animations, hover effects  
📺 **Videos** — Overlay effects, transitions  
✨ **Art** — Generative art, visual experiments  
🎬 **Presentations** — Eye-catching animations  

---

## Technologies Used

- **HTML5 Canvas** — Particle rendering
- **Vanilla JavaScript** — Physics simulation
- **CSS3** — Responsive UI

---

## Performance

- Optimized for 500+ particles
- 60 FPS target
- Efficient particle pool
- Auto-cleanup of dead particles

---

## Future Ideas

- [ ] Multiple colors per effect
- [ ] Trail effects
- [ ] Particle collision
- [ ] Export as GIF/WebM
- [ ] Preset library sharing
- [ ] Brush modes (draw mode)
- [ ] Vector field simulation
- [ ] Particle groups/emitters

---

## License

MIT

---

Made with ✨ by **TheUndeadKnightDev**
