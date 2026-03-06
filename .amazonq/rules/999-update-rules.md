When asked to update rules from base repository:

Process:
1. Create temporary directory: /tmp/amazonq-rules-update
2. Download index from: https://raw.githubusercontent.com/PauloFerreira25/aws-qdeveloper-base-rules/main/.amazonq/rules/00-rules-index.md
3. Parse index to get list of rule files
4. Download each rule file to temporary directory using base URL: https://raw.githubusercontent.com/PauloFerreira25/aws-qdeveloper-base-rules/main/.amazonq/rules/
5. Compare each downloaded file with existing file in .amazonq/rules/
6. Update existing files with new content from downloaded files
7. Add new files that don't exist locally
8. Remove temporary directory

Commands:
```bash
# Create temp directory
mkdir -p /tmp/amazonq-rules-update

# Download files (example for one file)
curl -o /tmp/amazonq-rules-update/00-rules-index.md https://raw.githubusercontent.com/PauloFerreira25/aws-qdeveloper-base-rules/main/.amazonq/rules/00-rules-index.md

# Copy to project (after comparison)
cp /tmp/amazonq-rules-update/*.md .amazonq/rules/

# Cleanup
rm -rf /tmp/amazonq-rules-update
```

Never:
- Skip file comparison
- Delete local rules without backup
- Update without user confirmation
