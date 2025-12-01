# Resume Development - Session Context

**Last Updated:** December 1, 2025
**Owner:** Ryan Bryson
**Purpose:** Resume development for internal promotion and external job search (Senior Software Engineer, Frontend Architect roles)

---

## Overview

This repository contains Ryan's resume and supporting materials for career advancement. The resume has been developed through a comprehensive questionnaire process to capture accurate technical details and bridge his hardware-to-software transition story.

---

## Key Context: Career Transition Story

**Critical Background:**
- Ryan transitioned from analog hardware design to software engineering in Dec 2022
- This was NOT an abrupt transition - he built the bridge during his hardware role
- During Hardware Engineer II role (2019-2022), he:
  - Built Python test automation GUI (wxPython) with FFT distortion analyzer
  - Developed React-based calibration dashboards
  - Wrote embedded firmware for test fixtures
- This experience eliminates the credibility gap and shows intentional career progression
- Formal internal transfer at Fluke in Dec 2022 ("Baseline was my first software project. No ramp.")

**Why This Matters:**
The transition story is the most critical element of Ryan's resume. Without the context that he was already doing software work during his hardware role, the Dec 2022 pivot looks suspicious (designing precision amplifiers → leading React Native architecture). The questionnaire revealed this bridge work, which is now prominently featured.

---

## User Preferences & Values

### What Ryan Cares About (Prioritize These):
1. **Architecture over metrics** - He explicitly does NOT want to emphasize vanity metrics like build times, test coverage percentages, component counts
2. **Maintainability and customer experience** - These are his north stars, not velocity
3. **Patterns and principles** - GoF patterns, Clean Architecture, DRY - he values architectural rigor
4. **Hardware background as differentiator** - He wants to EMPHASIZE, not minimize, his analog hardware experience
5. **Solo architectural ownership** - He's the sole frontend architect on a 5-person team and wants this clear

### What to Avoid:
- ❌ Arbitrary metrics (24hr delivery, 10x builds, 80% duplication reduction) - he finds these irrelevant
- ❌ Counting components, tests, commits - "irrelevant"
- ❌ Deployment velocity claims - "maintainable, robust, and reliable" matter more
- ❌ Platitudes, superlatives, self-promotion
- ❌ Over-engineering or feature creep language

### His Philosophy (from questionnaire):
> "I feel these are irrelevant since deployment should be maintainable, robust, and reliable. Velocity is ideal goal, but not primary to infrastructure. I care more about what customer sees and how easy is it for us to fix issues released to client."

---

## Resume Development Process

### Phase 1: Initial Review (Completed)
- Reviewed LinkedIn experience and original resume
- Identified critical gaps (transition story, missing metrics, timeline overlaps)
- Created comprehensive 65-question questionnaire

### Phase 2: Questionnaire Analysis (Completed)
- Ryan completed questionnaire with detailed responses
- Key findings documented in RESUME-QUESTIONNAIRE.md
- Discovered Python/React work during hardware role (critical bridge)
- Learned team structure (sole frontend on 5-person team)
- Confirmed his values (architecture > metrics)

### Phase 3: Resume Update (Completed)
- Updated RESUME.md with questionnaire findings
- Added transition story to summary
- Added Python/React work to Hardware Engineer II role
- Changed title to "Sole Frontend Architect"
- Specified hardware projects (Fluke 5560A, 5730A, Boeing NMA, Blackmore LIDAR)
- Added FE certification
- Removed Node.js, added accurate tools (Cadence, Altium, Vite, Vitest, Turbo)

### Phase 4: Git Tracking (Completed)
- Initialized git repository in /resume directory
- First commit: Original resume version
- Second commit: Updated resume with questionnaire findings
- Full change history tracked (42 additions, 53 deletions)

---

## Repository Structure

```
/Users/ryanbryson/Documents/fluke/resume/
├── .git/                          # Git repository (isolated to this directory)
├── .gitignore                     # Ignores .DS_Store, temp files
├── RESUME.md                      # Current resume (TRACKED)
├── RESUME-QUESTIONNAIRE.md        # Questionnaire with Ryan's responses (TRACKED)
└── CONTEXT.md                     # This file (session context)
```

**Git History:**
```
d3a979f - Update resume with questionnaire findings
ceb1c7f - Initial resume version
```

**Parent Directory NOT Tracked:**
- `/Users/ryanbryson/Documents/fluke/` contains other directories (career/, pa/) that are NOT git-tracked
- Only the resume/ subdirectory is a git repository

---

## Current Resume State

### Summary Strategy:
- Lead with "Software engineer specializing in frontend architecture"
- Explicitly mention transition: "after building test automation tools and calibration dashboards during hardware role"
- Emphasize "sole frontend engineer on 5-person team"
- Focus on capabilities enabled, not metrics

