## General Rules

- **Avoid folder structure changes** unless necessary.
    - Renaming or restructuring commits should have no other changes.
- **Use branches for unfinalized work** or commits that do not follow these guidelines.
    - Keep the `master` branch clean.
- **File & Folder Naming**
    - No spaces in filenames or directories.
    - Use **Train-Case** for folders and files (e.g., `Project-Documentation`).
    - Use **snake_case** for front matter properties (e.g., `property_name`).
    - Use **ALLCAPS single word names** for GitHub-specific files (e.g., `README`, `LICENSE`).

## Branch Naming Conventions

- **ADRs:**
    - Format: `ADR-Decision-To-Be-Made` (e.g., `ADR-Decide-On-Vehicle-Class`).

## Commit Message Guidelines

### Simple Commits

- **Creating a file:**
    
    ```
    Add {filename}.{extension} ({optional description})
    
    {optional explanation}
    ```
    
- **Creating a folder:**
    
    ```
    Add {FULL directory path} directory ({optional description})
    {optional explanation}
    ```
    
    Example:
    
    ```
    Add Operations/Administration/ directory
    ```
    
- **Deleting a file:**
    
    ```
    Delete {filename}.{extension} ({optional description})
    
    {mandatory explanation}
    ```

---

Following these guidelines ensures a clean, structured, and easy-to-navigate repository. If you have any questions, feel free to ask %%add link%%!
