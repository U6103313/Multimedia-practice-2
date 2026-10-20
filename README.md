# CV Website – Júlia Ferrer Puig

Hypermedia project, Part 1: design and development of a single-page website that shows a Curriculum Vitae and a small portfolio.

The CV belongs to a fictional professional, **Júlia Ferrer Puig**, a front-end developer and UX designer. All names, links and contact details are examples.

## Links

- **Live website:** https://u6103313.github.io/Multimedia-practice-2/
- **Figma project:** https://www.figma.com/design/aP7jTOo3BVPSoGMGqAVVO1/Sin-t%C3%ADtulo?node-id=0-1&t=va8IvEIVc4X5HiyF-1

## 1. Project analysis

### 1.1 User profile

The website is designed mainly for recruiters and hiring managers who need to evaluate a candidate quickly. A secondary user is a small-business owner looking for a freelance web designer.

#### Primary persona

| | |
|---|---|
| **Name** | Marta Soler |
| **Age** | 38 |
| **Job** | Talent Acquisition Specialist at a technology consultancy in Barcelona |
| **Context** | Reviews 30–50 candidates per week and spends about 60–90 seconds on each CV in a first screening. Works mostly on a laptop. |
| **Goals** | Understand who the candidate is, what technologies they use and how much experience they have. Check real projects. Find a clear way to get in touch. |
| **Frustrations** | Slow or cluttered websites, key information hidden behind menus, heavy PDFs, and portfolios with no explanation of what the person actually did. |
| **What she expects to find** | Name and role at the top, a short summary, experience in reverse chronological order, visible skills, linked projects and a clear contact option. |


#### Secondary persona

**Laia Vidal, 45**, owns a restaurant in Olot and wants a new website. She is not technical. She wants to see examples of similar work (restaurants and shops), understand quickly if the designer is reliable, and find an easy way to contact them. This is why the freelance experience and the projects have a visible place on the page.

### 1.2 Information architecture

The CV is a single page organised for fast scanning, because the main user spends only a short time on a first review. The page has three zones: header, main content and footer.

**Header.** It answers the question "who is this person?" in a few seconds. The name appears in the largest size on the page, with the job title below it, next to a photo and a summary card with a short pitch, the location and the age. The essential identity is placed at the very top, where the eye lands first.

**Main content, in two columns.** The wide left column (about two thirds of the width) tells the professional story in the order a recruiter looks for it: Education, Experience and Selected Projects. Inside each section, entries follow reverse chronological order, so the most recent information comes first. Experience entries include short bullet points with concrete numbers (pages designed, components reused), which makes the claims easy to verify. Projects close the column, each with a short description, the technologies used and a "View project" button that links to its repository.

The narrower right column contains supporting information that works as a quick checklist: Skills grouped by Design, Frontend and Tools; Languages with their level; and an "Outside the screen" block about photography and music, which adds personality without competing with the professional content.

**Footer.** Contact details, professional profiles (LinkedIn and GitHub) and a "Contact" button are placed at the end, so a reader who has been convinced can act immediately.

Everything is grouped into cards with a small blue section title, so each block can be identified at a glance and the text in each one stays short. On smaller screens the columns stack in the same order.

### 1.3 Visual design

The visual style is calm, editorial and professional. The aim is to put the content first and let a few clear decisions create the hierarchy.

**Colour palette.** It combines warm neutrals with one blue accent. Ivory (`#F5F3ED`) is the page background and white (`#FFFFFF`) is used for the cards, which creates a soft contrast without shadows. Ink (`#20211F`) is the main text colour, medium grey (`#66675F`) is used for secondary text such as descriptions, dates and universities, and light grey (`#C8C9C0`) for borders and separators. Blue (`#294FDB`) is reserved for section titles and buttons, so it always signals "where am I" or "what can I click".

**Typography.** Two families are used. *Inter* (Regular, Medium and Semi Bold) is used for reading text and headings because it is clean and legible on screen. *IBM Plex Mono* (Regular, 11 px) is used for metadata: section labels, dates, technologies, languages levels, links and contact data. This gives the page a subtle technical touch that suits a developer's CV. The hierarchy is clear: 56 px for the name, 28 px for the highlighted phrase, 21 px for entry titles and 20 px for the job title, down to 15, 14, 13, 12 and 11 px for the rest of the text.

**Layout.** A grid with a wide main column and a narrow side column, with a constant 24 px spacing between blocks. Cards have a thin 1 px border and small rounded corners, and there are no shadows or decorative elements.

**Design system.** In Figma, colours and type sizes are stored as variables in two collections: base colours and semantic colours (for example *text/primary* or *button/primary-background*). The CSS mirrors them as custom properties in `:root`, so the design can be changed in a single place.


## 2. Technologies

- **HTML** and **CSS** only. The website is a single static page with simple content.
- **Google Fonts** to load Inter and IBM Plex Mono.
- **CSS custom properties**, **CSS Grid** and **Flexbox** for the layout.
- **Responsive design** with two breakpoints (900 px and 600 px). On tablets the columns stack, and on phones the header becomes a single column.

## 3. Project structure

```
├── index.html
├── styles.css
├── images/
│   └── JuliaCV.jpg
└── README.md
```