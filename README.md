
---

# 🧩 Checklist Review for VS Code


A Visual Studio Code extension that integrates markdown-based code review checklists directly into your editor. Part of the Checklist Review Toolchain, this extension helps developers ensure code quality and consistency before merging.

---

⚡️ **Supporting the Project**

> "Open source" does not mean "includes free support"

You can support the contributor and buy him a coffee.
[![coffee](https://www.buymeacoffee.com/assets/img/custom_images/black_img.png)](https://www.buymeacoffee.com/mpokornyetm)
Every second invested in an open-source project is a second you can't invest in your own family / friends / hobby.
That's the reason, why supporting the contributors is so important.

Thx very much for supporting us.

---

## ✨ Features

- Inline checklist rendering for markdown review files
- Visual indicators for completed/incomplete items
- Auto-validation on save or commit
- Integration with the `checklist-review-cli`
- Customizable checklist location and rules
- Works with local and remote repositories

---

## 📥 Installation

Install via the **Visual Studio Marketplace** or manually:

```bash
ext install checklist-review-vscode
```

Or search for `Checklist Review` in the Extensions tab.

---

## 📋 Usage Examples

### ✅ Example 1: Viewing a Checklist

1. Open `.github/review-checklist.md` in VS Code.
2. The extension highlights checklist items:
   - ✅ Completed items are marked green.
   - ❌ Incomplete items are marked red.
3. Hover over items to see validation status.

---

### ✅ Example 2: Auto-Validation on Save

If enabled in `.checklist-review.yml`:

```yaml
checklist:
  path: .github/review-checklist.md
  autoValidateOnSave: true
```

Then every time you save the checklist file, the extension will:
- Run validation using the CLI
- Show a notification if items are missing

---

### ✅ Example 3: Manual Validation

You can trigger validation manually:

1. Open the Command Palette (`Ctrl+Shift+P`)
2. Run: `Checklist Review: Validate Checklist`
3. Results will appear in the output panel

---

### ✅ Example 4: Git Integration

When committing code:
- If the checklist is incomplete, the extension can block the commit (if configured)
- You’ll see a warning and a list of missing items

---

## ⚙️ Configuration

Add a `.checklist-review.yml` file to your project root:

```yaml
checklist:
  path: .github/review-checklist.md
  required: true
  autoValidateOnSave: true
  blockCommitIfIncomplete: true
```

---

## 🔌 Integration

This extension works best when paired with:

- `checklist-review-cli`
- CI/CD plugins for Jenkins and Azure DevOps *(coming soon)*

---

## 🛠 Development

Clone the repo and run the extension locally:

```bash
git clone https://github.com/your-org/checklist-review-vscode
cd checklist-review-vscode
npm install
code .
```

Press `F5` to launch the extension in a new VS Code window.

---

## 📄 License

MIT License. See LICENSE for details.

---

## 🤝 Contributing

We welcome contributions! Please see CONTRIBUTING.md for guidelines.

---

## 📬 Contact

Maintained by Martin Pokorný. For issues, use the GitHub issue tracker.

---

Would you like me to help you generate a matching `CONTRIBUTING.md` or add marketplace metadata like `extension.json` next?
