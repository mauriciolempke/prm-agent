# PRM Agent - Performance Review Workflow System

**Performance Review Management Agent System** - A multi-agent workflow for creating exceptional performance reviews across any AI platform.

---

## 🌐 Works Across All AI Platforms

PRM Agent is **platform-agnostic** and works with:
- ✅ **Claude Code CLI** (Recommended - full automation support)
- ✅ **Cursor IDE** (Great for developers)
- ✅ **Claude.ai** (Web interface - no installation needed)
- ✅ **Windsurf IDE** (AI-native development environment)
- ✅ **Any AI Assistant** (ChatGPT, Gemini, etc. with file support)

**📖 See [PLATFORM_GUIDE.md](PLATFORM_GUIDE.md) for detailed setup instructions for each platform.**

---

## 🎯 What is PRM Agent?

PRM Agent is an AI-powered workflow system that guides you through creating thorough, defensible, and impactful performance reviews. Inspired by the BMAD-METHOD, it uses **5 specialized AI agents** working together to transform raw performance data into polished review documents.

### Why PRM Agent?

- ✅ **Platform-Agnostic**: Works with Claude Code CLI, Cursor, Claude.ai, or any AI assistant
- ✅ **Structured Process**: Clear step-by-step workflow from data → final review
- ✅ **Quality Assurance**: Multi-stage validation ensures completeness
- ✅ **No Hallucinations**: Agents only use data you provide
- ✅ **Level-Aware Calibration**: Questions and ratings calibrated to employee level
- ✅ **URL Handling**: Can fetch and incorporate content from web URLs
- ✅ **Multiple Formats**: Supports PDF, Word, Markdown, and text files
- ✅ **Template-Driven**: Adapts to your company's review format
- ✅ **Iterative**: Full control at every step
- ✅ **No Lock-In**: Use your preferred AI tool

---

## 🤖 Meet Your Agent Team

### 1. **Oracle** - The Data Gatherer
*"I collect and organize performance data with precision."*

**What Oracle Does**:
- Collects employee information including **level/grade**
- Collects self-reviews, manager notes, and peer feedback
- **Can automatically fetch web URLs** (when supported by the platform)
- Handles external URL references (guides you to download)
- Confirms accuracy at every step
- Never hallucinates - only uses your provided data

**URL Integration** ✨:
- Web content - can attempt automatic fetching
- Documents - guidance for manual download
- No manual downloading needed for accessible links!

**Output**: `review-data.md` - Structured raw data file

---

### 2. **The Sorting Hat** - The Categorizer
*"I sort your data into meaningful performance categories."*

**What The Sorting Hat Does**:
- Organizes data into performance categories
- Works item-by-item with your guidance
- Maintains source attribution
- Allows re-categorization anytime

**Categories** (Customizable):
1. Strengths
2. Areas of Improvement
3. Peer Review
4. Others
5. (Custom categories as needed)

**Output**: `categorized-data.md` - Organized by category

---

### 3. **Sherlock** - The Quality Analyst
*"I ensure every claim is clear, evidenced, and impactful."*

**What Sherlock Does**:
- Enriches each item with context, evidence, and impact
- **Calibrates questions based on employee level/grade**
- Asks 3 key questions per item: Context? Evidence? Impact?
- Adjusts impact bar by level (junior: task-level, senior: org-level)
- Collects item ratings (+/=/-)
- Collects category ratings (MS/MM/CMA/EE/GE/RE)
- Ensures no gaps or vague statements

**Quality Checks**:
- ✓ Contextual Clarity - Can any reader understand it?
- ✓ Evidence-Based - Are there metrics/data?
- ✓ Impact Articulated - Why did it matter?
- ✓ Level-Appropriate - Does scope match employee level?

**Output**: `enhanced-review-data.md` - Rich, rated data

---

### 4. **Shakespeare** - The Review Writer
*"I transform data into compelling performance narratives."*

**What Shakespeare Does**:
- Uses your template and writing style guide
- Writes section-by-section with your approval
- Adheres to word count limits
- Creates thesis with "why not higher/lower" justifications
- Manages multiple versions (v1, v2, v3...)

**Output**: `performance-review-v1.md` (and subsequent versions)

---

### 5. **The IRS** - The Impartial Reviewer
*"I'm your calibration partner who asks the tough questions."*

