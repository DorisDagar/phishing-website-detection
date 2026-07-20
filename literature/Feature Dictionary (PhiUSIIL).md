# 📖 Feature Dictionary

## 📊 Dataset Overview

| 🏷️ Property | 📌 Value |
|-------------|-----------|
| **Dataset Name** | PhiUSIIL Phishing URL Dataset (UCI) |
| **Total Samples** | **235,795** |
| **Total Columns** | **56** |
| **Input Features** | **55** |
| **Target Variable** | `label` |
| **Problem Type** | 🔍 Binary Classification |

---

# 🆔 Group 1 — Identification Features

> These features identify the webpage but **are not useful for prediction.**

| 🏷️ Feature | 📝 Description | 🎯 Importance |
|------------|---------------|---------------|
| **FILENAME** | Unique webpage identifier | ❌ Drop before training |
| **URL** | Complete webpage URL | ⚠️ Keep for analysis only |
| **Domain** | Extracted domain name | ⚠️ Used to derive other features |

---

# 🌐 Group 2 — URL Features

These features describe the structure and characteristics of the URL.

| 🔍 Feature | 💡 Meaning | 🎯 Why Useful |
|------------|-----------|---------------|
| URLLength | Number of characters in URL | Long URLs are often suspicious |
| URLSimilarityIndex | Similarity to legitimate domains | Detects look-alike domains (`g00gle.com`) |
| CharContinuationRate | Continuous character sequences | Random strings indicate phishing |
| URLCharProb | Probability that characters resemble normal URLs | Low probability → suspicious |
| HasObfuscation | Encoded/obfuscated URL present | Attackers hide malicious URLs |
| NoOfObfuscatedChar | Number of encoded characters | More encoded characters → higher risk |
| ObfuscationRatio | Percentage of encoded characters | Higher ratio often indicates phishing |

---

# 🌍 Group 3 — Domain Features

| 🔍 Feature | 💡 Meaning | 🎯 Why Useful |
|------------|-----------|---------------|
| DomainLength | Length of the domain | Extremely long domains are suspicious |
| IsDomainIP | Uses an IP instead of a domain | Common phishing technique |
| TLD | Top-Level Domain (`.com`, `.org`) | Some TLDs are abused more frequently |
| TLDLength | Length of TLD | Unusual lengths may indicate phishing |
| NoOfSubDomain | Number of subdomains | Excessive subdomains can hide fake websites |

---

# 🔤 Group 4 — Character Statistics

These features describe the composition of characters in the URL.

| 🔠 Feature | 📝 Meaning |
|------------|------------|
| NoOfLettersInURL | Number of alphabetic characters |
| LetterRatioInURL | Percentage of letters |
| NoOfDegitsInURL | Number of digits |
| DegitRatioInURL | Percentage of digits |
| NoOfEqualsInURL | Count of `=` |
| NoOfQMarkInURL | Count of `?` |
| NoOfAmpersandInURL | Count of `&` |
| NoOfOtherSpecialCharsInURL | Count of special characters |
| SpacialCharRatioInURL | Ratio of special characters |

### 🚨 Typical Phishing Characteristics

- 🔢 More digits
- ❗ More special characters
- 🔗 More query parameters

---

# 🔒 Group 5 — Security Features

| 🛡️ Feature | 📝 Meaning |
|------------|------------|
| IsHTTPS | Indicates whether the website uses HTTPS |

> ⚠️ **Important:** HTTPS **does NOT guarantee** that a website is legitimate. Many phishing websites also use valid SSL certificates.

---

# 🏗️ Group 6 — HTML Structure

| 🏷️ Feature | 📝 Meaning |
|------------|------------|
| LineOfCode | Total HTML lines |
| LargestLineLength | Length of the longest HTML line |
| HasTitle | Presence of a `<title>` tag |
| Title | Webpage title |

---

# 🎯 Group 7 — Similarity Features

| 🔍 Feature | 📝 Meaning |
|------------|------------|
| DomainTitleMatchScore | Similarity between domain and page title |
| URLTitleMatchScore | Similarity between URL and page title |

### 📌 Example

**🌐 Domain**

```text
amazon.com
```

**📄 Title**

```text
Amazon Shopping
```

✅ High similarity generally indicates a legitimate website.

---

# 📑 Group 8 — Page Metadata

| 🏷️ Feature | 📝 Meaning |
|------------|------------|
| HasFavicon | Website contains a favicon |
| Robots | `robots.txt` exists |
| IsResponsive | Mobile responsive webpage |
| HasDescription | Meta description exists |

💡 Legitimate websites generally include these elements.

---

# 🔀 Group 9 — Redirect Features

| 🔍 Feature | 📝 Meaning |
|------------|------------|
| NoOfURLRedirect | Total redirects |
| NoOfSelfRedirect | Redirects within the same domain |

---

# 📝 Group 10 — Form Features

| 🏷️ Feature | 📝 Meaning |
|------------|------------|
| HasExternalFormSubmit | Form submits to another domain |
| HasSubmitButton | Submit button exists |
| HasHiddenFields | Hidden HTML fields present |
| HasPasswordField | Password input field present |

🎯 These features help detect fake login pages.

---

# 🖼️ Group 11 — Webpage Content

| 🏷️ Feature | 📝 Meaning |
|------------|------------|
| HasCopyrightInfo | Copyright information exists |
| NoOfImage | Number of images |
| NoOfCSS | Number of CSS files |
| NoOfJS | Number of JavaScript files |

---

# 🔗 Group 12 — Hyperlinks

| 🔍 Feature | 📝 Meaning |
|------------|------------|
| NoOfSelfRef | Internal hyperlinks |
| NoOfEmptyRef | Empty hyperlinks |
| NoOfExternalRef | External hyperlinks |

---

# 💳 Group 13 — Business Indicators

| 💰 Feature | 📝 Meaning |
|------------|------------|
| Bank | Banking-related keywords |
| Pay | Payment-related keywords |
| Crypto | Cryptocurrency-related keywords |

💡 These keywords frequently appear in phishing websites targeting financial information.

---

# 🌐 Group 14 — Social Features

| 👥 Feature | 📝 Meaning |
|------------|------------|
| HasSocialNet | Links to official social media profiles |

✅ Legitimate organizations often provide official social media links.

---

# 🎯 Group 15 — Target Variable

| 🏷️ Feature | 📝 Meaning |
|------------|------------|
| **label** | Target class used for prediction |

After loading the dataset, verify the encoding:

```text
0 → ✅ Legitimate Website
1 → 🚨 Phishing Website
```

---

# 💡 Summary

| 📂 Category | 🔢 Features |
|-------------|------------|
| 🆔 Identification | 3 |
| 🌐 URL Features | 7 |
| 🌍 Domain Features | 5 |
| 🔤 Character Statistics | 9 |
| 🔒 Security | 1 |
| 🏗️ HTML Structure | 4 |
| 🎯 Similarity | 2 |
| 📑 Metadata | 4 |
| 🔀 Redirect | 2 |
| 📝 Forms | 4 |
| 🖼️ Content | 4 |
| 🔗 Hyperlinks | 3 |
| 💳 Business Indicators | 3 |
| 🌐 Social | 1 |
| 🎯 Target | 1 |