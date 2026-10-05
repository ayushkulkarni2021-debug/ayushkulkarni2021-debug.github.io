# Activity 5: AI Prompt Log & Refinement Journal

**Student Name:** Ayush Kulkarni  
**Target URL:** `https://ayushkulkarni.github.io`  
**Activity Title:** AI-Driven Personal Portfolio Web Page  

---

## 1. Initial Generation Prompt (Step 2)

```text
Act as an expert frontend web developer. Create a single-page modern personal portfolio blog website as a standalone index.html file containing all HTML, inline CSS, and JavaScript.

Here are the details for the portfolio:
- Name: Ayush Kulkarni
- Role: 4th Semester Computer Science & Engineering Student
- Tone: Professional, modern, and approachable
- Design Style: Dark mode theme with sleek glassmorphism, blue/indigo accent colors, dynamic hover animations, clean typography, and mobile responsive layout.

Required Sections:
1. Header / Navigation: Brand logo, navigation links (About, Projects, Skills, Contact).
2. Hero / About Section: Brief introduction highlighting my bio, 4th semester CSE status, and career goal: "To master cloud-native architecture and contribute to open-source software projects while preparing for a Software Engineering Internship."
3. Projects Section: Showcase my 4 core lab activity projects:
   - Activity 1: VS Code Environment Setup (Custom development setup with extensions and keyboard shortcuts)
   - Activity 2: Git & GitHub Setup (Repository link: https://github.com/ayushkulkarni/hello-world)
   - Activity 3: GitLens & Live Share Collaboration (Repository link: https://github.com/ayushkulkarni/pair-programming-log)
   - Activity 4: LeetCode Practice Repository (Repository link: https://github.com/ayushkulkarni/leetcode-solutions)
4. Skills Section: Categories for Programming Languages (C, C++, Python, JavaScript, HTML/CSS), Developer Tools (Git, GitHub, VS Code, GitLens, Live Share), and Core Concepts (DSA, Version Control, Pair Programming).
5. Contact Section: Include my GitHub profile link (https://github.com/ayushkulkarni), email placeholder, and a contact form UI.
6. Footer: Copyright and social links.

Please output the complete, valid, self-contained single-file HTML page without using external CSS libraries like Bootstrap or Tailwind, using pure custom modern CSS.
```

---

## 2. Review of Initial AI Output (Step 3)

### Initial Output Evaluation:
* **Accurate Bio:** Yes, correctly included name, branch, semester, and career goal.
* **Projects Covered:** Listed 4 projects, but the description for Activity 3 was vague and lacked details about real-time pair programming.
* **Repository Links:** Included placeholders (`#`) for two repositories instead of using the exact GitHub URLs provided in the brief.
* **Generic Content / AI Hallucinations:** Added generic backend skill badges (Node.js, Express, MongoDB) that were not in my original brief.
* **Visual Tone:** Good dark mode layout, but contact form lacked client-side submission feedback.

---

## 3. Follow-Up Refinement Prompts & Prompt Log (Step 4)

### Refinement Prompt 1: Correcting Repositories & Removing Hallucinated Skills
> **Prompt:** "Please make two specific updates to the HTML:
> 1. In the Projects section, update the link for Activity 2 to `https://github.com/ayushkulkarni/hello-world` and Activity 4 to `https://github.com/ayushkulkarni/leetcode-solutions`. Make sure all project cards have working 'View Repository' buttons.
> 2. In the Skills section, remove Node.js, Express, and MongoDB. Keep only the skills mentioned in my brief: C, C++, Python, JavaScript, HTML5, CSS3, Git, GitHub, VS Code, GitLens, Live Share, DSA, Version Control, and Pair Programming."

* **What Changed After Prompt 1:** All project cards now feature accurate, explicit GitHub URLs with target `_blank` attributes, and all unrequested/invented backend tech stack badges were removed from the Skills grid.

---

### Refinement Prompt 2: Enhancing Project Details & Adding Interactive Contact Feedback
> **Prompt:** "In the Projects section, expand the card for Activity 3 (GitLens & Live Share) to explicitly mention inline code blame inspection and real-time remote pair programming co-authoring. Also, add a simple JavaScript submission handler on the contact form so that clicking 'Send Message' displays a sleek green success toast notification without reloading the page."

* **What Changed After Prompt 2:** Detailed collaborative features were added to Activity 3's card description, and a smooth JavaScript popup toast was integrated into the contact form submit event.

---

## 4. Reflection (Step 6)

1. **Which prompt produced the biggest improvement?**  
   Refinement Prompt 1 produced the biggest improvement because it eliminated AI-hallucinated skills (like Node.js/MongoDB) and restored exact GitHub repository links for Activity 2 and Activity 4, ensuring 100% alignment with my actual academic work.

2. **What was one thing the AI got wrong?**  
   The AI initially substituted exact repository URLs with generic `#` anchor tags and assumed standard full-stack student skills (inserting backend frameworks not present in the original brief).

3. **How did you identify and correct the issue?**  
   I audited the generated page against my Portfolio Brief checklist, flagged the missing links and extra skill badges, and issued targeted follow-up prompts directing the AI to enforce strict adherence to the brief without manually touching the code.