**What The IRS Does**:
- Reviews ONLY the draft (maintains independence)
- **Calibrates review to employee level/grade**
- Asks level-appropriate critical calibration questions
- Challenges scope/rating claims that don't match level
- Checks grammar, thesis, completeness, impact
- Provides actionable feedback
- Helps make your review defensible

**Level-Aware Calibration**:
- Junior: Are claims realistic for early-career?
- Mid-level: Is this leadership or just execution?
- Senior: Is scope truly significant and cross-functional?
- Challenges over/under-rating based on evidence vs. level bar

**Output**: `review-report-[filename].md` - Detailed feedback

---

## 🚀 Getting Started - Choose Your Platform

### Option 1: Claude Code CLI (Recommended)
**Best for**: Power users, full automation

```bash
cd prm-agent
claude
@agents/oracle.agent.md
start-data-collection
```

**Advantages**:
- ✅ Automatic file operations
- ✅ Advanced URL fetching capabilities
- ✅ Seamless workflow

### Option 2: Cursor or Windsurf IDE
**Best for**: Developers, engineers

```
1. Open prm-agent folder in IDE
2. Open AI chat
3. @agents/oracle.agent.md "Act as this agent"
4. start-data-collection
```

**Advantages**:
- ✅ Integrated development environment
- ✅ File system access
- ✅ Familiar workflow

### Option 3: Claude.ai (Web - No Installation)
**Best for**: Managers, non-technical users, anywhere access

```
1. Create a Project on claude.ai
2. Upload all agent files + your input files
3. Say: "Read oracle.agent.md and act as Oracle"
4. start-data-collection
5. Copy outputs and save as files
```

**Advantages**:
- ✅ No installation required
- ✅ Works anywhere
- ✅ Easy to share

### Option 4: Other AI Assistants
**Best for**: Specific AI platform preferences

```
1. Copy agent file content
2. Paste into AI chat
3. Upload/paste input files
4. Follow agent workflows
5. Save outputs manually
```

**See [PLATFORM_GUIDE.md](PLATFORM_GUIDE.md) for complete instructions for each platform.**

---

## 📋 Complete Workflow

```
┌─────────────────────────────────────────────────────────┐
│  1. ORACLE - Data Collection                            │
│     • Gather self-review, manager notes, peer feedback  │
│     • Handle URLs and supplementary docs                │
│     Output: review-data.md                              │
└────────────────┬────────────────────────────────────────┘
                 │
                 ▼
┌─────────────────────────────────────────────────────────┐
│  2. THE SORTING HAT - Categorization                    │
│     • Sort into 8 performance categories                │
│     • Maintain source attribution                       │
│     Output: categorized-data.md                         │
└────────────────┬────────────────────────────────────────┘
                 │
                 ▼
┌─────────────────────────────────────────────────────────┐
│  3. SHERLOCK - Quality Analysis & Rating                │
│     • Enrich with context, evidence, impact             │
│     • Collect item signals (+/=/-)                      │
│     • Collect category ratings (MS/MM/CMA/EE/GE/RE)     │
│     Output: enhanced-review-data.md                     │
└────────────────┬────────────────────────────────────────┘
                 │
                 ▼
┌─────────────────────────────────────────────────────────┐
│  4. SHAKESPEARE - Review Writing                        │
│     • Apply template and style guide                    │
│     • Write section-by-section                          │
│     • Create thesis with rating justification           │
│     Output: performance-review-v1.md, v2.md, v3.md...   │
└────────────────┬────────────────────────────────────────┘
                 │
                 ▼
┌─────────────────────────────────────────────────────────┐
│  5. THE IRS - Peer Review                               │
│     • Independent review of draft                       │
│     • Critical calibration questions                    │
│     • Actionable feedback                               │
│     Output: review-report-[filename].md                 │
└─────────────────────────────────────────────────────────┘
                 │
                 ▼
          [Iterate as needed]
                 │
                 ▼
          ✅ Final Review Ready!
```

---

## 🚀 Getting Started

### Prerequisites
- Claude Code CLI installed and running
- Input files ready (in any supported format):
  - Employee self-review (`.md`, `.pdf`, `.doc`, `.docx`, `.txt`)
  - Your manager notes (`.md`, `.pdf`, `.doc`, `.docx`, `.txt`)
  - Peer feedback (`.md`, `.pdf`, `.doc`, `.docx`, `.txt`)
  - Performance review template - optional (`.md`, `.pdf`, `.doc`, `.docx`, `.txt`)
  - Writing style guide - optional (`.md`, `.pdf`, `.doc`, `.docx`, `.txt`)

