#!/usr/bin/env python3
"""
TEST SCRIPT - Verify your setup before sending real emails
===========================================================
This sends ONE test email to yourself first.
Run this first to make sure everything works!
"""

import smtplib
import ssl
import os
from email.mime.text import MIMEText
from email.mime.multipart import MIMEMultipart
from email.mime.base import MIMEBase
from email import encoders

# ===================== UPDATE THESE 4 THINGS =====================

YOUR_EMAIL = "your.email@gmail.com"           # Your Gmail address
YOUR_APP_PASSWORD = "abcd efgh ijkl mnop"     # Your 16-digit Gmail App Password
YOUR_NAME = "Your Name"                        # Your full name
RESUME_PATH = "/path/to/your/resume.pdf"       # FULL path to your resume PDF

# =====================================================================


def test_email():
    print("=" * 60)
    print("EMAIL SETUP TEST")
    print("=" * 60)
    
    # 1. Check resume file
    print("\n[1/4] Checking resume file...")
    if not os.path.exists(RESUME_PATH):
        print(f"   ❌ FAIL: Resume not found at: {RESUME_PATH}")
        print("   Fix: Update RESUME_PATH with correct full path")
        return False
    print(f"   ✅ PASS: Resume found ({os.path.getsize(RESUME_PATH)} bytes)")
    
    # 2. Check email format
    print("\n[2/4] Checking email format...")
    if "@" not in YOUR_EMAIL:
        print("   ❌ FAIL: Email looks invalid")
        return False
    print(f"   ✅ PASS: Email format OK ({YOUR_EMAIL})")
    
    # 3. Check app password
    print("\n[3/4] Checking app password...")
    if len(YOUR_APP_PASSWORD.replace(" ", "")) != 16:
        print(f"   ⚠️  WARNING: App password should be 16 characters (yours: {len(YOUR_APP_PASSWORD.replace(' ', ''))})")
    else:
        print("   ✅ PASS: App password length OK")
    
    # 4. Try sending test email to yourself
    print("\n[4/4] Sending test email to yourself...")
    print(f"   Sending to: {YOUR_EMAIL}")
    
    try:
        subject = f"TEST - Job Application Email Setup - {YOUR_NAME}"
        body = f"""This is a test email from your job application script.

If you received this, your setup is working correctly!

Details:
- Sender: {YOUR_NAME}
- Email: {YOUR_EMAIL}
- Resume attached: {os.path.basename(RESUME_PATH)}

You can now run the main script to send emails to all 20 companies.
"""
        
        msg = MIMEMultipart()
        msg["From"] = YOUR_EMAIL
        msg["To"] = YOUR_EMAIL
        msg["Subject"] = subject
        msg.attach(MIMEText(body, "plain"))
        
        # Attach resume
        with open(RESUME_PATH, "rb") as f:
            part = MIMEBase("application", "octet-stream")
            part.set_payload(f.read())
        encoders.encode_base64(part)
        part.add_header("Content-Disposition", "attachment; filename=resume.pdf")
        msg.attach(part)
        
        # Send
        context = ssl.create_default_context()
        with smtplib.SMTP("smtp.gmail.com", 587) as server:
            server.starttls(context=context)
            server.login(YOUR_EMAIL, YOUR_APP_PASSWORD)
            server.sendmail(YOUR_EMAIL, YOUR_EMAIL, msg.as_string())
        
        print("   ✅ PASS: Test email sent successfully!")
        print(f"\n   📧 Check your inbox ({YOUR_EMAIL}) for the test email.")
        print("   If you see it with the resume attached, you're ready to go!")
        return True
        
    except smtplib.SMTPAuthenticationError as e:
        print(f"   ❌ FAIL: Authentication failed!")
        print(f"   Error: {e}")
        print("\n   Common fixes:")
        print("   - Make sure 2-Step Verification is ON in Gmail")
        print("   - Use App Password (not your regular Gmail password)")
        print("   - Generate new App Password at myaccount.google.com/apppasswords")
        return False
        
    except Exception as e:
        print(f"   ❌ FAIL: {e}")
        return False


if __name__ == "__main__":
    success = test_email()
    print("\n" + "=" * 60)
    if success:
        print("🎉 ALL TESTS PASSED! You're ready to send real emails.")
        print("   Run: simple_email_sender.py")
    else:
        print("⚠️  TEST FAILED. Fix the issues above and try again.")
    print("=" * 60)
