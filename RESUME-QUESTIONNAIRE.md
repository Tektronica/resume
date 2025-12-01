# Resume Questionnaire - Ryan Bryson

Complete this questionnaire to provide missing context, metrics, and details for your resume. Answer as many questions as possible. If you don't remember exact numbers, provide estimates or ranges.

---

## SECTION 1: Career Transition (Hardware → Software)

### The Big Question: How did you transition from analog hardware to leading React/TypeScript architecture?

**Context:** You were designing precision amplifiers in Nov 2022, then leading React Native architecture in Jan 2023. This is the biggest question recruiters will have.

1. **When did you start learning software development?**
   - [x] During hardware role (side projects, evenings/weekends)
       - started software write test automation gui in python and wxPython. The test automation was a distortion analyzer that ran fft analysis on a measured input signal. This was sped up our validation process for our voltage and current output boards for calibrator.
   - [ ] Internal Fluke training program
   - [ ] Bootcamp
   - [x] Self-taught (online courses, books)
   - [ ] Other: ___________

2. **If you learned during your hardware role, what was the timeline?**
   - When did you start? (Month/Year): Nearly when I joined Fluke
   - What resources did you use? (Udemy, freeCodeCamp, official docs, etc.): official docs and books
   - Did you build any side projects? If yes, describe:
       - My wedding portfolio was a launchpad for learning React using nextjs and hosting on vercel. Solved how I wanted to run my CDM by using backblaze to store images cheap and securely and used backblaze endpoints to get my image lists. Also explored mongodb but felt unnecessary complexity for simple image delivery.

3. **Was the transition formal or informal?**
   - [x] Formal internal transfer at Fluke with role change
   - [ ] Gradual shift (started doing some software work while still hardware engineer)
   - [ ] Applied internally to software position
   - [ ] Manager suggested transition based on interest/aptitude
   - [ ] Other: ___________

4. **Did you do any software work during your Hardware Engineer II role?**
   - [x] Yes - built test automation tools
   - [x] Yes - built calibration dashboards/GUIs
   - [x] Yes - Python scripting for data analysis
   - [x] Yes - embedded firmware for test fixtures
   - [ ] No software work during hardware role
   - [ ] Other: ___________

5. **What made you want to transition?** (1-2 sentences)

   Enjoyed the encapsulation of knowledge like lightning in a bottle. I was able to employ my love for analysis, pattern architecture, and frontend creativity.

6. **How did Fluke support the transition?** (Training budget? Mentorship? Gradual ramp-up?)
    Baseline was my first software project. No ramp.

---

## SECTION 2: Software Engineer II (Current Role) - Metrics & Context

### Team Structure

7. **What is your team structure?**
   - Total team size: ___________
   - Number of frontend developers: ___________
   - Number of backend developers: ___________
   - Your formal title: ___________ (is "Frontend Lead" official or informal?)
   - Do you have direct reports? [ ] Yes [ ] No
   - If yes, how many? ___________

8. **How many developers report to you vs collaborate with you as peers?**
    Mothra is most relevant. I was offered subordinates but we are a lean team of 5 core players. 3+ backend, 2+ devops, 1 for frontend. I manage all levels of frontend for platform agnostic deployment.

   ___________

### Platform-Agnostic Architecture

9. **What percentage of code is shared between web and mobile?**
   - Estimated percentage: 100% shared apart from auth security requiring platform impls
   - What's platform-specific? (navigation? native modules?): authentication. Msal not used on mobile. React navigation is used for our core router and thus is completely agnostic. Any specific native modules are used in the parent app that merely thinly wraps our core app (we do support expanded supersets of core, but just isn’t scoped yet)

10. **Build time improvements - what are the actual numbers?**
    - Build time BEFORE (Next.js): 20 seconds, but it’s irrelevant that I want to share with an interview. I would use any tooling they prescribed
    - Build time AFTER (Vite + Turbo): 10 seconds, but irrelevant. I would use their tooling.
    
    Largely the point isn’t specific numbers but the fact that I made this architectural decision to improve our development and be purely CSR

11. **Do you have deployment velocity metrics?**
    - Average time from design mockup to deployed feature: ___________
    - Number of deployments per week/month: ___________
    - Any CI/CD metrics? (build success rate, test pass rate): ___________

    I feel these are irrelevant since deployment should be maintainable, robust, and reliable. Velocity is ideal goal, but not primary to infrastructure. I care more about what customer sees and how easy is it for us to fix issues released to client.

### Domain Plugin System

12. **How many domains are currently supported?**
    - Number of business domains: We support any number of domains via domain config contract. We employ GoF principles to ensure we scale.
    - Examples (without naming internal projects): Solar, Electrical, HVAC, etc.: ___________