**Supported File Formats:**
- **Markdown** (`.md`) - Native support
- **PDF** (`.pdf`) - Full text and visual extraction
- **Word Documents** (`.doc`, `.docx`) - Full document support
- **Text Files** (`.txt`) - Plain text support

Claude Code's Read tool natively supports all these formats, so Oracle, Shakespeare, and all agents can read them directly.

### Directory Structure

```
your-project/
├── prm-agent/
│   ├── agents/
│   │   ├── oracle.agent.md
│   │   ├── sorting-hat.agent.md
│   │   ├── sherlock.agent.md
│   │   ├── shakespeare.agent.md
│   │   └── irs.agent.md
│   ├── [employee-name]/              # Created by Oracle
│   │   ├── input/                    # Your input files
│   │   │   ├── self-review.pdf
│   │   │   ├── manager-notes.md
│   │   │   ├── peer-feedback.pdf
│   │   │   ├── template.md
│   │   │   └── style-guide.md
│   │   └── output/                   # Generated outputs
│   │       ├── review-data.md
│   │       ├── categorized-data.md
│   │       ├── enhanced-review-data.md
│   │       ├── performance-review-v1.md
│   │       └── review-report-*.md
│   └── resources/
└── WORKFLOW_DEVELOPMENT.md
```

**Note**: The employee-specific folder structure (`./[employee-name]/`) is created automatically by Oracle after you provide the employee's name and level.

### Step-by-Step Usage

#### Step 1: Start with Oracle
1. Load the Oracle agent in Claude Code
2. Say: `start-data-collection`
3. Oracle will ask for employee name and level
4. **Oracle creates the employee's folder structure**: `./[employee-name]/input/` and `./[employee-name]/output/`
5. Place your input files in the employee's input folder:
   - Self-review file (`.md`, `.pdf`, `.doc`, `.docx`, or `.txt`)
   - Manager notes file (any supported format)
   - Peer feedback file(s) (any supported format)
   - Template (optional, any supported format)
   - Style guide (optional, any supported format)
6. Continue following Oracle's prompts to collect all data
7. Oracle will generate: `./[employee-name]/output/review-data.md`

#### Step 2: Categorize with The Sorting Hat
1. Load The Sorting Hat agent
2. Say: `start-categorization`
3. Provide employee name when asked
3. Categorize each item into performance dimensions
4. Sorting Hat will generate: `./[employee-name]/output/categorized-data.md`

#### Step 3: Analyze with Sherlock
1. Load Sherlock agent
2. Say: `start-analysis`
3. Provide employee name when asked
4. Answer the 3 quality questions for each item
5. Provide item ratings (+/=/-)
6. Provide category ratings (MS/MM/CMA/EE/GE/RE)
7. Sherlock will generate: `./[employee-name]/output/enhanced-review-data.md`

#### Step 4: Write with Shakespeare
1. Load Shakespeare agent
2. Say: `start-writing`
3. Provide employee name when asked
4. Provide template and style guide files from employee's input folder
5. Approve each section as Shakespeare writes
6. Provide overall rating
7. Approve thesis
8. Shakespeare will generate: `./[employee-name]/output/performance-review-v1.md`

#### Step 5: Review with The IRS
1. Load The IRS agent
2. Say: `review-document performance-review-v1.md`
3. Provide employee name when asked
4. The IRS will generate: `./[employee-name]/output/review-report-performance-review-v1.md`
5. Review the feedback
6. Make changes (Shakespeare can create v2, v3, etc.)
7. Request new reviews as needed

---

## 💡 Pro Tips

### For Best Results:

**With Oracle**:
- Be thorough in data collection - more data = better review
- Download important URLs as files for Oracle to read
- Confirm accuracy at each step

**With The Sorting Hat**:
- When in doubt, choose the most specific category
- Use "Others" sparingly - most items fit somewhere
- You can always recategorize later

**With Sherlock**:
- Be generous with context - explain like the reader knows nothing
- Add concrete metrics whenever possible
- Ratings guide Shakespeare's emphasis in writing

**With Shakespeare**:
- Provide a good template and style guide for best results
- Review each section carefully before approving
- Use version control - keep v1, v2, v3 for comparison

**With The IRS**:
- Take the feedback seriously - these are calibration questions
- Don't argue with The IRS - make the document stronger instead
- Do multiple review rounds until The IRS says "ready"

