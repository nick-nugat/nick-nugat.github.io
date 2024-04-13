---
aliases: "202403121753"
tags: 
date: 2024-03-12
created: 2024-03-12T17:53
updated: 2024-03-20T13:12
---
# [[Process for JavaFX]]
%% documenting because i hate javafx sm and i always have problems %%

> [!important]
> [VM Arguments for IntelliJ](obsidian://open?vault=content&file=VM%20arguments%20for%20JavaFX)

## IntelliJ Idea CE
1. File -> Project Structure -> Libraries
	1. Add Java library - point it to `lib/` directory of the JavaFX download
2. Run -> Edit Configurations
	1. Add new **Application**
	2. Name it, add main class
	3. Click "Modify options" and make sure "Add VM options" is checked
	4. Under VM options, add this:
```sh
--module-path <path/to/lib> --add-modules javafx.controls,javafx.fxml
```

> [!NOTE]
> - if on windows, use foward slashes for separation instead
> - also, if other modules are needed, add them separated by commas

___
# References
- https://openjfx.io/openjfx-docs/