<img width="709" height="169" alt="image" src="https://github.com/user-attachments/assets/a1407063-edb2-4342-bd9c-66a53405c7d5" />
# 📝 n8n Automated Blog Publishing Workflow

This n8n workflow automates the **complete blog publishing process** from topic research to WordPress publication. It researches topics, writes **SEO-optimized content**, generates images, publishes posts, and notifies your team—all automatically from **Google Sheets input**! 🚀

---

## 🌟 How It Works

### Step 1: Client Management & Scheduling
- **Client Data Retrieval**: Scans master Google Sheet for clients with `Active` project status and `Automation` blog publishing setting.
- **Publishing Schedule Validation**: Checks if current day matches client's weekly frequency (Mon-Sun) or if set to `Daily`.
- **Content Source Access**: Connects to client-specific Google Sheet using stored document ID and sheet name. 📊

### Step 2: Content Planning & Selection
- **Topic Filtering**: Retrieves rows where `Status for Approval` = `Approved` and `Live Link` = `Pending`.
- **Content Validation**: Ensures `Focus Keyword` field is populated before proceeding. 🔍
- **Single Topic Processing**: Selects the first available topic to maintain quality and prevent API rate limits.

### Step 3: AI-Powered Research & Writing
- **Comprehensive Research**: Google Gemini analyzes search intent, competitor content, audience needs, trending subtopics, and LSI keywords.
- **Content Generation**: Creates 800-1000 word articles with **natural keyword integration**, internal linking, and conversational tone tailored for Indian investors.
- **Quality Assessment**: Evaluates content for human-like writing, readability, and engagement factors. ✅
- **Content Optimization**: Automatically fixes grammar, punctuation, sentence flow, and readability while maintaining HTML structure.

### Step 4: Visual Content Creation
- **Image Prompt Generation**: OpenAI creates prompts based on blog title and content for professional visuals. 🎨
- **Image Generation**: Ideogram AI produces **1248x832 resolution images** with realistic styling.
- **Binary Processing**: Downloads and converts images to binary format for WordPress upload.

### Step 5: WordPress Publication
- **Media Upload**: Uploads image to WordPress media library with proper filename and headers.
- **Content Publishing**: Creates new WordPress post with title, optimized content, and embedded image.
- **Featured Image Assignment**: Sets uploaded image as post thumbnail. 🖼️
- **Category Assignment**: Automatically assigns posts to predefined category.

### Step 6: Tracking & Communication
- **Status Updates**: Updates Google Sheet with live blog URL in `Live Link` column.
- **Team Notification**: Sends Discord message to designated channel with published blog link and review request. 💬
- **Process Completion**: Triggers next iteration or ends workflow based on remaining topics.

---

## ⚙️ Setup Steps
- **Estimated Setup Time**: 45-60 minutes  

### Required API Credentials:
1. **Google Sheets API**
   - Service account & OAuth2 credentials
   - Proper sharing permissions
2. **Google Gemini API**
   - Active API key with Gemini Pro access
3. **OpenAI API**
   - GPT-4 access & sufficient tokens
4. **Ideogram AI API**
   - Premium account for high-quality images
5. **WordPress REST API**
   - Application passwords, REST API enabled, Editor/Admin role
6. **Discord Bot API**
   - Bot token, channel ID, proper permissions

---

## 🗂️ Master Sheet Configuration
**Columns Needed:**
- Client Name | Project Status | Blog Publishing | Website URL | Blog Posting Auth Code | On Page Sheet | WeeklyFrequency | Discord Channel  

**Content Planning Sheet Columns:**
- S.No. | Focus Keyword | Content Topic | Target Page | Words | Brief URL | Content URL | Status for Approval | Live Link

---

## 🖥️ WordPress Configuration
- REST API activation  
- Dedicated user with Editor/Admin role  
- Application passwords  
- Category setup for automated posts  
- Media upload permissions  

---

## 💬 Discord Integration Setup
- Bot creation & permissions ✅  
- Channel setup for notifications  
- User mentions for targeted alerts  
- Customizable message templates

---

## 🎯 Workflow Features & Capabilities

**Content Quality Standards**:
- SEO Optimization with LSI keywords  
- Readability & conversational tone  
- Proper HTML formatting, headings & lists  
- Consistent 800-1000 word length  
- Tailored for **Indian investor audience**

**Image Generation Specs**:
- Resolution: 1248x832 px  
- Style: Realistic, professional, human subjects  
- Design: Clean layout with heading placement  
- Branding: Beige to gradient backgrounds with golden overlay ✨

**Error Handling & Reliability**:
- Graceful failures with retries  
- API rate limit handling  
- Data validation & backup processes  
- Comprehensive logging  

**Security & Access Control**:
- Credential encryption 🔒  
- Limited permissions & basic auth  
- Data privacy and access logging

---

## 🛠️ Troubleshooting
- **API Rate Limits**: Check quotas  
- **WordPress Authentication**: Verify credentials  
- **Sheet Access**: Ensure proper permissions  
- **Image Generation Failures**: Check Ideogram API key and quota

---

## 🚀 Ready to Automate Your Blog Publishing!
This workflow ensures your content is **research-backed, SEO-friendly, visually appealing**, and published automatically, saving time and boosting engagement. 🏆
