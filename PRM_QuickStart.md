# PRM Agent Quick Start Guide

Get started with your first performance review in 5 simple steps - **works on any AI platform!**

---

## 🌐 Choose Your Platform

PRM Agent works with any AI assistant. Pick what works for you:

- **Claude Code CLI** - Full automation, advanced capabilities
- **Cursor/Windsurf IDE** - Developer-friendly
- **Claude.ai** - No installation, web-based
- **Other AI** - ChatGPT, Gemini, etc.

**📖 Detailed platform instructions**: See [PLATFORM_GUIDE.md](PLATFORM_GUIDE.md)

---

## ⚡ Quick Setup (5 minutes)

### 1. Understand the Folder Structure
The PRM Agent now creates **employee-specific folders** automatically:
- After you provide employee name and level to Oracle, a folder `./[employee-name]/` is created
- Inside: `./[employee-name]/input/` for your files
- Inside: `./[employee-name]/output/` for generated outputs
- Each employee's review work stays in their own folder

### 2. Prepare Your Files
You'll place files in the employee's input folder after Oracle creates it.

**Supported Formats:** `.md`, `.pdf`, `.doc`, `.docx`, `.txt`

**Required:**
- `self-review.pdf` - Employee's self-review
- `manager-notes.*` - Your 1:1 notes and observations (any format)
- `peer-feedback.pdf` - Peer feedback

**Note:** Oracle will tell you where to place these files after creating the employee's folder.

**Optional but Recommended:**
- `template.*` - Your company's review template (any format)
- `style-guide.*` - Writing style examples (any format)

**Workflow:**
1. Start Oracle and provide employee name/level
2. Oracle creates `./[employee-name]/input/` and `./[employee-name]/output/`
3. Place your files in the employee's input folder
4. Continue with Oracle's data collection process

**Examples of files you'll add:**
- `./jane-smith/input/self-review.pdf`
- `./jane-smith/input/manager-notes.md` (your own notes)
- `./jane-smith/input/peer-feedback.pdf`
- `./jane-smith/input/template.doc`
- `./jane-smith/input/style-guide.md`

### 3. Load Your First Agent

**Choose your method based on platform**:

#### Claude Code CLI:
```bash
cd prm-agent
claude
@agents/oracle.agent.md
```

#### Cursor/Windsurf IDE:
```
1. Open prm-agent folder in IDE
2. Open AI chat (Cmd+L or Ctrl+L)
3. @agents/oracle.agent.md "Act as this agent"
```

#### Claude.ai:
```
1. Create a Project
2. Upload agents/oracle.agent.md
3. Say: "Read oracle.agent.md and act as the Oracle agent"
```

#### Other AI Assistants:
```
1. Copy contents of agents/oracle.agent.md
2. Paste into chat with: "Please act as this agent: [paste content]"
```

### 4. Start the Process

**Same for all platforms**:
```
start-data-collection
```

### 5. Follow the Flow

**Same workflow regardless of platform**:
```
Oracle → Sorting Hat → Sherlock → Shakespeare → IRS
```

**Platform difference**: File handling
- Claude Code/Cursor/Windsurf: Automatic file creation
- Claude.ai/Other: Copy outputs and save manually

---

## 🎯 The 5-Agent Journey

### Agent 1: Oracle (30 min)
**What you'll do**: Answer questions about the employee and provide file locations

**Important**: Oracle will create the employee's folder structure (`./[employee-name]/input/` and `./[employee-name]/output/`) right after you provide their name and level.

**Commands to know**:
- `start-data-collection` - Begin
- `list-data` - See what's collected
- `export-data-file` - Finish

**Output**: `./[employee-name]/output/review-data.md`

---

### Agent 2: The Sorting Hat (20 min)
**What you'll do**: Categorize each data point into performance dimensions

**Note**: Sorting Hat will ask for the employee name to locate their folder.

**Commands to know**:
- `start-categorization` - Begin
- `view-categories` - See current state
- `export-categorized-data` - Finish

**Output**: `./[employee-name]/output/categorized-data.md`

---

### Agent 3: Sherlock (60 min)
**What you'll do**: Enrich each item with context, evidence, and impact ratings

**Note**: Sherlock will ask for the employee name to locate their folder.

**Commands to know**:
- `start-analysis` - Begin
- `view-progress` - Check which categories done
- `view-ratings-summary` - See all ratings
- `export-enhanced-data` - Finish

**Output**: `./[employee-name]/output/enhanced-review-data.md`

**Remember**: For each item, answer:
1. Context? (What was it?)
2. Evidence? (Metrics/data?)
3. Impact? (Why did it matter?)
4. Signal? (+/=/-)

Then for each category, provide rating: BE/ME/EE/GE

---

### Agent 4: Shakespeare (45 min)
**What you'll do**: Review and approve each section, provide overall rating

**Note**: Shakespeare will ask for the employee name to locate their folder and enhanced data.

**Commands to know**:
- `start-writing` - Begin
- `revise-section` - Change a section
- `view-draft` - See current state
- `export-final-review` - Finish

**Output**: `./[employee-name]/output/performance-review-v1.md`

**Remember**:
- Provide template and style guide when asked
- Approve each section before moving forward
- Give overall rating before thesis
- All versions are saved (v1, v2, v3...)

---

### Agent 5: The IRS (15 min per round)
**What you'll do**: Read feedback and make improvements

