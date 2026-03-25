When implementing solutions:
- Never solve the same problem in multiple places
- Always evaluate the best single location for the solution
- Prefer infrastructure-level solutions (Dockerfile) over configuration (docker-compose.yml)

When you identify two approaches that solve the same problem:
- Analyze which location is most appropriate
  - Dockerfile: For image-level configuration (WORKDIR, ENV, USER)
  - docker-compose.yml: For service-level overrides and runtime behavior
  - Code: For application-specific logic
- Choose the single best location
- Remove all duplicates
- If uncertain about the best location, present both options to the user and ask for guidance

Common redundancies to avoid:
- WORKDIR in Dockerfile + working_dir in docker-compose.yml (keep in Dockerfile only)
- ENV in Dockerfile + environment in docker-compose.yml (keep ENV in Dockerfile, use docker-compose only for overrides)
- USER in Dockerfile + user in docker-compose.yml (keep in Dockerfile only)

Remember: One source of truth per configuration concern.