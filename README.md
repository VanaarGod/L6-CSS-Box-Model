# CTI-110 L6 — CSS Box Model

Welcome to your sixth web development assignment! Every element on a webpage is really just a box — this assignment is about understanding what's inside that box, and using DevTools to actually *see* it. You'll build a brand new site from scratch and use the Edge Browser Inspector to experiment with the CSS Box Model.

## Step 1: Choose Your Topic

Before you create your repository, pick a topic for your new site. To make sure everyone's project is different, **choose a unique topic** — check with classmates if you're worried about overlap. Here are 10 starter ideas if you need inspiration:

1. A profile page for a fictional band or musician
2. A "planet guide" page for a planet in our solar system
3. A recipe page for your favorite dish
4. A fan page for a video game
5. A page reviewing your top 3 favorite movies
6. A page about a historical event that interests you
7. A "meet the pet" page for a real or imaginary animal
8. A travel guide for a city you'd like to visit
9. A page about a sport or team you follow
10. A "how it's made" page explaining a hobby or craft you enjoy

> ‼️This should be a **new** topic and a **new** repository — don't reuse your L4 or L5 site for this one.

## Step 2: Create Your Repository

1. Go to [GitHub](https://github.com) and log in.
2. Click **New repository**.
3. Name your repository exactly:
   ```
   CTI-110_L6-BoxModel
   ```
4. Set the repository to **Public**
5. Check the box to **Add a README file**.
6. Click **Create repository**.

## Step 3: Clone Your Repository into VS Code

1. Open VS Code.
2. Click Clone Git Repository
3. Select your repository in the dropdown at the top of your screen.
4. Save it within a "GitHub" folder on your computer.
5. When prompted, click **Open** to open the cloned repository folder in VS Code.

> ‼️If you haven't already, navigate to your Extensions Store in VS Code and install "Live Server." You'll know you've found the right one if it has over 81,000,000 downloads!

## Step 4: Create Your Files

1. In the VS Code file explorer (left sidebar), create a new file named:
   ```
   index.html
   ```
2. Create a second new file named:
   ```
   styles.css
   ```
3. On the very first line of `index.html`, type `!` and then press the **Tab** key to generate the HTML boilerplate.
4. Update the `<title>` tag inside the `<head>` section with your **First and Last name**.
5. Link your stylesheet inside `<head>`:
   ```html
   <link rel="stylesheet" href="./styles.css">
   ```

## Step 5: Build Your Page with Semantic HTML

Just like previous assignments, build your `<body>` using semantic elements based on your new topic — **no `<div>` tags allowed**:

- **`<header>`** with an `<h1>`
- **`<nav>`** with a list of links
- **`<main>`** wrapping your primary content
  - At least **two** `<section>` elements
  - At least **one** `<article>` element
  - An **`<aside>`** element
- **`<footer>`**

Add at least **3 classes** and **2 IDs** to elements you plan to style, and include your **2+ images** with `alt` attributes.

## Step 6: Read Up on the Box Model

Before touching your CSS, read through W3Schools' page on the [CSS Box Model](https://www.w3schools.com/css/css_boxmodel.asp). Pay close attention to the diagram showing how **content**, **padding**, **border**, and **margin** stack around each other.

Every single HTML element on a page is a rectangular box made up of these four layers, from the inside out:

1. **Content** — the actual text, image, or other content inside the element.
2. **Padding** — clear space between the content and the border. Padding is "inside" the box — it's the same color/background as the content area.
3. **Border** — a line that wraps around the padding and content.
4. **Margin** — clear space *outside* the border, separating this box from its neighbors. Margin is always transparent.

> ‼️A common mix-up: padding pushes your border outward (making the box bigger), while margin pushes *other elements* away from your box. Neither one changes the content itself.

## Step 7: Inspect the Box Model in Edge

Now let's see the box model in action on your own page:

1. Open your `index.html` with **Live Server** in Microsoft Edge.
2. Right-click any element on the page (like a paragraph or heading) and select **Inspect**. This opens the Edge DevTools panel.
3. With the **Elements** tab selected, click on your element in the HTML panel on the left.
4. In the **Styles** pane on the right, scroll down until you see a small diagram of nested boxes labeled **margin**, **border**, **padding**, and **content** — this is a live view of that element's box model.
5. Try clicking directly on the padding or margin values in that diagram and typing in a new number. Watch how the element resizes on the page in real time.

> ‼️Changes you make in DevTools are **temporary** — they disappear on refresh. Use DevTools to experiment and figure out numbers you like, then copy the final values into your actual `styles.css` file.

## Step 8: Experiment in `styles.css`

Using what you found in DevTools, add `border`, `margin`, and `padding` properties to at least **3 different elements** (using their classes or IDs) in your `styles.css` file. Try out different values and see how the spacing and sizing of your boxes change.

Example:

```css
.topic-section {
  border: 3px solid #4C566A;
  padding: 20px;
  margin: 25px;
}

#main-heading {
  padding: 10px;
  border: 1px solid #88C0D0;
}

article {
  border: 2px dashed #A3BE8C;
  margin: 15px;
  padding: 15px;
}
```

Feel free to continue using your other CSS properties from L5 as well:
`color`, `background-color`, `font-family`, `font-size`, `a:hover`, `a:visited`, `opacity`, `height`, `width`.

## Step 9: Challenge — Match the Shapes and Sizes

Now that you can control the box model, put it to the test. Pick **4 different elements** on your page (they can be `<section>`, `<article>`, `<aside>`, an image, or anything else with a class or ID) and configure them to match the specs below exactly.

> ‼️To make some of these shapes, you'll need one new property not covered yet: `border-radius`. It rounds the corners of a box — a small value (like `10px`) gives soft rounded corners, and a large value (like `50%`) turns a box into a circle or oval.

**Shapes to replicate** — pick 2 of the following and build them using `border`, `width`, `height`, and `border-radius`:

1. **A perfect circle** — equal `width` and `height`, with `border-radius: 50%`.
2. **A rounded rectangle "card"** — a wider-than-tall box with `border-radius` between `10px`–`20px` and a visible `border`.
3. **A pill shape** — a short, wide box where `border-radius` is set to half the box's `height` (e.g., a box that's `40px` tall needs `border-radius: 20px`).
4. **A sharp-cornered square** — equal `width` and `height`, `border-radius: 0`, with a thick `border` (`5px` or more).

