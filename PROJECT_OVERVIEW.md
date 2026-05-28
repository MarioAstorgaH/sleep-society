# Project Overview

## Executive Summary
- Godot 4.6 project named Sleep_Society with main scene main.tscn (Node3D) and a GridMap using a custom MeshLibrary (RoadsLibrary.tres).
- Primary content comes from a 3D city pack (Demo City By Versatile Studio) including FBX models, PNG textures, and material assets.
- Auxiliary scene calle_library.tscn defines road pieces (MeshInstance3D + collision) based on asphalt and sidewalk textures.
- Plugins installed: GitHub Copilot (enabled), pretty-gd, and GitGodot (installed but not enabled in project.godot).
- Includes a subproject godot-mcp-enhanced-* (Godot MCP server) with TypeScript source, GDScript editor plugin, docs, and tests.

## Detailed Inventory

### Root
- project.godot: project config (name, main scene, icon, physics Jolt, Copilot plugin enabled).
- main.tscn: main Node3D scene with GridMap using RoadsLibrary.tres, Camera3D, and an instance of mid_house_1.fbx.
- calle_library.tscn: road library scene with multiple MeshInstance3D road pieces and StaticBody3D + CollisionShape3D.
- RoadsLibrary.tres: MeshLibrary with multiple road items (mesh, collision, previews).
- icon.svg and icon.svg.import.
- opencode.json: OpenCode config for MCP integration.

### Assets
- Assets/Versatile Studio Assets/Demo City By Versatile Studio/
  - Models/: FBX models with .import and .meta sidecars.
  - Textures/: PNG textures (diffuse, normal, occlusion, emissive) with .import and .meta.
  - Materials/: .mat and .mat.meta files from the asset pack.
  - Prefabs/: .prefab and .prefab.meta files (likely Unity origin).
  - DCbVS_Documentation.pdf.

### addons
- addons/github_copilot/: GitHub Copilot plugin (v2.1.0) with plugin.gd and copilot_* scripts.
- addons/pretty-gd/: GDScript formatter (v2.0.5).
- addons/GitGodot/: Git integration plugin (v3.0) with scenes and Save_Data/save.json.

### MCP Subproject
- godot-mcp-enhanced-b7d56f0ad1408a3f3a6e6586a258a156b77687ab/
  - src/: TypeScript source for the MCP server.
  - addons/godot_mcp_server/: Godot editor plugin (command handlers and tools).
  - docs/ and test/: documentation and tests.
  - package.json: build output entry point is build/index.js.
