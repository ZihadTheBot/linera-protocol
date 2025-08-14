# Linera Agent

This example application runs a Large Language Model (LLM) Agent which uses an LLM
to forge queries by introspecting the Linera Node Service GraphQL API.

## How it works

The agent wraps an LLM of choice and is provided with context on what Linera is and
the core concepts. Further context is provided by performing an introspection query
which injects the Linera Node Service GraphQL schema. The schema is quite large - 
the resulting context in ~15,000 tokens being used just for context.

After the context is provided, a chat is initiated between user and agent, where the
agent writes GraphQL queries on behalf of the user and uses the Linera Node Service 
tool to submit them.

## Usage

Assume a Linera Node Service is running on `localhost:8080` and is connected to a running
network (local or otherwise).

```bash
#!/bin/bash
# Git commit script for AI Agent - Zihad

# Configure Git identity (only needed once)
git config --global user.name "AI_Agent_Zihad"
git config --global user.email "zihadsk44@gmail.com"

# Navigate to project folder (AI agent's workspace)
cd /path/to/project || exit

# Stage all modified and new files
git add .

# Commit with a dynamic AI message
commit_message="Auto-commit from AI Agent at $(date '+%Y-%m-%d %H:%M:%S') - Hi from zihad"
git commit -m "$commit_message"

# Push to GitHub main branch
git push origin main