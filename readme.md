view:- https://quote-slider-ruddy.vercel.app/

📄 Quote Slide Documentation

🔸 Overview
This is a web-based Quote Slider that cycles through inspirational quotes, each with an author photo, name, and quote text. The design uses glassmorphism aesthetics with smooth transitions and border framing.


📁 File Structure
This is a single-file implementation:

HTML: Markup structure of the page.
CSS: Styling for the background, layout, and quote cards.
JavaScript: Logic for transitioning between quotes.

1. HTML Structure

Each quote block contains:
.author-img: Author's circular image.
.quote-title: Static text "Quotes".
.quote-text: The main quote.
.quote-author: The author’s name in italics and aligned right.

2. CSS Styling
Background: Linear gradient (purple to blue).
Centered content using Flexbox.
Height set to 542px.
Bordered using a ::before pseudo-element for aesthetic framing.

🔷 .frame
Provides an additional border container with rounded corners (top-right & bottom-left).

Glassmorphism effect using semi-transparent borders.

🔷 .quote-container
Width: 700px, Height: 280px.
Padding left for image space.
Rounded corners.
Glass effect: rgba(255, 255, 255, 0.1) background + box-shadow.
Initially hidden: opacity: 0; display: none.
Shown when .active: opacity: 1; display: block.

🔷 .author-img
Positioned top-left inside quote block.
Circular (border-radius: 50%).
White border for definition.

🔷 Typography
.quote-title: Bold, large font for heading.
.quote-text: Main quote, white font.
.quote-author: Italic and aligned to the bottom-right of the quote block.


3. JavaScript Functionality

✅ What it does:
Selects all .quote-container elements.
Starts with the first quote.
Every 4 seconds, hides the current quote and shows the next.
Loops back to the first quote after reaching the end.
