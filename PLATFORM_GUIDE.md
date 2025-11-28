# PRM Agent Platform Guide - How to Use Across Different AI Tools

**PRM Agent works with any AI assistant that can read files and follow agent instructions!**

---

## 🚀 Supported Platforms

PRM Agent works seamlessly across multiple AI platforms:

- ✅ **Claude Code CLI** - Official CLI tool from Anthropic
- ✅ **Cursor IDE** - AI-powered code editor
- ✅ **Claude.ai** - Web interface with Projects feature
- ✅ **Windsurf IDE** - AI-native IDE
- ✅ **Other AI Assistants** - Any AI that can read files and maintain context

---

## 📋 General Requirements

To use PRM Agent on any platform, you need:

1. **File Access**: AI must be able to read local files or access uploaded files
2. **Context Window**: Sufficient context to hold agent instructions (agents are ~500-1000 lines)
3. **Multi-Turn Conversation**: Ability to have iterative conversations
4. **File Output**: Ability to create/save output files (or you can manually save responses)

---

## Platform-Specific Instructions

### 1. Claude Code CLI (Recommended)

**Why Recommended**: Native support, MCP tools, file operations, optimal experience

**Setup**:
```bash
# No setup needed if you have Claude Code CLI installed
cd /path/to/PRM_Agent/prm-agent
```

**Usage**:
```bash
# Start Claude Code in the prm-agent directory
claude

# Load an agent (example: Oracle)
# Method 1: Use @ to reference the file
@agents/oracle.agent.md

# Method 2: Ask Claude to read it
"Please read and follow the instructions in agents/oracle.agent.md"

# Method 3: Paste the agent content directly
[Copy/paste agent file content]

# Then start working
start-data-collection
```

**Features Available**:
- ✅ Direct file reading/writing
- ✅ Meta MCP tools (auto-fetch Workplace URLs)
- ✅ PDF/Word/Markdown support
- ✅ Automatic file operations
- ✅ Background tasks

**Best For**: Meta employees, power users, full workflow automation

---

### 2. Cursor IDE

**Why Use**: Integrated coding environment, file system access, great for developers

**Setup**:
```bash
# Open the PRM Agent folder in Cursor
cursor /path/to/PRM_Agent/prm-agent
```

**Usage**:
```
1. Open Cursor AI chat (Cmd+L or Ctrl+L)

2. Reference the agent file:
   "Please read and act as the agent defined in agents/oracle.agent.md"

3. Or use @ to mention the file:
   @agents/oracle.agent.md "Act as this agent"

4. Start the workflow:
   start-data-collection

5. Cursor can read/write files directly in the workspace
```

**Features Available**:
- ✅ Direct file reading/writing
- ✅ PDF/Word/Markdown support (via extensions)
- ✅ Integrated file explorer
- ✅ Code-aware context
- ⚠️ No Meta MCP tools (manual download needed for Meta URLs)

**Best For**: Developers who live in their IDE, non-Meta users

**Tips**:
- Use Composer mode (Cmd+I) for longer interactions
- Keep agent file open in a tab for reference
- Use file tree to organize input/output folders

---

### 3. Claude.ai (Web Interface with Projects)

**Why Use**: Accessible anywhere, no installation, great for non-technical users

**Setup**:
```
1. Go to claude.ai
2. Create a new Project: "Performance Review - [Employee Name]"
3. Upload files to the Project:
   - All 5 agent files (oracle.agent.md, sorting-hat.agent.md, etc.)
   - Your input files (self-review.pdf, manager-notes.md, etc.)
   - Resources (manager-notes-example.md, style-guide-example.md)
```

**Usage**:
```
1. In your Project chat, say:
   "Please read agents/oracle.agent.md and act as the Oracle agent described in it"

2. Claude will read the uploaded file and adopt the agent persona

3. Start the workflow:
   start-data-collection

4. Oracle will ask questions and process your files

5. When Oracle creates output, copy/paste the output and save it as a file

6. Upload that output file to the Project for the next agent

7. Repeat for each agent in the workflow
```

**Features Available**:
- ✅ File uploads (PDF, Word, Markdown, text)
- ✅ Persistent Projects
- ✅ Multi-file context
- ⚠️ Manual file saving (copy/paste outputs)
- ⚠️ No Meta MCP tools (manual download for Meta URLs)

**Best For**: Non-technical users, managers without coding tools, anywhere access

