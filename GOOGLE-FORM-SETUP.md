# "Get First Dibs" Interest Form — Google Forms Setup

Purpose: replace the fake email-only box on the site with a short form that both builds your launch list AND tells you who your customer is — what they drive, which design they want, and what they'd pay. Every response lands in a Google Sheet you can sort/filter/chart.

Takes about 2 minutes to build.

## Step 1 — Create the form

1. Go to **forms.google.com** (signed in as adamarchila@gmail.com) → **Blank form**.
2. Title: **Son of a Hitch — Get First Dibs**
3. Description: **Tell us a bit about your rig and we'll make sure your first hitch cap actually fits your life. Takes 60 seconds.**

## Step 2 — Add these questions, in order

**1. Email**
- Type: Short answer
- Turn on **Response validation → Text → Email address** (keeps out typos/junk)
- Required: Yes

**2. What should we call you?**
- Type: Short answer
- Required: No

**3. What do you drive?**
- Type: Multiple choice
- Options: `Truck` / `SUV or crossover` / `Jeep or off-road rig` / `Van` / `Something else`
- Required: Yes

**4. Which collection speaks to you?**
- Type: Checkboxes (allows more than one)
- Options: `The Trailhead — outdoors & hunting` / `Old Glory — patriotic` / `The Punchline — funny` / `Heads-Up — useful & safety` / `Not sure yet`
- Required: Yes

**5. How many would you probably grab?**
- Type: Multiple choice
- Options: `Just one for me` / `2–3 — outfitting my whole fleet` / `4+ — hooking up my friends too`
- Required: No

**6. What would feel like a fair price for one hitch cap?**
- Type: Multiple choice
- Options: `Under $15` / `$15–$25` / `$25–$40` / `$40+`
- Required: Yes — *(this is the key price-point signal — keep it required)*

**7. Anything else you want us to know?**
- Type: Paragraph
- Required: No

## Step 3 — Connect it to a Sheet

1. In the form editor, click the **Responses** tab → the green Sheets icon → **Create a new spreadsheet**. Name it `Son of a Hitch — Interest Form Responses`.
2. Every submission now appears as a row automatically. Once you have responses, you can pivot column F (price) against column D (collection) or column C (vehicle) to see what different customer segments will pay.

## Step 4 — Get the link and send it back

1. Click **Send** (top right) → the link icon (🔗) → check **Shorten URL** → **Copy**.
2. Send me that link (looks like `https://forms.gle/xxxxxxx`) and I'll wire the site's "Get First Dibs" button to open it, so the whole flow is live.

## Optional polish (not required)

- **Settings → Presentation**: write a custom "Thanks!" confirmation message, e.g. *"You're on the list. Welcome to the family. 🤝"* — matches the site's existing success message.
- **Settings → Responses → Get email notifications for new responses** — so you know the moment someone signs up.
- Theme color: click the palette icon (top right) and set it close to your brand's blaze orange (`#e8531f`) so the form doesn't feel totally disconnected from the site, even though it'll still look like a Google Form.
