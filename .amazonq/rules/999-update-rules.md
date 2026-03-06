When asked to update rules from base repository:

Process:
1. Download and extract repository to temporary directory
2. Compare each file from downloaded rules with existing rules
3. Update existing files with new content
4. Add new files that don't exist locally
5. Clean up temporary directory

Step 1 - Download and extract:
```bash
mkdir -p /tmp/amazonq-rules-update
cd /tmp/amazonq-rules-update
curl -L -o repo.zip https://github.com/PauloFerreira25/aws-qdeveloper-base-rules/archive/refs/heads/main.zip
unzip -q repo.zip
```

Step 2 - Compare and update:
- Read each file from /tmp/amazonq-rules-update/aws-qdeveloper-base-rules-main/.amazonq/rules/
- Compare with existing files in project's .amazonq/rules/
- Update files that have changes
- Add new files that don't exist

Step 3 - Cleanup:
```bash
rm -rf /tmp/amazonq-rules-update
```

Never:
- Skip file comparison
- Delete local rules without backup
- Update without user confirmation