### Software Engineer II Role:
- **Title:** "Sole Frontend Architect" (informal, but accurate)
- **Team:** 5-person team (3+ backend, 2+ devops, 1 frontend)
- **Key work:** Platform-agnostic architecture, domain plugin system, schema-driven renderer, component library, thermal image editor
- **Tech:** React, React Native, TypeScript, Python, Vite, Vitest, Turbo
- **Image editor specs:** 300+ images, sub-second processing, Lightroom-style selective updates
- **No subordinates:** Offered but declined (lean team preference)
- **MVP:** August 2026 (still pre-customer)

### Hardware Design Engineer II Role:
- **Models:** Fluke 5560A and 5730A Calibrators
- **Critical addition:** Python test automation GUI (wxPython) with FFT analyzer
- **Critical addition:** React-based calibration dashboards
- **EOL work:** A11 DAC, A21 FPGA, A7 compensation boards
- **Tools:** LTSpice, Cadence, MATLAB, Python, React

### Other Roles:
- **Boeing (5 months):** NMA program (scrapped after 737 MAX + COVID), left because "too much system design, wanted to be an individual contributor"
- **Blackmore:** LIDAR for autonomous vehicles and defense (pre-Aurora acquisition)
- **LANL:** Uranium oxide solar cells for radiation-hardened space applications

### Certifications:
- Fundamentals of Engineering (FE) - Electrical Engineering

---

## Technical Details from Questionnaire

### Software Role Details:
- **Code sharing:** 100% shared between web/mobile (except auth - MSAL not used on mobile)
- **Routing:** React Navigation (platform-agnostic)
- **Domain plugins:** Support any number of domains via contract-based architecture (GoF principles)
- **Schema renderer:** Enables domain experts and engineers to configure forms, workflows, validation without deployment
- **Quality gates:** TypeScript, ESLint, Jest, integration tests, E2E (Playwright)
- **Python usage:** Backend APIs, data processing, test utilities

### Hardware Role Details:
- **Test automation:** wxPython GUI with FFT distortion analyzer for voltage/current output boards
- **React dashboards:** Calibration and test interfaces
- **Inductive loading:** Square wave roll-off, triangle wave instability in non-ideal loads
- **EOL components:** FPGAs, MOSFETs, op-amps, diodes
- **Compensation techniques:** Lead-lag networks, Miller compensation, pole-zero cancellation, nested feedback loops

---

## Target Roles & Use Cases

### Primary Purpose:
- Internal promotion at Fluke (Senior Software Engineer)
- External job search (Senior Software Engineer, Frontend Architect)
- Updating LinkedIn
- Full-stack roles (not frontend-only)

### Resume Variants Needed:

#### 1. Full Version (Current - RESUME.md)
- **Use for:** Internal promotion, portfolio, historical record
- **Includes:** All roles including Acuity Design (2012)
- **Length:** ~1.5 pages

#### 2. Pruned External Version (NOT YET CREATED)
- **Use for:** External job applications
- **Remove:** Acuity Design (13 years old, not relevant)
- **Condense:** Blackmore (5 bullets → 3), LANL (3 bullets → 2)
- **Length:** 1 page target

#### 3. LinkedIn Version (NOT YET CREATED)
- **Use for:** LinkedIn profile
- **Based on:** Pruned version without Acuity
- **Format:** LinkedIn-specific formatting (remove phone, adjust structure)

---

## Key Decisions Made

### Included in Resume:
1. ✅ Python/React work during Hardware Engineer II role (critical bridge)
2. ✅ "Sole Frontend Architect" title (informal but accurate)
3. ✅ Specific models: Fluke 5560A, 5730A, Boeing NMA, Blackmore LIDAR
4. ✅ Image editor specs: 300+ images, sub-second processing
5. ✅ FE certification
6. ✅ Acuity Design (kept for historical record, can prune later)
7. ✅ Space solar cells context for LANL uranium oxide work

### Removed from Resume:
1. ❌ Node.js (just a dependency, not a skill)
2. ❌ HTML/CSS (implied by React)
3. ❌ Build time metrics (10x, etc.)
4. ❌ Test coverage percentages
5. ❌ Component counts (29 components)
6. ❌ Arbitrary "80% duplication reduction"
7. ❌ "24-hour feature delivery"

### Technical Skills Updated:
- **Added:** Cadence, Altium Designer, Vite, Vitest, Turbo, GitHub Actions, Figma
- **Removed:** Node.js, HTML, CSS
- **Clarified:** Specific hardware domains (Transconductance Amplifiers, PLLs, ADCs)

---

## Open Questions / Next Steps

### Potential Future Work:

1. **Pruned 1-page version** for external applications
   - Remove Acuity Design
   - Condense Blackmore and LANL
   - Target: 1 page strict

2. **Cover letter template**
   - Explain hardware → software transition story
   - Address Boeing 5-month tenure
   - Emphasize systems thinking as differentiator

3. **LinkedIn "About" section**
   - Based on resume summary
   - Slightly longer, more conversational
   - Emphasize architectural leadership

4. **LinkedIn experience bullets**
   - Match resume but optimized for LinkedIn format
   - May need slight rewording for platform

