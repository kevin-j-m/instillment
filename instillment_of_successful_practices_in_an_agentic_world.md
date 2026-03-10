# Title

InstiLLMent of Successful Practices in an Agentic World

# Elevator Pitch

(You have 300 characters to sell your talk. This is known as the "elevator pitch". Make it as exciting and enticing as possible.)

Let’s leverage the expectations that developers have interacting with LLMs to receive a satisfactory output. We will highlight that through the lens of how we can manage humans and ourselves. Rubyists use a language which promotes developer happiness. Our processes and systems should too.

# Description

(This field supports Markdown. The description will be seen by reviewers during the CFP process and may eventually be seen by the attendees of the event. You should make the description of your talk as compelling and exciting as possible. Remember, you're selling both the organizers of the events to select your talk, as well as trying to convince attendees your talk is the one they should see.)S

Congrats on joining Hours Unlimited. The Math and Numbers team is excited to have you join us on our journey to redefine the importance of numerals. This introductory session will provide tips and tricks for best interacting with powerfuLLMachine, the next-level platform we use to unlock productivity and effectiveness.

# Notes

(This field supports Markdown. Notes will only be seen by reviewers during the CFP process. This is where you should explain things such as technical requirements, why you're the best person to speak on this subject, etc...)
This talk will begin by setting the stage for the audience. They are all attending orientation for a new role where they will be interacting with a Large Language Model developed in-house by the organization: powerfuLLMachine. In this brave new world, rather than removing vowels from company or product names, we're *adding* consonants.

## Interacting with the LLM

### Prompting

As an introduction, we begin by prompting powerfuLLMachine with targeted requests for output. We learn that the smaller we are able to break the problem down, the more predictable results we receive. We observe how specificity and clarity are critical in reducing the feedback loop. We are willing to throw away results that don’t match our expectations. We experiment with alternative implementations. We aren’t precious with the code that’s output while we’re in the development phase.

### Agentic

Taking this a step further, we can provide powerfuLLMachine with more autonomy. Given input requesting a higher-level output, such as a whole feature, we leave the system alone to generate a result. powerfuLLMachine will submit a patch with a review request to our source code management system when it’s done, tagging you as a reviewer.

When asking powerfuLLMachine to complete the task, we must provide a detailed description. It needs to explain what is known in the result we want and where any wiggle room may exist in how it may interpret the instructions.

To reduce repetitive prompting, our code repository has a set of markdown files that powerfuLLMachine knows to ingest prior to any work.

#### background.md

In this file, we identify the qualifications we expect powerfuLLMachine to have and use to complete the task. This can be a paragraph description or bullet points. Examples include:

* Senior developer with 5-10 years of experience with Ruby on Rails
* Familiar with TDD
* Uses Postgres
* Prefers using Turbo over other JavaScript interactions

#### motivation.md

Here we provide a more conversational tone to demonstrate what is driving the system to achieve its goal. It cares about deeply testing functionality, but is mindful of the impact that tests remaining in the regression suite have on our Continuous Delivery system.

We share how it values system design with modularity that increases the number of options we retain while adding features. It is looking to be more aware of existing functionality in the code base, as well as in its dependencies, rather than building something from the ground-up.

#### guardrails.md

This file contains a very important list of instructions that powerfuLLMachine knows it absolutely must follow. This includes statements like:

* No credentials or secret values may be committed in any patches.
* All changes must include tests demonstrating the behavior implemented.
* Do not connect to any deployed environment while developing (don’t ask what led us to need to add that one in).

#### preferences.md

This is the most squishy of our inputs. There are standards we like to live by. They should be our default operating model. However, we recognize that sometimes different approaches are necessary.

* We prefer low-level unit tests over full-scale feature and system tests. However, not at the cost of excessive mocking that’s unrealistic for how the units will be used.
* We value detailed commit messages that explain the why behind the change and explain other options that were considered.
* We like shipping small, atomic units that can be reviewed and delivered quickly.
* When a large change is necessary, consider a “stacked diff” delivery so that reviews can be targeted, even if they’re merged together or in quick succession.

### Reviewing Agentic Coding

We wrap up by sharing expectations for how we expect developers to interact with the code that our agentic powerfuLLMachine delivers for review. It is important to review any patches quickly. It’s likely that more revisions will be necessary, so we should kick off that process as early as possible. We wipe the context of any agentic runners on a regular basis, but retain them for a short period of time for the review phase. We also have limited compute power granted to powerfuLLMachine agents once it delivers code for review. Therefore, we should be very clear about when feedback is required or they are optional suggestions. The system will make an attempt to deliver on suggestions but will balance this against available compute resources in an intelligent fashion.

We also highlight the importance of more qualitative feedback. Praise and positive reactions to particular results, including the reason why it’s appreciated, is important. That feedback will be pushed back into the training corpus for powerfuLLMachine to be used in future changes. Asking a question will cause powerfuLLMachine to reach back into its context to justify choices made, share resources used in making a determination, and highlighting other approaches that could be used, along with their trade-offs.

## Recontextualizing

At this point, we will step outside of our experience at Hours Unlimited for a dramatic reveal: powerfuLLMachine does not exist. At least, not as a product. However, we can reflect on how having such a system could be desirable. And how the work we’ve done to set up our interactions with the system are worthwhile.

Even without powerfuLLM, we can, and should have these benefits.

__H__ ours
__U__ nlimited (our fictional company)
__M__ ath
__A__ nd
__N__ umbers (our fictional department)

HUMAN. We, as humans, deserve the same consideration we’ve been providing to this computer. All of this is for humans. Not text prediction machines. Humans have context and memory. We should embrace this strategy for the humans on our teams before the computers we work on. We should apply Ruby’s ethos of developer happiness to benefit our developers above the tools they’re using to complete their tasks.

### Active Development

We can take the experience we had with prompting powerfuLLMachine step-by-step to inform how we develop changes. The smaller the surface area of the problem we’re solving, while also armed with the entire goal, the more focus we can provide. If we don’t have details about the problem we’re trying to solve, we should seek that out from our team or through research.

We shouldn’t accept that the first approach we take is the best one in all situations. We need to be willing to put it aside and try again, but informed by what we learned from that initial instinct. What was difficult that could be improved? What did we like that we want to continue? We can explore and play with options. It could, dare I say, even be fun.

### Expectations

All the work to set our agentic coding models up for success isn’t lost. This is valuable information that should be shared and documented. When setting out on feature development, we need to know what success looks like. What are we willing to live with, and where can we be flexible?

All the documents we generated for our LLM have value for all of our humans as well. We as individuals are agents. Even more capable of agency than our LLM.

background.md == Job Description
motivation.md == Career Goals and Growth Opportunities
guardrails.md == Policies and Procedures
preferences.md == Team Norms and Expectations

These can, and should be, written out and readily available for all team members. They should be up for debate and modification, much like you would propose a change to these markdown files for a LLM.

### Reviewing Code

These tips and tricks are all valuable for human beings! Work presented for review is either believed to be close to shipping or blocked and needs help. As such, it should be reacted to in a timely fashion. Authors can forget details in their thought process as time goes on.

Authors have moved on to other work. Their capacity to re-engage with what they’ve delivered may be limited. Be clear about how the code should change so it can be merged and why.

Focusing only on what should change is a missed opportunity. Highlight what works well in the code that’s presented. Congratulate authors for the work they’ve done and voice your appreciation. Ask questions to gain insight on how this change was made. Learn from each other. Develop a shared understanding of how you all like to work. That has benefits not only for the change in question. It’s crucial in forming a long-lasting working relationship.

We’re willing to provide all of this for our automated development tools; why not ourselves?

Tags

Ruby, Professional Development, Career Growth

Initial Notes
=====

Running a Team in the World of LLMs

–Policy and procedures 
–Clarity
–Demonstrate what is known
–Show where wiggle room exists. What's unknown
–Task descriptions
–Breaking problems down
–Iterate/explore options
–Push changes - momentum
–Respond to feedback quickly - this is your work that's closest to being done
–Code review feedback suggestions

All of this is important for humans, not a text prediction machine. And humans have context and memory. Embrace these suggestions for the human on your team, not the computer you work on. It's insulting that we're investing in these changes because it will benefit a computer. Not when it would benefit the humans using the computer. Ruby's ethos of developer happiness over the benefit for computers. Hire an early career developer.

powerfuLLMachine

In this brave new world, rather than removing vowels from company/product names, we're adding consonants.

Onboarding at company or product or department with long name with initials that turns into human or person or something like that.

Sections: world building, active development, code review. 

Go through once for the computer and again for the human. 

Background becomes job description. Guardrails become norms, explaining what's expected. Where can we be loose? What must be right? Motivation is growth plans. 

Develop and ship in thin slices. Use feature flags to enable shipping without exposure. Constrain the problem while allowing opportunity to come up with next steps. Building a calculator, writing a test where you typo a letter rather than a number as input. Add a test description "handles non-numeric input" and move on. Later, consider options for how to handle that. 

Praise positive work in code review: adds weight to the training corpus. Be clear when things are suggestions or required (limited compute in the review stage, so llm needs to know where to focus). Ask for justification to learn options considered and why a solution was chosen.
