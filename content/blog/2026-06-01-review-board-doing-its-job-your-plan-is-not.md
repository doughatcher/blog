---
title: "The Review Board Is Doing Its Job. Your Plan Is Not."
date: 2026-06-01
pillar: "Wild Card"
tags: []
linkedin_copy: |
  The work is not gated by code. It is gated by who else has to read the document next.
  
  Review boards are not blockers. They are work your plan forgot to model.
  
  Full post: {{url}}
---

Every delivery team I know has a story about a review board that killed their momentum. Architecture review. Security review. Vendor management. Data privacy. The story always goes the same way: "We were ready to go. We submitted. And then we waited six weeks for a committee to read a document."

The implied villain is the review board. The review board is slow. The review board does not understand urgency. The review board is a bureaucratic obstacle between the team and progress.

This framing is wrong. The review board is doing its job. Your project plan failed to model the review board as work.

Here is what I mean. A typical enterprise commerce engagement has at least three approval gates between design and deployment. An architecture review board that validates the integration pattern. A security review that validates data handling, authentication, and PCI scope. A vendor-management review that validates the commercial terms of any new third-party dependency.

Each board meets on its own cadence. Biweekly, sometimes monthly. Each board has its own documentation requirements. Each board has a backlog of submissions from other projects. Your submission goes into a queue. The queue has a cycle time. That cycle time is measured in weeks, not days.

None of this is hidden. Every enterprise practitioner knows these boards exist. The failure is that project plans treat the approval as a milestone, a single point on a Gantt chart, instead of a dependency with duration, prerequisites, and its own critical path.

A two-week design pass followed by an architecture review does not take two weeks. It takes two weeks of design, plus one to two weeks to prepare the submission document to the board's standard, plus two to four weeks in the board's review queue, plus one week for revisions if the board has questions. That is five to nine weeks of elapsed time for what the plan called "two-week design pass."

When the project plan says two weeks and reality says seven, the team blames the board. But the board's cycle time was knowable before the plan was written. The plan chose not to know it.

I have watched this pattern play out with particular sharpness in AI tooling adoption. A team builds a working proof of concept. The proof of concept is good. It solves a real problem. The team is excited. They submit it for security and data-privacy review. The review takes eight weeks. By the time the review clears, the tool has been updated twice, the team has moved on to other work, and the proof of concept has aged out. The approval came through for a version of the tool that no longer matches what the team wants to deploy.

The instinct is to blame the review process. But the review process did exactly what it was supposed to do: evaluate the security and privacy posture of a tool that touches production data. That evaluation takes time. The failure was building the proof of concept without modeling the approval timeline. The team treated approval as a formality. It was not a formality. It was the longest dependency in the chain.

The fix is not faster review boards. Faster review boards would be nice, but they are not something the delivery team controls. The fix is modeling review boards as first-class dependencies in the project plan, with realistic cycle times, documentation prep time, and revision buffers.

This means three things in practice.

First, submit early. If the architecture review board meets biweekly and has a two-week queue, submit your design for review before the design is final. Submit a draft. Get in the queue. Refine while you wait. The board will review what you have and come back with questions. Those questions will improve the design. This is better than waiting until the design is perfect and then discovering the queue.

Second, treat the submission document as a deliverable, not as overhead. The architecture review board's template exists for a reason. Filling it out properly takes time. That time belongs in the plan. If the plan does not have a line item for "prepare ARB submission," the plan is incomplete.

Third, talk to the board before you need them. Every review board I have worked with has an informal pre-submission conversation available. "We are building this. Here is the rough shape. What should we be thinking about before we submit?" That conversation takes 30 minutes and saves weeks. It also builds a relationship with the reviewers that makes the formal submission go faster.

The broader point is this. Delivery teams in enterprise environments operate inside a system of governance. That governance exists because the organization has been burned before. Someone deployed a tool without a security review and it leaked data. Someone integrated a vendor without a commercial review and the contract was unfavorable. The boards are scar tissue. They are slow because the cost of being fast was higher than the cost of being slow.

Your plan needs to respect that history. Not fight it.

The work is not gated by code. It is gated by who else has to read the document next. If your plan does not account for that reader's calendar, your plan is wrong.