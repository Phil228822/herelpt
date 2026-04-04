# Hard-Won Lessons & Gotchas

## Squarespace CDN
- Squarespace serves images as WebP regardless of URL extension
- **Many URLs return WRONG images** - the CDN sometimes serves completely different photos than what's displayed on the actual Squarespace page
- dr-phil-2.webp = cactus photo (NOT Dr. Phil)
- dr-phil.webp = actual headshot (correct)
- location.webp = banana leaf plant (NOT the clinic location)
- hero-hands.webp = banana leaf close-up (NOT hands)
- treatment.webp = stock gym photo with rope girl (NOT their clinic)
- clinic-1, clinic-3, clinic-4, pilates = actual real clinic photos

## Chrome Automation Screenshots
- Screenshots from localhost often appear blank/white after scrolling - this is a tool limitation, not a site bug
- Content renders correctly even when screenshots show blank
- Verify via JavaScript DOM inspection instead of trusting screenshots
- Fresh page navigation screenshots work; scrolled screenshots don't

## Video
- The trail video from CloudFront has no people in it - user wanted walkers added
- Kling AI was used to generate walkers but degraded video quality significantly
- Final decision: use original clean trail video without walkers
- Video parallax effect is enabled (position: fixed)

## Server
- python3 -m http.server 8765 keeps dying when run via background tasks
- Use nohup to keep it alive: nohup python3 -m http.server 8765 > /dev/null 2>&1 &
- Must run from /Users/moph/Desktop/herelpt/ directory
