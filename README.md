# 🚀 Azure DevOps MCP Cursor Plugin

This repository contains a single Cursor plugin that helps users work with Azure DevOps through the Azure DevOps MCP Server.

## ✨ What this plugin provides

- Plugin manifest and metadata for Cursor Marketplace packaging.
- Skills for working with Azure DevOps work items and iterations.
- Branding assets and helper scripts used in this repository.

## 🗂️ Repository structure

```text
.
|-- .cursor-plugin/
|   |-- plugin.json
|-- assets/
|   |-- logo.png
|-- docs/
|   |-- add-a-plugin.md
|-- scripts/
|   |-- validate-template.mjs
`-- skills/
    |-- boards-my-work/
    |   `-- SKILL.md
    `-- work-iterations/
        `-- SKILL.md
```

## 📦 Plugin details

The plugin metadata is defined in `.cursor-plugin/plugin.json`:

- Name: `azure-devops-mcp-server`
- Display name: `Azure DevOps MCP Server`
- Homepage: `https://learn.microsoft.com/en-us/azure/devops/mcp-server/remote-mcp-server`

## 🧠 Included skills

`skills/boards-my-work/SKILL.md` defines a workflow to:

1. Determine the target Azure DevOps project.
2. Retrieve the current user's work items with `wit_work_item` using `action: my`.
3. Fetch detailed fields in batch with `wit_work_item` using `action: get_batch`.
4. Render grouped, sorted results with clickable work item links.

`skills/work-iterations/SKILL.md` defines a workflow to:

1. Resolve project and optional team context.
2. List project iterations with `work` using `action: list_iterations`.
3. List team iterations with `work` using `action: list_team_iterations`.
4. Create and assign iterations with `work_iteration_write` using `action: create` and `action: assign`.

## ✅ Local validation

Run the validation script from the repo root:

```bash
node scripts/validate-template.mjs
```

## 📝 Notes

- This repository is currently structured as a single plugin at the root.
- The guide in `docs/add-a-plugin.md` is available if you later expand to a multi-plugin layout.
