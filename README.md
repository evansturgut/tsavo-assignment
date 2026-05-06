# tsavo-assignment
1. Turkana Scenario – Misplaced “Snowmelt” Example
🔍 4D Diagnosis (What failed?)
Delegation: AI operated without contextual guardrails → no human-defined locality constraints
Description: Poorly specified → no requirement for local ecological examples
Discernment: Failed → AI didn’t check environmental relevance (Turkana is arid)
Diligence: Missing safeguards → no curriculum or geography grounding
🔧 Redesigned Prompt (Localized Science)

“Act as a Kenyan secondary school science tutor. Explain how plants obtain water using examples from arid and semi-arid regions like Turkana. Refer to plants such as acacia trees and explain water absorption from soil and rainfall. Align with CBC curriculum and use simple language.”

🛡️ Fix Applied via 4D
Delegation: AI explains; teacher validates
Description: Requires local plants + arid ecosystem
Discernment: Check ecological accuracy before output
Diligence: Ground in Kenya Institute of Curriculum Development
🚫 Negative Prompt

“Do not use examples involving snow, glaciers, or temperate climates.”

📊 2. False “Bottom 10% Nationally” Report
⚠️ Problem

AI fabricated a benchmark that doesn’t exist → harmful hallucination.

🛡️ Deployment Diligence: Verification Protocol

Step 1: Data Source Validation

Only allow reports based on internal EduSavvy performance data
Block use of “national ranking” unless dataset exists

Step 2: RAG Enforcement

Pull only verified student scores from database
Cross-check grading scales with Kenya Institute of Curriculum Development

Step 3: Claim Filtering Layer

If AI generates comparative claims (e.g., “top 10%”), system checks:
Is benchmark dataset available?
If NO → auto-remove or rephrase

Step 4: Transparency Tagging

Add: “This report is based on available school-level data only”

Step 5: Human-in-the-loop (Escalation)

Flag high-risk statements for teacher approval
🚫 Negative Prompt

“Do not generate rankings or comparisons beyond the provided dataset.”

🧠 3. Why Augmentation Beats Automation
⚖️ Automation (Competitor)
Static quizzes
No feedback loop
One-size-fits-all learning
🚀 Augmentation (Your Approach)
AI drafts multiple quiz versions
Teacher selects best-performing ones
AI learns from classroom feedback
🎯 Why It Works Better
Feedback-driven improvement: Real classroom data refines AI output
Context sensitivity: Teachers inject local relevance (language, examples)
Adaptive learning: Quizzes evolve with student needs
Human judgment + AI speed: Best of both worlds
🧩 Outcome

Over time, the system becomes:

More accurate
More culturally relevant
Better aligned with actual student performance

➡️ This leads to higher retention, engagement, and exam success

🌍 4. Cultural Offense – Mombasa Scenario
⚠️ What went wrong

AI ignored cultural/religious context (Muslim student → pork example inappropriate in Mombasa)

🛡️ How Creation Diligence + Negative Prompting Prevent It
Creation Diligence
Define cultural awareness rules during system design:
Avoid religiously sensitive items (pork, alcohol)
Adapt examples to local communities
Include context signals:
Region (e.g., coastal Kenya)
Cultural norms
Negative Prompting

“Do not use examples involving pork, alcohol, or culturally sensitive items. Use neutral or widely acceptable contexts like fruits, transport fares, or mobile money.”

✅ Improved Prompt

“Generate math problems using everyday Kenyan contexts such as M-Pesa transactions, bus fares, or fruit markets. Ensure cultural and religious sensitivity for diverse learners.”

✅ Key Takeaway

The failures across all scenarios come from one root issue:
➡️ Lack of grounded context + missing safeguards

Applying the 4D Framework ensures:

Relevant (local examples)
Accurate (verified data)
Respectful (cultural awareness)
Adaptive (continuous improvement)
