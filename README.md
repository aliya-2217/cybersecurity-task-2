# 📧 Phishing Email Analysis - Cybersecurity Internship Task 2

## 📝 Task Overview
As part of the cybersecurity internship, this task involved analyzing a suspicious phishing email and identifying the key traits that make it malicious. The objective was to gain hands-on experience with phishing indicators and email header analysis tools.


## 📬 Sample Phishing Email

**Filename:** `email.txt`  
**From:** security-alert@amaz0n-support.com  
**Subject:** Action Required: Suspicious Sign-In Attempt  

### Email Body (Excerpt):
> We detected an unusual sign-in attempt on your Amazon account from Lagos, Nigeria.  
> Please verify your identity by clicking: http://amaz0n-login.com/security-check  
> Failure to act within 24 hours may result in suspension of your account.

---

## 🕵️‍♂️ Phishing Indicators Identified

| Indicator | Description |
|----------|-------------|
| 🔗 **Spoofed Email Domain** | `amaz0n-support.com` mimics Amazon but replaces "o" with "0". |
| ⚠️ **Urgency/Threats** | Claims suspicious activity and threatens suspension within 24 hours. |
| 🧠 **Social Engineering** | Tries to scare users into clicking the link quickly. |
| 🚫 **Suspicious Link** | Hover reveals a fake login domain: `http://amaz0n-login.com` |
| 🙍 **Generic Greeting** | Uses "Dear Customer" instead of recipient’s name. |
| 🧪 **Header Failures** | Fails SPF, DKIM, and DMARC checks (see below). |

---

## 🔍 Email Header Analysis

**Tool Used:** [MXToolbox Email Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx)  

### Key Results:
- ❌ **SPF Authenticated**: Failed  
- ❌ **DKIM Authenticated**: Failed  
- ❌ **DMARC Compliant**: No DMARC record found  
- ✅ **SPF Alignment**: Passed  
- ❌ **DKIM Alignment**: Failed

> These failures confirm that the email did not originate from a trusted or authorized server.

---

## 🧰 Tools & Resources

- [MXToolbox Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx)
- GitHub for submission

---

## ✅ Conclusion

This email clearly demonstrates multiple phishing traits. It is designed to deceive users using fear tactics and spoofed domains while bypassing authentication mechanisms. Identifying such threats early helps prevent data theft and account compromise.

---

## 📁 Repository Contents

- `README.md` – This analysis report  
- `email.txt` – Sample phishing email content  
- `screenshot folder`– Screenshot of header analysis

