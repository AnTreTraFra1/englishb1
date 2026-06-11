# Exam Presentation: Elea / Velia — The Website and the Archaeological Site

**Duration:** ~20 minutes  
**Speaker:** Andrea Iannuzzelli  
**Course:** Informatica B1.3, UNISA

---

## 1. Introduction (2 min)

Good morning everyone. Today I'm going to present my project: a website about the ancient Greek city of Elea, also known as Velia. This is an educational website I created for my English exam, and I will also tell you about the real archaeological site that the website describes.

First, let me give you a quick overview. The website has five pages: a Home page, History, The Site, Philosophy, and a Visit page. It is a static HTML and CSS website, so just pure code.

Elea was a Greek city founded in 540 BC on the coast of Campania, in southern Italy. Today it is an archaeological park near the town of Ascea Marina. It is a UNESCO World Heritage site and one of the most important Greek settlements in Italy.

---

## 2. The Website — Technical Choices (3 min)

The design uses a warm, earthy colour palette inspired by the Mediterranean landscape:

- Brown and terracotta tones to reflect the ancient ruins
- Olive green to represent the natural environment of the Cilento National Park
- Gold accents to evoke the legacy of Greek philosophy

The typography uses two Google Fonts: Playfair Display for headings — a serif font that gives a classical, elegant feel — and Open Sans for body text, which is clean and readable.

The layout is fully responsive. I used CSS Grid and Flexbox to create a layout that adapts from desktop to tablet to mobile. There is a hamburger menu on small screens, and the card grids reflow automatically.

I also added some subtle animations: the hero background gradients shift slowly, giving a sense of depth, and cards have a hover effect that lifts them slightly.

One thing I want to highlight: the images on the site are not mine. They come from Wikimedia Commons and are licensed under Creative Commons. This is important to remember when building any website — you must respect copyright and use properly licensed content.

---

## 3. The Content — What the Website Describes (5 min)

Now let me walk through the actual content of the website.

### Home Page

The home page introduces Elea / Velia and gives three main topics: ancient history, philosophy, and archaeology. It explains that Elea was the Greek name and Velia was the Roman name. The city is located on a promontory between two rivers, the Palistro and the Fiumarella. In ancient times it had two harbours. Today, the coastline has changed and the ancient harbours are now inland.

### History Page

The history page uses a timeline structure. Let me highlight the key events:

- **540 BC** — Foundation. Greek people from Phocaea, modern-day Turkey, escaped the Persian invasion. They fought a naval battle near Alalia in Corsica against the Etruscans and Carthaginians. After the battle, they moved south and founded Elea.
- **5th Century BC** — The golden age. The city grew as a trade centre. Parmenides founded the Eleatic School and gave the city a constitution.
- **4th Century BC** — Porta Rosa was built, connecting the northern and southern parts of the city.
- **273 BC** — Alliance with Rome during the Punic Wars.
- **88 BC** — Velia became a Roman municipium. Famous Romans visited, including Cicero and Horace.
- **1st to 5th Century AD** — Decline due to flooding and soil erosion.
- **1927 to today** — Rediscovery and excavations.

The page also talks about a major discovery in 2022: an archaic temple of Athena with three bronze helmets, which are the first physical evidence of the Battle of Alalia.

### The Site Page

This page describes the main monuments you can see at the archaeological park:

- **Porta Rosa** — The most famous monument. It is not a gate but a viaduct with a semicircular arch, built in the 4th century BC. It is one of the oldest arch bridges in the world. It was discovered in 1964 by Mario Napoli, who named it after his wife Rosa.
- **The Acropolis** — The highest part of the city with a temple of Athena, a medieval tower, and a chapel.
- **The Theatre** — Could hold about 2,000 spectators, built into the hillside.
- **The Baths** — Two complexes: a Hellenistic public bath and a larger Roman bath with a sophisticated heating system.
- **The Agora and Quarters** — The public square and residential areas, including an archaic quarter with a regular street grid.
- **The 2022 Discovery** — The helmets from the Battle of Alalia, now in the exhibition "Exiles and Victors".

### Philosophy Page

This page covers the Eleatic School:

Parmenides was born in Elea around 515 BC. His main idea is that reality is one, eternal, and unchanging. Change is an illusion — our senses deceive us. True reality can only be understood through reason.

