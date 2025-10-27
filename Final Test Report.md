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
| R2 | Bonus Round | The score calculation in incorrect if the player's score is 0 when the bonus is applied | Medium | High | High | Add unit test and verify with multiple round sequences|  |  
| R3 | Reset Game | A user might accidentally click 'Reset' and lose their score instantly, as there is no confirmation dialog | High | Medium | High |  |  
| R4 | Leaderboard | The leaderboard does not sort scores correctly if multiple players have the same score | Medium | Medium | |
|R5 | Bonus Round | The bonus round trigger is not activated correctly if the 'PuzzlesSolved' count is not updated properly | Low | High | Medium | |  
| R6 | Usability | The game is not intuitive for new users who may not undestand the soring and bonus system without reading the rules | High | Low | Medium | 

### Risk Coverage

- Tested Risks Percent: 
- Untested Risks Percent: 

## Test Cases

| ID | Feature | Objective | Expected Result | Actual Result | Status | Risk Link |
|----|---------|-----------|----------------|---------------|--------|-----------|
| | | | | | | |

## Defects

| ID | Issue Title | Severity | Risk ID | Status | GitHub Link |
|----|-------------|----------|---------|--------|-------------|
| | | | | | |

## Metrics

- Test Case Pass Percent: 
- Defect Density: 
- Risk Coverage Percent: 
- Regression Success Rate: 

### Defect Summary

- Total Defects Logged: 
- Critical High: 
- Fix Rate: 

## Test Control & Project Management

### Phases

| Phase | Deliverable | Actual Output | Variance | Owner |
|-------|-------------|---------------|----------|-------|
| | | | | |

**Progress Tracking Method:**  
**Change Control Notes:**

## Lessons Learned

- Most Defect Prone Feature: 
- Risk Analysis Impact: 
- Team Communication Effectiveness: 
- Improvements for Next Cycle: 

## Attachments

- 

## Sign Off

| Name | Role | Initials | Date |
|------|------|-----------|------|
| | Test Manager | | |
| | Risk Analyst | | |
| | Test Executor | | |

## Overall Summary

**Statement:** 

**Test Status:** ☐ Completed / ☐ In Progress / ☐ Deferred
