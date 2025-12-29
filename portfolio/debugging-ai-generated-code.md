# Debugging AI‑Generated Code: Lessons Learned from Real‑World Iteration

This case study captures the part of AI‑augmented engineering that people rarely talk about:  
the debugging, the hallucinations, the late‑night fixes, the broken builds, and the persistence required to turn AI‑generated code into a working system.

This wasn’t a clean “AI wrote it and it just worked” experience.  
It was a real engineering process — with AI as a collaborator, not a shortcut.

---

## 🧠 The Starting Point

After building my first AI‑assisted project, I wanted to create a second one that would complement it.  
I had a working prototype of a small app (originally for tracking smoking, later converted to water intake), and I wanted to rebuild it cleanly using:

- A strong coder model  
- A clear prompt  
- A more focused architecture  
- A local development environment  
- A Docker deployment  

I expected some friction.  
I did not expect the amount of debugging that followed.

---

## ⚠️ Where Things Went Off the Rails

### **1. Overly general prompts**
My early prompts were too open‑ended:

- “Pick what you think is best”  
- “Choose the architecture you prefer”  

This gave the model too much freedom, and it drifted quickly.

### **2. Hallucinated components**
The model invented:

- Files that didn’t exist  
- Routes I never asked for  
- Variables that weren’t defined  
- Entire flows that didn’t match the project  

### **3. Incorrect assumptions**
The model assumed:

- Different frameworks  
- Different folder structures  
- Different database schemas  

### **4. Misleading debugging suggestions**
Some of the model’s “fixes” made things worse:

- Wrong error explanations  
- Incorrect dependency advice  
- Fixes that introduced new bugs  

### **5. The build broke repeatedly**
I deployed the app to my local Docker server and watched it fail in real time.

This was the turning point.

---

## 🛠️ Human‑in‑the‑Loop Debugging

This is where the project became valuable.

I:

- Reviewed every error manually  
- Forced the model to explain its reasoning  
- Overrode incorrect suggestions  
- Re‑prompted with tighter constraints  
- Rebuilt the project step‑by‑step  
- Used snapshots to preserve working states  
- Corrected hallucinations by hand  
- Re‑tested every fix  

This wasn’t “AI coding for me.”  
This was **AI‑augmented engineering**.

The model generated ideas.  
I validated them.  
The model wrote code.  
I corrected it.  
The model hallucinated.  
I grounded it.  
The model drifted.  
I steered it back.

This is the real workflow.

---

## 🔄 The Breakthrough

After several nights of iteration, the app finally:

- Built cleanly  
- Ran inside Docker  
- Connected to the database  
- Responded to requests  
- Behaved consistently  

It wasn’t perfect — but it worked.  
And it was mine.

---

## 🧠 What I Learned

### **1. AI is powerful, but not reliable without oversight
