# enshittification-calculator
A tool that helps creators understand when platform reach throttling destroys their economics and forces them into paid promotion models.

# Platform Enshittification Calculator

A tool that helps creators understand when platform reach throttling destroys their economics and forces them into paid promotion models.

🔗 **[Live Demo](https://TalelGabok.github.io/enshittification-calculator/index.html)** 

## What is this?

When platforms like LinkedIn, Instagram, or Facebook throttle organic reach and push creators toward paid "boost" features, it fundamentally changes creator economics. This calculator helps you:

- **Understand if your content is still economically viable** after reach drops
- **Calculate the break-even price** for paid promotion features
- **Simulate platform-wide effects** of aggressive monetization strategies
- **Make data-driven decisions** about whether to keep posting, pay for boosts, or leave the platform

## Features

### 🎯 Simple Mode
Quick personal analysis for individual creators:
- Calculate your critical viability threshold
- Determine if boost pricing is rational or just a "behavioral tax"
- See revenue per post before/after throttling
- Get clear recommendations on what to do

### 🔬 Complex Mode
Platform-wide simulation for understanding systemic effects:
- Simulate creator churn over 24+ months
- Model behavioral economics (loss aversion, social proof)
- Track platform revenue from boosts vs. ads
- Understand long-term sustainability vs. short-term extraction

### 💡 Educational Tooltips
Hover or click the info icons (ℹ️) next to each parameter to understand:
- What the metric means
- How to calculate it for your situation
- Why it matters to the model

## The Math Behind It

This calculator is based on a rigorous mathematical model that includes:

- **Prospect Theory**: Loss aversion (losses hurt ~2.5x more than equivalent gains)
- **Reference Point Dynamics**: Creators anchor to their historical reach
- **Economic Viability Thresholds**: The θ^crit below which posting becomes unprofitable
- **Creator Population Dynamics**: Churn, onboarding, and network effects
- **Two-Sided Market Effects**: How creator supply affects user engagement and ad revenue

### Key Formulas

**Critical Viability Threshold:**
```
θ^crit = (time cost per post) / (value per impression × baseline reach)
```

**Break-Even Boost Price:**
```
P* = (value per impression) × (boost reach multiplier) × (baseline reach)
```

If current reach < θ^crit, you're losing money on every post.  
If boost price > P*, the boost is irrational (but you might buy it anyway due to loss aversion).

## How to Use

### For Individual Creators (Simple Mode):

1. **Find your reach numbers** from platform analytics:
   - Average views before throttling started
   - Average views now

2. **Calculate your costs:**
   - Time spent per post × your hourly rate = time cost per post
   - Average customer value ÷ impressions needed to get a customer = value per impression

3. **Check the platform's boost pricing:**
   - What does one boost cost?
   - How much additional reach does it provide?

4. **Input the numbers** and see:
   - Are you still economically viable?
   - Is the boost worth it or is it a "behavioral tax"?
   - What should you do?

### For Platform Analysis (Complex Mode):

Use the complex mode to understand what happens to an entire platform when reach is throttled:

- **Moderate throttling** (60-70% of original reach): Platform usually stays healthy
- **Aggressive throttling** (30-40% of original reach): Mixed results, some creator churn
- **Severe throttling** (10-20% of original reach): Death spiral likely—short-term revenue spike, long-term collapse

Adjust parameters like loss aversion, churn sensitivity, and onboarding rates to model different creator behaviors.

## Why This Matters

### The Enshittification Pattern:

1. **Phase 1**: Platform is generous to attract creators (high organic reach)
2. **Phase 2**: Platform is good to creators, making money from ads and users
3. **Phase 3**: Platform throttles reach and charges creators for distribution
4. **Phase 4**: Creators leave, content quality drops, users leave, platform dies

This calculator shows you **where you are in this cycle** and helps you make informed decisions.

### Real-World Examples:

- **LinkedIn 2024**: Many creators reported 60-90% drops in organic reach, with aggressive boost prompts
- **Facebook 2018-2020**: Business pages saw massive reach declines, forced into ads
- **Instagram 2023**: Algorithm changes reduced reach for many accounts

## Technical Details

- **Built with**: React 18, Tailwind CSS
- **Runs entirely in browser**: No server, no data collection, no tracking
- **Single HTML file**: ~500 lines, self-contained
- **Mobile responsive**: Works on all devices
- **Hosted on**: GitHub Pages (free static hosting)

## Installation & Deployment

### Option 1: Use the Live Version
Just visit the [live demo](https://yourusername.github.io/enshittification-calculator) *(update with your URL)*

### Option 2: Run Locally
1. Download `index.html`
2. Open it in any modern web browser
3. That's it! No build process, no dependencies

### Option 3: Deploy Your Own
1. Fork this repository
2. Enable GitHub Pages in Settings → Pages
3. Your site will be live at `https://yourusername.github.io/enshittification-calculator`

See detailed deployment instructions in the [deployment guide](#deployment-guide) below.

## Deployment Guide

### GitHub Pages (Recommended - Free)

1. **Create a GitHub account** (free)
2. **Create a new repository**:
   - Name: `enshittification-calculator`
   - Visibility: Public
3. **Upload the file**:
   - Must be named exactly `index.html`
   - Commit to the main branch
4. **Enable GitHub Pages**:
   - Go to Settings → Pages
   - Source: Deploy from branch
   - Branch: main, folder: / (root)
   - Click Save
5. **Wait 2-3 minutes**, then visit: `https://yourusername.github.io/enshittification-calculator`

### Other Hosting Options

This is a single HTML file, so you can host it anywhere:
- **Netlify**: Drag and drop `index.html`
- **Vercel**: Upload via their dashboard
- **Cloudflare Pages**: Deploy in one click
- **Any web server**: Just upload `index.html`

## Customization

Want to modify the calculator? The code is well-commented and organized:

- **Lines 1-100**: HTML structure and dependencies
- **Lines 100-200**: React component setup and state management
- **Lines 200-300**: Calculation functions (simple and complex modes)
- **Lines 300-500**: UI rendering

Key parameters you might want to adjust:
- Default input values
- Behavioral coefficients (loss aversion, churn sensitivity)
- Simulation parameters (engagement curves, revenue models)

## Contributing

Contributions welcome! This is an open-source educational tool. To contribute:

1. Fork the repository
2. Make your changes
3. Submit a pull request with a description of what you changed and why

Particularly interested in:
- **Additional platform presets** (LinkedIn, Instagram, Facebook default values)
- **More sophisticated models** (heterogeneous creator types, competitive dynamics)
- **Data visualizations** (charts showing simulation results over time)
- **Export features** (download results as PDF/CSV)

## Academic & Research Use

This model is based on academic research in:
- Behavioral economics (Kahneman & Tversky's Prospect Theory)
- Platform economics (two-sided markets, network effects)
- Creator economy dynamics

If you use this calculator in academic work, please cite it as:
```
Platform Enshittification Calculator (2024)
GitHub: https://github.com/TalelGabok/enshittification-calculator
```

## License

MIT License - feel free to use, modify, and distribute this tool.

## Support

- **Issues**: Open an issue on GitHub
- **Questions**: Start a discussion in the GitHub Discussions tab
- **Updates**: Watch this repository for new features

## Disclaimer

This calculator is for educational purposes. It models economic relationships based on stated assumptions. Actual platform behavior may vary. Always do your own analysis before making business decisions.

The term "enshittification" was coined by Cory Doctorow to describe the pattern of platforms declining in quality as they prioritize revenue extraction over user experience.

---

**Made with love by Chris Wessling**

https://www.linkedin.com/in/chris-wessling-3019b07/

*Helping creators understand platform economics one calculation at a time.*
