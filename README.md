# Trick-or-Treat Bingo

A bingo card for trick-or-treaters in The Wedge run by the LHENA Volunteer Network (LVN).

**Play:** https://bingo.thewedge.org

## How it works

1. Enter your name and email to get a card.
2. Tap a square when you spot it during your rounds. Tap again to uncheck it.
3. Get five in a row, column, or diagonal for a bingo. The center square is free. You can earn more than one bingo.
4. Tap **Review & submit my card**. A Google Form opens with your name, bingo count, and checked squares filled in.
5. Upload your photos and press **Submit** in the form. Your entry only counts once you submit the form.

## Notes

- **Your card comes from your email.** The same email always gives the same card, on any device. Different emails give differently shuffled cards.
- **Checked squares are not saved until you submit.** Reloading the page before then clears them.
- **One entry per person.** This browser remembers if you already submitted and disables the button. The one-response limit is enforced by the Google Form, not this page.
- **Photos are what are evaluated to determine bingos.** The page does not verify anything. Photos go to the form, not to this site.
- **Your email stays in your browser.** The page uses it to build your card and to remember that you submitted. It is not sent to the form. Only your name, bingo count, and checked squares are.
- **Fonts load from Google Fonts**, so visiting the page makes a request to Google.

## For maintainers

The site is one file, `index.html`, with no build step or dependencies. It is hosted on GitHub Pages at the custom domain in `CNAME`.

| To change | Edit in `index.html` |
|---|---|
| Bingo squares | `ITEMS` array. It must keep at least 24 entries. Every card draws 24 of them. |
| Google Form | `FORM_BASE` (form URL) and `ENTRY` (the form's field IDs for name, bingo count, and squares) |
| Look and colors | CSS variables under `:root` |

To find a form field's ID, use the form's "Get pre-filled link" option, fill in each field, and read the `entry.NNN` values from the generated URL.

To test locally, open `index.html` in a browser.
