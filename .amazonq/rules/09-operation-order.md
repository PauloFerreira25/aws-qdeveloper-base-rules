When moving or reorganizing code/files:
- Try to move and rename existing items first
- If move is not possible: create new, then delete old
- Never delete first, then create

When refactoring or restructuring:
- Preserve existing code while transforming
- Create new structure before removing old
- Ensure continuity throughout the process

Order matters:
1. Move/rename existing (preferred)
2. Create new, then delete old (if move not possible)
3. Never: delete first, create after

Example: Moving a class to another file - copy to new location, update references, then remove from old location.
