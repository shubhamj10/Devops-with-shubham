# Container and Container Image

## What is a Container?

A **container** is a lightweight, isolated environment that runs your application **along with everything it needs**:

- Code  
- Runtime (Node.js, Python, Java etc.)  
- Libraries & dependencies  
- Configuration  

Unlike virtual machines (VMs), containers **do NOT include a full operating system**.  
They share the host OS kernel — making them:

- **Faster**  
- **More lightweight**  
- **Portable** (runs the same on any machine)

### 🧱 Analogy
Think of a container like a **tiffin box**:

- Inside the tiffin: your app (food), dependencies (spoon, napkin)  
- You give the same tiffin to anyone → they can run/eat it the same way

---

## What is a Container Image?

A **container image** is a **template or blueprint** used to create a container.

- **Read-only**
- Contains application code + dependencies
- A snapshot of everything needed to run the app

### 💡 Analogy

- Image = Recipe for making pav bhaji  
- Container = The actual cooked pav bhaji served to you

---


# Microservices 