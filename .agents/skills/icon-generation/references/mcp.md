# MCP tools and asset handling

## Generation

Discover available tools and inspect their live schemas. Use the provider and model requested by the user. The maintainer’s preference as of 2026-11-27 is Nano Banana 2.1 when the connected provider actually offers it. If it is unavailable, identify the available alternative. Use an authorized alternative when the model was a preference. If the user requires the exact model, return prompts for a manual run. Use only references authorized for that provider, and keep paid calls within the agreed scope. For a first trial, generate one grid before deciding whether another call would address a specific defect.

- **Figma MCP.** Use `generate_image` in the specified editable file. Request a square image and use a separate trial frame. This tool takes a text prompt and consumes Figma AI credits. Describe the references in the prompt. Save the returned node or frame link and download the raster from the returned image URL or with `download_assets`. Follow the active connector's session and skill requirements.
- **Imagine MCP.** Use its discovered generation tool and actual parameters. Attach reference images or cell crops only when the schema supports images. Retrieve and inspect the actual path or URL returned. If it is unavailable, use Figma only when that route is within the user's authorization and fits the task.
- **Without a generator.** For a grid, deliver the English generation prompt, cell map, and references to attach. For close-ups, deliver one English prompt per selected cell with the matching crop. Resume with the user’s grid or renders. If a generation call times out, check whether it already produced an image before spending another call.

## Placement in Figma

Use the authorized destination frame. Follow the active connector's session and skill requirements. Inspect the existing icon slots. Import the PNGs using `upload_assets` and apply them to the intended layers when supported. Use a test copy or a preview frame when requested. Confirm actual placement with a screenshot or frame export. If the connector cannot write, return the assets and placement map for manual insertion.

See the [Figma MCP tools documentation](https://developers.figma.com/docs/figma-mcp-server/tools-and-prompts/) when a tool's capability is unclear.
