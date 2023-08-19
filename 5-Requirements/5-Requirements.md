This section contains requirements for the system.

## Requirements Overview

**High-Level Active Requirements:**

{{
  
List and link to the high-level requirements of the system.

}}

**Important Active Requirements:**

{{
  
You may also list and link to the most impactful 10 to 20 requirements of the system.

}}

## Requirement ID

IDs help to easily reference requirements.
Requirement IDs may be grouped to create a hierarchy of requirements.
IDs of sub-requirements are separated by a dot "." from the parent ID.

**Note:** IDs must not include any whitespace or `-` to keep IDs readable in wiki titles.

**Examples:**

```
my_req
my_req.sub_req
other_req.sub_req.even_lower_req
```

## Requirement Phases

A requirement goes through the following phases:

1. **proposed** ... Requirements are **proposed**, by creating feature-request issues
2. **ready** ... Once a requirement has enough information available to be implemented, it is **ready**, and must be documented in the wiki with a unique ID for tracing
3. **Optional: declined** ... A requirement in **proposed** or **ready** state may be **declined**, meaning that it will not be implemented, and must be removed from the wiki if it already exists
4. **active** ... When the implementation of a requirement is merged, the requirement gets **active**, and the number of times the requirement is referenced is added to the wiki

   **Example:**

   ```
   # my_req: Some implemented requirement
   
   **References**

   - in branch main: 2
   ```

   If it is not possible to reference a requirement, `manual` may be set instead of the number of references.
   This marks the requirement as **active**, but requiring manual verification.

   **Example:**

   ```
   # my_req: Requirement that needs manual verification
   
   **References**

   - in branch main: manual
   ```

   A manually verified requirement may get references in the future.
   The number of references is then added after the `manual` keyword.

   **Example:**

   ```
   # my_req: Requirement that needs manual verification, but is also references in code
   
   **References**

   - in branch main: manual + 3
   ```

5. **deprecated** ... If a requirement is replaced or removed by another requirement, the requirement gets **deprecated**.

   Since the requirement might still be **active** in some branches, `deprecated` must be set manually to the branches
   the requirement is deprecated.

   The *references* list may be replaced by `**deprecated**` if the requirement is **deprecated** in all branches. 

   **Note:** A link should be added in the **deprecated** requirement, pointing to the new requirement for better traceability.

   **Examples:**

   ```
   # my_req: Got deprecated in latest version

   **References**

   - in branch main: deprecated
   - in branch stable: 2
   ```

   ```
   # my_req: Deprecated in all supported versions

   **deprecated**

   Deprecated by [req:new_req].
   ```

## Definition of Ready

A requirement may be considered **ready** if it fulfills the following statements:

- **General:**

  - It is clear where the requirement must be placed in the wiki
  - The ID for the requirement is decided and unique in the wiki
  - All currently raised concerns by stakeholders are resolved

- **For high-level requirements:**

  - The intent of the requirement is covered by the existing sub-requirements 
  - All sub-requirements fulfill their Definition of Ready

  **Note:** If the requirement does not fulfill these statements, try refining existing sub-requirements, or create additional ones.

- **For low-level requirements:**

  - At least one developer understands how to implement it
  - Implementation is estimated to take less than two weeks for one developer

  **Note:** If the requirement does not fulfill these statements, consider creating sub-requirements for it. 
