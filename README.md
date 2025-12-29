# Arbitrage Calculator Console

A precision-built 2-way arbitrage calculator with live EUR FX rate conversion. Designed for professional sports betting operators who need to calculate optimal stakes, exposure, and guaranteed returns across multiple currencies.

## Features

- **2-Way Arbitrage Calculator**: Calculate optimal stakes for two-outcome arbitrage opportunities
- **Live FX Rates**: Fetch real-time EUR exchange rates from Frankfurter API
- **Multiple Currencies**: Support for EUR, GBP, RON, and AUD
- **Three Calculation Modes**:
  - "I know Stake A" - Enter Stake A, solve for Stake B
  - "I know Stake B" - Enter Stake B, solve for Stake A
  - "Target EUR Payout" - Enter desired EUR return, solve for both stakes
- **Local Storage**: Cache FX rates for 24 hours to minimize API calls
- **Manual Override**: Enter manual FX rates if API is blocked
- **Arbitrage Detection**: Automatic surebet identification with ROI calculation

## Design Philosophy

This interface follows the **"Precision Terminal"** aesthetic - a distinctive, asymmetric design with intentional hierarchy. The design moves away from generic dark mode toward a financial instrument feel, featuring:

- **Cyan & Green Accent Palette**: High-contrast colors for critical information
- **Micro-Interactions**: Subtle hover states, focus animations, and result reveals
- **Semantic HTML**: Proper ARIA roles and landmarks for accessibility
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Performance**: CSS containment and optimized animations for smooth rendering

## Accessibility

- **WCAG AAA Compliant**: High contrast ratios, proper focus indicators
- **Screen Reader Support**: ARIA live regions for dynamic content
- **Keyboard Navigation**: Full keyboard accessibility with visible focus states
- **Reduced Motion**: Respects user's motion preferences
- **Color Blind Friendly**: Icon indicators supplement color-coded status

## Usage

### Quick Start

1. Open `index.html` in a modern web browser
2. Click "Fetch Rates (EUR base)" to get current FX rates
3. Select a calculation mode
4. Enter odds and stakes for both bookmakers
5. Click "Calculate" to see your stake plan

### Calculation Modes

#### Mode 1: I know Stake A
- Enter the odds and currency for both bookmakers
- Enter your known Stake A
- Calculator solves for Stake B to equalize outcomes

#### Mode 2: I know Stake B
- Enter the odds and currency for both bookmakers
- Enter your known Stake B
- Calculator solves for Stake A to equalize outcomes

#### Mode 3: Target EUR Payout
- Enter the odds and currency for both bookmakers
- Enter your desired guaranteed EUR return
- Calculator solves for both stakes

### Understanding Results

- **Stake A/B**: Amount to wager on each outcome
- **If A/B wins → EUR**: Payout in EUR if that outcome occurs
- **Exposure (EUR)**: Total amount wagered in EUR
- **Guaranteed Return (EUR)**: Minimum payout regardless of outcome
- **Profit (EUR)**: Guaranteed profit (return - exposure)
- **ROI %**: Return on investment percentage
- **Arbitrage Check**: Shows if opportunity is a surebet (inverse sum < 1)

## Technical Details

### Browser Support
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+

### Dependencies
- None (vanilla HTML/CSS/JavaScript)
- External API: Frankfurter (for FX rates)

### Storage
- LocalStorage for FX rate caching (24-hour expiry)

## License

MIT License - See LICENSE file for details

## Credits

Built with precision by [Amplify Creative Lab](https://github.com/amplifycreativelab)
