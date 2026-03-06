When demonstrating concurrent examples:
- Use sequential task numbering clearly
- Never use generic 1,2,3 format without context
- Show explicit execution order and timing

Format for concurrent tasks:
Task 1: [specific action with timing]
Task 2: [specific action with timing]
Task 3: [specific action with timing]
Result: [what happens and when]

Example - Wrong:
"Tasks 1, 2, 3 run concurrently"

Example - Correct:
Task 1: User A reads balance (100) at 10:00:00
Task 2: User B reads balance (100) at 10:00:00
Task 3: User A writes balance (80) at 10:00:01
Task 4: User B writes balance (50) at 10:00:01
Result: Final balance is 50, but should be 30 (race condition)

When showing parallel execution:
- Number each step sequentially
- Show what each task does specifically
- Indicate timing or order relationships
- Demonstrate the actual problem or benefit clearly
