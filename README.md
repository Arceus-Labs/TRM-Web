# The Ruin Machine

### Interactive Gambling Math Simulator

<img src="https://raw.githubusercontent.com/Arceus-Labs/TRM-Web/main/Assets/TRM-Cover.png" alt="The Ruin Machine Cover" width="600"/>

[![Next.js](https://img.shields.io/badge/Next.js-14-black?style=flat-square&logo=next.js&logoColor=white)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Framer Motion](https://img.shields.io/badge/Framer_Motion-11-FF0055?style=flat-square&logo=framer&logoColor=white)](https://www.framer.com/motion/)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-success?style=flat-square)]()

A beautiful, interactive web simulator that mathematically proves why gambling strategies always lose to probability theory and house edge.

[Live Demo](https://the-ruin-machine-web.vercel.app) • [Report](https://crocus-zenobia-863.notion.site/The-Ruin-Machine-Technical-Report-2dc1ebfe2064806a9625f49a9871aaf3?pvs=73)

## About

Think you can beat the house? Think again. The Ruin Machine is an interactive web application that demonstrates through real-time simulation why every gambling strategy eventually fails. Watch your virtual bankroll disappear as mathematics proves its undefeated record.

This is the web companion to our ESP32 hardware project, bringing the same mathematical principles to your browser with beautiful animations and comprehensive statistics.

<table>
<tr>
<td width="50%">

### Key Features

- Real-time Coin Flip Simulation - 3D animated betting
- Live Bankroll Charts - Watch your decline in real-time
- Multiple Strategies - Martingale, Flat Bet, Quit on Loss
- Mass Simulation - Run 1000+ parallel simulations
- Educational Content - Learn the math behind the ruin
- Bankruptcy Animation - Particle explosion on ruin

</td>
<td width="50%">

### What You'll Learn

- Expected Value (EV) calculations
- Law of Large Numbers
- Gambler's Ruin theorem
- Why Martingale fails
- House edge compounding
- Probability convergence

</td>
</tr>
</table>

## The Math

<details>
<summary><b>Click to expand mathematical proof</b></summary>

### Expected Value

```
EV = (Win Probability × Win Amount) - (Loss Probability × Loss Amount)
EV = (0.495 × ₹100) - (0.505 × ₹100)
EV = -₹1 per bet
```

Over 1000 bets, expected loss = **₹1,000**

### Gambler's Ruin Probability

```
P(ruin) = Casino Bankroll / (Your Bankroll + Casino Bankroll)

With ₹10,000 vs ₹10 Crore casino:
P(ruin) = 99.99%
```

### Martingale Fallacy

| Consecutive Losses | Required Bet | Total Risk | Potential Profit |
|:------------------:|:------------:|:----------:|:----------------:|
| 5 | ₹3,200 | ₹6,300 | ₹100 |
| 10 | ₹102,400 | ₹204,700 | ₹100 |
| 15 | ₹3,276,800 | ₹6,553,500 | ₹100 |

Risk millions to win ₹100

</details>

## Tech Stack

| Technology | Purpose |
|:-----------|:--------|
| Next.js 14 | React framework with App Router |
| TypeScript | Type-safe development |
| Tailwind CSS | Utility-first styling |
| Framer Motion | Smooth animations |
| Recharts | Data visualization |
| Lucide React | Beautiful icons |

## Quick Start

### Clone Repository
```bash
git clone https://github.com/Arceus-Labs/TRM-Web.git
cd TRM-Web
```

### Install Dependencies
```bash
npm install
```

### Run Development Server
```bash
npm run dev
```

### Open Browser
Navigate to `http://localhost:3000`

## Usage

### Betting Strategies

| Strategy | Description | Death Speed |
|:--------:|:------------|:-----------:|
| Martingale | Double bet after each loss | Fastest |
| Flat Bet | Constant bet amount | Slow |
| Quit on Loss | Reset session after loss | Variable |

### Simulation Modes

| Mode | Description |
|:----:|:------------|
| Single Bet | Manual coin flip |
| Auto Play | 100 automated games |
| Mass Sim | 1000+ parallel simulations |

### Controls

| Setting | Range | Default |
|:--------|:-----:|:-------:|
| Starting Bankroll | ₹1,000 - ₹100,000 | ₹10,000 |
| Base Bet | ₹10 - ₹5,000 | ₹100 |
| Win Probability | 45% - 50% | 49.5% |
| Simulation Speed | Instant - Slow | Normal |

## Project Structure

```
TRM-Web/
├── app/
│   ├── page.tsx              # Main page
│   ├── layout.tsx            # Root layout
│   ├── globals.css           # Global styles
│   └── components/
│       ├── Hero.tsx          # Landing section
│       ├── Simulator.tsx     # Main game logic
│       ├── ControlPanel.tsx  # Settings & controls
│       ├── CoinFlip.tsx      # 3D animated coin
│       ├── StatsCard.tsx     # Live statistics
│       ├── BankrollChart.tsx # Real-time chart
│       ├── BankruptcyModal.tsx
│       ├── MassSimulation.tsx
│       ├── EducationalSection.tsx
│       └── Footer.tsx
├── lib/
│   ├── simulation.ts         # Core game logic
│   └── utils.ts              # Helper functions
└── public/
```

## Design

### Color Palette

| Color | Hex | Usage |
|:-----:|:---:|:------|
| Background | `#020617` | Main background |
| Danger | `#dc2626` | Losses, warnings |
| Success | `#10b981` | Wins |
| Gold | `#fbbf24` | Accents, highlights |
| Text | `#f1f5f9` | Primary text |

### Visual Effects

- Glassmorphism cards
- Smooth Framer Motion transitions
- 3D coin flip animation
- Particle explosion on bankruptcy
- Real-time animated charts

## Links

| Resource | Link |
|:--------:|:----:|
| GitHub | [Arceus-Labs/TRM-Web](https://github.com/Arceus-Labs/TRM-Web) |
| Live Demo | [Vercel](https://the-ruin-machine-web.vercel.app) |
| Hardware Version | [GitHub](https://github.com/Arceus-Labs/The-Ruin-Machine) |
| Slide Deck | [Google Drive](https://drive.google.com/file/d/19qsP3uPnF_kbo4SKc0cpCnif0oX9e3MH/view?usp=sharing) |
| Overview Video | [Google Drive](https://drive.google.com/file/d/1EbXJda__bJuiQr_99y3YCqOkgEXG2dLL/view?usp=sharing) |

## Disclaimer

This is an educational tool demonstrating probability theory. If you or someone you know has a gambling problem, please seek help:

- **National Problem Gambling Helpline**: 1-800-522-4700
- **Gamblers Anonymous**: [www.gamblersanonymous.org](https://www.gamblersanonymous.org)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Made with mathematical certainty by [Arceus Labs](https://github.com/Arceus-Labs)

Star this repo if you learned something!

*Remember: The house always wins. Math is undefeated.*