**Tips**:
- Create one Project per employee review
- Upload all agents and resources upfront
- Keep a local folder to save outputs (copy from Claude responses)
- Use Artifacts feature for long outputs

**Workflow Example**:
```
Project: "Jane Smith Q4 Review"
Files uploaded:
  - oracle.agent.md
  - sorting-hat.agent.md
  - sherlock.agent.md
  - shakespeare.agent.md
  - irs.agent.md
  - self-review.pdf
  - manager-notes.md
  - peer-feedback.pdf
  - style-guide-example.md

Chat:
You: "Read oracle.agent.md and become the Oracle agent"
Claude: [Reads file] "I'm Oracle, the Data Gatherer..."
You: "start-data-collection"
Oracle: "What is the employee's name?"
[... continue workflow ...]
Oracle: [Generates review-data.md content]
You: [Copy output, save as review-data.md, upload to Project]
You: "Read sorting-hat.agent.md and become the Sorting Hat"
[... continue through all agents ...]
```

---

### 4. Windsurf IDE

**Why Use**: Modern AI-native IDE with deep file integration

**Setup**:
```bash
# Open the PRM Agent folder in Windsurf
windsurf /path/to/PRM_Agent/prm-agent
```

**Usage**:
```
1. Open Windsurf AI panel

2. Reference the agent:
   "Read and follow the instructions in agents/oracle.agent.md"

3. Start working:
   start-data-collection

4. Windsurf can create/edit files directly
```

**Features Available**:
- ✅ Direct file reading/writing
- ✅ Multi-file context
- ✅ Integrated AI chat
- ⚠️ No Meta MCP tools

**Best For**: Developers who prefer Windsurf, modern IDE experience

---

### 5. Other AI Assistants (ChatGPT, Gemini, etc.)

**Generic Workflow**:

**Setup**:
```
1. Download/copy all agent files to your computer
2. Prepare input files in a local folder
```

**Usage**:
```
1. Copy the full agent file content (e.g., oracle.agent.md)

2. Paste it into the AI chat with:
   "Please read these instructions and act as the agent described.
    Here is the agent definition:

    [paste full oracle.agent.md content]"

3. The AI will adopt the agent persona

4. Start the workflow:
   start-data-collection

5. For file inputs:
   - Upload files if supported
   - Or copy/paste file contents when asked

6. Copy AI outputs and save them manually as files

7. For next agent, repeat: paste new agent definition, start workflow
```

**Features Available**:
- ⚠️ Varies by platform
- ⚠️ May require manual file handling
- ⚠️ No Meta MCP tools
- ⚠️ May need to break into multiple sessions (context limits)

**Best For**: Users committed to specific AI platform, experimental use

**Tips**:
- Use longest context window available
- Save conversations/outputs frequently
- May need to summarize and continue in new chat if context fills up
- Copy agent definitions to a text file for easy reuse

---

## 🎯 Recommended Workflows by Platform

### Full Automation (Best Experience)
**Platform**: Claude Code CLI
**Best For**: Meta employees, power users
**Workflow**: Load agent → Run commands → Automatic file operations → Seamless handoff between agents

### Developer-Friendly
**Platform**: Cursor IDE or Windsurf
**Best For**: Developers, engineers
**Workflow**: Open in IDE → Reference agent files → IDE handles file I/O → Integrated experience

### No-Installation
**Platform**: Claude.ai Projects
**Best For**: Managers, non-technical users, anywhere access
**Workflow**: Upload files → Paste agent instructions → Copy/paste outputs → Manual file management

### Platform-Agnostic
**Platform**: Any AI with file upload
**Best For**: Experimentation, specific AI preferences
**Workflow**: Copy/paste agent definitions → Upload/paste inputs → Manual output saving

---

## 📝 Step-by-Step: Universal Workflow

**Regardless of platform, the process is the same**:

```
1. ORACLE (Data Collection)
   - Load oracle.agent.md
   - Run: start-data-collection
   - Provide employee info and files
   - Output: review-data.md

2. SORTING HAT (Categorization)
   - Load sorting-hat.agent.md
   - Provide: review-data.md (from step 1)
   - Run: start-categorization
   - Output: categorized-data.md

3. SHERLOCK (Quality Analysis)
   - Load sherlock.agent.md
   - Provide: categorized-data.md (from step 2)
   - Run: start-analysis
   - Output: enhanced-review-data.md

4. SHAKESPEARE (Review Writing)
   - Load shakespeare.agent.md
   - Provide: enhanced-review-data.md (from step 3)
   - Provide: template and style guide
   - Run: start-writing
   - Output: performance-review-v1.md

5. IRS (Peer Review)
   - Load irs.agent.md
   - Provide: performance-review-v1.md (from step 4)
   - Run: review-document performance-review-v1.md
   - Output: review-report-v1.md

6. ITERATE
   - Make changes based on IRS feedback
   - Create v2, v3, etc.
   - Re-review with IRS until ready
```