---

## 📊 Rating System Reference

### Item Signals (Sherlock)
- **`+`** = Above expectations (exceptional, standout work)
- **`=`** = Aligned with expectations (solid, expected performance)
- **`-`** = Below expectations (needs improvement)

### Category Ratings (Sherlock)
- **RE** = Redefines Expectations (exceptional, industry-leading)
- **GE** = Greatly Exceeds (significant impact beyond role)
- **EE** = Exceeds Expectations (strong performance, clear impact)
- **CMA** = Consistently Meets All Expectations (solid performance)
- **MM** = Meets Most (generally good with some gaps)
- **MS** = Meets Some (needs improvement in this area)

---

## 🎓 Example: Complete Flow

```
You: "I need to write a performance review for my direct report Jane"

[Load Oracle]
You: start-data-collection
Oracle: Collects self-review, your notes, peer feedback
Result: output/review-data.md

[Load Sorting Hat]
You: start-categorization
Sorting Hat: Sorts 15 items into categories
Result: output/categorized-data.md

[Load Sherlock]
You: start-analysis
Sherlock: Enriches each item, collects ratings
You: Provide context, evidence, impact for each item
You: Rate items (+/=/−) and categories (MS/MM/CMA/EE/GE/RE)
Result: output/enhanced-review-data.md

[Load Shakespeare]
You: start-writing
Shakespeare: Writes review section-by-section
You: Approve each section, provide overall rating
Result: output/performance-review-v1.md

[Load IRS]
You: review-document performance-review-v1.md
IRS: Reviews and finds 3 issues
Result: output/review-report-performance-review-v1.md

[Back to Shakespeare]
You: Make changes based on IRS feedback
Result: output/performance-review-v2.md

[Back to IRS]
You: review-document performance-review-v2.md
IRS: "Ready for submission!"
Result: output/review-report-performance-review-v2.md

✅ Done!
```

---

## 🔧 Customization

### Adding Custom Categories
The Sorting Hat supports custom categories:
1. During categorization, say: `add-category`
2. Provide category name and description
3. Items can now be sorted to your custom category

### Different Templates
Shakespeare adapts to any template:
1. Format your template with section names and word counts
2. Provide to Shakespeare during setup
3. Shakespeare will match the structure exactly

### Different Writing Styles
Shakespeare matches your style guide:
1. Provide example reviews or style guide
2. Shakespeare will analyze and match the tone
3. You can request style changes anytime with `change-style`

---

## 📚 Documentation

- **WORKFLOW_DEVELOPMENT.md** - Complete design documentation
- **agents/*.agent.md** - Individual agent documentation
- Each agent file contains:
  - Role and principles
  - Commands and workflows
  - Examples and constraints
  - Output formats

---

## 🤝 Contributing

Contributions, feedback, and suggestions are welcome! This project is open source and built for the community.

**Ways to Contribute:**
- 🐛 **Report bugs** - Open an issue on GitHub
- 💡 **Suggest features** - Share your ideas for improvements
- 📖 **Improve documentation** - Help make the guides clearer
- 🔧 **Submit pull requests** - Add new features or fix issues
- 🎨 **Create variations** - Adapt for different review styles or industries
- 💬 **Share feedback** - Tell us what works and what doesn't

**How to Contribute:**
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

**Questions or Ideas?**
Open an issue on GitHub or reach out on LinkedIn!

---

## 📝 License

MIT License - Free to use, modify, and distribute.

Copyright (c) 2024 Mauricio Lempke

See the [LICENSE](LICENSE) file for full details.

**You are free to:**
- ✅ Use commercially
- ✅ Modify and customize
- ✅ Distribute and share
- ✅ Use privately

**Under the condition that:**
- You include the original copyright notice and license

---

## 🙏 Acknowledgments

**Created by**: Mauricio Lempke

Inspired by the **BMAD-METHOD** multi-agent architecture.

Built for managers who want to write thoughtful, thorough, and defensible performance reviews.

**Special Thanks:**
- The AI agent community for pioneering multi-agent workflows
- All engineering managers who spend countless hours writing thoughtful reviews
- Contributors and users who provide feedback and suggestions

---

**Ready to start?** Load Oracle and begin your performance review journey!

```
Load: prm-agent/agents/oracle.agent.md
Say: start-data-collection
```

---

*PRM Agent - Performance reviews done right, one agent at a time.*
