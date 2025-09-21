# Insurance Lead Capture Engine 🚀

# Problem we wanted to solve

Insurance teams run ads across Google, Meta, LinkedIn, but often face:

❌ Missed leads (emails stuck in spam, spreadsheets forgotten)
❌ Delayed follow-ups (agents don’t get notified instantly)
❌ No campaign tracking (hard to tell if Google or Meta worked better)

# What we built

A lightweight serverless lead capture engine on AWS that:

1. Captures lead data from any form (website, landing page, ad form).

2. Stores every lead securely in DynamoDB.

3. Sends instant email alerts to the sales team.

4. Sends an auto-reply with a brochure to the customer.

5. Tracks UTM tags (source, campaign) for ROI analysis.

# How it works (Architecture Flow)

![Insurance Lead Capture Architecture](insurance-lead-capture-architecture.png)


🖥️ Prospect clicks ad and fills the form.

🌐 Form calls API Gateway endpoint.

⚡ Lambda processes data, saves to DynamoDB, and triggers emails.

📩 SES sends:
Alert to sales team (lead + brochure).
Auto-reply to customer (confirmation + brochure).

🗃️ S3 hosts:
Static demo form
PDF brochures

🔔 SNS raises alerts if errors occur.

# Why it matters

✅ Faster follow-ups → team notified in seconds
✅ Professional customer touch → auto-reply with brochure
✅ No missed leads → all data safe in DynamoDB
✅ Attribution ready → UTM tags logged with each lead
✅ Pay-as-you-go → scales with ad budget
