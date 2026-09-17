DENTAL-MARKETING.ORG
Static site package, 17 September 2026

WHAT THIS IS
Three static HTML pages. No framework, no build step, no dependencies.
Vercel serves these files as they are.

STRUCTURE (keep it exactly like this)

  site/
  |- index.html                            ->  /
  |- vercel.json                           ->  project root, REQUIRED
  |- robots.txt                            ->  /robots.txt
  |- sitemap.xml                           ->  /sitemap.xml
  |- favicon.png                           ->  /favicon.png
  |- og-image.jpg                          ->  /og-image.jpg
  |- case-studies/
     |- kraja-sidhu-dental.html            ->  /case-studies/kraja-sidhu-dental
     |- private-practice.html              ->  /case-studies/private-practice

vercel.json is what strips the .html from those URLs. Without it, every
internal link on the homepage returns 404. It must sit next to index.html.

DEPLOYING
Git project:  replace the files, keep the structure, commit and push.
No Git:       drag the whole "site" FOLDER into the Vercel upload box.
              Do not drag the files individually or case-studies/ is lost.

THE DOMAIN
dental-marketing.org was bought through Vercel, so there are no DNS
records to add by hand. Project > Settings > Domains > add the domain >
choose to serve the apex and redirect www to it. See the Word brief.

AFTER DEPLOYING, CHECK
  [ ] Homepage booking calendar shows a real Calendly calendar
  [ ] Both case study links open without a 404
  [ ] Both case study pages have a Book a Call button top right
  [ ] Both case study pages have a sticky bar along the bottom
  [ ] Both YouTube thumbnails play when clicked
  [ ] /sitemap.xml lists three URLs

QUESTIONS
Flag anything that does not behave as described rather than working
around it.
