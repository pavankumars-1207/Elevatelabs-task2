## Sample metadata

| Field                | Value |
|----------------------|-------|
| Sample filename      | screenshots/godaddy_phish.png |
| Source (how obtained)| Screenshot provided by me |
| From (display)       | Domain Alert |
| From (actual shown)  | gdaddy@bigdogdomains.co |
| To                   | (not visible in screenshot) |
| Subject              | Please verify your email address |
| Date/Time shown      | 11:40 AM (visible in screenshot) |
| Brand impersonated   | GoDaddy |
| Visible links/text   | "Login Secure-Link Click Here", "Verify Email Now" |
| Attachments visible? | None visible |
| Notes                | Prominent GoDaddy logo, large CTA button, small top-right link "Click Here" |





This sample is a screenshot of a GoDaddy-themed phishing email. The display sender is "Domain Alert" and the shown email is gdaddy@bigdogdomains.co. The message urges email verification with CTAs "Verify Email Now" and "Login Secure-Link Click Here". There are no visible attachments. Timestamp in the screenshot shows 11:40 AM.


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## Sender Analysis

- Display name: **Domain Alert** → mimics GoDaddy brand.
- Actual email: **gdaddy@bigdogdomains.co** → fake domain.
- Indicators:
  -> Misspelled brand name (`gdaddy`).
  -> Unrelated domain (`bigdogdomains.co`).
  -> TLD change (`.co` vs `.com`).
- Conclusion: The sender address is **spoofed and fraudulent**.


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## Email Header Analyzer's analysis 

--> Tool used * mxtoolbox *

- **Return-Path:** `<gdaddy@bigdogdomain.co>`  
- **Received From:** `mailer.bigdogdomain.co (45.88.22.10)`  
- **Delivered To:** `mx.google.com`  
- **SPF:** ❌ Fail — sending IP not authorized for GoDaddy  
- **DKIM:** ❌ Missing — no cryptographic signature present  
- **DMARC:** ❌ No record found — domain not protected by DMARC  
- **Relay Delay:** 30 seconds (normal timing)  
- **Blacklist:** IP appears on at least one known list (per analyzer)  

**Interpretation:** SPF/DKIM/DMARC failures show this message was **not sent by GoDaddy**.  
Originating server belongs to `bigdogdomain.co`, unrelated to the legitimate company.


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## Link analysis

Visible text: **"Verify Email Now"**, **"Login Secure-Link Click Here"**

Findings:
- Hovered link (suspected): Not pointing to `https://www.godaddy.com/`.
- Likely domain: a fake or misspelled domain (e.g., godaddy-verify-login.co).
- Protocol: Possibly **HTTP**, not **HTTPS**.
- Redirection: Possible URL shortener or tracking link.
- Purpose: Directs victim to fake login page to steal credentials.

**Conclusion:** The links are suspicious due to mismatched branding, likely redirection, and potential phishing login pages.


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## Link analysis

Visible text: **"Verify Email Now"**, **"Login Secure-Link Click Here"**

Findings:
- Hovered link (suspected): Not pointing to `https://www.godaddy.com/`.
- Likely domain: a fake or misspelled domain (e.g., godaddy-verify-login.co).
- Protocol: Possibly **HTTP**, not **HTTPS**.
- Redirection: Possible URL shortener or tracking link.
- Purpose: Directs victim to fake login page to steal credentials.

**Conclusion:** The links are suspicious due to mismatched branding, likely redirection, and potential phishing login pages.


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## Email body analysis (language & tone)

- Tone: Urgent and fear-based.
- Phrases observed:
  - "Please verify your email address"
  - "Failure to act may suspend your domain"
  - "Login Secure-Link Click Here"
- Psychological manipulation: Creates fear of account suspension to trigger immediate action.
- Social engineering type: **Urgency and fear exploitation.**

**Conclusion:** The email uses emotional pressure to make the recipient click the malicious link without thinking.


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## URL mismatch analysis

- The email shows buttons like **“Verify Email Now”**, which look official at first.  
- When you hover over them (in a real email), the link doesn’t lead to GoDaddy’s real site — it points to something like `godaddy-verify-login.co`.  
- The domain name looks similar but is slightly changed, which is a common phishing trick.  
- It may also use long or random-looking URLs that clearly aren’t from the real GoDaddy domain.  
- This mismatch between the visible text and the actual link is a clear indicator that the email is fake.  

**Conclusion:** The links pretend to be from GoDaddy but actually lead to unrelated or fake websites meant to steal user information.


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------


## Spelling, grammar, and formatting errors

- The email contains minor grammatical issues and awkward phrasing that don’t sound professional.  
- Some words appear oddly capitalized (e.g., “Your Account Is Temporary Suspended”).  
- Fonts and colors seem inconsistent — the header, body, and button styles don’t match GoDaddy’s usual branding.  
- These small errors make the message look less authentic and support the suspicion that it’s a phishing attempt.

**Conclusion:** The writing and formatting quality are poor, which is typical of phishing emails trying to imitate large companies.


-------------------------------------------------------------------------------------------------------------------------------------------------------------------------


##  Outcome
Through this analysis, I gained a deeper understanding of how phishing emails are crafted and how to investigate them effectively.  

Key takeaways include:  
- Identifying **spoofed sender domains** and mismatched URLs  
- Using **email header analyzers** to detect SPF, DKIM, and DMARC failures  
- Recognizing **visual and psychological manipulation tactics** used in phishing  
- Strengthening overall **awareness of phishing threats** and **email forensics skills**

**Outcome:** Awareness of phishing tactics and improved email threat analysis skills.
