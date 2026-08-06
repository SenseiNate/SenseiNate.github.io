# senseinate.github.io

Personal portfolio site. Single file, no framework, no build step.

Live at https://senseinate.github.io

## What this is

A visual companion to my resume. I'm an engineering project manager and systems engineer with ten years across systems engineering, program management, and product ownership. This page exists so a hiring manager can get the picture in about thirty seconds instead of parsing a PDF. It also doubles as the place I keep the three AI tools I built for my own use.

## Stack

Deliberately boring. One index.html holding all the markup, CSS, and JavaScript. No framework, no bundler, no dependencies, no build step. Type is Sora for display, Inter Tight for body, and JetBrains Mono for labels and data, all from Google Fonts. Deployed through GitHub Pages off the master branch. Push and it's live.

## Design

The visual language is liquid glass over a dark field, and every panel shares one material. A translucent fill with backdrop blur and saturation, an inner lens ring that brightens what passes behind the edge so the glass reads as having thickness rather than being a flat frosted sheet, and a rim that splits light from white into cyan into violet the way a real glass edge does.

Cyan is the primary accent. Amber does exactly one job, marking credentials a third party verified. Clearance and the Part 107 certification get amber. Degrees do not.

## Performance

Backdrop blur is expensive, and one rule governs the whole page: anything repainting behind a blurred surface forces it to re-blur. Learning that cost me most of a rebuild.

Three things got cut for it. The background orbs used to drift, and continuous motion behind twenty glass panels meant nonstop full-page re-blur, so they're static now. A cursor-tracking light had the same problem on every mouse move, and was replaced by a trailing bead that moves on transform alone, which costs nothing. Small pulsing status dots inside the demo panels were forcing those panels to re-blur twice a second.

The page went from 5fps to roughly 60 after those three changes, with no visible loss.

## Accessibility

Reduced motion preferences disable every animation and collapse the horizontal product track into a vertical stack. No horizontal overflow at 390px. Keyboard focus rings on everything interactive.

## Structure

Ordered for scan-first reading, cheapest-to-read proof first and highest-effort reading last.

Hero, with name, one-line positioning, and a quick-facts card. Then four figures at scale. Then three shipped tools in a horizontal scroll-linked track. Then the record across BAE Systems, GE Healthcare, Northrop Grumman, and the U.S. Air Force. Then 104 capabilities across six filterable domains. Then a short about, then credentials, then contact.

## The tools

All three live in a separate repo at https://github.com/SenseiNate/business-ventures. None are hosted. Clone and run them.

Figured is a Socratic learning tool that refuses to give the answer, built on Python, the Claude API, and Streamlit. Web Scraper Agent takes a plain-language research goal and returns a scored, sourced report, running two search passes and keeping only perfect matches. Job Matcher scores job listings against a distilled profile of real experience rather than keyword overlap.

## How this was built

I'm not a software engineer. I know basic Python. This was built with heavy AI assistance while I learn front-end properly, and the intent is to lean on that less over time rather than stay on autopilot with it.

## License

Code is free to learn from. The content, copy, and career history are mine.
