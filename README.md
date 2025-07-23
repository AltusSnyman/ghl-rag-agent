# DIY Go HighLevel Support Widget

Welcome to the **DIY Go HighLevel Support Widget**! 🚀

This guide will walk you through setting up a **custom chatbot** trained on [Go HighLevel's documentation](https://help.gohighlevel.com/support/solutions). By the end of this tutorial, you’ll have a fully functional chatbot widget inside your agency's Go HighLevel dashboard that responds using real-time data from a **Supabase vector database** and **OpenAI** via **n8n** automations.

📽️ **How-To Instructional Video**  
Watch the full setup tutorial here:  
➡️ *[Placeholder for video link]*

---

## 💡 What You’ll Learn

- How to **vectorize Go HighLevel documentation** and store it in Supabase
- How to **retrieve relevant answers using OpenAI and n8n**
- How to **embed a custom widget** (left or right side) inside your Go HighLevel agency portal

---

## 🧰 What You’ll Need

### 1. **Create an n8n Account**
- Official (Paid) Version: [https://n8n.io/](https://n8n.io/)
- Budget Option ($3/mo): [https://repocloud.io/?ref=n72aexk](https://repocloud.io/?ref=n72aexk)

### 2. **Set Up Supabase**
- Sign up: [https://supabase.com/](https://supabase.com/)
- Create a **new project** and **new database**
- Save your **Supabase URL** and **API Key**

### 3. **Get an OpenAI API Key**
- Sign up: [https://platform.openai.com/](https://platform.openai.com/)
- Create and copy your **OpenAI secret key**

---

## 📁 Step-by-Step Instructions

### 🔹 Step 1: Import the RAG Agent Workflow
1. Open the file: `ghl-rag-agent.json`  
2. **Option 1**: Download the file and import it into your n8n instance  
3. **Option 2**: Open the file, copy the full text, and paste it into a new workflow  
4. Configure modules with:
   - Your Supabase credentials
   - Your OpenAI key  
5. **Run** the RAG Agent Workflow to start vectorizing the GoHighLevel docs

### 🔹 Step 2: Set Up the Chatbot Workflow
1. Open the file: `ghl-rag-chat.json`  
2. Import it or paste it as a new workflow in n8n  
3. Set up your:
   - Supabase inputs
   - OpenAI config
4. Run the chatbot workflow

---

## 🧠 Embedding the Widget

### Choose your preferred position:
- **Left Side Widget**: `ghl-left.txt`
- **Right Side Widget**: `ghl-right.txt`

### Steps:
1. Open the respective `.txt` file and **copy all text**
2. Go to Go HighLevel:
   - Agency View → Settings → White Label → Custom JS Code
3. Paste the copied widget code
4. Replace the placeholder URL in the JS code with:
   - **Webhook URL** from the **Webhook Module** (for right side)
   - **Chat URL** from the **Chat Module** (for left side)
5. **Save changes**

---

## ✅ Done! Your custom AI support widget is now live inside Go HighLevel.

---

## 🛠️ Files Included

| File Name             | Description                                 |
|----------------------|---------------------------------------------|
| `ghl-rag-agent.json`  | n8n workflow to vectorize documentation     |
| `ghl-rag-chat.json`   | n8n chatbot workflow                        |
| `ghl-left.txt`        | Widget JS for left side injection           |
| `ghl-right.txt`       | Widget JS for right side injection          |

---

## 💬 Support

For questions or issues, feel free to open an issue on this repo or reach out directly.

---
Made with ❤️ by Altus Snyman
