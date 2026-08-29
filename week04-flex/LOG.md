# Lab 4 — Error Log

PATRICK BOMA
**Lab Session:** [Time, 10:16 am -03:23a m]

---

## Error 1

Task I was working on: Task 2

**What I was trying to do:**
Show an image inside my `.clearfix` div using `<img src="Screenshot 2026-08-22 183207.png">`.

**The exact error or problem I saw:**
Image didn't show — broken image icon, blank space where it should be.

**Steps I took to fix it:**
1. Compared the folder location of `index.html` and the image in VS Code's Explorer.
2. Found the image was outside the `week04-flex` folder, `index.html` was inside it.
3. Moved the image into `week04-flex`, refreshed — image loaded.

**What I learned from this:**
An `<img src="...">` path is relative to the HTML file's location, not the whole project folder.

---

## Error 2

**Task I was working on:** Task 3

**What I was trying to do:**
Test my media queries at 500px using Chrome DevTools' device toolbar.

The exact error or problem I saw
Typed 500 into the width field, but the layout still showed 2 columns instead of 1.

Steps I took to fix it
1. Double-checked my `min-width: 600px` / `900px` breakpoints — they were correct.
2. Noticed my `<head>` had no viewport meta tag.
3. Added `<meta name="viewport" content="width=device-width, initial-scale=1.0">`, refreshed — layout snapped to 1 column correctly.

**What I learned from this:**
Without a viewport meta tag, the browser lays the page out at a fixed ~980px width and just scales the image down, so media queries don't match the number typed into DevTools.