5. **Portfolio projects** (if desired)
   - Wedding portfolio (Next.js, Backblaze CDN) - could be showcased
   - Side projects to demonstrate skills

---

## Important Notes for Future Sessions

### When Reviewing/Updating Resume:

1. **Always prioritize Ryan's values:**
   - Architecture and maintainability over metrics
   - Hardware background as differentiator, not weakness
   - Customer experience over developer velocity

2. **Preserve the transition story:**
   - Python/React work during hardware role MUST stay
   - This is the credibility bridge

3. **Don't add metrics Ryan doesn't want:**
   - He explicitly rejected build times, test counts, velocity claims
   - Focus on capabilities enabled, not numbers

4. **Git workflow:**
   ```bash
   cd /Users/ryanbryson/Documents/fluke/resume
   # Edit RESUME.md
   git add RESUME.md
   git commit -m "Description of changes"
   ```

5. **Boeing tenure:**
   - 5 months because he wanted IC hardware work, not systems/requirements
   - NMA program was scrapped after 737 MAX + COVID
   - This is NOT a red flag when explained

6. **Acuity Design:**
   - Kept in full version for historical record
   - Should be removed for external applications
   - 2012 internship (13 years old)

### Key Files to Reference:

- **RESUME.md** - Current resume
- **RESUME-QUESTIONNAIRE.md** - Ryan's detailed responses (65 questions)
- **Git history** - `git log` and `git diff` to see changes

### Ryan's Communication Style:

- Direct, no-nonsense
- Values technical accuracy over marketing speak
- Will call out bullshit immediately ("you dumbass" when git was in wrong folder)
- Prefers succinct, impact-driven language
- Hates platitudes and superlatives

---

## Questionnaire Key Insights

### Section 1: Career Transition
- Started learning software during hardware role (nearly when he joined Fluke)
- Built wedding portfolio with Next.js (learning project on Vercel, Backblaze CDN)
- Formal internal transfer in Dec 2022
- Motivation: "Enjoyed the encapsulation of knowledge like lightning in a bottle"

### Section 2: Software Role
- Team: 5 core (3+ backend, 2+ devops, 1 frontend)
- Offered subordinates but declined (lean team)
- 100% code sharing except auth
- Image editor: 300 image capacity, <1s processing
- MVP: August 2026

### Section 3: Hardware Role
- Fluke 5560A Calibrator transconductance amplifiers
- Python GUI: wxPython + FFT analyzer
- React dashboards for calibration
- A11 DAC, A21 FPGA, A7 compensation EOL work
- Tools: Cadence (Fluke), Altium (Blackmore), KiCAD (hobby)

### Section 4: Boeing
- NMA program (scrapped)
- Left after 5 months for IC hardware work at Fluke
- "Too much system design, wanted to be an individual contributor"

### Section 5: Blackmore
- LIDAR for autonomous vehicles + defense
- Pre-Aurora acquisition
- 200W power board for computing + laser
- Automotive compliance: CISPR 25, ISO 7637, ISO 16750

### Section 6: LANL
- After graduation (May-Dec 2017)
- No clearance required
- Uranium oxide solar cells for space satellites

### Section 7: Certifications
- FE in Electrical Engineering

### Section 8: Goals
- Target: Senior Software Engineer, Frontend Architect
- Full-stack roles (not frontend-only)
- Emphasize hardware as differentiator

---

## Git Commands Reference

### View history:
```bash
cd /Users/ryanbryson/Documents/fluke/resume
git log --oneline
git log --stat
```

### View changes:
```bash
git diff ceb1c7f d3a979f           # Compare commits
git show d3a979f                   # Show specific commit
```

### Revert to old version:
```bash
git checkout ceb1c7f RESUME.md     # Revert to original
git checkout d3a979f RESUME.md     # Revert to updated
```

### Make new changes:
```bash
# Edit RESUME.md
git add RESUME.md
git commit -m "Description of changes"
```

---

## Session Summary

**What We Accomplished:**
1. ✅ Reviewed original resume and LinkedIn
2. ✅ Created comprehensive 65-question questionnaire
3. ✅ Ryan completed questionnaire with detailed responses
4. ✅ Analyzed responses and identified key findings
5. ✅ Updated resume with questionnaire findings
6. ✅ Set up git repository (correctly, after initial mistake)
7. ✅ Created context document for future sessions

**Outcome:**
- Resume accurately reflects Ryan's experience
- Transition story is clear and credible
- Hardware background positioned as strength
- Architecture focus emphasized over metrics
- Ready for pruning into 1-page external version

**Ready for Next Phase:**
- Create pruned 1-page version
- Draft cover letter template
- Update LinkedIn profile
- Generate additional variants as needed

---

## Contact Info

**Ryan Bryson**
- Email: ryalho@gmail.com
- LinkedIn: https://www.linkedin.com/in/tektronica/
- Phone: (406) 529-5031
- Location: Missoula, Montana (Remote)

---

*This context document should be read at the start of any new session working on Ryan's resume. It captures the key decisions, preferences, and technical details needed to continue the work effectively.*
