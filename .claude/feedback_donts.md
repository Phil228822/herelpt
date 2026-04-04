# Things NOT To Do

## Icons
- DO NOT use emoji icons anywhere on the site
- DO NOT use Lucide icon boxes on cards - user called them "tacky and AI"
- DO NOT use card-icon divs - just clean typography
- Exception: contact page info card can use inline SVG icons (map pin, phone, etc.)

## Design
- DO NOT use Playfair Display font (AI cliche)
- DO NOT use DM Serif Display (was replaced with Fustat)
- DO NOT use uniform/symmetric grid layouts everywhere
- DO NOT use pure white (#fff) backgrounds for the body
- DO NOT use pure black (#000) text
- DO NOT create placeholder boxes with emoji descriptions
- DO NOT use em dashes (--) anywhere in content, use simple dashes

## Images
- DO NOT trust Squarespace CDN URLs - they serve wrong images
- DO NOT use dr-phil-2.webp as Dr. Phil (it's a cactus)
- DO NOT use location.webp as the clinic (it's a banana leaf)
- DO NOT use hero-hands.webp as hands (it's a banana leaf)
- DO NOT duplicate the same image in multiple places without checking

## Layout
- DO NOT create double footers (prefooter + footer was a mistake)
- DO NOT make images too tall (cap heights, use reasonable sizing)
- DO NOT use object-fit:contain in framed images (causes white space)

## Video
- DO NOT use Kling AI generated video (quality degradation)
- Use the original CloudFront trail video as-is

## Images - CRITICAL
- The filenames are a mess. Here is the TRUTH as of now:
  - anna.webp = farmer's market lady (THIS IS MONICA)
  - anna-new.webp = woman on hay bale by river (THIS IS ANNA)
  - monica.webp = farmer's market lady (same as anna.webp - MONICA)
  - dr-phil.webp = actual Dr. Phil headshot
  - dr-phil-2.webp = CACTUS, not Dr. Phil
- DO NOT swap filenames again. Just change the src in HTML to point to the right file.
- Monica card → uses anna.webp (farmer's market)
- Anna card → uses anna-new.webp (hay bale)
- Dr. Phil is NOT in the "Our People" team grid (he has his own bio section above)

## General
- DO NOT add features without being asked
- DO NOT over-explain changes
- When user says something is wrong, fix it immediately, don't argue
- DO NOT keep going back and forth on image swaps - verify with Read tool first
- When user is frustrated, fix the thing and shut up