Zeno, his student, created famous paradoxes. The most famous is "Achilles and the Tortoise": if the tortoise starts with a small advantage, Achilles can never catch it, because every time he reaches the tortoise's position, it has moved forward. This creates an infinite series.

These ideas influenced Plato and Aristotle. Zeno's paradoxes are still relevant in modern mathematics, especially in calculus and the study of infinity.

### Visit Page

This is a practical page for tourists, with information about location, opening hours, tickets, and how to get there by car, train, or bus.

---

## 4. Technical Details — How the Site Works (3 min)

Let me go deeper into the technical implementation.

The entire site is a single-page application in spirit, though technically it is five separate HTML files sharing one CSS file. This keeps the code clean and maintainable.

The CSS is organized with custom properties at the root level. This means I define colours, shadows, and spacing once and reuse them throughout. If I want to change the primary colour, I change it in one place.

The navigation bar is fixed at the top and uses a blur effect with backdrop-filter. On mobile, the menu is hidden and can be toggled with a simple JavaScript one-liner.

The hero sections on each page use different gradient backgrounds. Each gradient has an animation that shifts the background position over 15 to 20 seconds. This creates a subtle moving effect that catches the eye without being distracting.

The content sections use a two-column grid layout. On mobile, this collapses to a single column. The images are set to object-fit: cover, which means they fill their container while maintaining their aspect ratio.

I also added a timeline on the history page using pure CSS — a vertical line with dots, no JavaScript required.

The card layout uses auto-fit with a minimum width, so the number of columns adjusts automatically based on the screen size.

---

## 5. The GitHub Actions Workflow (1 min)

I also set up a CI/CD pipeline using GitHub Actions. Every time I push new code to the master branch, the workflow automatically deploys the site to GitHub Pages.

The workflow is simple: it checks out the code, configures Pages, uploads the files as an artifact, and deploys them. Since it is a static site with no build step, it takes only about 30 seconds.

This is a good example of modern DevOps practice — even for a small project, automation saves time and reduces errors.

---

## 6. Challenges and Lessons Learned (2 min)

Building this project taught me several important lessons.

First, working with images from external sources requires attention to licensing. I had to find images that were freely usable and give proper attribution. This is a skill that is useful for any web developer.

Second, designing a responsive layout from scratch without a framework is more work, but it gives you full control. I learned a lot about CSS Grid, Flexbox, and media queries.

Third, the content itself was interesting to research. I read about Greek philosophy, archaeology, and ancient history. This reminded me that a website is not just about code — it is about communicating information effectively.

One challenge was the gradient hero animations. Getting the colours to blend smoothly across different screens required some experimentation with background-size and animation timing.

Another challenge was the timeline layout. Making it look good on both desktop and mobile required careful use of padding and relative positioning.

---

## 7. Conclusion (2 min)

To conclude, this project combines two of my interests: web development and history. The website is a simple but effective presentation of the archaeological site of Elea / Velia.

Technically, it uses pure HTML and CSS with responsive design, custom properties, and subtle animations. It is deployed automatically through GitHub Actions.

The content covers over 2,500 years of history — from the Greek foundation in 540 BC, through the Roman period, to the modern archaeological park and the latest discoveries.

If you are interested in visiting, the park is in Ascea Marina, about 100 km south of Salerno. The ticket also includes Paestum and is valid for three days.

Thank you for your attention. I am happy to answer any questions.

---

## 8. Possible Questions (for Q&A)

Here are some questions the examiner might ask and suggested answers:

**Q: Why did you choose this topic?**  
A: I have always been interested in ancient history, and when I discovered that a Greek city existed in Campania with such a rich philosophical tradition, I thought it would make a great topic for a website.

**Q: What would you add to the website in the future?**  
A: I would like to add an interactive map, a gallery with more images, and possibly an audio guide in English and Italian.

**Q: Did you use any JavaScript frameworks?**  
A: No, the site is pure HTML and CSS with only one line of JavaScript for the mobile menu. I wanted to keep it simple.

**Q: How long did it take to build?**  
A: The development took about two weeks, including research, design, and writing the content.

**Q: Is the site accessible?**  
A: I used semantic HTML, alt text for images, and good colour contrast, but there is room for improvement, like adding ARIA labels and keyboard navigation enhancements.

**Q: How does the responsive design work?**  
A: I used CSS Grid with auto-fit and minmax for the card layouts, media queries for the navigation and content sections, and relative units for typography and spacing.

---

*Good luck with your exam!*
