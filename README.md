# AFKL Flight Search URL Builder

A clean, browser-based tool for building deep-link search URLs for KLM and Air France metasearch engines. Perfect for travel agents, frequent flyers, and anyone who needs to quickly generate direct links to specific flight searches.

## What It Does

This tool generates the complex URLs that take you directly to KLM or Air France search results for specific flights, bypassing the usual search forms. Instead of manually entering dates and routes on the airline websites, you can build a URL that opens directly to your exact itinerary.

**Example:** Instead of going to klm.com → search form → enter "AMS to CDG on Oct 17" → wait for results, you get a direct link that opens straight to those search results.

## Features

- **Manual segment builder** — Add flights one by one with intuitive forms
- **Paste itinerary** — Bulk import from a simple text format
- **Smart defaults** — Auto-fills connecting airports and dates as you build
- **Flight number formatting** — Automatically pads short codes (AF1 → AF0001)
- **Validation** — Highlights missing required fields
- **Multiple domains** — Supports .fr, .de, .nl, .ie, .co.uk, .us, .co.in for both airlines
- **Mobile responsive** — Works on phones, tablets, and desktops
- **No tracking** — Pure client-side tool, no data sent anywhere

## How to Use

### Method 1: Manual Entry
1. Choose your airline (Air France or KLM) and website domain
2. Select cabin class and passenger count  
3. Add flight segments using the form fields
4. Click "Copy URL" or "Open in Browser"

### Method 2: Paste Itinerary
1. Click "▸ Paste itinerary" to expand the import section
2. Paste your flights in this format:
   ```
   AMS CDG 2026-10-17 14:25 AF1341
   CDG JFK 2026-10-17 16:50 AF0007
   ---
   JFK CDG 2026-10-31 18:30 AF0006
   CDG AMS 2026-11-01 10:00 AF1342
   ```
3. Use `---` on its own line to separate outbound from return flights
4. Click "Load Itinerary"

## URL Format

The tool generates URLs in the Air France/KLM metasearch format:
```
https://www.klm.nl/search/landing/metasearch?tp=1000&connections=AMS:A:20261017@1425:AF1341:X:ZZZ:BUSINESS%3ECDG:A&pax=1:0:0:0&cabinClass=BUSINESS
```

Key features:
- Handles complex multi-city trips with stopovers
- Supports open-jaw routing (different departure/arrival cities)
- Encodes trip breaks properly for extended stays
- Automatically formats flight numbers to 4-digit codes

## Technical Details

- **Pure HTML/CSS/JavaScript** — No build process, frameworks, or dependencies
- **Client-side only** — All processing happens in your browser
- **Responsive design** — Mobile-first grid layout with progressive enhancement
- **Keyboard shortcuts** — Enter key navigation between fields
- **Accessibility** — Proper labels, focus management, and screen reader support

## Why This Exists

Airlines' deep-search URLs are complex and undocumented. Building them manually is error-prone and time-consuming. This tool makes it easy for:

- **Travel professionals** who need to quickly generate search links for clients
- **Frequent travelers** planning complex multi-city trips  
- **Travel hackers** researching routing options and availability
- **Anyone** who wants to bookmark or share specific flight searches

## Getting Started

1. **Download** the `afkl-url-builder.html` file
2. **Open** it in any modern web browser
3. **Start building** your flight search URLs

No installation, no server, no dependencies — just open and use.

## License

MIT License — Use it, modify it, share it freely. See LICENSE file for details.

## Contributing

Found a bug or have a feature request? This tool is open source and welcomes contributions. The codebase is intentionally simple — pure HTML/CSS/JS with no build process.

## Disclaimer

This tool is for informational purposes only. Always verify fares and availability on the airline's official website. Flight search URLs may change without notice as airlines update their systems.