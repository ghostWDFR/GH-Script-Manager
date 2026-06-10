# Importing Scripts

---

The **Import Script** feature allows you to add existing Python scripts to GH Script Manager.

This is useful when:

* Migrating scripts from another project
* Organizing existing Blender tools
* Sharing scripts between computers
* Building a personal script library

<br>

![Import Script](/images/Create_Script.png)

**Import Script Dialog**

---

## Importing a Script

To import a Python script:

1. Open the **Create New Script** section
2. Select a target group (optional)
3. Click **Import Script**
4. Choose a `.py` file
5. Confirm the import

The selected script will be copied into the configured scripts directory.

Only Python files (`.py`) are supported.

---

## Import Destination

Imported scripts are copied into the selected script group.

Example:

Group selected:

```text
Utilities
```

Imported file:

```text
RenameObjects.py
```

Result:

```text
Scripts
└── Utilities
    └── RenameObjects.py
```

---

## Importing Into Nested Groups

Scripts can also be imported into nested folders.

Example group:

```text
Tools/Export
```

Result:

```text
Scripts
└── Tools
    └── Export
        └── ExportFBX.py
```

Missing folders are created automatically when needed.

---

## Duplicate File Protection

GH Script Manager prevents accidental overwriting.

Example:

Existing file:

```text
RenameObjects.py
```

Imported file:

```text
RenameObjects.py
```

Result:

```text
Import Cancelled
```

The original file remains unchanged.

An error message will be displayed.

---

## Automatic Refresh

After importing a script:

* The script list is refreshed automatically
* New folders become visible immediately
* Imported scripts appear without restarting Blender

No manual reload is required.

---

## Organizing Imported Scripts

A common workflow is to organize scripts by category.

Example structure:

```text
Scripts
├── Utilities
│   ├── RenameObjects.py
│   ├── CleanNames.py
│   └── BatchExport.py
│
├── Animation
│   ├── BakeActions.py
│   └── CurveTools.py
│
└── Pipeline
    ├── FBXExporter.py
    └── AssetValidator.py
```

This makes navigation easier when working with larger script collections.

---

## Typical Workflow

1. Select a group:

```text
Utilities
```

2. Click:

```text
Import Script
```

3. Select:

```text
RenameObjects.py
```

4. Confirm the import

5. The script appears in the list automatically

6. Select the script and use **Run Script** or **Edit**