13. **How many enterprise customers are using the customization system?**
    - Number of customers: ___________
    - Or is this still internal? [x] Yes [ ] No

    - MVP is August 2026
    
14. **What can domain experts configure without code deployment?**
    - [x] Forms/layouts
    - [x] Workflows
    - [x] Validation rules
    - [x] UI components
    - [x] Reports
    - [ ] Other: ___________

### Component Library

15. **How many components did you build?**
    - Total number: irrelevant but our core library that meets ux requirements
    - Any particularly complex ones worth highlighting? No because ux is not my core concern. Architecture is and the framework and patterns I build around component library (like radix, primitives, blocks, and the goal of maintainability)

16. **What was the design-to-implementation improvement?**
    - Before: Time to implement a UX design: ___________
    - After: Time to implement a UX design: ___________
    - Or describe qualitatively: ___________

### Schema-Driven Renderer

17. **How many hardcoded forms did this eliminate?**
    - Number of forms converted to schema: ___________
    - Lines of code eliminated (estimate): ___________

    - not relevant. Our goal was to avoid this. We will support static and custom templates
    
18. **Who configures the schemas?**
    - [x] Domain experts (non-technical)
    - [ ] Product managers
    - [x] Engineers
    - [ ] Mix of above: ___________
    - we do not have a ui for creating custom templates yet, but the goal is to be low-code for devs and no code for non technical. This already works in isolated environments just not deployed.
### Image Editor

19. **What are the performance specs?**
    - Number of images it can handle simultaneously: unbounded, but limited to pc hardware. We cap to 300 as our target.
    - Processing time per image: <1 seconds (limited by wasm abstraction of the underlying cpp renderer I didn’t write.)
    - Annotation types supported: ___________ (rectangle, polygon, text, markers, etc.). Full blown drawing annotator, so yes. All. We also support rotation of items and groups (not selectable groups but layers)

20. **What was the workflow improvement?**
    - Time to process 100 images BEFORE: ___________
    - Time to process 100 images AFTER: ___________
    - Or % reduction in inspection time: 100%
	100% improvement, but the rendering strategy changed. We no longer do a rolling update. We perform only the updates to images the user indicates. (Think of Lightroom and how they perform updates of subsets)
### Testing & Quality

21. **Do you have test coverage metrics?**
    - Number of tests written: ___________
    - Test coverage percentage: ___________%
    - Any TypeScript strictness metrics? (e.g., "0 errors across X files"): ___________
	This is an internal metric and not related to customer driven priorities. I don’t want to mention these because unit tests are important but not a priority when a manager is reading my resume.

22. **Do you have quality gates in CI/CD?**
    - [x] TypeScript type checking
    - [x] Linting (ESLint)
    - [x] Unit tests (Jest)
    - [x] Integration tests
    - [x] E2E tests (Playwright, Cypress)
    - [ ] Other: ___________

### Python Usage

23. **You list Python as a skill - what Python work did you do in this role?**
    - [x] Backend API development
    - [x] Data processing scripts
    - [ ] Build/deployment automation
    - [x] Test utilities
    - [ ] None (should be removed from skills)
    - [ ] Other: ___________

---

## SECTION 3: Hardware Design Engineer II - Specifications & Details

### Transconductance Amplifiers

24. **What were the performance specifications you achieved?**
    - Gain flatness: ± ___________%
    - THD (Total Harmonic Distortion): < ___________ppm
    - Bandwidth: ___________ Hz to ___________ MHz/GHz
    - Output noise: ___________ μV RMS
    - Or state "don't remember specific numbers": ___________
	Specifics were documented in our required specifications listed for the calibrator we were designing (and released Fluke 5560)

25. **What Fluke Calibrator model were you working on?**
    - Model number: 5560A (5730A? 5560A? other?)
    - Or state "prefer not to specify model": ___________

26. **What was the improvement over previous design?**
    - Distortion reduced by: ___________%
    - Or qualitative improvement: ___________
	previous design was built on the target spec. The goal of the analyzer was to achieve this spec by constant validation across our frequency and output ranges.

### Loop Gain & Compensation

27. **What specific compensation techniques did you use?**
    - [x] Lead-lag networks
    - [x] Miller compensation
    - [x] Pole-zero cancellation
    - [x] Nested feedback loops
    - [ ] Other: ___________

    The specific compensation networks are not as important as the fact how and where they were implemented in our output gain network while reducing an accumulated delay in the network.
    
29. **What was the inductive loading challenge?**
    - Briefly describe the problem and solution (1-2 sentences): ___________
	inductive loading is one of the performance gates we perform on our calibrators. Since our calibrators provides a signal to a load of known quality by the tester, we must support that non ideal loads contain little or a lot of induction. So the goal of our output sense was to provide an output full swing will ensuring the output compensation was robust to support inductive loading on specific signal outputs (square wave roll off and triangle wave leading instability due to sharp turns in output signal)

