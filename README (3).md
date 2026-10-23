# 9709 Workbook

A free revision website for **Cambridge International AS & A Level Mathematics (9709)**. It has notes, worked examples, exam-style practice questions with step-by-step solutions, and a downloadable formula sheet for each paper.

The whole site is a single HTML file: `9709-maths-workbook.html`. Nothing needs installing.

---

## What's inside

| Paper | Name | Level | Topics | Questions |
|---|---|---|---|---|
| Paper 1 | Pure Mathematics 1 (P1) | AS | 8 | 49 |
| Paper 5 | Probability & Statistics 1 (S1) | AS | 5 | 29 |
| Paper 4 | Mechanics (M1) | AS | 5 | 30 |
| Paper 3 | Pure Mathematics 3 (P3) | A Level | 9 | 54 |
| Paper 6 | Probability & Statistics 2 (S2) | A Level | 5 | 30 |
| | **Total** | | **32** | **192** |

Each topic has:

- **Notes**: the key ideas, with formulas in highlighted boxes, exam tips and common mistakes
- **Two worked examples**, each with a full solution
- **3–5 practice questions**, each with a mark allocation, step-by-step solution and final answer. Many also have a hint.

### Topics

**Pure Mathematics 1:** Quadratics · Functions · Coordinate Geometry · Circular Measure · Trigonometry · Series · Differentiation · Integration

**Probability & Statistics 1:** Representation of Data · Permutations & Combinations · Probability · Discrete Random Variables · The Normal Distribution

**Mechanics:** Forces & Equilibrium · Kinematics in a Straight Line · Momentum · Newton's Laws of Motion · Energy, Work & Power

**Pure Mathematics 3:** Algebra · Logarithms & Exponentials · Trigonometry · Differentiation · Integration · Numerical Solution of Equations · Vectors · Differential Equations · Complex Numbers

**Probability & Statistics 2:** The Poisson Distribution · Linear Combinations of Random Variables · Continuous Random Variables · Sampling & Estimation · Hypothesis Tests

Paper 2 (Pure Mathematics 2) is not covered.

---

## Features

- **AS Level and A Level tabs**, with each paper in its own tab and a topic list down the side
- **Formula sheets** for every paper:
  - A ★ marks formulas that are **not** in the official MF19 list of formulae, so you know which ones to memorise
  - The S1 and S2 sheets include a full Φ(z) normal distribution table and critical values
  - **Download** saves the sheet as an HTML file that works offline
  - **Print or save as PDF** prints the sheet on its own
- **Show hint / Show solution** buttons on practice questions, so you can try each one first
- **Progress tracking**: tick "I can do this" on a question and the topic list shows how many you've done
- **Random question** picks a question you haven't ticked yet
- **Search** across every topic and question
- **Dark mode**, and a layout that works on phones

---

## How to use it

1. Download `9709-maths-workbook.html`.
2. Double-click it to open it in any modern browser (Chrome, Edge, Firefox or Safari).

Things to know:

- **You need an internet connection** to see the maths symbols. They're drawn by KaTeX, which loads from the internet. If it can't load, a yellow banner appears at the top. Downloaded formula sheets work fully offline.
- **Progress is saved in your browser only.** It doesn't sync between devices. Clearing your browser's site data, or using a private window, resets it.

---

## Put it online for free

### GitHub Pages

1. Make a free account at [github.com](https://github.com) and create a new **public** repository, for example `9709-workbook`.
2. Rename `9709-maths-workbook.html` to **`index.html`**, then upload it and this `README.md` with **Add file → Upload files**.
3. Go to **Settings → Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, choose the **main** branch and the **/ (root)** folder, then click **Save**.
4. After a minute or two, the site is live at `https://<your-username>.github.io/9709-workbook/`.

### Netlify

Make a free account at [netlify.com](https://www.netlify.com), put `index.html` in a folder, and drag the folder onto the Netlify Drop page. You get a public link straight away.

---

## Linking straight to a page

Add a name after `#` at the end of the site's address. For example, `https://<your-site>/#p3.complex` opens P3 Complex Numbers.

| Page | Link name |
|---|---|
| Home | `#home` |
| AS Level / A Level | `#as-level` / `#a-level` |
| Formula sheets | `#formula-sheets` |
| A whole paper | `#p1`, `#s1`, `#m1`, `#p3`, `#s2` |

<details>
<summary>Link names for every topic</summary>

| Paper | Topic link names |
|---|---|
| P1 | `p1.quadratics` `p1.functions` `p1.coordinate` `p1.circular` `p1.trig` `p1.series` `p1.differentiation` `p1.integration` |
| S1 | `s1.data` `s1.perms` `s1.probability` `s1.drv` `s1.normal` |
| M1 | `m1.forces` `m1.kinematics` `m1.momentum` `m1.newton` `m1.energy` |
| P3 | `p3.algebra` `p3.logs` `p3.trig3` `p3.diff3` `p3.int3` `p3.numerical` `p3.vectors` `p3.de` `p3.complex` |
| S2 | `s2.poisson` `s2.linear` `s2.crv` `s2.sampling` `s2.hypothesis` |

</details>

---

## Editing or adding questions

All the content is inside the HTML file, in the `<script>` block near the bottom. Open the file in a text editor such as VS Code or Notepad++, not Word.

- `DATA.p1`, `DATA.s1`, `DATA.m1`, `DATA.p3` and `DATA.s2` hold each paper's topics.
- `FORMULAS.p1` and so on hold the formula sheets.

Each topic looks like this:

```js
{id:'quadratics', title:'Quadratics', sum:'One-line summary',
 notes:R`<h4>Heading</h4><p>Notes with maths like $b^2-4ac$</p>`,
 ex:[ /* worked examples */ ],
 pr:[ /* practice questions */ ]}
```

Each question looks like this:

```js
{m:3,                                    // marks
 q:R`Solve $x^2-5x+6=0$.`,               // question
 h:R`Factorise.`,                        // hint (optional)
 s:[R`$(x-2)(x-3)=0$`, R`So $x=2$ or $x=3$.`],  // solution steps
 a:R`$x=2$ or $x=3$`}                    // final answer
```

Tips for writing content:

- Maths is written in **LaTeX**: `$...$` inside a sentence, `$$...$$` on its own line.
- Text is wrapped in `` R`...` ``, so type each backslash once: `\frac`, not `\\frac`.
- Don't type `${` anywhere in the text, because it breaks the file. If you need `$` followed by `{`, put a small space in between: `$\,{}^nC_r$`.
- Use `\lt` and `\gt` instead of `<` and `>` inside maths.
- In formula sheets, each row is `[label, formula, star]`. Use `1` for the star if the formula is not in MF19, and `0` if it is.

After editing, open the file in your browser and check the topic you changed.

---

## Conventions

- In Mechanics, $g = 10\ \text{m s}^{-2}$.
- Non-exact answers are given to 3 significant figures, and angles in degrees to 1 decimal place, as Cambridge expects unless a question says otherwise.

---

## Disclaimer

The questions are original. They're written in the style of Cambridge 9709 past papers but aren't copied from any paper, so practise with real past papers too.

This site is not affiliated with or endorsed by Cambridge University Press & Assessment. Always check the current 9709 syllabus and the MF19 list of formulae for your exam series.
