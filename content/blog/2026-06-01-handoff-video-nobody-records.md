---
title: "The Handoff Video Nobody Records"
date: 2026-06-01
pillar: "The Optimism Cascade"
tags: []
linkedin_copy: |
  The team understood the spec. They did not understand the deal.
  
  The fix is a 15-minute video that almost nobody records.
  
  Full post: {{url}}
---

Every delivery team I have worked with in the last five years has had the same experience. The project kicks off. The team reads the SOW. They review the architecture diagrams. They skim the RFP response. They attend the kickoff meeting.

And then, three weeks in, someone asks a question that reveals the entire team misunderstood why the client bought.

Not what the client bought. Why.

The spec was clear. The integration map was attached. The timeline was aggressive but legible. What was missing was the conversation that happened in the sales cycle where the client's VP said, "We need to be off this platform before the contract expires in November, and if we are not, I will have failed publicly." Or the one where the CTO said, "I do not care about the search integration. I care about the OMS. That is the one that has been killing us."

That context lives in the seller's head. It does not live in the SOW. It does not live in the RFP response. It rarely survives the kickoff meeting, because the kickoff meeting is structured around scope and timeline, not motivation and risk.

The fix is embarrassingly simple. A 15-minute video, recorded by the person who sold the deal, before the kickoff meeting happens. Answering three questions:

1. Why did this client buy now?
2. What are they most afraid of?
3. What did we promise that I want the delivery team to know I promised?

That is it. Fifteen minutes. A screen recording with a talking head. Stored in the project folder. Watched by the tech lead, the project manager, and the solution architect before the first standup.

I have seen this done exactly twice in fifteen years.

The reason it does not happen is not that people think it is a bad idea. Everyone agrees it is a good idea. The reason it does not happen is incentive structure. The person who sold the deal is already selling the next one. Recording a handoff video is an asynchronous task with no deadline, no owner, and no consequence for skipping it. The live kickoff meeting is the path of least resistance. Show up, talk for an hour, answer questions, move on.

The live kickoff is the lowest-effort path for the seller and the highest-cost path for everyone downstream.

Here is what happens without the video. The delivery team builds to spec. They make reasonable assumptions about priority. They sequence work based on technical dependency, not client anxiety. And then the client gets frustrated, not because the work is wrong, but because the team is solving the wrong problem first.

The client wanted the OMS integration locked down in sprint two. The team scheduled it for sprint six because it had fewer technical dependencies. Both decisions were rational. Neither side knew the other's reasoning. The gap between "what the team built" and "what the client expected to see first" is where trust erodes.

Trust erosion in the first month of an engagement is almost impossible to recover. Not because the client is unreasonable. Because the client made a decision to trust a new partner, and the first signal they received was that the partner did not understand their priorities. That signal is hard to override with good work later.

I have heard people argue that the kickoff meeting serves this purpose. It does not. The kickoff meeting is a group setting with slides and introductions and logistics. Nobody says, "I am afraid this project will fail because my last vendor burned me on the OMS and I cannot survive that again." That sentence gets said in a one-on-one sales call, in a moment of candor, and it never gets written down.

I have also heard people argue that the SOW captures this. The SOW captures scope. It does not capture fear. It does not capture the political context inside the client's organization that determines whether the project is perceived as a success. Two projects with identical SOWs can have completely different success criteria based on what the client's internal stakeholders are watching for.

The handoff video is not a process improvement. It is a trust-transfer mechanism. The seller earned the client's trust over months. The delivery team needs to inherit that trust on day one. The video is how the seller says, "Here is what I learned about this person and this organization that you need to know before you start."

Without it, delivery starts cold. Every time.

The pattern I keep seeing is this: organizations invest enormous energy in the sales process and the delivery process, and almost nothing in the seam between them. That seam is where the context drops. And context that drops at the seam shows up as rework, misalignment, and trust erosion downstream.

If you run a delivery org and you want one process change that costs almost nothing and changes almost everything, make the handoff video mandatory. Not optional. Not suggested. Mandatory, with a due date, before the kickoff meeting is scheduled.

Fifteen minutes of one person's time. That is the price of the most important context your delivery team will ever receive.