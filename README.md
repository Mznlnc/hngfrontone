https://github.com/Mznlnc/hngfrontone.git
# 🌟 Accessible Profile Card Component

A responsive, accessible **Profile Card** built with semantic **HTML**, modern **CSS (Flexbox/Grid)**, and lightweight **vanilla JavaScript**.  
This project meets accessibility, responsiveness, and automation-testing requirements — each visible element includes a `data-testid` attribute for stable UI tests.

---

## 🚀 Live Demo
**[👉 View on GitHub Pages]([https://github.com/Mznlnc/hngfrontone.git])**  
(After you enable GitHub Pages in your repo settings, this link will go live.)

---

## 📁 Project Structure
profile-card/
├── index.html
├── avatar.png
├── README.md
└── (optional CSS/JS folders)

yaml
Copy code

---

## ⚙️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/Mznlnc/hngfrontone.git
cd profile-card
2. Run Locally
You can open the project directly in a browser:

bash
Copy code
open index.html
# or double-click index.html
No build tools are required — it’s 100 % static HTML/CSS/JS.

3. Optional: Serve Locally
If you prefer a lightweight local server:

bash
Copy code
# Using Python
python3 -m http.server 8000
# or using Node (http-server package)
npx http-server .
Then open:
👉 http://localhost:8000/

🧠 Accessibility Checklist
Requirement	Status	Notes
Semantic HTML structure (<article>, <header>, <section>, <nav>, <figure>)	✅	Fully implemented
Each visible element has data-testid attribute	✅	For automation tests
All images have descriptive alt text	✅	alt="Profile photo of ..."
All interactive links are keyboard-focusable	✅	Proper <a> tags with focus states
Sufficient color contrast	✅	Meets WCAG AA contrast
Responsive at mobile, tablet, and desktop widths	✅	Tested with flex and media queries
Descriptive aria-labels for landmarks	✅	e.g., <nav aria-label="User social links">

🧩 Testing Guidelines
Automated Tests (Example using Jest + @testing-library)
js
Copy code
import { getByTestId } from '@testing-library/dom'

const card = document.querySelector('[data-testid="test-profile-card"]')
expect(getByTestId(card, 'test-user-name').textContent).not.toBe('')
expect(getByTestId(card, 'test-user-time')).toBeTruthy()
Manual Testing
 Verify all elements exist with their data-testid attributes

 Ensure test-user-time shows Date.now() in ms (updating as expected)

 Tab through the page — keyboard navigation must work

 Resize window (mobile → tablet → desktop) for responsive layout

 Confirm social links open in new tabs (target="_blank", rel="noopener noreferrer")

🧑‍💻 Technical Notes
HTML: Semantic tags for structure & accessibility

CSS: Flexbox + media queries for responsiveness

JavaScript: Simple Date.now() update logic

Hosting: GitHub Pages, Netlify, or any static server

🌍 Deployment (GitHub Pages)
Go to your GitHub repo → Settings → Pages

Under Build and deployment, choose:

Source: Deploy from a branch

Branch: main

Folder: /(root)

Click Save

Your site will appear at https://mznlnc.github.io/profile-card/ within a minute.

🧾 Data-TestIDs Reference
Element	Data Test ID
Root container	test-profile-card
User name	test-user-name
Biography	test-user-bio
Current time (ms)	test-user-time
Avatar image	test-user-avatar
Social links container	test-user-social-links
Social links (e.g., Twitter)	test-user-social-twitter
Hobbies list	test-user-hobbies
Dislikes list	test-user-dislikes

🛠️ Future Enhancements
Add image-upload functionality for avatar

Include dark/light-mode toggle

Integrate automated accessibility tests (e.g., axe-core)

Support dynamic user data from JSON or API

📬 Contact
Author: Njoagwuani Emeka Martins
📧 emekamartins98@gmail.com
🌐 linkedin.com/in/emeka-martins-njoagwuani
💻 github.com/mznlnc
