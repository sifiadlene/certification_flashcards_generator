# Azure & GitHub Certification Flashcards

High-quality, exam-realistic flashcards for Azure and GitHub certifications, designed for use with [Anki](https://apps.ankiweb.net/) spaced repetition software.

## 📚 Available Flashcard Decks

All flashcard files are located in the [`flashcards/`](flashcards/) directory:

- **AI-102**: Microsoft Azure AI Engineer Associate
- **AI-900**: Microsoft Azure AI Fundamentals
- **AZ-104**: Microsoft Azure Administrator
- **AZ-204**: Developing Solutions for Microsoft Azure
- **AZ-305**: Designing Microsoft Azure Infrastructure Solutions
- **GH-300**: GitHub Foundations

> 💡 **Want more flashcards?** See [Generating New Flashcards](#-generating-new-flashcards) to learn how to generate additional flashcards for these or other Azure/GitHub certifications.

## ✨ Features

- **Exam-Realistic Questions**: Scenario-based questions that mirror actual certification exams
- **Three-Option Format**: Each question includes three plausible answer choices
- **Detailed Explanations**: Every answer includes justification and reference links to official documentation
- **Valuable Insights**: Extra field with architectural comparisons, common pitfalls, and decision frameworks
- **Organized Tags**: Tagged by exam, domain, and topic for easy filtering

## 🚀 Getting Started

### Prerequisites

- [Anki](https://apps.ankiweb.net/) desktop application (free, available for Windows, Mac, and Linux)

### Importing Flashcards into Anki

1. **Download the CSV file** for your desired certification from the [`flashcards/`](flashcards/) directory

2. **Open Anki** and select or create a deck for your flashcards

3. **Import the file**:
   - Go to **File → Import** (or press `Ctrl+Shift+I` / `Cmd+Shift+I` on Mac)
   - Select the downloaded CSV file

4. **Configure import settings**:
   - **Type**: Choose "Basic" or create a custom note type (see below)
   - **Deck**: Select your target deck
   - **Fields separated by**: Comma
   - **Field mapping**:
     - Field 1 → Front
     - Field 2 → Back
     - Field 3 → Extra (if using custom note type)
     - Field 4 → Tags
   - ⚠️ **Important**: Check **"Allow HTML in fields"** to render formatting properly

5. **Click Import**

### Creating a Custom Note Type (Recommended)

For the best experience with the Extra field:

1. In Anki, go to **Tools → Manage Note Types**
2. Click **Add → Clone: Basic**
3. Name it "Certification Flashcard" or similar
4. Click **Fields** and add a field called "Extra"
5. Click **Cards** and edit the back template to include the Extra field:

```html
{{FrontSide}}

<hr id=answer>

{{Back}}

{{#Extra}}
<br><br>
<div style="color: #666; font-size: 90%; border-left: 3px solid #ccc; padding-left: 10px; margin-top: 15px;">
  <strong>💡 Additional Insight:</strong><br>
  {{Extra}}
</div>
{{/Extra}}
```

6. Use this note type when importing your flashcards

## 🤖 Generating New Flashcards

This repository includes a GitHub Copilot agent that can generate additional flashcards. The agent is located at [`.github/agents/flashcards_generator.agent.md`](.github/agents/flashcards_generator.agent.md).

### Using the Flashcard Generator Agent

If you have GitHub Copilot enabled in VS Code:

1. Open the Command Palette (`Ctrl+Shift+P` / `Cmd+Shift+P`)
2. Type and select "GitHub Copilot: Chat"
3. Use the `@flashcards_generator` agent with your desired certification

**Example prompts:**
```
@flashcards_generator Generate 20 flashcards for AZ-305 focusing on networking

@flashcards_generator Create flashcards for AZ-104 identity and governance

@flashcards_generator Generate 15 advanced difficulty flashcards for AZ-204
```

**Input Parameters:**
- **Exam Certification**: Required (e.g., AZ-305, AZ-104, GH-300)
- **Number of Flashcards**: Optional, default is 50
- **Topic Focus**: Optional (e.g., "networking", "security", "identity")
- **Difficulty Level**: Optional (e.g., "intermediate", "advanced")

The agent will:
- Research current exam objectives and patterns
- Generate high-quality, diverse questions
- Create a CSV file named `{exam}_flashcards_{YYYY-MM-DD}.csv`
- Include reference links to official Microsoft documentation

## 📖 Flashcard Structure

Each flashcard contains:

- **Front**: Scenario-based question with three answer options (A, B, C)
- **Back**: Correct answer with brief justification and reference link
- **Extra**: Architectural insights, comparisons, and decision frameworks
- **Tags**: Organized by exam, domain, and topic (e.g., "AZ-305 Networking VPN")

## 🎯 Study Tips

1. **Use Tags**: Filter cards by specific domains or topics you need to focus on
2. **Review Extra Field**: The additional insights help build deeper understanding
3. **Follow Reference Links**: Read official documentation for comprehensive knowledge
4. **Consistent Study**: Use Anki's spaced repetition algorithm—study daily for best results
5. **Mark Difficult Cards**: Flag challenging questions to review them more frequently

## 📝 Contributing

Contributions are welcome! If you'd like to:
- Add flashcards for additional certifications
- Improve existing questions
- Fix errors or update outdated information

Please open an issue or submit a pull request.

## 📄 License

This project is provided as-is for educational purposes.

## 🔗 Useful Resources

- [Microsoft Learn](https://learn.microsoft.com/) - Official Azure documentation
- [Anki Manual](https://docs.ankiweb.net/) - Learn more about using Anki effectively
- [Azure Architecture Center](https://learn.microsoft.com/azure/architecture/) - Best practices and reference architectures

## ⚠️ Disclaimer

These flashcards are study aids and should be used alongside official Microsoft certification materials. They are not affiliated with or endorsed by Microsoft Corporation or GitHub.

---

**Good luck with your certification journey! 🚀**