### End-of-Life Component Redesign

29. **Which components went EOL?**
    - Component types: ___________ (op-amps? resistor networks? references?)
    - Number of components replaced: ___________
	My EOL components were FPGA’s, mosfets that were tied to battery life if not chosen correctly, opamps, and diodes for compensation networks for 5730.

30. **What was the scope of the redesign?**
    - [ ] Single board
    - [ ] Multiple boards
    - [ ] Entire signal chain
    - [ ] Other: ___________
	Depends on the board. A11 DAC was researching scoping that would have required thermally stable diodes, A21 was an FPGA replacement for the IO rear board interfacing with one of Fluke’s transcendence amplifier models, a7 was compensation network for current.

31. **Did you achieve cost savings?**
    - BOM cost reduction: ___________%
    - Or dollar amount: $___________
    - Or state "cost-neutral, maintained specs": ___________
    - cost savings was in meeting deadline without drop ship on orders. The goal was to address EOL not cost savings on the BOM.
    - 
### Tools & Software

32. **What PCB design tool did you use?**
    - [x] Altium Designer (Blackmore)
    - [x] Cadence (fluke)
    - [ ] OrCAD
    - [x] KiCAD (hobby)
    - [ ] PADS
    - [ ] Other: ___________

33. **Did you use Python or other scripting during hardware work?**
    - [x] Yes - test automation scripts
    - [x] Yes - data analysis (MATLAB/Python)
    - [x] Yes - calibration procedures
    - [ ] No
    - [ ] Other: ___________

34. **Skills section lists "React.js" for this role - was this accurate?**
    - [x] Yes - I built test dashboards/calibration GUIs
    - [ ] No - copy/paste error, should be removed
    - [ ] Other: ___________

---

## SECTION 4: Boeing - Timeline & Context

### Duration & Type

35. **Why was this role only 5 months (Apr 2019 - Aug 2019)?**
    - [ ] Contract role (intended to be short-term)
    - [ ] Internship that ended
    - [x] Better offer from Fluke
    - [ ] Layoffs/program cancellation
    - [x] Personal decision to leave
    - [ ] Other: ___________

	too much system design. Interfaced with contractor over hw requirements. I wanted to be an individual contributor designing hardware. So I left Boeing.

36. **Was this a contract or full-time position?**
    - [ ] Contract
    - [x] Full-time
    - [ ] Internship
    - [ ] Other: ___________

### Technical Details

37. **What aircraft program was this for?**
    - [ ] 737 MAX
    - [ ] 777X
    - [ ] 787
    - [ ] Prefer not to specify
    - [ ] Other: ___________

	NMA (new mediumhual aircraft) that was scrapped after 737 MAX and covid.

38. **What were the power system specifications?**
    - Input voltage: ___________ VDC
    - Output voltage: ___________ VDC
    - Current capacity: ___________ A
    - Redundancy: [ ] Single [ ] Dual [ ] Triple
    - Or state "don't remember specs": Don’t remember
    I documented and performed a power study of the full loading on the power control unit for existing aircrafts to build requirements for the NMA project based on its specifications. 

39. **What were the key design drivers from the trade study?**
    - [ ] Weight minimization
    - [ ] Thermal management
    - [x] Fault tolerance
    - [x] Efficiency
    - [ ] Cost
    - [ ] Other: ___________

40. **What were the trade-offs?** (e.g., "Selected buck topology over boost for 15% weight reduction")

    ___________

---

## SECTION 5: Blackmore Sensors - LIDAR Context & Metrics

### Company Context

41. **What was the LIDAR application?**
    - [x] Autonomous vehicles (primary customer)
    - [ ] Industrial sensing
    - [ ] Aerospace
    - [x] Defense
    - [ ] Other: ___________

42. **Was this before or after Aurora acquisition?**
    - [x] Before acquisition
    - [ ] During acquisition
    - [ ] After acquisition (working for Aurora)
    - [ ] Don't remember

### Photodetector

43. **What were the photodetector specifications?**
    - Bandwidth: ___________ kHz to ___________ GHz (you stated 300kHz-1GHz, confirm?)
    - Crosstalk: < ___________ dB
    - Sensitivity: ___________ A/W or dBm
    - Or state "don't remember exact specs": don't remember exact specs
      
44. **Did this go into production?**
    - [ ] Yes - production unit
    - [x] No - prototype only
    - [ ] Don't know

### Power Distribution

45. **What was the 200W power board for?**
    - [ ] LIDAR sensor main power
    - [ ] Laser driver
    - [x] Computing module
    - [ ] Other: ___________

    Computing and laser power management
    
47. **What automotive standard compliance was required?**
    - [x] CISPR 25 (EMC)
    - [x] ISO 7637 (transients)
    - [x] ISO 16750 (environmental)
    - [ ] Other: ___________