**Numerical sizes to match** — pick 2 different elements and give them these *exact* box model measurements:

1. An element that is exactly `300px` wide, `150px` tall, with `20px` of `padding` and a `5px` solid `border`.
2. An element with `10px` of `padding`, `30px` of `margin`, and a `3px` `border` — no fixed `width` or `height`, so its size comes only from its content plus the box model.

Use the Edge Inspector's box model diagram from Step 7 to double-check your actual rendered numbers match what's requested — remember that `padding` and `border` add to an element's visible size on top of its `width` and `height`.

> ‼️Label each of your 4 challenge elements somewhere on the page (like a small caption or heading) so it's clear to your instructor which element is which shape/size.

## Step 10: Test Your Page

Test your site using the **Live Server** extension:

1. Right-click your `index.html` file in the VS Code file explorer.
2. Select **"Open with Live Server."**
3. Confirm your border, margin, and padding changes look correct in the browser tab that opens.

## Step 11: Submit Your Work with Git

Once your page looks correct, submit it using Git:

1. Open a new **Terminal** in VS Code.
2. Run the following commands one at a time:

```bash
git add .
git commit -m "COMMIT MESSAGE GOES HERE"
git push
```

> ‼️Replace `"COMMIT MESSAGE GOES HERE"` with a short, descriptive message about what you did (e.g. `"Completed Box Model assignment"`).

## Step 12: Publish Your Site with GitHub Pages

Once your work is pushed to GitHub, turn your repository into a live website:

1. On GitHub, go to your `CTI-110_L6-BoxModel` repository page.
2. Click the **Settings** tab.
3. In the left sidebar, click **Pages**.
4. Under **Build and deployment**, set the **Source** to **Deploy from a branch**.
5. Under **Branch**, select **main** (or **master**) and keep the folder set to **/ (root)**.
6. Click **Save**.
7. Wait a minute or two, then refresh the Pages settings screen. GitHub will display a link like:
   ```
   https://your-username.github.io/CTI-110_L6-BoxModel/
   ```
8. Click the link to view your live site.

> ‼️Every time you `git push` new changes, GitHub Pages will automatically update your live site within a minute or two.

> ‼️GitHub Pages defaults to render your README.md file unless it finds an "index.html" file in the root folder. Always make sure your home page is set to "index.html"! This is case sensitive.

---

### Checklist Before You Submit
- [ ] Chose a **unique** topic (not reused from a previous assignment)
- [ ] Repository `CTI-110_L6-BoxModel` created on GitHub
- [ ] Repository cloned into VS Code
- [ ] `index.html` and `styles.css` files created inside the cloned repo
- [ ] HTML boilerplate generated with `!` + `Tab`
- [ ] `<title>` updated with your First and Last name
- [ ] `./styles.css` properly linked inside `<head>`
- [ ] Page built with semantic elements (`header`, `nav`, `main`, `section` x2, `article`, `aside`, `footer`) — **no `<div>` tags**
- [ ] At least 3 classes and 2 IDs added to HTML elements
- [ ] At least 2 images included, each with an `alt` attribute
- [ ] Read the W3Schools Box Model article
- [ ] Inspected at least one element in Edge DevTools and viewed its box model diagram
- [ ] `border`, `margin`, and `padding` applied to at least 3 different elements in `styles.css`
- [ ] Challenge: 2 shapes replicated (circle, rounded rectangle, pill, or sharp square) using `border-radius`
- [ ] Challenge: 2 elements matched to the exact numerical padding/border/width/height/margin specs
- [ ] Challenge elements labeled/captioned on the page
- [ ] Page tested with Live Server
- [ ] Work committed and pushed with Git commands in the VS Code Terminal
- [ ] GitHub Pages enabled in repository Settings
- [ ] Live site link verified and working
- [ ] ‼️YOU MUST SUBMIT CLICKABLE LINKS TO YOUR GITHUB REPOSITORY AND YOUR LIVE SITE THROUGH GITHUB PAGES. 2 LINKS. BOTH CLICKABLE OR YOU WILL RECEIVE A ZERO.
