# How to Contribute to Open Lab

You do not need to know Git, write code, or understand GitHub to contribute to Open Lab.

If you have experience, an idea, a question, a better approach, or you've tried one of these tools and learned something from it, you already have something useful to contribute.

Start wherever you're comfortable.

## First: A Few GitHub Words

GitHub has its own vocabulary.

You only need a handful of terms to get started.

**Repository (repo)**  
The shared Open Lab project and everything in it — tools, documentation, discussions, and contribution history.

**Issue**  
A conversation about a problem, question, idea, or possible improvement.

Opening an Issue does not change anything in the repository.

**Fork**  
Your own copy of the Open Lab repository.

You can experiment in your fork without changing the shared version.

**Branch**  
A separate workspace for a particular change.

**Commit**  
A saved checkpoint describing a change you made.

**Pull Request (PR)**  
Essentially:

*"I made these changes. Should we bring them into the shared version?"*

That's enough GitHub vocabulary to participate.

---
## Where Should I Start?

Not every contribution needs to begin with a file change.

Open Lab has a few different places to start depending on what you want to do.

### Start a Discussion

Use a **Discussion** when you want to explore something.

Maybe you:

- have a question for other practitioners;
- want to compare approaches;
- have an idea that isn't fully formed yet;
- want to share something you've learned;
- are wondering whether other people see the same problem;
- want feedback before building something.

A Discussion doesn't need to end with a change.

Sometimes the conversation itself is useful.

### Open an Issue

Use an **Issue** when you've identified something specific that should be investigated or improved.

Maybe:

- something doesn't work;
- instructions are confusing;
- an assumption doesn't fit your environment;
- information is missing;
- you've found an accessibility problem;
- you have a concrete idea for a new tool or improvement.

You don't need to know how to fix it.

Identifying the problem is a contribution.

### Submit a Pull Request

Use a **Pull Request** when you've actually made a change you'd like Open Lab to consider.

That might mean:

- correcting documentation;
- improving an existing tool;
- adding an example or variant;
- improving accessibility;
- contributing a new artifact;
- changing how Open Lab itself works.

### Just Want the Tool?

You don't have to contribute anything.

Source lives in the repository.

When packaged versions are available, **Releases** provide ready-to-use copies in practical formats.

Use the work.

If you eventually find something worth changing, come back.

---

# Path A: I Just Want to Help

If GitHub is new to you, start here.

You can participate through your web browser.

## The Easiest Contribution: Open an Issue

Maybe:

- a question doesn't make sense;
- a tool doesn't work in your environment;
- something important is missing;
- you've found an assumption that doesn't hold up;
- you have an idea for improving something;
- you tried a tool and learned something unexpected;
- you have an idea for a completely new tool.

You don't need to know how to fix it.

Go to the **Issues** section of the Open Lab repository and choose **New Issue**.

Describe what you noticed and why you think it matters.

That's a contribution.

## Suggest a Change Yourself

If you know what you would change, GitHub lets you edit many text-based files directly in your browser.

Open the file.

Choose the edit option.

Make your change.

GitHub can guide you through creating your own copy or branch when necessary.

When describing your change, tell us:

1. What did you change?
2. Why?
3. What problem does it solve?
4. Have you tried it? If so, what happened?

When you're finished, GitHub will allow you to create a **Pull Request** proposing the change.

## What Happens Next?

A Pull Request starts a conversation.

Someone may:

- accept the change;
- ask a question;
- suggest another change;
- disagree and explain why;
- suggest keeping both approaches;
- help develop the idea further.

A Pull Request isn't a test you pass or fail.

It's a place to work on the idea together.

---

# Path B: I Want to Work Locally

If you're comfortable with Git, GitHub, VS Code, another editor, or the command line, you can work with Open Lab like any other Git repository.

## 1. Fork the Repository

On GitHub, choose **Fork**.

This creates your own copy of Open Lab.

## 2. Clone Your Fork

```bash
git clone git@github.com:YOUR-USERNAME/open-lab.git
cd open-lab
```

## 3. Create a Branch

```bash
git switch -c improve-handoff-diagnostic
```

Use a short name that describes the change.

## 4. Make Your Changes

Use whatever application is appropriate for the artifact.

Open Lab does not require contributors to use a particular editor, office suite, operating system, or development environment.

Where practical, work in the artifact's open source format.

Examples might include:

- Markdown for documentation;
- ODT for formatted documents;
- ODS for spreadsheets;
- ODP for presentations;
- SVG for vector graphics;
- plain-text formats for structured data;
- source code for software.

Follow the artifact's README and the Open Lab artifact standards where applicable.

## 5. Review What Changed

```bash
git status
git diff
```

Make sure you're contributing what you intended.

Check that you haven't accidentally included confidential information, credentials, temporary files, personal information, or unrelated changes.

## 6. Commit Your Changes

```bash
git add .
git commit -m "Improve handoff ownership questions"
```

A useful commit message briefly explains what changed.

## 7. Push Your Branch

```bash
git push -u origin improve-handoff-diagnostic
```

## 8. Open a Pull Request

GitHub will normally offer to create a Pull Request from the branch you just pushed.

Describe:

- what you changed;
- why;
- what problem it addresses;
- what you learned from using or testing it, if applicable.

Submit the Pull Request.

Now we're back to the same place as Path A:

**conversation.**

---

# Contributing a New Tool

Open Lab isn't limited to improving tools already here.

If you've built something useful and have the right to share it, we'd like to see it.

Before submitting it, ask yourself:

- What problem does this solve?
- Who is it intended to help?
- What assumptions does it make?
- Where has it been useful?
- Where might it not work?
- Can someone else understand and modify it?
- Can I provide the source in an open format?
- Am I legally and ethically allowed to share everything included?

It does not need to be perfect.

In fact, please don't wait for perfect.

The point of Open Lab is that useful things can continue improving after they're shared.

If you're unsure how or where to contribute something, open an Issue and describe what you've built.

We'll figure it out together.

---

# A Note About Different Answers

Not every disagreement needs to end with one approved solution.

A tool that works well in pharmaceutical manufacturing may need to work differently in healthcare, laboratories, software, aerospace, logistics, or somewhere else entirely.

Sometimes the right answer is to improve the shared tool.

Sometimes the right answer is an industry-specific variant.

Sometimes two genuinely different approaches deserve to exist.

That's okay.

**Open Lab is allowed to branch.**

---

# What Not to Share

Please do not contribute:

- confidential or proprietary information;
- employer-controlled documents;
- customer or employee information;
- credentials, passwords, keys, or other secrets;
- copyrighted commercial products you do not have permission to distribute;
- lightly modified versions of proprietary material;
- information restricted by contract, regulation, policy, or law.

If professional experience taught you something valuable, share the **principle**, not the protected material that taught it to you.

---

# AI-Assisted Contributions

AI is welcome here.

Use it to brainstorm, challenge an idea, write, code, analyze, prototype, or improve something.

But submitting a contribution means **you** have reviewed it, understand it, and are willing to stand behind it.

AI can help build the tool.

It cannot accept accountability for it.

---

# Still Overwhelmed?

That's okay.

You don't need to fork anything.

You don't need to understand branches.

You don't need to submit a Pull Request.

Open an Issue and tell us:

- what you saw;
- what you tried;
- what didn't work;
- what you think could be better;
- or what you've built.

We'll start there.

---

**Use it. Challenge it. Change it. Make it better. Share what you learned.**