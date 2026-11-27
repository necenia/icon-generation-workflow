# From brief to icons in a layout

Reply to the user in Russian throughout the workflow, including when the brief is in English. This applies to questions, proposals, progress updates, and the final handoff. Write generation prompts and new repository documentation in English. README.md is maintained in Russian.

Follow the workflow up to the deliverable requested by the user. Record the categories, purpose, target icon size, background, palette, constraints, and target frame link if available. Ask only about gaps that block the next step. Save artifacts in `runs/<run-name>/`. When resuming, open the previous run, recover the chosen direction and cell map, and start at the first incomplete step.

## 1. Find references and propose icon concepts

Start with the materials supplied by the user. Search by specific visual properties when needed, such as `matte white product render three-quarter soft studio light`, and by objects that could represent the categories. Open sources and verify that the images are visible. Propose two or three directions and recommend one. For each direction, share one or two source links, explain which camera angle, material, and lighting to borrow, and suggest an object for each category. Offer an alternative where the subject is ambiguous. Record the chosen direction in `references.md`. If the user has already selected a direction, use it in step 2.

## 2. Write the prompt and map the cells

For a step-by-step run, use the [example requests](examples/agent-requests.md) as a guide. Write a new generation prompt based on the selected references. Specify the camera angle, lighting, background, materials, visual weight, margins, and use of the palette. List the cells in each row from left to right. If there are fewer than nine categories, use spare cells for alternatives or make a smaller grid. For a longer series, use multiple grids with consistent constraints. Save the cell map, such as R1C1 through R3C3, and the English generation prompt in `grid-prompt.md`.

When changing the style, update the visual properties and check that they still fit the grid constraints. Keep the subjects in the same positions for comparison. Update the map when you replace an object.

## 3. Generate the grid

Inspect the available MCP tools and their schemas. Use the generator requested by the user. Send only materials authorized for that external service.

- **Figma MCP.** Use `generate_image` in the specified editable file. Request a square image and use a separate frame for the trial. Account for Figma AI credit usage. The tool accepts a text prompt. Describe the visual properties of the references in words. Export with the returned image URL or `download_assets` and save the frame link. Follow the active client's requirements for Figma sessions and skills.
- **Imagine MCP.** Find the connected generation tool and read its schema. If it supports image inputs, attach authorized references using its declared parameters. Use the actual path or URL returned by the tool. If Imagine is unavailable, propose Figma MCP within the available permissions and budget or provide the prompt for a manual run.
- If neither route can generate an image, save the cell map and prompt. Explain what is blocking generation and ask the user to provide the resulting grid so you can resume.

Save `grid.png` or a link to the result alongside its prompt. In `selection.md`, record the exact grid version and the selected coordinates. Save new directions as separate versions. Review the full series and check how each object reads at the target size without a caption. Check camera angle, lighting, visual weight, palette, and whether each silhouette fits its cell. Show the grid and recommend the strongest cells by coordinate. If the user delegated selection, record your picks.

## 4. Make close-ups

For each selected cell, record the coordinate, subject, and distinctive details. Crop the cell from the actual grid. If the cell boundaries are uneven, locate them in the image. Pass the crop to the generator when it supports image input. For text-only Figma generation, describe the visible features of the crop and compare the rerender with the original. If the silhouette must match exactly and rerendering changes it, process the original crop and report its usable resolution. If the client cannot crop or rerender, save the coordinates and prepared prompt so the user can provide the needed image and resume.

Export each selected object as a separate PNG. Check the alpha channel and inspect edges on light and dark backgrounds. Remove halos and preserve fine details. Upscale when the source resolution is too low. Save `icons/<category>.png`, the prompts used, and the mapping from files to cells.

## 5. Place and verify icons in the layout

In Figma, import the PNGs with `upload_assets`. Use the existing slots and sizes. In a test frame, check that each full silhouette fits, and review optical size, alignment, and legibility next to text. Verify the final appearance from a screenshot. When the file or write access is unavailable, deliver the PNGs with a placement map listing each category, file, slot, and size.

In the handoff, link to the grid, selected PNGs, and the layout or placement map. State which steps were completed and what is needed to resume, if anything. Keep working materials and exports inside the run directory. Publish them only with the owner's permission.
