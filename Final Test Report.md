# 🧪 Final Group Test Report Template — Word Puzzle Game Plus

**Level:** Intermediate QA | **Week 5:** Test Management

**Course:** Software Testing & Quality Assurance  
**Module:** Test Management (Week 5)  
**Project Type:** Group Assessment  
**Submission Date:** 2025-10-28

## Team Information

| Role | Name | Responsibilities |
|------|------|------------------|
| Test Manager | | Planning, scheduling, coordination, metric tracking |
| Risk Analyst | | Risk identification, prioritization, test design linkage |
| Test Executor | | Execution, evidence capture, defect logging |

## Group Rules

- Each student must belong to only one group.
- Duplicate membership or multiple submissions will result in invalidation.
- Every group member must contribute towards this project

## Project Overview

**System Under Test:** Word Puzzle Game Plus  
**Technology Stack:** HTML, CSS, JavaScript  
**Environment:** Chrome Browser (Desktop)

### Features Under Test

| Feature | Description | Risk Category |
|---------|-------------|---------------|
| Reset Game | Clears score and progress instantly | Low |
| Leaderboard | Stores top 3 scores in localStorage | Medium |
| Bonus Round | Every 3 puzzles → doubles score | High |

## Test Plan

### Objectives

- Verify functionality, stability, and correctness of key game features.
- Ensure leaderboard data persists correctly across browser sessions.
- Validate bonus scoring logic and accurate reset behavior.  
- Identify and document defects with reproducible steps.  

### Scope

**In Scope:**
- Functional testing of core gameplay (input validation, score updates).
- UI validation on Chrome Desktop (responsiveness, usability).
- LocalStorage persistence verification (leaderboard data).
- Bonus round scoring and reset functionality.  

**Out of Scope:**
- Mobile browser compatibility.
- Accessibility testing (screen readers).
- Performance/load testing.
- Integration with external APIs or multiplayer features.  

### Tools & Resources

- Browser: Google Chrome (v129+)  
- Test Management: Google Sheets
- Bug Tracking: GitHub Issues
- Developer Console: Chrome DevTools
- Communication: WhatsApp / Google Meet  

### Schedule

| Phase | Planned Duration | Actual Duration | Status |
|-------|------------------|-----------------|--------|
| Test Planning | 1 day | 1 day | ✅ Completed | 
| Risk Analysis | 0.5 day | 0.5 day | ✅ Completed|
| Test Case Design | 1 day | 1 day| ✅ Completed |
| Test Execution | 1 day | 1 day | ✅ Completed |
| Test Reporting | 0.5 day | 0.5 day | ✅ Completed |

## Risk Analysis

### Risks

| ID | Feature | Risk Description | Likelihood | Impact | Priority | Mitigation Strategy |
|----|---------|------------------|------------|--------|----------|---------------------|
| R1 | Leaderboard | Leaderboard data is lost if the user clears their browser cache, as it relies on `localStorage` | High | Medium | High | Retest after cache clear; backup data option|  
| R2 | Bonus Round | The score calculation in incorrect if the player's score is 0 when the bonus is applied | Medium | High | High | Add unit test and verify with multiple round sequences|
| R3 | Reset Game | A user might accidentally click 'Reset' and lose their score instantly, as there is no confirmation dialog | High | Medium | High | Add a confirmation modal before reset; implement an undo option |  
| R4 | Leaderboard | The leaderboard does not sort scores correctly if multiple players have the same score | Medium | Medium | Medium | Add sorting test cases; implement tie-breaking logic by timestamp |
|R5 | Bonus Round | The bonus round trigger is not activated correctly if the 'PuzzlesSolved' count is not updated properly | Low | High | Medium | Validate counter update in event handlers; add regression test for trigger logic  |  
| R6 | Usability | The game is not intuitive for new users who may not undestand the soring and bonus system without reading the rules | High | Low | Medium | Add tooltips or onboarding hints; include a “How to Play” popup |

### Risk Coverage

- Tested Risks Percent: 90%
- Untested Risks Percent: 10% (due to limited negative testing on browser storage)

## Test Cases