### Test Automation

47. **What was the efficiency improvement from LabVIEW automation?**
    - Test time BEFORE: ___________ minutes/hours per unit
    - Test time AFTER: ___________ minutes/hours per unit
    - Improvement: ___________x faster or ___________%

	Atomization wasn’t measured. But the goal was to provide a methodology for calibrating and validating

49. **How many optical sub-assemblies did you test?**
    - Units per day: ___________
    - Total units tested: ___________
    - Or state "don't remember": ___________


---

## SECTION 6: Los Alamos National Laboratory - Internship Context

### Timeline

49. **Was this during college?**
    - [ ] Yes - summer + fall semester 2017
    - [ ] Yes - gap year
    - [x] After graduation
    - [ ] Other: ___________

50. **Did you have a security clearance?**
    - [ ] Yes - Secret
    - [ ] Yes - Q Clearance
    - [x] No clearance required
    - [ ] Other: ___________

### Underwater Optical Transceiver

51. **What was the detection sensitivity or performance?**
    - Angular resolution: ___________ degrees
    - Detection range: ___________ meters
    - Modulation frequency: ___________ Hz/kHz
    - Or state "don't remember": ___________

52. **What was the application?**
    - [ ] Underwater communications research
    - [ ] Sensor positioning
    - [ ] Classified/can't disclose
    - [ ] Other: ___________

### Uranium Oxide Devices

53. **What was the application of these devices?**
    - [ ] Radiation sensors
    - [ ] Nuclear materials research
    - [ ] Classified/can't disclose
    - [ ] Other: ___________

Uranium oxide devices for solar cells in rad environments (space satellites)

54. **Can you mention this on a public resume?**
    - [x] Yes - unclassified research
    - [ ] No - should remove or generalize
    - [ ] Unsure

---

## SECTION 7: General Questions

### Publications & Patents

55. **Do you have any patents?**
    - [ ] Yes - issued patents
    - [ ] Yes - pending patents
    - [x] No
    - If yes, list titles/numbers: ___________

56. **Do you have any publications?**
    - [ ] Yes - peer-reviewed papers
    - [ ] Yes - conference presentations
    - [x] Yes - internal white papers
    - [ ] No
    - If yes, list titles: ___________

### Certifications

57. **Do you have any relevant certifications?**
    - [ ] AWS Certified
    - [ ] Professional Engineer (PE)
    - [ ] Other technical certifications
    - [ ] No certifications

FE in electrical engineering

### Open Source & Side Projects

58. **Do you contribute to open source?**
    - [ ] Yes - active maintainer
    - [ ] Yes - occasional contributor
    - [x] No
    - If yes, notable projects: ___________

59. **Do you have any side projects worth mentioning?**
    - [ ] Yes - deployed products
    - [ ] Yes - GitHub projects
    - [x] No
    - If yes, describe: ___________

### Skills Verification

60. **Node.js is listed in your skills - have you used it professionally?**
    - [ ] Yes - in role: ___________
    - [ ] No - should be removed
    - [ ] Side projects only

Node is a dependency of react and our development chain.

61. **Which of these tools have you actually used professionally?** (Check all that apply)
    - [x] Jest (testing) and vitest
    - [x] Vite (build tool)
    - [x] Turbo (monorepo)
    - [ ] Webpack
    - [ ] Docker
    - [x] GitHub Actions / CI/CD
    - [x] Figma (design collaboration)

---

## SECTION 8: Goals & Target Roles

### Resume Purpose

62. **What is the primary purpose of this resume?**
    - [x] Internal promotion at Fluke
    - [x] External job search
    - [x] Updating LinkedIn
    - [x] All of the above

63. **What roles are you targeting?**
    - [x] Senior Software Engineer
    - [ ] Staff Engineer
    - [x] Frontend Architect
    - [ ] Technical Lead
    - [ ] Other: ___________

64. **Are you targeting frontend-only roles or full-stack roles?**
    - [ ] Frontend only
    - [x] Full-stack
    - [ ] Either
    - [ ] Other: ___________

65. **Do you want to emphasize your hardware background or minimize it?**
    - [x] Emphasize - it's a differentiator
    - [ ] Minimize - focus on software only
    - [ ] Balance both equally

---

## Instructions

1. **Answer as many questions as possible** - the more detail you provide, the better the resume
2. **Estimates are fine** - "approximately 50 tests" or "around 80% reduction" is better than nothing
3. **Be honest about gaps** - if you don't remember or can't disclose, say so
4. **Save this file when done** - I'll analyze your responses and generate a revised resume

---

## Next Steps

After completing this questionnaire:
- I will analyze your responses
- Identify which metrics/details to include in the resume
- Generate a revised resume with proper context and quantification
- Suggest which details to save for cover letters vs. include in resume
