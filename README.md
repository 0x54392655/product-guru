# Product Guru

Product tickets and explanations that people can understand and act on.

Product Guru is a Codex skill for drafting and editing tickets, acceptance criteria, short product briefs, and product explanations. It uses explicit clarity rules inspired by Simplified Technical English. It preserves requirements and makes missing decisions visible.

This is an initial draft. It has not yet been evaluated across models or tested with working product teams.

## Use it

Copy `skills/product-guru` into your personal Codex skills directory, `~/.agents/skills/`, or your repository's `.agents/skills/` directory. Copy the whole folder so that the examples remain available.

Codex detects skill changes automatically. Restart Codex if the skill does not appear. See the [official skill documentation](https://learn.chatgpt.com/docs/build-skills) for discovery and installation locations.

Example requests:

```text
Use $product-guru to turn these notes into an engineering ticket.
Keep unresolved decisions as questions: ...
```

```text
Use $product-guru to rewrite this ticket. Preserve every requirement
and exact API field name: ...
```

```text
Use $product-guru to explain this proposal to a product manager: ...
```

The skill can also be selected automatically when its description matches a writing task. It does not need a connector, script, or API key. It drafts text; it does not authorize publishing tickets or changing external systems.

## What it changes

- Long sentences become focused sentences with named actors.
- Vague product language becomes concrete behavior where the source supports it.
- Requirements remain requirements; suggestions and unknowns stay visible.
- Acceptance criteria describe observable results.
- The output follows the user's format and contains only useful sections.

See the [before-and-after examples](skills/product-guru/references/examples.md).

## Relationship to ASD-STE100

[ASD-STE100](https://www.asd-ste100.org/) uses writing rules and a controlled dictionary. Product Guru contains original PM instructions inspired by the goal of clear, consistent technical writing. It does not reproduce the standard or its dictionary and does not claim conformance, certification, or endorsement.

The sentence-length target and PM workflow in this skill are project conventions. They are not a summary of the official standard. Use the [official standard](https://www.asd-ste100.org/STE_downloads.html) when formal ASD-STE100 conformance is required. The maintainers also discuss the limits of AI-generated STE on that page.

## Improve it with evidence

Run the [evaluation cases](evals/cases.md) before changing the instructions. Compare results with both a normal prompt and a prompt that simply asks for STE-inspired PM writing. Record the model and date.

Report failures with a sanitized input, the output, and the specific requirement that was lost, invented, or left unclear. Do not include confidential tickets or customer information in public examples.

Start with tickets and short briefs. Add other PM workflows when real examples show what guidance they need.

## License

The original files in this repository use the [MIT License](LICENSE). The license does not cover the external ASD-STE100 standard.
