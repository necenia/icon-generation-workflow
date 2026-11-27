---
name: icon-generation
description: Build or refine a coordinated set of raster UI icons from a brief or reference grid. Use for finding visual references, proposing icon concepts, writing generation prompts, generating a grid with Figma MCP or Imagine MCP, producing close-ups, or placing the resulting PNGs in a layout.
---

# Generate an icon series

Reply to the user in Russian, including progress and decisions, even when the brief is in English. Write prompts sent to image generators in English.

Start from the stage the user needs. If the user provides an approved grid or finished PNGs, pick up at close-ups or placement. For a new run, capture the categories, use case, target size, background, palette, and any supplied references or Figma destination. Ask only for missing information that blocks the next action.

Keep work in `runs/<run-name>/` or the workspace the user specified. Store the chosen direction, actual generation prompts, grid versions, and cell selections so you can resume without generating an existing result again. Keep these outputs local unless the user authorizes sharing.

## 1. Find references and propose concepts

Separate references for visual treatment from references for the objects. Search for missing traits or concepts and verify that the linked images are visible. When direction is open, propose two or three options with references, a recommendation, and an object for each category. Describe the specific shape, material, lighting, or camera angle to borrow. For an ambiguous category, offer an alternative. If the direction is already chosen, use it.

## 2. Write the generation prompt

Translate the chosen style into observable traits. Specify materials, camera angle, lighting, palette, background, optical size, and spacing. Use a square 3 × 3 grid as a starting point, with one complete object per cell and no captions or logos. List cells from left to right by row. Use spare cells for alternatives or use a smaller grid. For larger sets, keep rendering parameters consistent across batches. Save the prompt and the cell map.

When comparing styles, keep the cell map fixed unless the user also wants to change the concepts. Update the visible traits based on the new reference.

## 3. Generate and review a grid

For live generation, read [MCP tools and asset handling](references/mcp.md). Keep each trial with its exact prompt, provider, and version or frame link. Inspect the actual image before recommending cells. Check category recognition at target size, even visual weight, consistent lighting and palette, and complete silhouettes. Identify candidates by grid version, row, column, and object. If the user wants to choose, show the grid and pause at selection. If selection was delegated or supplied, proceed.

## 4. Produce close-ups

Crop the selected cells using the actual image boundaries. Use a provider that accepts the crop when fidelity matters. For text-only generation, describe the visible silhouette, distinctive details, accent placement, angle, and light, then compare the output with the crop. If rerendering materially changes a shape that must match, process the source crop when its usable resolution is sufficient.

Export one PNG with real alpha per chosen icon when feasible. Check edges against light and dark backgrounds and preserve fine structures. Upscale when necessary and recheck the silhouette. If clean transparency or needed resolution is unavailable, report that on the affected file. Record which grid and cell produced each PNG.

## 5. Place and verify the icons

For Figma placement, read the placement section in [MCP tools and asset handling](references/mcp.md). Check the actual slots at UI size, including full silhouettes, optical scale, spacing, and legibility next to text. Verify with a screenshot or exported frame. If placement is blocked, deliver the PNGs with a category-to-file, slot, and size mapping.

Hand off the available grid, selected PNGs, and layout preview or placement map in Russian. Name any incomplete stage and the exact input or capability needed to continue.
