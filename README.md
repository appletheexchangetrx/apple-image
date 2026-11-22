# Apple Image Skill

A conversational, approval-driven skill for extracting product color variants, variant IDs, and image URLs from a product page supplied by the user. Supabase integration is optional.

## Contents

- `SKILL.md` — primary skill instructions and workflow.

## Default workflow

1. User provides a product-page URL.
2. Skill analyzes the page and reports the detected product, color options, variant IDs, and media structure.
3. Skill recommends the next stage and waits for approval.
4. Skill extracts and validates image URLs per color.
5. Skill previews results.
6. Optionally, with explicit approval, it compares and writes data to Supabase:
   - Destination: `products_duplicate`
   - Comparison/source: `products`
   - Default matching key: `variants_id` (verified against the live schema before use)

## Important

A GitHub repository stores the skill source; it does not by itself activate the skill inside ChatGPT. The skill must be imported or made available through a ChatGPT feature or integration that supports skills. The exact installation route depends on the ChatGPT environment and its enabled capabilities.
