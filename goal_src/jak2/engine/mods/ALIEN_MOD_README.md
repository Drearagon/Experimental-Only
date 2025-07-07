# Alien Mod

## Overview
The Alien mod adds a mysterious alien entity that follows Jak around the game world. The alien spawns automatically and maintains a safe distance while following Jak's movements.

## Features

### **Alien Behavior**
- **Automatic Spawning**: Alien spawns 10 seconds after Jak spawns
- **Following AI**: Alien follows Jak at a distance of 5 units
- **Smart Movement**: Alien moves toward Jak but maintains safe distance
- **Visual Feedback**: Alien appears as a collectable object with increased scale

### **Mod Controls**
- **Automatic**: Alien spawns and follows automatically
- **Debug Functions**: Available in REPL for testing

## How It Works

### **Spawn System**
- Alien spawns 10 seconds after Jak spawns (600 frames at 60fps)
- Only one alien can exist at a time
- Alien is removed when Jak dies or enters a new level

### **Movement AI**
- Alien calculates direction to Jak every frame
- Moves toward Jak at 0.1 speed units per frame
- Maintains minimum distance of 5 units from Jak
- If alien gets too far (>10 units), it teleports closer

### **Integration**
- Fully integrated with existing mod system
- Works alongside Eco Fusion mod
- Uses existing game objects and functions
- No custom assets required

## Debug Functions

### **Available in REPL:**
```lisp
;; Manually spawn alien
(debug-spawn-alien)

;; Remove alien
(debug-remove-alien)

;; Toggle alien mod on/off
(debug-toggle-alien-mod)
```

## Configuration

### **Mod Variables (in mod-custom-code.gc):**
```lisp
(define *alien-mod-enabled* #t)           ;; Enable/disable mod
(define *alien-spawn-cooldown* 600)       ;; Spawn delay (10 seconds)
(define *alien-follow-distance* 5.0)      ;; Distance from Jak
(define *alien-move-speed* 0.1)           ;; Movement speed
```

## Installation

The alien mod is now fully integrated into `mod-custom-code.gc` and will automatically load when you run `(mi)` in the REPL.

## Troubleshooting

### **Alien not spawning:**
1. Check if `*alien-mod-enabled*` is set to `#t`
2. Wait 10 seconds after Jak spawns
3. Use `(debug-spawn-alien)` to force spawn

### **Alien not following:**
1. Make sure Jak (`*target*`) exists
2. Check if alien entity was created successfully
3. Use `(debug-remove-alien)` then `(debug-spawn-alien)` to reset

### **Performance issues:**
1. Alien updates every frame - this is normal
2. If lag occurs, increase `*alien-spawn-cooldown*`
3. Disable mod with `(debug-toggle-alien-mod)` if needed 