**Note**: The IRS will ask for the employee name to locate their folder and review documents.

**Commands to know**:
- `review-document performance-review-v1.md` - Begin
- `fresh-review` - Review updated version

**Output**: `./[employee-name]/output/review-report-[filename].md`

**Remember**:
- The IRS only reads the draft (stays independent)
- Make changes in Shakespeare, then ask IRS for new review
- Iterate until IRS says "ready for submission"

---

## 📝 Example Session

```bash
# Step 1: Load Oracle
[Load prm-agent/agents/oracle.agent.md in Claude Code]

You: start-data-collection
Oracle: What is the employee's name?
You: Jane Smith
Oracle: What is Jane's role?
You: Senior Software Engineer
Oracle: What is the review period?
You: Jan 2024 - Dec 2024
Oracle: Please provide the self-review file...
You: self-review.pdf
[Continue until Oracle says "export-data-file"]

# Step 2: Load The Sorting Hat
[Load prm-agent/agents/sorting-hat.agent.md]

You: start-categorization
Sorting Hat: Item 1 of 15: "Led API redesign..." Which category?
You: 1 (Strengths)
[Continue for all items]

# Step 3: Load Sherlock
[Load prm-agent/agents/sherlock.agent.md]

You: start-analysis
Sherlock: Let's examine the first category...
Sherlock: Context Check: Does this have enough information?
You: Add: It was the payment processing API...
[Continue for all categories]

# Step 4: Load Shakespeare
[Load prm-agent/agents/shakespeare.agent.md]

You: start-writing
Shakespeare: Please provide template file
You: template.pdf
Shakespeare: Please provide style guide
You: style-guide.docx
Shakespeare: Here's the first section draft...
You: Perfect
[Continue for all sections]

# Step 5: Load The IRS
[Load prm-agent/agents/irs.agent.md]

You: review-document performance-review-v1.md
IRS: [Generates review report with feedback]
You: [Make changes in Shakespeare → v2]
You: review-document performance-review-v2.md
IRS: Ready for submission!

✅ Done!
```

---

## ⏱️ Time Estimates

| Agent | Time | What Takes Time |
|-------|------|-----------------|
| Oracle | 30 min | Gathering files, confirming data |
| Sorting Hat | 20 min | Categorizing 15-20 items |
| Sherlock | 60 min | Enriching items, providing ratings |
| Shakespeare | 45 min | Reviewing sections, approving drafts |
| IRS | 15 min/round | Reading feedback, 2-3 rounds typical |

**Total**: ~3 hours for a thorough review

---

## 💡 Pro Tips for First-Timers

1. **Prepare files beforehand** - Have all inputs ready before starting Oracle
2. **Don't rush Sherlock** - This is where quality is built
3. **Be generous with context** - More details = better review
4. **Use real metrics** - Numbers make everything more credible
5. **Take IRS feedback seriously** - Those are calibration questions
6. **Keep all versions** - v1, v2, v3 help you see progress
7. **Take breaks** - 3 hours is a lot, split across days if needed

---

## 🆘 Troubleshooting

### "Oracle isn't reading my file"
- Check file is in `prm-agent/input/` folder
- Provide full filename with extension
- Make sure file isn't empty

### "Sorting Hat lost track of items"
- Use `view-categories` to see current state
- Use `restart-categorization` to start over if needed

### "Sherlock is asking too many questions"
- That's normal! Quality takes time
- You can use `skip-category` if a category doesn't apply
- Use `remove-item` to remove irrelevant items

### "Shakespeare's draft doesn't match my style"
- Provide a better style guide example
- Use `change-style` to request adjustments
- Use `revise-section` to rewrite specific sections

### "The IRS is too critical"
- The IRS is designed to be tough - it's helping you!
- Address the feedback and request another review
- Think of it as calibration practice

---

## 📁 File Checklist

Before starting, make sure you have:

**Required**:
- [ ] Employee self-review file (any format: .md, .pdf, .doc, .docx, .txt)
- [ ] Your manager notes file (any format: .md, .pdf, .doc, .docx, .txt)
- [ ] Peer feedback file (any format: .md, .pdf, .doc, .docx, .txt)

**Highly Recommended**:
- [ ] Performance review template (any format)
- [ ] Writing style guide or example reviews (any format)

**Optional**:
- [ ] Links to relevant documents or posts
- [ ] Project deliverables documentation
- [ ] Metrics/data spreadsheets

---

## 🎓 Your First Review

Follow these agents in order:

1. **Oracle** → Collect all data
2. **Sorting Hat** → Organize into categories
3. **Sherlock** → Enrich with quality
4. **Shakespeare** → Write the review
5. **IRS** → Validate and improve

Each agent builds on the previous one.

---

## 🚀 Ready to Start?

```bash
# Start in the prm-agent directory
cd prm-agent

# Load Oracle in Claude Code
# File: prm-agent/agents/oracle.agent.md

# Say this:
start-data-collection

# Oracle will:
# 1. Ask for employee name and level
# 2. Create ./[employee-name]/input/ and ./[employee-name]/output/
# 3. Guide you to place files in the employee's input folder
# 4. Continue with data collection
```

**You're ready!** Follow Oracle's prompts and enjoy the journey.

---

*Questions? Check the full README.md or individual agent files for detailed documentation.*
