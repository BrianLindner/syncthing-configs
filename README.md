# Syncthing Configs & Related Information <!-- omit from toc -->

Collection of various Ignore patterns and other [Syncthing](https://syncthing.net) related information

- [Installation](#installation)
- [Ignore Files](#ignore-files)


## Installation

1) Place stglobalignore file in folder and include it in the stignore file (or UI)
   in .stignore file
    ```text
    #include .stglobalignore
    ```
2) Copy contents of stglobalignore into stignore file (or UI)
    ```text
    (?d).DS_Store
    (?d).localized
    (?d)._*
    (?d).Icon*
    (?d).fseventsd
    (?d).Spotlight-V100
    (?d).DocumentRevisions-V100
    ...
    ...
    (?d)(?i)*_log
    ```
3) Mix of both, and use some overrides. Import stglobalignores, override things needed for specific folder.

    Example: allow sync of log files
    ```text
    !*.log

    #include .stglobalignore
    ```

---

## Ignore Files

Files:

- [.stignore](.stignore)
- [.stglobalignore](.stglobalignore)

---