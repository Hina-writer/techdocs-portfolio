# Style Guide for Documentation

A style guide serves as a foundation for creating clear, consistent, and user-friendly documentation. While each writer brings their own unique tone and communication style, this individuality can sometimes lead to inconsistencies, causing confusion and disrupting the overall cohesion of voice and tone.

This guide is designed to streamline the documentation process by establishing key principles that ensure a unified style, voice, and tone. It empowers writers to produce content that not only adheres to best practices but also remains adaptable to diverse audiences and contexts, encouraging clarity and professionalism across all documentation.

> **Note:** Some parts of this style guide are inspired by Microsoft Docs, reflecting industry-standard practices for technical documentation.

---

## Table of Contents

- [Voice and tone for writing](#voice-and-tone-for-writing)
- [Using inclusive language](#using-inclusive-language)
- [Writing principles](#writing-principles)
- [Active vs Passive voice](#active-vs-passive-voice)
- [Writing in first and second person (we, our, you, your)](#writing-in-first-and-second-person-we-our-you-your)
- [Scannable content and writing principles](#scannable-content-and-writing-principles)
- [Add Notes, Tips, and Warnings](#add-notes-tips-and-warnings)
- [Special terms and formatting](#special-terms-and-formatting)
- [Documenting Code](#documenting-code)
- [Reference](#reference)

---

## Voice and tone for writing

The voice and tone of your documentation are crucial in shaping how users perceive and engage with your content. To create a modern and approachable voice, focus on three core elements:

### 1. Clear

- Use straightforward language and avoid jargon wherever possible.
- Prioritize simplicity and conciseness, ensuring content is easy to understand on the first read.
- Structure information logically, using headings, lists, and visual aids to guide readers.
- Avoid ambiguous phrases or overly technical terms unless absolutely necessary; provide context or definitions when used.

### 2. Human

- Write in a conversational yet professional tone. Use "you" to address the reader directly and engage them.
- Acknowledge user challenges empathetically and offer solutions that are approachable and actionable.
- Avoid sounding overly formal. Aim for a tone that is warm and encouraging without being too casual.
- Use inclusive language that respects all audiences.

### 3. Reliable

- Ensure your content is accurate and up to date, reflecting the latest best practices and product details.
- Be authoritative without condescension. Present information with confidence, backed by facts and examples.
- Avoid overpromising or underexplaining; set clear expectations about what the reader can achieve.
- Maintain consistency in terminology and style across documentation to reinforce trust and professionalism.

---

## Using inclusive language

Creating inclusive and diverse content ensures all readers feel respected and represented.

- Avoid using gender-specific pronouns as defaults; prefer the singular "they" for gender neutrality.
- Refrain from violent or biased language such as "kill," "abort," or "master/slave"; use neutral alternatives like "primary/secondary."
- Avoid anthropomorphism (e.g., machines don’t "think" or "hear")—use precise terms.
- Avoid color-based metaphors like "blacklist" or "whitelist;" use "blocklist" or "allowlist" instead.
- Prioritize accessibility by considering readability, alt text for images, and clear formatting.

### Examples:

- Avoid: *The player can upgrade his farm by earning experience points (XP).*
- Preferred: *The player can upgrade their farm by earning experience points (XP).*

- Avoid: *Kill the old files by hitting Delete.*
- Preferred: *Click Delete to erase the old files from the system.*

---

## Writing principles

Good grammar and punctuation make a difference in clarity.

- Follow standard English grammar rules.
- Stick to American or British spelling consistently depending on your audience.

### Active vs Passive voice

| Rule                                             | Example                          |
|--------------------------------------------------|---------------------------------|
| **Active Voice:** Subject + Action + Object.      | To save the file, click Save.   |
| **Passive Voice:** Action done on object, subject less important. | Access is restricted to authorized users.|

**Key takeaway:** Prefer active voice for clarity, but retain passive if rephrasing reduces clarity.

---

## Writing in first and second person (we, our, you, your)

### Use "We" to represent your organization

Using "we" fosters warmth and collaboration, especially for smaller teams.

**Example:**

- Avoid: *This feature has been designed to help users achieve their goals.*
- Preferred: *We've designed this feature to help you achieve your goals.*

### Use "You" to engage your audience

Address the reader as "you" to maintain an approachable tone.

**Example:**

- Avoid: *The user can customize their dashboard.*
- Preferred: *You can customize your dashboard.*

---

## Scannable content and writing principles

- Use short paragraphs and line breaks to avoid clutter.
- Break down long sentences into smaller thoughts.
- Use sentence case for headings, no numbering or punctuation (except question marks).
- Use bullets for key points, steps, or to break up walls of text.
- Limit bullets to 5–7 items where possible.
- Maintain consistency in bullet lead-ins (verbs or nouns).

### Bullets with lead-ins

- **System Requirements** include at least 8GB of RAM and 500GB of storage.
- **Installation Time** typically takes about 15 minutes.

### Starting bullets with verbs

- Analyze the project scope.
- Coordinate with stakeholders.

---

## Add Notes, Tips, and Warnings

| Element  | Purpose                             | Example                              |
|----------|-----------------------------------|------------------------------------|
| **Note** | Supplemental information          | *Note: This feature requires v2.0.*|
| **Tip**  | Helpful insights or best practices| *Tip: Use keyboard shortcuts.*     |
| **Warning** | Alerts to risks or critical issues| *Warning: Changing this setting may cause data loss.*|

---

## Special terms and formatting

| Type of Element         | Format           | Example                                   |
|------------------------|------------------|-------------------------------------------|
| On-screen elements      | **Bold**         | Click **Settings** in the toolbar.        |
| Subtle emphasis        | *Italics*        | The team retrospective is *scheduled*.   |
| Labels/Parameters      | *Italics*        | Use the *apiKey* and *clientId*.          |
| Methods/Classes        | **Bold** or `Code` | `UserAccount.CreateNewAsync()`            |
| User Input             | "Quotes and *Italics*" | Enter: "restart-server".                 |

---

## Documenting Code

When documenting code:

- Start with an introduction explaining the functionality.
- Include code samples.
- Add step-by-step explanations.
- Use tables to describe attributes if applicable.

### Example: Creating a User Account

**Introduction:**  
This example demonstrates creating a user account using the `UserAccount` class.

**Code sample:**

```csharp
using System;

namespace UserManagement
{
    public class UserAccount
    {
        public string UserId { get; private set; }
        public string Username { get; set; }
        public string Password { get; set; }

        public UserAccount(string username, string password)
        {
            UserId = Guid.NewGuid().ToString();
            Username = username;
            Password = password;
        }

        public void DisplayUserInfo()
        {
            Console.WriteLine($"UserID: {UserId}, Username: {Username}");
        }
    }

    // Example usage:
    var newUser = new UserAccount("JohnDoe", "SecureP@ssw0rd!");
    newUser.DisplayUserInfo();
}
```

---

## Reference

The references below guided the creation of this style guide and serve as excellent resources for further reading:

- [Microsoft Writing Style Guide](https://learn.microsoft.com/en-us/style-guide/)
- [Gender-Neutral Pronouns](https://learn.microsoft.com/en-us/style-guide/word-choice/gender-neutral-language)
- [Accessibility Guidelines](https://learn.microsoft.com/en-us/style-guide/accessibility/)
- [Scannable Content Best Practices](https://learn.microsoft.com/en-us/style-guide/scannable-content/)