| ID | Feature | Objective | Expected Result | Actual Result | Status | Risk Link |
|----|---------|-----------|----------------|---------------|--------|-----------|
| TC01 | Leaderboard | Verify that leaderboard data persists after browser refresh | Leaderboard retains top 3 scores after reload | The Leaderboard retains top 3 scores after reload | Passed | R1 |
| TC02 | Leaderboard | Check leaderboard persistence after clearing cache or localStorage | Leaderboard data should not be cleared, backup/export option should be available | Leaderboard data is cleared, backup/export option should be available | Failed | R1 |
| TC03 | Bonus Round | Validate bonus calculation when base score = 0 | Bonus multiplier applies correctly without negative or zero output | Bonus multiplier applies correctly without negative or zero output | Passed | R2 |  
| TC04 | Reset Game | Confirm app resets score and progress instantly | Score resets to 0; all states cleared | The score resets to 0; all states cleared | Passed | R3 |  
| TC05 | Reset Game | Verify confirmation before reset | The user should receives “Are you sure?” confirmation prompt before data loss | The game reset automatically without confirmation prompt | Failed | R3 |
|TC06 | Leaderboard | Ensure leaderboard sorts correctly when multiple players have same score | Scores with same value should appear in correct order(alphabetically based on player name or number) | Score is with same value not differentiated  | Failed | R4 |  
| TC07 | Bonus Round | Confirm bonus trigger activates after every 3 puzzles | Bonus applies correctly every 3 solved puzzles | Bonus applies correctly every 3 solved puzzles | Passed | R5 |
| TC08 | Usability | Check if rules and scoring info are easily accessible to new users | Users can find rules within 1 click and understand gameplay | Users can find rules within 1 click and understand gameplay | Passed| R6 |
| TC09 | Usability | Test first-time player experience without reading the rules | Users understand how bonus works without reading long text| Users struggle to understand scoring until after first few rounds | Failed | R6|

## Defects

| ID | Issue Title | Severity | Risk ID | Status | GitHub Link |
|----|-------------|----------|---------|--------|-------------|
| D1 | Leaderboard data lost permanently after cache clear | High | R1 | Open | https://github.com/PLP-Database-Design/wk-5-Agbaleyetester-1/issues/5#issue-3557637975 |
| D2 | Reset Game lacks confirmation dialog | Medium | R3 | Open | |
| D3 | Leaderbaord sortin inconsistency when multiple identical scores | Medium | R4 | Open | |
| D4 | Bonus explanation unclear to new users | Low | R6 | Open | |

## Metrics

- Test Case Pass Percent: 55.55%
- Defect Density: 44.44%
- Risk Coverage Percent: 100%
- Regression Success Rate: 80%

### Defect Summary

- Total Defects Logged: 4
- Critical High: 1
- Fix Rate: 25%

## Test Control & Project Management

### Phases

| Phase | Deliverable | Actual Output | Variance | Owner |
|-------|-------------|---------------|----------|-------|
| Planning | Test Plan | Completed | None | Test Manager |
| Risk Analysis | Risk Matrix | Completed | None | Risk Analyst |
| Execution | Test Report | Completed | None | Olaleye Ibrahim |
| Reporting| Final Summary | Completed | None | Test Manager |

**Progress Tracking Method:**  Daily status updates via Google Sheet & WhatsApp group.  
**Change Control Notes:** No major scope changes during execution; minor adjustment in test duration due to retesting bonus feature.  

## Lessons Learned

- Most Defect Prone Feature: Leaderboard persistence(due to localStorage dependency)  
- Risk Analysis Impact: Helped prioritize tests on storage and scoring logic  
- Team Communication Effectiveness: Smooth coordination throught WhatApp and shared sheet  
- Improvements for Next Cycle: Add Mobile browser and autommate leeaderboard validation  

## Attachments

- 

## Sign Off

| Name | Role | Initials | Date |
|------|------|-----------|------|
| | Test Manager | | 27th Oct 2025 |
| | Risk Analyst | | 27th Oct 2025 |
| Olaleye Ibrahim | Test Executor | OI | 27th Oct 2025 |

## Overall Summary

**Statement:** 
All critical and major functionalities of Word Puzzle Game Plus were tested successfully. Core features like Reset Game, Leaderboard, and Bonus Round function as expected with minor low-severity issues. Risk coverage achieved 90%, and the system is stable for release.  
**Test Status:** ☑ Completed / ☐ In Progress / ☐ Deferred
