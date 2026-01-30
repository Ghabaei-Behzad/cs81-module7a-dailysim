#Behzad Ghabaei
#CS 81 - JavaScript
#dailySimulation.html
#Reflection.md
#Instructor Seno
#1/27/2026
# Reflection – Daily Schedule Simulator

## What was your approach to designing the schedule?
Explain how you chose your activities and what made them personal or interesting.

My approach was to simulate a high-productivity day for a developer in 2026. I chose activities that reflect a balance between modern technology like: Virtual Reality Brainstorming and Slack, and physical health: like running and meditation. It is personal because it captures the inner thoughts of a student ("trying my best!") and the realistic difficulty of daily goals, such as running anywhere from 1 km to 5 km depending on energy levels. 

## What was one challenge or unexpected behavior you encountered?
Describe anything surprising that happened when you tested the timing.

The most significant observation was the "Execution Gap." When I increased the delays to 4-second intervals (4000 ms, 8000 ms, 12000 ms), dead-air time was not desirable, but also giving a chance to read the messages is important. This taught me that setTimeout is great for managing user expectations. Wait times should not be long and being able to read the messages is important.

## What does this assignment teach you about async code?
Compare this to a regular script that runs top to bottom without delays.

It teaches me that JavaScript doesn't wait for one task to finish before setting up the next one.
In regular script, if this were synchronous, the browser would "freeze" for 24 seconds until the final "Sleep Mode" message appeared.  With async code, due to setTimeout, the script can schedule all seven activities almost instantly, it then remains free to handle other tasks while it waits for the timers to pop. The code is non-blocking.  This simulation uses setTimeout to visualize the flow of asynchronous JavaScript, where code execution is scheduled for the future rather than running instantly.

## What creative element did you add?
Did you add randomization, surprise content, a twist, or other enhancements?

We have included a dynamic randomization twist at the 16-second mark, using Math.floor(Math.random() * surprises.length). The simulation pulls a random outcome from an array. This adds a game-like element and the user doesn't know what they will get (1.) a surprise package, (2.) a pizza invitation, or finally (3.) fix a long-standing bug. Also there is an added timerDisplay to provide a "sub-context" comment to each main activity under our emojis.

## How does this project simulate or differ from real-world schedules?
Explain how well your simulation represents how time works in real life.

In this simulation we saw that it accurately demonstrates the linear progression of time from morning to night, just like a regular day. Just as 9:00 AM always follows 7:00 AM, the 4000 ms event always follows the 0 ms event. In real life there is no trigger really. The "Sleep" event will trigger even if the "Meditation" event fails. But also, in real life, if you don't wake up, you can't go for a run. So the chain of events were somewhat realistic. In advanced JavaScript, we would use Promises to ensure one event successfully completes before the next begins. Promises are the foundation of async programs.  An object returned by an async function represents the current state of operations.  At the time the promise is returned to the caller, the operation isn't finished often.  However, the promise object provides methods to handle the eventual success or failure of an operation. Async functions are used where you might otherwise use promise chains.  In promise chains "await" forces the async function to be completed in series. Promise's "then" method handles with 2 arguments, fulfilled or rejected.  Our code executed from 0 ms to 24 ms and gives our simulation a nice similarity to real-life schedules.
  
