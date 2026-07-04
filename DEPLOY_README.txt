INDIAOLYMPIAD.COM — DEPLOYMENT PACKAGE (Wave 1) · HOSTINGER EDITION
====================================================================
Contents: 9 HTML pages + styles.css + sitemap.xml + robots.txt + CNAME

PART A — PUT THE SITE LIVE (GitHub Pages, ~20 min)
---------------------------------------------------
1. github.com -> create free account (5 min)
2. New repository -> name: indiaolympiad -> Public -> Create (2 min)
3. "uploading an existing file" -> drag ALL files from this zip -> Commit (5 min)
4. Settings -> Pages -> Source: Deploy from branch -> main -> /(root) -> Save
5. Wait ~2 min. Site live at https://YOUR-USERNAME.github.io/indiaolympiad/
6. Settings -> Pages -> Custom domain -> www.indiaolympiad.com -> Save
   (tick "Enforce HTTPS" when it becomes available, ~15 min later)

PART B — HOSTINGER DNS FOR THE SITE (~15 min)
---------------------------------------------------
hpanel.hostinger.com -> Domains -> indiaolympiad.com -> DNS / Name Servers
-> DNS records:
1. DELETE any existing A record for "@" (usually points to Hostinger parking)
2. ADD these 4 A records (Name: @ , TTL default):
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
3. ADD CNAME record: Name: www -> Target: YOUR-USERNAME.github.io
4. Save. Propagation: minutes to a few hours.

PART C — EMAIL FORWARDING ON HOSTINGER (~10 min, free)
---------------------------------------------------
hpanel.hostinger.com -> Emails -> indiaolympiad.com
-> choose "Email forwarding" (free) -> Create forwarder:
   contact@indiaolympiad.com   -> support@unlockiqinstitute.com
   grievance@indiaolympiad.com -> support@unlockiqinstitute.com
Send yourself a test mail to both aliases and confirm arrival.
NOTE: Forwarding is receive-only. Replies go out from
support@unlockiqinstitute.com — that is fine (disclosed publisher).
In Gmail, add filter: to:grievance@indiaolympiad.com -> label "DPDP-Grievance"
(protects the 72-hour acknowledgement clock).
If "Email forwarding" is not visible on your plan, fallback:
Cloudflare Email Routing (free) — ask Claude for the click-path.

PART D — GOOGLE SEARCH CONSOLE (~15 min)
---------------------------------------------------
search.google.com/search-console -> Add property: indiaolympiad.com
-> verify via DNS TXT record (add in same Hostinger DNS panel)
-> Sitemaps -> submit: https://www.indiaolympiad.com/sitemap.xml

PART E — REDIRECT THE SUPPORTING DOMAINS (~10 min, do after site is live)
---------------------------------------------------
hpanel.hostinger.com -> Domains -> mathsolympiadindia.com -> Redirects
-> 301 (permanent) -> https://www.indiaolympiad.com
Repeat for: mathsolympiadindia.in
Optional now / later: famousolympiad.com, topolympiad.com -> same 301.
LEAVE singaporeolympiad.com parked (separate future decision).

BEFORE GOING LIVE — TWO DECISIONS FOR DIP:
A. Grievance officer name on contact.html (currently "[Name to be appointed]")
B. Confirm forwarding test mails arrived at support@unlockiqinstitute.com
