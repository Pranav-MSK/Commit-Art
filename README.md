# 🎨 Issue-Ink  
### Built with GitHub Issues + GitHub Actions
**A GitHub-native, multiplayer pixel canvas powered entirely by Issues and Actions.**

Turn a repository into a living, collaborative artwork—where every contribution is a commit, and every pixel tells a story.

👉 **[Paint a pixel now](../../issues/new?template=paint.yml)**

Check out [Rules](https://github.com/Pranav-MSK/Issue-Ink#-rules) and [How to Use](https://github.com/Pranav-MSK/Issue-Ink#-how-to-use)

---

## 🖼 Live Canvas

![Canvas](map.svg?ts=0)

---

## 🎯 Rules  

- 🕒 One paint per user every **24 hours**  
- 🔒 Each tile is locked for **1 hour** after being painted  
- 🎨 Any user can overwrite any tile (after lock expires)

---

## ✨ Overview  

**Issue-Ink** transforms GitHub into a **real-time, serverless collaborative canvas**.

Users interact with the system by opening issues. Each valid request triggers an automated workflow that updates the canvas, commits the change, and responds instantly—all within GitHub.

No external servers. No databases. Just pure GitHub.

---

## ⚙️ Architecture  
```
User opens Issue
↓
GitHub Actions workflow triggers
↓
Input is validated and processed
↓
Canvas (SVG) + state (JSON) updated
↓
Changes committed back to repository
↓
User receives automated response
```

---

## 🧠 Core Concepts  

- **Issues as Input** → Users “paint” by submitting structured issue titles  
- **Actions as Compute** → GitHub Actions process logic and enforce rules  
- **Repository as Database** → State is stored in version-controlled JSON  
- **Commits as History** → Every pixel change is permanently recorded  

---

## 🚀 How to Use  

1. Click **“Paint a pixel”**  
2. Submit an issue in the format:  

Paint [A5] #FF5733

3. The system will:
- Validate your input  
- Update the canvas  
- Commit the change  
- Respond to your issue  

---

## 🧩 Key Features  

- ⚡ **Fully serverless** — runs entirely on GitHub infrastructure  
- 🔁 **Event-driven** — powered by GitHub Issue events  
- 🧠 **Stateful logic** — tracks cooldowns, locks, and history  
- 🎨 **Live visual output** — SVG canvas updates on every action  
- 🤖 **Automated interaction** — comments, labels, and issue handling  

---

## 🌐 Why it’s interesting  

Issue-Ink demonstrates how GitHub can function as a **complete application platform**, combining:

- Event handling  
- Automation  
- Persistent storage  
- User interaction  

All without leaving the ecosystem.

---

## 💥 Philosophy  

> Build systems where users don’t just contribute code—  
> they **interact, compete, and create together**.

In Issue-Ink:
- Collaboration and chaos coexist  
- Order emerges from randomness  
- Every pixel is intentional—or not  

---

## 🚀 Try it  

Paint something meaningful.  
Or don’t.

👉 **[Start painting](../../issues/new?template=paint.yml)**

---

## 📬 Support

For questions or issues, contact: pranavmskrishnan@gmail.com
