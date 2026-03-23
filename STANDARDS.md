
**Framework:** No framework — vanilla CSS only  

**Architecture:**  
- Static site, single `index.html` in root  
- All images in `/images` folder, referenced by relative path  
- Resume is **not linked or embedded**  

**Responsiveness:**  
- Fully responsive from 320px and wider  
- No horizontal scrolling  

**Accessibility — WCAG 2.2 Level AA:**  
- `<img>` elements must have descriptive `alt` text  
- Color contrast minimum 4.5:1 for normal text, 3:1 for large text  
- Logical heading hierarchy: `<h1>` → `<h2>` → `<h3>`  
- Descriptive links only — no “click here” or bare URLs  
- Page `<title>` descriptive  
- All interactive elements keyboard navigable  

**Compatibility:**  
- Chrome, Safari, Firefox; mobile responsive from 375px width  

**Security:**  
- External links open in new tab (`target="_blank"` with `rel="noopener noreferrer"`)

---

## 3. Design Standards
**Color palette:**

| Role                | Hex Code | Usage |
| ------------------- | -------- | ------------------------------------- |
| Background          | #F8F9FA  | Page background |
| Primary text        | #212529  | Body text |
| Accent              | #0D6E6E  | Section headings, links, skill tags |
| Secondary background| #E9ECEF  | Section/card backgrounds |

**Typography:**  
- Heading font: Inter (Google Fonts)  
- Body font: Inter  
- Body size: 16px, line height 1.6  
- H1 (full name): 1.5rem, bold  
- H2 (section headings): 1.25rem, bold, accent color  

**Imagery:**  
- Professional headshot only, circular crop, ~160px, centered in hero section  
- No stock photos, emojis, or clip art  

**Layout:**  
- Max content width 800px, centered  
- Single column on mobile, two-column for project cards on desktop  
- Generous whitespace; ~60px top/bottom padding per section  

**Component styles:**  
- Skill tags: rounded pill badges; accent background for technical, secondary background for interpersonal skills  
- Contact links: labeled icons opening in new tab (LinkedIn, GitHub, Email)  
- Navigation links: plain text, accent color on hover, no underline  

**Tone:**  
- Three words: Professional, Approachable, Data-driven  
- Writing tone: First person, direct, confident. Avoid buzzwords like “passionate” or “synergy.”  

**Reference sites:**  
- `read.cv` — simplicity, whitespace  
- `brittanychiang.com` — section hierarchy, light background only  

_Remember: this document is a living artifact. Update it as needed._
