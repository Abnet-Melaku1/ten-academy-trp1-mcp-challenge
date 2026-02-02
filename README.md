## Tenx MCP Setup Challenge (TRP 1)

This repository contains my work for the **TRP 1 – MCP Setup Challenge** for 10 Academy / Tenx.  
The goal is to configure my IDE with the **Tenx MCP Analysis server**, design an effective **rules file** for my coding agent, and document how these changes affect the agent’s behaviour.

### Challenge Overview

- **Task 1 – Setup**
  - Configure my IDE (Cursor in this repo) to connect to the **Tenx MCP Analysis** server.
  - Ensure the MCP connection stays active during my interactions so that my usage is logged.

- **Task 2 – Research & Configure**
  - Study best practices for AI coding agent rules, including:
    - Boris Cherny’s workflow and community examples.
    - General patterns for controlling agent behaviour, style, safety, and tool usage.
  - Use these insights to design and refine my rules file:
    - For Cursor: `.cursor/rules/agent.mdc`

- **Task 3 – Documentation**
  - Record what I tried, what worked, what didn’t, and the insights I gained while:
    - Connecting the Tenx MCP server.
    - Iterating on the rules file and testing the agent’s behaviour.

### Repository Structure

- `README.md` — This file, describing the challenge and repo purpose.
- `.cursor/`
  - `mcp.json` — MCP configuration (includes Tenx MCP Analysis server).
  - `rules/agent.mdc` — Main rules file guiding the coding agent in Cursor.
- `MCP-Setup-Report.md` — Detailed documentation of:
  - What I did
  - What worked
  - What didn't work / challenges
  - Insights about how rules affect the agent
- `EXPERIMENTS-LOG.md` — Detailed log of rules file iterations, test results, and experimentation process showing the evolution from v1.0 to v1.3

### How to Run / Use Tenx MCP in Cursor

Follow these steps to use the Tenx MCP Analysis server with this repository in **Cursor**:

1. **Open this repo in Cursor**  
   - Open the folder containing this project (`ten-academy-trp1-mcp-challenge`) in Cursor.

2. **Ensure MCP config exists**  
   - Check that `.cursor/mcp.json` exists and contains the `tenxfeedbackanalytics` / `tenxanalysismcp` server pointing to `https://mcppulse.10academy.org/proxy` with headers:
     - `"X-Device": "windows"`  
     - `"X-Coding-Tool": "cursor"`

3. **Ensure rules file exists**  
   - Verify `.cursor/rules/agent.mdc` is present. This file controls how the coding agent behaves in this repo.

4. **Start the Tenx MCP server in Cursor**  
   - Open the MCP servers panel in Cursor (via the status bar icon or the Command Palette search for “MCP”).  
   - Locate the **tenxfeedbackanalytics / tenxanalysismcp** server and click **Start**.  
   - Complete the GitHub authentication flow in your browser if prompted, then return to Cursor.

5. **Use the agent as normal**  
   - Open a file (for example `README.md` or `agent.mdc`) and ask the agent for help.  
   - While you interact, the Tenx MCP Analysis server will log your interactions in the background.



### Author

**Abnet Melaku**
