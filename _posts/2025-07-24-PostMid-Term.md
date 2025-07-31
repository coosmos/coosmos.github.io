---
layout: post
title: "Post Mid-Term Evaluation | GSoC 2025"
date: 2025-07-24
categories: [GSoC, KDE]
tags: [GSoC, KDE, Mankala, QML, Kirigami, Post-MidTerm]
---
<h2 style="color: #4285F4;">Post Mid-Term Evaluation</h2>


The mid-term evaluation period for GSoC 2025 took place from July 14th to July 18th. During this phase, contributors are required to submit a progress report via the official GSoC dashboard. At the same time, mentors provided their evaluations based on our performance, communication, and code contributions.

I'm happy to share that I’ve successfully passed the mid-term evaluation ✅

This milestone was more than just a checkpoint — it was a chance to reflect on how far I’ve come since the beginning of the project. From setting up the development environment and understanding the GCompris codebase, to contributing my first features and collaborating with mentors, the journey so far has been packed with learning, growth, and problem-solving.

The feedback from my mentors has been encouraging and constructive. It helped me realign and improve both in terms of development quality and clarity of communication and pacing up for final lap. With the mid-term behind me, I now feel more confident and focused heading into the final stretch of GSoC.

<h2 style="color: #FBBC05;">What's Done So Far</h2>

From my last blog post, I had outlined a few key tasks in my to-do list.
 Here’s a summary of what’s been completed:

✅ 1. Fixed the Editor UI Break (childRect height issue)

The editor UI was previously breaking due to layout issues with childRect height. This has now been fixed by usage of SpinBoxes, which are more stable and major thing is it handles locale conversion effectively .

✅ 2. Built the Editor for Learn Decimals Addition & Subtraction

![AdditionsEditor](/resources/Gsoc/learnDecimalsAddition.png){: width="400" height="300"}

✅ 3.  Refactored Dataset Logic in Learn Decimals

One of the major changes in this phase was the refactoring of the dataset logic in the Learn Decimals activity. Previously, there were different types of datasets for learn decimals  which made the codebase unnecessarily complex.

I restructured the logic so that the activity now share a unified dataset format. This change significantly reduces complex if-else checks , simplifies parsing, and makes the code more maintainable in the long run.

This refactoring also involved updating the legacy dataset handling logic to align with the new structure, resulting in cleaner code overall.

---
<h2 style="color: #EA4335;">The Journey: Problems Faced and Solutions Found</h2>


A major chunk of my time during this phase was spent figuring out why things were breaking whenever I introduced new changes — especially while restructuring the dataset and integrating the editor UI. Since the codebase is quite modular and parts of it interact behind the scenes, even a small tweak would sometimes lead to unexpected behavior.

To deal with this, I relied heavily on:

    Log statements: Adding custom logs at multiple points helped me trace values and flow step-by-step.

    Reading through the existing codebase: Understanding the older logic was important before replacing or restructuring anything.

    Debugging through trial and error: Often, it came down to testing small blocks of code and observing what broke.

    Asking mentors: When I got stuck  I discussed it with my mentors to avoid going in circles.

    Going through Gcompris + QMl documentation: Especially helpful for understanding how binding, layouts, or components behaved internally.

    debugging things using :
    Component.onCompleted: {
        console.info("adding debugging statements ")
    }
    onValueChanged: {
        console.info("adding logs to track a variable or a UI component")
    }
    helped me a lot to understand


Most of the bugs weren’t just simple one-liners — they came from misunderstandings of how parts of the system were tied together. Fixing those required digging into the logic deeply, which — although time-consuming — gave me a stronger understanding of the internals and improved the way I now approach changes.

---

<h2 style="color: #34A853;">Feedback Received</h2>


As part of the mid-term evaluation, I received formal confirmation from Google  that I successfully passed the evaluation phase.
![AdditionsEditor](/resources/Gsoc/passed.png){: width="400" height="300"}

I received feedback from my mentor acknowledging the current status of the project and the areas where I need to improve. The feedback was clear:

    “Ashutosh needs to be more involved in this project. His work is way behind schedule and a big effort will be needed if he wants to deliver what is planned for the end of GSoC.”

This was a much-needed reality check. While I’ve made progress in understanding the codebase and solving tricky issues, I recognize that my overall pace has been slower than expected. A lot of time went into debugging and learning the internals, which slowed down feature development.

---
<h2 style="color: #4285F4;"> Roadmap Ahead</h2>

With the mid-term evaluation complete and feedback taken into account, I’ve reassessed my remaining tasks and adjusted the schedule accordingly.

✅ Progressed So Far:

    Learn Decimals dataset editor (Random + Fixed)

    Learn Decimal Addition/Subtraction

    Learn Quantities

These were part of the planned deliverables for Weeks 1–4, and despite some delays, these activites are functional.
In the next phase (remaining ~30 days), I plan to do the following:
<br>

<b style="color: #FBBC05;">📌 Graduate Lines – Read / Use</b><br>
<span style="color: #777;">→ Build the dataset editor and refactor legacy dataset structure.</span><br>
<b style="color: #999;">🗓 Planned completion: August 7–8</b>

<br>

<b style="color: #EA4335;">📌 Fractions – Create / Use</b><br>
<span style="color: #777;">→ Start working on editor for fraction-based activities.</span><br>
<b style="color: #999;">🗓 Planned start: Before mid-August</b>

<br>

<b style="color: #4285F4;">📌 Final Cleanup & Submission</b><br>
<span style="color: #777;">→ Clean up all merge requests and prepare a final status report.</span><br>
<b style="color: #999;">🗓 Final wrap-up: End of August</b>

---


