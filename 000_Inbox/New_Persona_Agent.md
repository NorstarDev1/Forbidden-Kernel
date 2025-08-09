---
tags:
  - workflow
  - agent
banner:
---
Topics:: new agents

# ⚙️ 🧠 Creating a New Persona Agent with File Access
---
# 🧩 Adding a New Persona Agent with File Access in Windsurf

This guide supports setting up a new agent (e.g. Prof Spaghetti, Nexus, Apex) in Windsurf including:

- MCP persona script
- Cascade integration
- Working directory access for `agent_data/`
- Shared and global memory handling

---

## 1. ✅ Create Persona MCP Script

Place it under:

/media/norstar66/agent_data/agent_store/{agent}_mcp.sh


Example content for `prof_spaghetti_mcp.sh`:

```bash
#!/bin/sh
cat <<'EOF'
System:
You are **Prof. Spaghetti**, co-founder of SIVERSE Labs…
(Insert full Wind‑surfed persona prompt here)
EOF
while read -r line; do echo "$line"; done

Make executable:

chmod +x .../prof_spaghetti_mcp.sh
```

## 2. 🌐 Add MCP Server to Windsurf

In ~/.codeium/windsurf/mcp_config.json (or via Settings → Cascade → Add Custom Server):

{
  "mcpServers": {
    "prof_spaghetti": {
      "command": "/media/.../prof_spaghetti_mcp.sh",
      "args": [],
      "env": {}
    }
  }
}

Then click Refresh in Windsurf to enable the server.

## 3. 🛡️ Set Up Directory Permissions Automatically

Create setup_agent_access.sh:
```bash
#!/bin/bash
AGENT=$1
BASE="/media/norstar66/agent_data"
SHARED="$BASE/${AGENT}_shared"
GLOBAL="$BASE/global-mem0"
USER="norstar66"
GROUP="aiagents"

sudo groupadd -f $GROUP
sudo usermod -aG $GROUP $USER
sudo mkdir -p "$SHARED" "$GLOBAL"

sudo chown -R $USER:$GROUP "$SHARED" "$GLOBAL"
sudo chmod -R 2775 "$SHARED" "$GLOBAL"
echo "Agent $AGENT can now access $SHARED and $GLOBAL"
```
Run it:
```bash
./setup_agent_access.sh prof_spaghetti
```
This ensures:

    Shared memory directory (agent-specific)

    Global memory accessible to all personas

## 4. 🧾 Verify Access
```bash
ls -ld $SHARED $GLOBAL
touch $SHARED/test.txt
cat $SHARED/test.txt
```
Expected permissions: drwxrwsr-x and group aiagents.
## 5. 🧠 Configure Cascading Persona + Memories
### Select Model + MCP:

- Choose "gpt-4o + prof_spaghetti" in Cascade → you’ll chat as Prof Spaghetti.

### Add contextual memory:

- Navigate Cascade → Manage Memories, add:

	- “Norstar is CEO of SIVERSE Labs”

	- “Prof Spaghetti co‑founded NeuroWave”

### Set interaction rules:

Add global_rules.md in vault:
```xml
<persona_rules>
- When prompted “Prof Spaghetti”, respond with enthusiastic & helpful tone
- Reference SIVERSE’s mission and short-term goals
</persona_rules>
```
## 6. 🔁 Test Flow End-to-End

    Switch to gpt-4o + prof_spaghetti

    Prompt: “Hey Prof Spaghetti, can you write a log into your memory folder?”

    Cascade should recognize the persona and prompt you to write into /agent_data/prof_spaghetti_shared via an MCP file tool


## 📋 Summary Table

| Step               | Purpose                                    |
| ------------------ | ------------------------------------------ |
| MCP Script         | Defines persona system prompt              |
| MCP Config         | Enables Cascade to call your script        |
| Directory Setup    | Provides read/write access to memory store |
| Permissions Script | Automates access setup                     |
| Memories & Rules   | Anchors persona identity and behavior      |
| Cascade Testing    | Verifies multi-model persona consistency   |


⚙️ Integration Tips:

Use Windsurf’s Filesystem or filesystem MCP to allow read_file, write_file, list_directory, etc.

 Be mindful of model-handler bugs (some MCP support may vary)

