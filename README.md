# Abinetic Artificial Intelligence

![Abinetic AI Banner](https://abinetic.online/banner.png) <!-- Optional if you have one -->

## Project Overview

**Abinetic Artificial Intelligence** is a next-generation AI platform designed to help individuals and businesses operate **10× faster and smarter**. The platform leverages cutting-edge machine learning, deep learning, and automation technologies to optimize workflows across domains like healthcare, education, customer service, finance, and more.

Our mission is to deliver **ethical**, continuously learning, and practically applicable AI tools that empower real-world solutions.

---

## 🌐 Website & Deployment Info

- **Live Site**: [abinetic.online](https://abinetic.online)
- **Server IP**: `52.77.173.228`
- **Server OS**: Ubuntu 22.04 (EC2 Instance)
- **Domain Provider**: Namecheap

---

## 📁 Project Structure

- `index.html` – Main portal page with login section
- `dashboard.html` – AI tools showcase and feature dashboard
- `style.css` / `tailwind` – TailwindCSS via CDN for styling
- `JavaScript` – For navigation, theme toggling, and login redirect
- `particles.js` – Background animation on the dashboard

---

## 🚀 Installation & Deployment Instructions

To deploy this project on your own server:

1. **Launch EC2 Instance** (Ubuntu 22.04):
   ```bash
   ssh -i "your-key.pem" ubuntu@52.77.173.228
   ```

2. **Update the system**:
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```

3. **Install Apache**:
   ```bash
   sudo apt install apache2 -y
   ```

4. **Link Domain (Namecheap DNS)**:
   - Set **A Record** for `abinetic.online` to point to `52.77.173.228`

5. **Enable HTTPS (Optional)**:
   ```bash
   sudo apt install certbot python3-certbot-apache -y
   sudo certbot --apache
   ```

---

## 🔐 SSH Access (for DevOps)

```bash
ssh -i "abin.pem" ubuntu@ec2-52-77-173-228.ap-southeast-1.compute.amazonaws.com
```

---

## 💡 Features

- 🌙 Light/Dark theme toggle
- 🔐 Secure Login (UI only)
- 📊 Interactive dashboard
- 🧠 AI tools: Model Trainer, Data Analyzer, Smart Chatbot
- 📩 Contact form powered by Formspree

---

## 📚 Learning Outcomes

This project demonstrates:

- Cloud server provisioning (AWS EC2)
- Secure SSH configuration
- DNS management and SSL certificate setup
- Web development using HTML, Tailwind CSS, and JavaScript
- User interface design and responsive web layout

---

## 👤 Developer Info

- **Name**: Abin Ajan Mathew  
- **Student ID**: 35573777  
- **Course**: ICT171 – Cloud Server Project  
- **University**: Murdoch University  

---

## 📄 License

This project is for educational use. Commercial use or reproduction without permission is prohibited.

---

## 📬 Contact

Questions? Suggestions? Submit an issue or contact via the [contact form](https://abinetic.online#contact).

---

> _Think big. Think AI. Abinetic – powering tomorrow, today._