---

## 🔧 Platform Comparison Matrix

| Feature | Claude Code CLI | Cursor IDE | Claude.ai | Windsurf | Other AI |
|---------|----------------|------------|-----------|----------|----------|
| **File Reading** | ✅ Automatic | ✅ Automatic | ✅ Upload | ✅ Automatic | ⚠️ Varies |
| **File Writing** | ✅ Automatic | ✅ Automatic | ⚠️ Manual | ✅ Automatic | ⚠️ Manual |
| **PDF Support** | ✅ Native | ✅ Yes | ✅ Yes | ✅ Yes | ⚠️ Varies |
| **Meta MCP Tools** | ✅ Yes | ❌ No | ❌ No | ❌ No | ❌ No |
| **Setup Effort** | Low | Low | Very Low | Low | Medium |
| **Context Size** | Large | Large | Large | Large | Varies |
| **Cost** | Paid | Paid | Free/Paid | Paid | Varies |
| **Best For** | Meta users | Developers | Everyone | Developers | Specific needs |

---

## 💡 Tips for Success Across Platforms

### Universal Tips:
1. **Save Everything**: Keep all agent files and outputs organized
2. **One Agent at a Time**: Load one agent, complete its work, move to next
3. **Follow the Order**: Oracle → Sorting Hat → Sherlock → Shakespeare → IRS
4. **Iterative Process**: Multiple rounds of Shakespeare ↔ IRS is normal
5. **Context Management**: If context fills up, save work and continue in new chat

### Platform-Specific Tips:

**Claude Code CLI**:
- Use MCP tools for Meta URLs
- Let it handle file operations automatically
- Use background tasks for long operations

**Cursor/Windsurf**:
- Keep agent files open in tabs
- Use file explorer to track outputs
- Leverage IDE's file management

**Claude.ai**:
- Create Projects for each review
- Upload all files upfront
- Use Artifacts for long outputs
- Save outputs locally as you go

**Other Platforms**:
- Test context limits early
- Have backup copy/paste strategy
- Save progress frequently
- Be prepared to resume in new chat

---

## 🚨 Common Issues & Solutions

### "AI doesn't remember the agent persona"
**Solution**: Re-paste agent instructions, or keep agent file in context

### "File not found"
**Solution**:
- Claude Code/Cursor: Check file path
- Claude.ai: Re-upload file to Project
- Other: Copy/paste file contents directly

### "Output not saved"
**Solution**: Copy AI's response and manually save as file, then provide to next agent

### "Context limit reached"
**Solution**:
- Save current state
- Start new chat
- Provide summary + current files
- Continue workflow

### "Meta URLs not working"
**Solution**: Only Claude Code CLI has MCP tools. Other platforms: manually download and upload files

---

## 📚 Quick Reference Cards

### Claude Code CLI
```bash
cd prm-agent
claude
@agents/oracle.agent.md
start-data-collection
# Continue workflow...
```

### Cursor/Windsurf
```
Open folder in IDE
Open AI chat
@agents/oracle.agent.md "Act as this agent"
start-data-collection
# Continue workflow...
```

### Claude.ai
```
Create Project
Upload all files
"Read oracle.agent.md and act as Oracle"
start-data-collection
Copy outputs → Save → Upload for next agent
# Continue workflow...
```

---

## 🎓 Learning Path

**New Users**: Start with Claude.ai Projects (easiest, no setup)
**Developers**: Use Cursor or Windsurf (integrated experience)
**Meta Employees**: Use Claude Code CLI (full automation + MCP tools)
**Power Users**: Use Claude Code CLI (maximum control)

---

**Bottom Line**: PRM Agent is platform-agnostic! The agent files are just structured instructions that any AI assistant can follow. Choose the platform that fits your workflow.

---

**Need Help?** Check the README.md and QUICK_START.md for detailed workflows, or try the platform that requires the least setup for you!
