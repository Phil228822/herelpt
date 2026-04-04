# Workflows

## Start Dev Server
```bash
cd /Users/moph/Desktop/herelpt
nohup python3 -m http.server 8765 > /dev/null 2>&1 &
# Visit http://localhost:8765
```

## Kill Dev Server
```bash
lsof -ti :8765 | xargs kill -9
```

## Deploy to Netlify (not yet done)
1. Push to GitHub
2. Connect repo to Netlify
3. Point herelpt.com domain to Netlify

## Add New Images
1. Place image in /images/ directory
2. Reference in HTML as `images/filename.webp`
3. Use `object-fit: cover` for framed images
4. Use `object-fit: contain` if full image must be visible
5. Verify the image is actually what you think it is (Squarespace CDN is unreliable)

## Trim Video (requires moviepy)
```bash
pip3 install moviepy
python3 -c "
from moviepy import VideoFileClip
clip = VideoFileClip('input.mp4')
cropped = clip.cropped(y1=START, y2=END)
cropped.write_videofile('output.mp4', codec='libx264', audio=False)
"
```

## Update Footer on All Pages
Footer HTML is duplicated across all 7 pages. When changing footer, use sed or a loop:
```bash
for f in index.html about.html why-us.html team.html patient-info.html optimize.html contact.html; do
  # sed command here
done
```
