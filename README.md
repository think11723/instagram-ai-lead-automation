# 🤖 Instagram AI Automation

An AI-powered Instagram Comment Automation built using **n8n**, **OpenRouter LLMs**, **Instagram Graph API**, and **Google Sheets**.

The workflow automatically detects new Instagram comments, intelligently classifies them using AI, generates human-like replies, prevents spam through cooldown logic, posts replies publicly, and logs every interaction for analytics.

---

## ✨ Features

- 💬 Automatically detects new Instagram comments
- 🧠 AI-based comment classification
- 😊 Sentiment detection (Positive, Negative, Neutral)
- 🚫 Spam & profanity detection
- 🔑 Keyword-based priority replies
- 🤖 Human-like AI generated responses
- ⏳ Cooldown system to avoid repetitive replies
- 📊 Google Sheets interaction logging
- 📈 AI usage analytics
- ⚡ Fully automated workflow built in n8n
- 🔄 Retry & fallback mechanisms
- 📝 Detailed execution logs

---

# 🏗 Workflow

```
Instagram Comment
        │
        ▼
Receive Webhook
        │
        ▼
Check Duplicate Comment
        │
        ▼
Cooldown Check
        │
        ▼
Keyword Detection
      /     \
    Yes      No
    │         │
    ▼         ▼
Keyword     AI Classification
 Reply          │
                ▼
         Generate AI Reply
                │
                ▼
        Public Instagram Reply
                │
                ▼
       Log to Google Sheets
```

---

# 🧠 AI Capabilities

The automation uses Large Language Models to

- Understand user intent
- Detect sentiment
- Identify spam
- Detect offensive language
- Generate natural human replies
- Maintain conversational tone
- Handle unknown comment types

---

# 🛠 Tech Stack

## Automation

- n8n

## AI

- OpenRouter
- GPT-OSS 20B

## APIs

- Instagram Graph API
- Meta Graph API

## Database

- Google Sheets

## Languages

- JavaScript
- JSON

## Authentication

- Meta Access Token
- Google OAuth

---

# 📂 Workflow Modules

## 1. Webhook

Receives Instagram comment events.

---

## 2. Duplicate Detection

Checks whether the comment has already been processed.

---

## 3. Cooldown Manager

Prevents replying multiple times to the same user within a configurable time window.

---

## 4. Keyword Matching

Replies instantly for predefined keywords.

Example:

```
ebook
guide
pdf
course
price
```

---

## 5. AI Classification

Classifies comments into categories like

- Positive
- Question
- Negative
- Spam
- Offensive
- General

---

## 6. AI Reply Generation

Creates a short, friendly, human-like response.

Example

> Thanks so much! Glad you enjoyed it 😊

---

## 7. Instagram Reply

Publishes the generated reply using the Instagram Graph API.

---

## 8. Google Sheets Logging

Every interaction is stored with

- Username
- Timestamp
- Original Comment
- Classification
- AI Reply
- Status
- AI Model Used
- Execution Time
- Reply Source

---

# 📊 Google Sheets Structure

## ProcessedComments

Stores

- Comment ID
- Username
- Timestamp

Used for duplicate detection.

---

## InteractionLog

Stores

- Username
- Timestamp
- Comment
- Classification
- Reply
- Status
- AI Model
- Execution Time
- AI Success
- Reply Source

---

# 🔄 Cooldown Logic

```
User comments
      │
      ▼
Search previous replies
      │
      ▼
Within cooldown?

 YES ─────► Skip AI Reply

 NO ──────► Generate Reply
```

---

# ⚙ Environment Variables

Create the following variables in n8n.

```env
GRAPH_API_VERSION=v23.0

INSTAGRAM_ACCESS_TOKEN=YOUR_TOKEN

OPENROUTER_API_KEY=YOUR_API_KEY

USER_REPLY_COOLDOWN_MINUTES=60
```

---

# 🚀 Future Improvements

- DM automation
- AI lead qualification
- CRM Integration
- Analytics Dashboard
- Multi-language support
- Voice response generation
- Image understanding
- Auto follow-up messages
- Conversation memory
- RAG-powered replies

---

# 📸 Example

**User**

```
Loved this video!
```

**AI**

```
Thanks so much! Glad you enjoyed it 😊
```

---

# 🎯 Use Cases

- Content Creators
- Influencers
- Coaches
- Small Businesses
- Agencies
- Personal Brands
- Marketing Teams

---

# 📈 Benefits

- Saves hours of manual replying
- Improves engagement
- Responds instantly
- Consistent communication
- Human-like AI conversations
- Tracks all interactions
- Easy to customize

---

# 🤝 Contributing

Contributions are welcome.

1. Fork the repository

2. Create a new branch

```
git checkout -b feature-name
```

3. Commit changes

```
git commit -m "Add new feature"
```

4. Push

```
git push origin feature-name
```

5. Open a Pull Request

---

# 📄 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

**Pratik Waghral**

Passionate about AI Automation, Agentic AI, Workflow Automation, and Intelligent Systems.

⭐ If you found this project useful, consider giving it a star!
