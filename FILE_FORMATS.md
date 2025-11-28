# Supported File Formats

PRM Agent supports multiple file formats for maximum flexibility.

## Supported Formats

All file-reading agents (Oracle, Shakespeare, IRS) accept:

| Format | Extension | Support Level | Use Case |
|--------|-----------|---------------|----------|
| **Markdown** | `.md` | ✅ Full | Native format, best for plain text |
| **PDF** | `.pdf` | ✅ Full | Text + visual extraction, common for formal docs |
| **Word** | `.doc`, `.docx` | ✅ Full | Full document support, corporate standard |
| **Text** | `.txt` | ✅ Full | Plain text, simple notes |

## Which Agents Support What

### Oracle (Data Gatherer)
✅ Reads all formats for:
- Self-review files
- Manager notes
- Peer feedback
- Downloaded URL content

### Shakespeare (Review Writer)
✅ Reads all formats for:
- Performance review templates
- Writing style guides
- Example reviews

### IRS (Peer Reviewer)
✅ Reads all formats for:
- Performance review drafts
- Any version (v1, v2, v3...)

### Other Agents
- **Sorting Hat**: Reads from Oracle's output (always .md)
- **Sherlock**: Reads from Sorting Hat's output (always .md)

## Examples

### Mixed Format Usage
```
input/
├── self-review.pdf          ← Employee's self-review (PDF)
├── manager-notes.docx       ← Your notes (Word)
├── peer-feedback-1.txt      ← Peer feedback (Text)
├── peer-feedback-2.pdf      ← More feedback (PDF)
├── template.doc             ← Company template (Word)
└── style-guide.md           ← Style guide (Markdown)
```

All work seamlessly together!

### Single Format Usage
```
input/
├── self-review.pdf
├── manager-notes.pdf
├── peer-feedback.pdf
├── template.pdf
└── style-guide.pdf
```

Also works perfectly!

## Format Capabilities

### PDF Support
- ✅ Text extraction
- ✅ Visual content interpretation
- ✅ Multi-page documents
- ✅ Formatted content
- ✅ Tables and lists

### Word Support
- ✅ Formatted text
- ✅ Headings and structure
- ✅ Tables
- ✅ Lists
- ✅ Comments (extracted as text)

### Markdown Support
- ✅ Native format
- ✅ Code blocks preserved
- ✅ Links maintained
- ✅ Formatting intact

### Text Support
- ✅ Plain text
- ✅ Simple and fast
- ✅ Universal compatibility

## Best Practices

1. **Use what you have**: Don't convert files - use them as-is
2. **Consistent naming**: Use clear filenames regardless of format
3. **Check readability**: Make sure PDFs aren't scanned images (OCR may be needed)
4. **File extensions**: Always include the correct extension

## Technical Details

PRM Agent leverages Claude Code's native `Read` tool, which supports:
- PDF text and visual extraction
- Word document parsing (.doc, .docx)
- Markdown rendering
- Plain text reading

No additional libraries or conversions needed!

## Limitations

**Not Currently Supported:**
- Scanned PDFs without OCR (image-only)
- Excel/Spreadsheet files (.xls, .xlsx) - convert to PDF or copy to text
- PowerPoint files (.ppt, .pptx) - export to PDF
- Image files (.jpg, .png) - unless embedded in supported formats
- Email files (.eml, .msg) - copy content to supported format

**Workarounds:**
- Scanned PDFs: Run OCR first or retype key points
- Excel: Export to PDF or copy relevant data to Word/text
- PowerPoint: Export slides to PDF
- Images: Embed in Word/PDF or describe in text
- Emails: Copy content to text/Word document

## FAQ

**Q: Can I mix formats?**
A: Yes! Use any combination of supported formats.

**Q: Which format is best?**
A: Use whatever format you already have. All work equally well.

**Q: Will PDFs slow down processing?**
A: No, Claude Code handles all formats efficiently.

**Q: Can I use Google Docs?**
A: Download as .docx or .pdf first, then use.

**Q: What about scanned documents?**
A: If they're searchable (OCR'd), they work. If image-only, you'll need to OCR them first.

**Q: Do tables and formatting matter?**
A: Yes! Agents can read formatted content including tables, lists, and structure.

---

**Bottom Line**: Use whatever format is convenient. PRM Agent handles them all! 🎉
