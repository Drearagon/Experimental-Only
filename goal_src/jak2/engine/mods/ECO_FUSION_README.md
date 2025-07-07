# Eco Fusion Mod

## Overview
The Eco Fusion mod adds a strategic eco combination system to Jak and Daxter. Players can now collect different types of eco and combine them to create powerful temporary abilities.

## How It Works

### Eco Collection
- Collect eco as normal throughout the game
- The mod tracks how much of each eco type you've collected
- Maximum of 3 charges per eco type

### Fusion Combinations

#### Basic Fusions (2 eco types required):
1. **Yellow + Red = Super Jump**
   - Duration: 10 seconds
   - Effect: 2.5x jump power
   - Cooldown: 5 seconds

2. **Red + Blue = Fire Trail**
   - Duration: 15 seconds
   - Effect: Jak turns red (visual indicator)
   - Cooldown: 5 seconds

3. **Blue + Yellow = Time Slow**
   - Duration: 7.5 seconds
   - Effect: 1.5x movement speed
   - Cooldown: 5 seconds

4. **Green + Blue = Mega Heal**
   - Duration: 5 seconds
   - Effect: Restores health and eco to 100, Jak turns green
   - Cooldown: 10 seconds

#### Advanced Fusion (3 eco types required):
5. **Yellow + Red + Blue = Triple Power**
   - Duration: 20 seconds
   - Effect: All three basic effects active simultaneously
   - Cooldown: 15 seconds

## Gameplay Features

### Strategic Elements
- Choose which eco combinations to use
- Manage cooldown timers
- Plan eco collection routes
- Time your fusions for maximum effectiveness

### Visual Feedback
- Console messages show eco collection progress
- Fusion activation messages
- Jak changes color during active effects
- Debug mode shows current eco charges

### Balance Features
- Cooldown system prevents spam
- Effects automatically expire
- Charges reset on death/spawn
- Fusion system can be disabled

## Technical Details

### Files Modified
- `mod-custom-code.gc` - Complete implementation

### Key Functions
- `check-eco-combinations()` - Detects valid combinations
- `apply-fusion-effects()` - Applies active effects
- `update-fusion-timers()` - Manages cooldowns and durations
- `reset-eco-charges()` - Clears all eco charges

### Variables
- `*eco-fusion-enabled*` - Master toggle
- `*yellow-eco-charge*`, `*red-eco-charge*`, etc. - Current charges
- `*fusion-cooldown*` - Cooldown timer
- `*fusion-effect-duration*` - Effect duration timer

## Installation
1. The mod is already implemented in `mod-custom-code.gc`
2. Compile and run the game
3. The Eco Fusion system will be active by default

## Customization
You can easily modify:
- Fusion requirements (change the numbers in `check-eco-combinations()`)
- Effect durations (modify the duration values)
- Cooldown times (adjust cooldown values)
- Effect strengths (modify multipliers in `apply-fusion-effects()`)

## Tips for Players
1. Plan your eco collection route
2. Save powerful combinations for difficult sections
3. Use Mega Heal when health is low
4. Triple Power is best for boss fights
5. Watch the console for status updates

Enjoy the enhanced eco system! 