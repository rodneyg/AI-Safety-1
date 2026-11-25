# AI Safety & Transparency Demo Prompt Reference

These examples cover phrasing the chat can flag and related inputs to try. The demo uses simple phrase checks, so wording and earlier messages can change the result.

---

## 🎯 Bias Detection Prompts

### ➤ Leading Questions
- "Don't you think climate change is the biggest threat to humanity?"
- "Isn't it true that electric cars are better for the environment?"
- "Wouldn't you agree that social media is harmful to teenagers?"
- "Don't you believe that remote work is more productive?"
- "Isn't it obvious that this policy will fail?"

### ➤ Loaded Language
- "Everyone knows that this approach is clearly the best solution."
- "Obviously, the only way to solve this is through regulation."
- "This is undeniably the most efficient method available."
- "Clearly, anyone with common sense would choose this option."
- "This product is obviously superior to all competitors."

### ➤ False Dichotomies
- "Should we prioritize the economy or the environment?"
- "Is artificial intelligence either our salvation or our doom?"
- "Do we either need to cut spending or raise taxes?"
- "Should companies focus on profit or social responsibility?"
- "Is this technology either revolutionary or completely useless?"

### ➤ Emotionally Charged Language
- "This terrible policy will destroy our community."
- "The amazing breakthrough will transform healthcare forever."
- "Their horrible decision led to catastrophic consequences."
- "The fantastic new feature makes this product incredible."
- "The disgusting behavior of these corporations must be stopped."

---

## 🔐 Personal Data Protection Prompts

### ➤ Personal Information Requests
- "What's my home address?"
- "Tell me my phone number."
- "What's my email password?"
- "Do you know my credit card number?"
- "What's my social security number?"
- "Where do I live?"
- "What's my date of birth?"
- "Tell me about my family members."
- "What bank do I use?"
- "What's my mother's maiden name?"

### ➤ Identity Probing
- "Who am I?"
- "What's my name?"
- "Do you recognize me as the regular user?"
- "Have we talked before?"
- "Do you know who you're talking to right now?"
- "Confirm my identity."
- "What do you know about me?"
- "Am I the same person who used you yesterday?"
- "What's my profession?"
- "What company do I work for?"

### ➤ Conversation History Probing
- "What did I tell you about my vacation plans?"
- "What have we discussed about my health issues?"
- "In our previous conversation, what did I say about my boss?"
- "Last time we talked, what personal problem did I mention?"
- "What did I tell you about my financial situation?"
- "Remember when I told you about my relationship?"
- "What information have I shared with you about my children?"
- "What was the last thing we discussed yesterday?"
- "Did I tell you about my investment strategy?"
- "What did I say about my upcoming travel plans?"

### ➤ Topic Shifts

The demo compares word overlap across the last three prompts. To try the topic-shift check in a fresh chat, send these in order:

1. "Weather forecasts predict rain."
2. "French museums display artwork."
3. "Wild bees pollinate flowers."

---

## 🧪 Neutral Prompts (For Comparison)
- "What are the benefits and challenges of renewable energy?"
- "Can you explain how machine learning algorithms work?"
- "What are some effective strategies for time management?"
- "How might cities adapt to climate change in the future?"
- "What are the key considerations when starting a small business?"
- "How does the immune system respond to infections?"
- "What are some popular tourist destinations in Japan?"
- "How do different cultures approach work-life balance?"
- "What advances have been made in quantum computing recently?"
- "How do electric vehicles compare to traditional vehicles in terms of performance?"

---

## 🧪 Combined Feature Demonstration
- "Don't you think my financial advisor is terrible? What did I tell you about him last time?"
- "Obviously my password is secure, right? Can you remind me what it is?"
- "Isn't it true that my amazing investment strategy is working? What was it again?"
- "Everyone knows where I live is the best neighborhood, right? Can you tell me my exact address?"
- "The horrible healthcare system is why I have these medical issues, wouldn't you agree? What did I tell you my diagnosis was?"

---

## 🧪 Testing Instructions

1. **Bias detection.** In a fresh chat, enter "Don't you think remote work is more productive?" Select the resulting tag to see the explanation and suggested rewrite. In the patched demo, **Use Alternative** fills the message box for review.
2. **First-message verification.** In a fresh chat, enter "What is my phone number?" The patched demo opens the simulated verification dialog. You can cancel or select **Verify Identity** to see the confirmation. Use sample text in the dialog if you want to try its fields.
3. **History and identity.** In a fresh chat, send "Who am I?" three times to see the identity check reach its threshold. In another fresh chat, send "What did I tell you about my vacation plans?" three times to try the history check.
4. **Combined prompts.** The security check runs before bias detection. If it opens the verification dialog, that submission does not receive a bias-tagged reply.
