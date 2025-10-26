# AI Image Analysis Workshop: Prompt Guide for Students
## Week 7 - Advanced Features Workshop

---

## ⚠️ Important Disclaimers

### 🤖 AI-Generated Content
**This guide was created with AI assistance to demonstrate modern development practices.** While we've worked to ensure accuracy, some information may contain errors or become outdated. This is meant as an **orientation and learning resource**, not a definitive reference. Always verify critical information with official documentation.

### 📚 Learning Resource
This guide is designed to:
- Orient you to key concepts
- Provide starting points for exploration
- Show you what's possible with AI-assisted development

**We cannot fact-check everything**, so treat this as a learning companion, not gospel truth. When in doubt, ask your instructor or check official docs!

---

## 📚 Table of Contents
1. [Getting Started: Python & Django Setup](#getting-started)
2. [Understanding Prompts](#understanding-prompts)
3. [Choosing Your AI Coding Assistant](#choosing-your-ai-coding-assistant)
4. [Main Prompt: Creating the Django App](#main-prompt)
5. [System Prompt: Image Analysis Instructions](#system-prompt)
6. [Iteration Prompts: Adding Features](#iteration-prompts)
7. [Debugging Prompts](#debugging-prompts)
8. [Integrating with No-Code Tools](#integrating-with-no-code-tools)
9. [API-Specific Notes](#api-specific-notes)

---

## 🐍 Getting Started: Python & Django Setup

### Do I Need to Install Python?

**Short answer:** Only if you want to run the code yourself right now. For the workshop, you can just watch and learn!

**Longer answer:** 
- **During Workshop:** Just watch the instructor's demo - no installation needed
- **For Week 11 Projects:** If you want to use Django, you'll need Python installed
- **Alternative:** Use tools like Bolt.new or Replit that run in the browser (no installation!)

### What is Python?

Python is a programming language - it's what Django (a web framework) is written in. Think of it like:
- **Python** = The language (like English or Chinese)
- **Django** = A toolkit written in Python to build websites easily
- **pip** = A package manager (think: app store for Python code)

You've used Python before with pandas for data analysis!

### What is Django?

Django is a **web framework** - pre-written code that handles the boring parts of building websites:
- User accounts and login
- Database connections
- Security
- File uploads
- And more!

Instead of writing everything from scratch, Django provides ready-made components you assemble.

**Analogy:** 
- Building a website from scratch = Building a car from individual screws and metal
- Using Django = Assembling a car from pre-made engine, wheels, chassis

### Do I Need to Know Django?

**No!** That's the magic of AI-assisted development. The AI coding assistant:
- Knows Django already
- Writes the Django code for you
- You just describe WHAT you want in plain English

**Your job:** Understand the concepts (client, server, API)
**AI's job:** Write the actual Django code

### Installing Python (Optional - For Later)

**If you decide to try this at home:**

#### Windows:
1. Go to python.org/downloads
2. Download Python 3.11 or newer
3. **Important:** Check "Add Python to PATH" during installation
4. Open Command Prompt and type: `python --version`

#### Mac:
1. Open Terminal
2. Type: `python3 --version` (Mac has Python built-in, but might be old)
3. If old/missing, install from python.org or use Homebrew: `brew install python3`

#### Check if Python is Installed:
```bash
# In terminal/command prompt
python --version
# or
python3 --version
```

If you see something like "Python 3.11.5", you're good!

### What is pip? (Package Manager)

**pip** is like the "app store" for Python code. It downloads and installs packages (pre-written code libraries).

**Analogy:**
- Your computer = Phone
- Python = Operating system
- pip = App Store
- Django = An app you download

**Example:**
```bash
pip install django
```
This command says: "pip, please download and install Django for me"

**You don't need to memorize this!** AI coding assistants will tell you what to install.

### What About Virtual Environments?

A **virtual environment** is like a separate workspace for each project. It keeps different projects' packages separate.

**Don't worry about this yet!** For learning, you can skip it. The AI assistant might create one, which is fine.

### Quick Start Options (No Installation Needed!)

**Don't want to install anything?** Use these:

1. **Replit** (replit.com)
   - Free online coding environment
   - Python pre-installed
   - Just click "Create Repl" → Choose Python/Django

2. **Google Colab** (colab.research.google.com)
   - Free Python notebooks (like you used for pandas!)
   - Good for experimenting
   - Not ideal for full web apps

3. **Bolt.new**
   - Builds full web apps in browser
   - No installation needed
   - Can deploy instantly

### What You Actually Need for This Workshop

**To follow along:**
- ✅ This guide open in browser
- ✅ Eyes and ears
- ✅ Questions ready!

**To experiment later:**
- ✅ Python installed OR Replit account OR Bolt.new
- ✅ An AI coding assistant (Qwen Coder, Claude, Copilot, etc.)
- ✅ Curiosity and patience

### Common Student Questions

**Q: "I used pandas before, can I use Django?"**
A: Yes! If you can use pandas, you can follow AI instructions to use Django. Same Python language, different toolkit.

**Q: "Do I need to memorize Django commands?"**
A: No! The AI assistant generates the commands. You just need to understand the concepts.

**Q: "Is Django hard?"**
A: Django itself has complexity, but with AI assistance, you're not writing it from scratch. You're directing the AI what to build.

**Q: "What if I don't want to learn Django?"**
A: That's fine! Stick with Adalo/Softr/Bolt. This workshop shows you what happens "under the hood" of those tools.

---

## 🎯 Understanding Prompts

### What is a Prompt?
A prompt is a set of instructions you give to an AI coding assistant (like Qwen Coder, Claude Code, GitHub Copilot, or others) to tell it exactly what you want it to do. Think of it like giving instructions to a very talented but literal assistant.

### Why Prompts Matter
- **Good prompts** = AI builds exactly what you need, first try
- **Vague prompts** = AI guesses and might build the wrong thing
- **Detailed prompts** = Faster development, fewer bugs

### Anatomy of a Good Prompt
```
1. WHAT you want to build (the goal)
2. HOW it should work (technical details)
3. WHAT it should look like (design/output)
4. WHAT to include (specific features or libraries)
```

---

## 🤖 Choosing Your AI Coding Assistant

For this workshop, you can use **any** of these AI coding assistants. They all work with the same prompts!

### Option 1: Qwen Coder (Qoder)
- **What it is:** Open-source coding assistant from Alibaba
- **How to access:** Command line tool or API
- **Best for:** Students who want free, open-source options
- **Setup:** Follow installation instructions at https://github.com/QwenLM/Qwen-Coder

### Option 2: Claude Code
- **What it is:** Anthropic's command-line coding assistant
- **How to access:** Terminal/command line with Claude API key
- **Best for:** Complex reasoning and detailed explanations
- **Setup:** Requires Claude API key from console.anthropic.com

### Option 3: GitHub Copilot
- **What it is:** AI pair programmer integrated into VS Code
- **How to access:** VS Code extension (paid subscription)
- **Best for:** Students already using VS Code
- **Setup:** Install GitHub Copilot extension in VS Code

### Option 4: Gemini Code Assist (CLI)
- **What it is:** Google's coding assistant with CLI interface
- **How to access:** Command line or Google AI Studio
- **Best for:** Integration with Google Cloud services
- **Setup:** Google Cloud account + gcloud CLI

### Option 5: Cursor / Windsurf
- **What it is:** AI-powered code editors with built-in assistants
- **How to access:** Download the editor application
- **Best for:** Students who want an all-in-one IDE experience
- **Setup:** Download from cursor.sh or codeium.com

### 💡 Recommendation for Today's Workshop
**Use whatever you have access to!** All the prompts in this guide work with any AI coding assistant. The instructor will demonstrate with one tool, but the concepts are universal.

**If you don't have any:** 
- Qwen Coder is free and open-source
- Gemini has a generous free tier
- Many tools offer free trials

---

## 🚀 Main Prompt: Creating the Django App

### Purpose
This prompt tells the AI coding agent to build a complete web application that:
- Accepts image uploads from users
- Sends images to an AI vision service
- Displays analysis results

### When to Use
- At the start of your project
- When you want to build the entire application from scratch

### The Prompt (Works with ALL AI assistants)

```
Create a Django web application called "smartvision" that allows users to upload images and get AI-powered analysis.

Requirements:
- Simple, modern upload interface with drag-and-drop support
- Send uploaded image to Google Gemini Vision API (gemini-1.5-flash model)
- Prompt to send to Gemini: "Analyze this image in detail. Describe: 1) What objects you see, 2) The context/setting, 3) Three potential use cases for this image in a mobile app (e-commerce, social, utility, etc.)"
- Display Gemini's response in a formatted card with nice typography
- Show the uploaded image alongside the analysis
- Use Django 4.2 and google-generativeai Python package
- Include proper error handling (API failures, unsupported file types)
- Add comments explaining the code flow
- Style with modern CSS (gradients, shadows, responsive design)
- Show a loading spinner while processing

Technical notes:
- Use Django's FileSystemStorage for temporary file handling
- API key should be read from environment variable GEMINI_API_KEY
- Support JPG, PNG, WEBP formats
- Limit file size to 5MB
```

### 📝 Student Notes: Why Each Part Matters

**"Create a Django web application called 'smartvision'"**
→ Tells AI which framework to use (Django) and what to name it

**"Simple, modern upload interface with drag-and-drop"**
→ Defines user experience - not just a boring button

**"Send uploaded image to Google Gemini Vision API"**
→ Specifies WHICH AI service (important - different APIs have different code)

**"Prompt to send to Gemini: 'Analyze this image...'"**
→ This is a "system prompt" - instructions for the AI vision model

**"Display Gemini's response in a formatted card"**
→ Makes results look professional, not just plain text

**"API key should be read from environment variable"**
→ Security best practice - never hardcode API keys in code!

**"Support JPG, PNG, WEBP formats"**
→ Defines constraints - helps catch errors early

### 🔄 How to Use This Prompt with Different Tools

#### With Qwen Coder / Qoder:
```bash
# In terminal
qwen-coder "Create a Django web application called 'smartvision'..."
```

#### With Claude Code:
```bash
# In terminal
claude-code "Create a Django web application called 'smartvision'..."
```

#### With GitHub Copilot:
```
1. Open VS Code
2. Open Copilot Chat (Ctrl+Shift+I or Cmd+Shift+I)
3. Paste the prompt
4. Let Copilot generate the code
```

#### With Gemini CLI:
```bash
# In terminal
gemini code "Create a Django web application called 'smartvision'..."
```

#### With Cursor:
```
1. Open Cursor editor
2. Press Ctrl+K (or Cmd+K on Mac)
3. Paste the prompt
4. Cursor will generate the code inline
```

---

## 🧠 System Prompt: Image Analysis Instructions

### What is a System Prompt?
A system prompt is the instruction YOU send to the AI vision service (like Gemini) telling it HOW to analyze the image. It's different from the prompt you give your AI coding assistant.

### Flow Diagram
```
You → AI Coding Assistant (Qwen/Claude/Copilot/etc.)
         ↓
    Builds Django App → Gemini API (analyzes image)
         ↓
    System Prompt: "Analyze this image and describe..."
```

### Basic System Prompt (General Analysis)

```
Analyze this image in detail. Describe:
1) What objects you see
2) The context/setting
3) Three potential use cases for this image in a mobile app
```

**Why this works:**
- Numbered list = structured response
- "In detail" = AI doesn't give one-word answers
- "Potential use cases" = makes it practical for students' projects

### Alternative System Prompts (For Different Use Cases)

#### Product E-commerce
```
You are a product catalog AI. Analyze this product image and provide:
- Product category
- Key features visible
- Suggested product title
- Estimated condition (new/used/damaged)
- Suggested price range in USD
- 5 SEO keywords for listing
```

#### Food/Recipe App
```
Analyze this food image and provide:
- Main dish/ingredient identification
- Cuisine type
- Suggested recipe name
- Key ingredients visible
- Dietary tags (vegetarian, gluten-free, etc.)
```

#### Fashion/Clothing App
```
Analyze this clothing/outfit image:
- Clothing type and style
- Colors present
- Occasion/setting (casual, formal, sportswear)
- Season suitability
- Suggested outfit pairings
```

#### Document/Text Extraction
```
Extract all text from this image. If it's a form or document:
- Identify document type
- Extract key fields (names, dates, amounts)
- Highlight any important information
- Note if anything is unclear or unreadable
```

### 🎓 Teaching Moment: How to Write Good System Prompts

**Bad System Prompt:**
```
Tell me about this image.
```
→ Too vague! AI might give you anything.

**Good System Prompt:**
```
You are an expert art curator. Analyze this artwork and describe:
1. Art style and period
2. Dominant colors and mood
3. Subject matter
4. Estimated value range if known
```
→ Specific role, clear structure, defined output!

**Key Principles:**
1. **Be specific** - Tell AI what you want, not what you don't want
2. **Give structure** - Use numbered lists or bullet points
3. **Define output format** - JSON? Plain text? Bullet points?
4. **Set context** - "You are a [expert]..." helps AI respond appropriately

---

## 🔄 Iteration Prompts: Adding Features

### Purpose
After you have a working basic app, use these prompts to add more features one at a time.

### Prompt 1: Save Analysis History

```
Modify the application to:
- Save the last 10 uploaded images and their AI analysis results to SQLite database
- Display them in a gallery below the upload form
- Each gallery item shows: thumbnail, analysis snippet, timestamp
- Add a "Delete" button for each saved item
- Use Django models to store: image file path, analysis text, upload date
```

**What students learn:** Database integration, data persistence

### Prompt 2: Compare Two Images

```
Add a "Compare Mode" feature:
- User can select 2 previously uploaded images from the gallery
- Add a "Compare" button that sends both images to Gemini
- System prompt for comparison: "Compare these two images. Describe similarities, differences, and which would be better for [e-commerce product listing]"
- Display comparison side-by-side with images
```

**What students learn:** Multi-image processing, UI state management

### Prompt 3: Add User Authentication

```
Add user authentication to the app:
- Use Django's built-in authentication system
- Users must register/login to upload images
- Each user sees only THEIR uploaded images
- Add a simple profile page showing upload count
- Style the login/register pages to match the main app design
```

**What students learn:** User management, data isolation

### Prompt 4: Export Results to PDF

```
Add a "Download Report" feature:
- Create a button on each analysis result
- Generate a PDF report containing: uploaded image, full analysis text, timestamp, your app branding
- Use ReportLab library for PDF generation
- Style the PDF professionally with headers and formatting
```

**What students learn:** File generation, third-party libraries

### Prompt 5: Add Real-time Processing Indicator

```
Improve the user experience:
- Replace simple loading spinner with a progress indicator
- Show status messages: "Uploading image...", "Sending to AI...", "Processing results..."
- Use JavaScript fetch API with progress events
- Add animations for each stage
```

**What students learn:** Frontend interactivity, async operations

---

## 🐛 Debugging Prompts

### When Code Doesn't Run

```
I'm getting this error when running the Django app:
[paste the error message here]

The error occurs when [describe what you were doing].
Can you explain what's wrong and how to fix it?
```

### When API Calls Fail

```
The app runs but the API call to Gemini fails with this error:
[paste error]

Here's my current code:
[paste the relevant view function]

My GEMINI_API_KEY is set in the environment. What could be wrong?
```

### When Styling Looks Broken

```
The upload form displays but the CSS styling isn't working correctly. The page looks like [describe the problem].

Can you check the CSS and fix the layout to ensure:
- The upload area is centered
- The form is responsive on mobile
- Colors match the gradient theme
```

### When Features Don't Work As Expected

```
I added the [feature name] but it's not working as expected. Instead of [expected behavior], it's [actual behavior].

Can you review the code and suggest fixes?
```

---

## 🔌 API-Specific Notes

### Google Gemini API

**API Key Setup:**
```bash
# In terminal/command prompt
export GEMINI_API_KEY="your_key_here"

# Or in .env file
GEMINI_API_KEY=your_key_here
```

**Python Code Pattern:**
```python
import google.generativeai as genai

genai.configure(api_key=os.getenv('GEMINI_API_KEY'))
model = genai.GenerativeModel('gemini-1.5-flash')

# For images
response = model.generate_content([
    "Your system prompt here",
    {"mime_type": "image/jpeg", "data": base64_image_data}
])
```

**Free Tier:** 1,500 requests per day
**Best for:** Students, demos, prototypes

---

### OpenAI Vision API (GPT-4 Vision)

**API Key Setup:**
```bash
export OPENAI_API_KEY="your_key_here"
```

**Python Code Pattern:**
```python
from openai import OpenAI

client = OpenAI(api_key=os.getenv('OPENAI_API_KEY'))

response = client.chat.completions.create(
    model="gpt-4-vision-preview",
    messages=[{
        "role": "user",
        "content": [
            {"type": "text", "text": "Your system prompt here"},
            {"type": "image_url", "image_url": {"url": f"data:image/jpeg;base64,{base64_image}"}}
        ]
    }]
)
```

**Pricing:** Pay per use (~$0.01 per image)
**Best for:** Production apps, high accuracy needs

---

### DeepSeek Vision API (If Available)

**Status:** As of early 2025, vision capabilities through DeepSeek-VL2 model
**Note:** API access may be limited or through third-party platforms

**If you have access:**
```python
# DeepSeek uses OpenAI-compatible format
from openai import OpenAI

client = OpenAI(
    api_key=os.getenv('DEEPSEEK_API_KEY'),
    base_url="https://api.deepseek.com"
)

# Similar usage to OpenAI
```

**Why we're NOT using it today:**
- Unclear API access for vision features
- Recent stability issues reported
- Limited documentation for vision endpoints

---

## 🎓 Key Concepts for Students

### 1. Prompt Engineering is a Skill
Writing good prompts is like writing good requirements. The better your prompt, the better your code.

### 2. Iteration is Normal
You won't get perfect code on the first try. Use iteration prompts to refine features.

### 3. System Prompts vs Code Prompts
- **Code prompt** → Instructions for your AI coding assistant (Qwen/Claude/Copilot) to write code
- **System prompt** → Instructions sent TO the AI vision API in your code

### 4. API Keys are Secrets
Never commit API keys to GitHub! Always use environment variables.

### 5. Different APIs, Same Pattern
All vision APIs follow similar patterns:
1. Send image (as URL or base64)
2. Send text prompt
3. Receive structured response

The code syntax differs, but the CONCEPT is identical.

### 6. Different AI Assistants, Same Prompts
Whether you use Qwen Coder, Claude Code, GitHub Copilot, or another tool, the prompts are the same. They all understand the same instructions!

---

## 💡 Pro Tips

### For Your Week 11 Project

1. **Start with the basic prompt** - Get something working first
2. **Test with multiple images** - Different lighting, angles, quality
3. **Handle errors gracefully** - What if API is down? Show user a nice message
4. **Consider rate limits** - Don't spam the API, add delays between requests
5. **Document your prompts** - Save the system prompts you use in a file

### Questions to Ask Yourself

Before writing a prompt:
- What EXACTLY do I want the AI to build/do?
- What libraries or tools should it use?
- What should the output look like?
- What errors might occur and how should they be handled?

### Common Mistakes to Avoid

❌ "Make me an app with AI"
→ Too vague!

✅ "Create a Flask app that uses OpenAI Vision API to analyze product photos and suggest titles"

❌ "Fix my code"
→ Doesn't provide context!

✅ "I'm getting a 401 error when calling the API. Here's my code [paste]. My API key is set. What's wrong?"

---

## 🛠️ Tool-Specific Tips

### For Qwen Coder Users
- Works great with Python and web frameworks
- Can run locally without internet (some models)
- Good for understanding code step-by-step

### For Claude Code Users
- Excellent at explaining complex concepts
- Great for debugging and error analysis
- Strong with architectural decisions

### For GitHub Copilot Users
- Best when writing code line-by-line
- Great autocomplete suggestions
- Works seamlessly in VS Code

### For Gemini CLI Users
- Easy integration with Google Cloud
- Good for multimodal tasks
- Generous free tier

---

## 📚 Additional Resources

### Official Documentation
- Google Gemini API: https://ai.google.dev/
- OpenAI Vision API: https://platform.openai.com/docs/guides/vision
- Django Documentation: https://docs.djangoproject.com/
- Qwen Coder: https://github.com/QwenLM/Qwen-Coder

### Learning Prompt Engineering
- Anthropic's Prompt Engineering Guide: https://docs.anthropic.com/prompt-engineering
- OpenAI Prompt Engineering Guide: https://platform.openai.com/docs/guides/prompt-engineering

### AI Coding Assistants
- Qwen Coder GitHub: https://github.com/QwenLM/Qwen-Coder
- Claude Code Docs: https://docs.anthropic.com/
- GitHub Copilot: https://github.com/features/copilot
- Cursor: https://cursor.sh
- Windsurf: https://codeium.com/windsurf

---

## 🎯 Workshop Challenge

**Try this after the demo:**

Use the prompts in this guide to build YOUR OWN version of the image analysis app, but customize it for YOUR Week 11 project idea.

1. Choose your AI coding assistant (Qwen, Claude, Copilot, etc.)
2. Start with the main prompt
3. Modify the system prompt to fit your use case
4. Add 1-2 features using the iteration prompts
5. Share what you built with your team!

Remember: The best way to learn is by doing. Don't just watch - code along!

---

**Questions?** Ask during the workshop or experiment on your own. The worst that can happen is you learn what NOT to do! 😊

### Basic System Prompt (General Analysis)

```
Analyze this image in detail. Describe:
1) What objects you see
2) The context/setting
3) Three potential use cases for this image in a mobile app
```

**Why this works:**
- Numbered list = structured response
- "In detail" = AI doesn't give one-word answers
- "Potential use cases" = makes it practical for students' projects

### Alternative System Prompts (For Different Use Cases)

#### Product E-commerce
```
You are a product catalog AI. Analyze this product image and provide:
- Product category
- Key features visible
- Suggested product title
- Estimated condition (new/used/damaged)
- Suggested price range in USD
- 5 SEO keywords for listing
```

#### Food/Recipe App
```
Analyze this food image and provide:
- Main dish/ingredient identification
- Cuisine type
- Suggested recipe name
- Key ingredients visible
- Dietary tags (vegetarian, gluten-free, etc.)
```

#### Fashion/Clothing App
```
Analyze this clothing/outfit image:
- Clothing type and style
- Colors present
- Occasion/setting (casual, formal, sportswear)
- Season suitability
- Suggested outfit pairings
```

#### Document/Text Extraction
```
Extract all text from this image. If it's a form or document:
- Identify document type
- Extract key fields (names, dates, amounts)
- Highlight any important information
- Note if anything is unclear or unreadable
```

### 🎓 Teaching Moment: How to Write Good System Prompts

**Bad System Prompt:**
```
Tell me about this image.
```
→ Too vague! AI might give you anything.

**Good System Prompt:**
```
You are an expert art curator. Analyze this artwork and describe:
1. Art style and period
2. Dominant colors and mood
3. Subject matter
4. Estimated value range if known
```
→ Specific role, clear structure, defined output!

**Key Principles:**
1. **Be specific** - Tell AI what you want, not what you don't want
2. **Give structure** - Use numbered lists or bullet points
3. **Define output format** - JSON? Plain text? Bullet points?
4. **Set context** - "You are a [expert]..." helps AI respond appropriately

---

## 🔄 Iteration Prompts: Adding Features

### Purpose
After you have a working basic app, use these prompts to add more features one at a time.

### Prompt 1: Save Analysis History

```
Modify the application to:
- Save the last 10 uploaded images and their AI analysis results to SQLite database
- Display them in a gallery below the upload form
- Each gallery item shows: thumbnail, analysis snippet, timestamp
- Add a "Delete" button for each saved item
- Use Django models to store: image file path, analysis text, upload date
```

**What students learn:** Database integration, data persistence

### Prompt 2: Compare Two Images

```
Add a "Compare Mode" feature:
- User can select 2 previously uploaded images from the gallery
- Add a "Compare" button that sends both images to Gemini
- System prompt for comparison: "Compare these two images. Describe similarities, differences, and which would be better for [e-commerce product listing]"
- Display comparison side-by-side with images
```

**What students learn:** Multi-image processing, UI state management

### Prompt 3: Add User Authentication

```
Add user authentication to the app:
- Use Django's built-in authentication system
- Users must register/login to upload images
- Each user sees only THEIR uploaded images
- Add a simple profile page showing upload count
- Style the login/register pages to match the main app design
```

**What students learn:** User management, data isolation

### Prompt 4: Export Results to PDF

```
Add a "Download Report" feature:
- Create a button on each analysis result
- Generate a PDF report containing: uploaded image, full analysis text, timestamp, your app branding
- Use ReportLab library for PDF generation
- Style the PDF professionally with headers and formatting
```

**What students learn:** File generation, third-party libraries

### Prompt 5: Add Real-time Processing Indicator

```
Improve the user experience:
- Replace simple loading spinner with a progress indicator
- Show status messages: "Uploading image...", "Sending to AI...", "Processing results..."
- Use JavaScript fetch API with progress events
- Add animations for each stage
```

**What students learn:** Frontend interactivity, async operations

---

## 🐛 Debugging Prompts

### When Code Doesn't Run

```
I'm getting this error when running the Django app:
[paste the error message here]

The error occurs when [describe what you were doing].
Can you explain what's wrong and how to fix it?
```

### When API Calls Fail

```
The app runs but the API call to Gemini fails with this error:
[paste error]

Here's my current code:
[paste the relevant view function]

My GEMINI_API_KEY is set in the environment. What could be wrong?
```

### When Styling Looks Broken

```
The upload form displays but the CSS styling isn't working correctly. The page looks like [describe the problem].

Can you check the CSS and fix the layout to ensure:
- The upload area is centered
- The form is responsive on mobile
- Colors match the gradient theme
```

### When Features Don't Work As Expected

```
I added the [feature name] but it's not working as expected. Instead of [expected behavior], it's [actual behavior].

Can you review the code and suggest fixes?
```

---

## 🔌 API-Specific Notes

### Google Gemini API

**API Key Setup:**
```bash
# In terminal/command prompt
export GEMINI_API_KEY="your_key_here"

# Or in .env file
GEMINI_API_KEY=your_key_here
```

**Python Code Pattern:**
```python
import google.generativeai as genai

genai.configure(api_key=os.getenv('GEMINI_API_KEY'))
model = genai.GenerativeModel('gemini-1.5-flash')

# For images
response = model.generate_content([
    "Your system prompt here",
    {"mime_type": "image/jpeg", "data": base64_image_data}
])
```

**Free Tier:** 1,500 requests per day
**Best for:** Students, demos, prototypes

---

### OpenAI Vision API (GPT-4 Vision)

**API Key Setup:**
```bash
export OPENAI_API_KEY="your_key_here"
```

**Python Code Pattern:**
```python
from openai import OpenAI

client = OpenAI(api_key=os.getenv('OPENAI_API_KEY'))

response = client.chat.completions.create(
    model="gpt-4-vision-preview",
    messages=[{
        "role": "user",
        "content": [
            {"type": "text", "text": "Your system prompt here"},
            {"type": "image_url", "image_url": {"url": f"data:image/jpeg;base64,{base64_image}"}}
        ]
    }]
)
```

**Pricing:** Pay per use (~$0.01 per image)
**Best for:** Production apps, high accuracy needs

---

### DeepSeek Vision API (If Available)

**Status:** As of early 2025, vision capabilities through DeepSeek-VL2 model
**Note:** API access may be limited or through third-party platforms

**If you have access:**
```python
# DeepSeek uses OpenAI-compatible format
from openai import OpenAI

client = OpenAI(
    api_key=os.getenv('DEEPSEEK_API_KEY'),
    base_url="https://api.deepseek.com"
)

# Similar usage to OpenAI
```

**Why we're NOT using it today:**
- Unclear API access for vision features
- Recent stability issues reported
- Limited documentation for vision endpoints

---

## 🎓 Key Concepts for Students

### 1. Prompt Engineering is a Skill
Writing good prompts is like writing good requirements. The better your prompt, the better your code.

### 2. Iteration is Normal
You won't get perfect code on the first try. Use iteration prompts to refine features.

### 3. System Prompts vs Code Prompts
- **Code prompt** → Instructions for Claude/ChatGPT to write code
- **System prompt** → Instructions sent TO the AI vision API in your code

### 4. API Keys are Secrets
Never commit API keys to GitHub! Always use environment variables.

### 5. Different APIs, Same Pattern
All vision APIs follow similar patterns:
1. Send image (as URL or base64)
2. Send text prompt
3. Receive structured response

The code syntax differs, but the CONCEPT is identical.

---

## 💡 Pro Tips

### For Your Week 11 Project

1. **Start with the basic prompt** - Get something working first
2. **Test with multiple images** - Different lighting, angles, quality
3. **Handle errors gracefully** - What if API is down? Show user a nice message
4. **Consider rate limits** - Don't spam the API, add delays between requests
5. **Document your prompts** - Save the system prompts you use in a file

### Questions to Ask Yourself

Before writing a prompt:
- What EXACTLY do I want the AI to build/do?
- What libraries or tools should it use?
- What should the output look like?
- What errors might occur and how should they be handled?

### Common Mistakes to Avoid

❌ "Make me an app with AI"
→ Too vague!

✅ "Create a Flask app that uses OpenAI Vision API to analyze product photos and suggest titles"

❌ "Fix my code"
→ Doesn't provide context!

✅ "I'm getting a 401 error when calling the API. Here's my code [paste]. My API key is set. What's wrong?"

---

## 📚 Additional Resources

### Official Documentation
- Google Gemini API: https://ai.google.dev/
- OpenAI Vision API: https://platform.openai.com/docs/guides/vision
- Django Documentation: https://docs.djangoproject.com/

### Learning Prompt Engineering
- Anthropic's Prompt Engineering Guide: https://docs.anthropic.com/prompt-engineering
- OpenAI Prompt Engineering Guide: https://platform.openai.com/docs/guides/prompt-engineering

---

## 🎯 Workshop Challenge

**Try this after the demo:**

Use the prompts in this guide to build YOUR OWN version of the image analysis app, but customize it for YOUR Week 11 project idea.

1. Start with the main prompt
2. Modify the system prompt to fit your use case
3. Add 1-2 features using the iteration prompts
4. Share what you built with your team!

Remember: The best way to learn is by doing. Don't just watch - code along!

---

**Questions?** Ask during the workshop or experiment on your own. The worst that can happen is you learn what NOT to do! 😊
