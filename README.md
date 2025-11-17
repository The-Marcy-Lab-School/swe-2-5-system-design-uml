# swe-2-5-system-design-uml

**Table of Contents:**
- [Reminders](#reminders)
  - [Asking ChatGPT for Help](#asking-chatgpt-for-help)
  - [Be Okay With Being "Provisionally Complete"](#be-okay-with-being-provisionally-complete)
- [Setup](#setup)
- [System Design Problem](#system-design-problem)
  - [Part 1: Design Your System](#part-1-design-your-system)
  - [Part 2: Create a UML Diagram](#part-2-create-a-uml-diagram)
  - [Step 3: Record Your Explanation](#step-3-record-your-explanation)

## Reminders

### Asking ChatGPT for Help

If you’re stuck, you may use ChatGPT to clarify the assignment — but not to solve it for you. To do this, copy the meta-prompt below into ChatGPT along with the assignment question.

> You are acting as a tutor. Your job is to explain what this coding question is asking, clarify confusing wording, and highlight the relevant concepts students need to know — but do not provide the full solution or code that directly answers the question. Instead, focus on rephrasing the problem in simpler terms, identifying what’s being tested, and suggesting what steps or thought processes might help. Ask guiding questions to ensure the student is thinking critically. Do not write the final function, algorithm, or code implementation.

Be mindful of your AI usage on assignments. AI can be a great tool to help your learning but it can also be detrimental if you let it do too much of the thinking for you.

### Be Okay With Being "Provisionally Complete"

We know many of you will feel the urge to hold off on submitting until your assignment feels 100% perfect. That drive for excellence is an asset!

But perfectionism can also get in the way of learning — especially when we need to cover a lot in a short amount of time.

That’s why we encourage you to be comfortable with being **“provisionally complete.”** This means:

- Submitting your work even if it isn’t perfect yet
- Treating submission as a checkpoint, not a finish line
- Committing to return, revise, and improve later

Learning to move forward with provisional completeness will help you make steady progress while still building the habit of continuous improvement.

## Setup

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/how-tos/working-with-assignments#how-to-work-on-assignments).

Here are some useful commands to remember.

```sh
npm i                   # install dependencies
git checkout -b draft   # switch to the draft branch before starting

npm test # run the automated tests
npm run test:w # run the automated tests and rerun them each time you save a change

git add -A              # add a changed file to the staging area
git commit -m 'message' # create a commit with the changes
git push                # push the new commit to the remote repo
```

## System Design Problem

### Part 1: Design Your System

**Scenario**: You are tasked with designing an **Doctor's Appointment Management system**. Your system design should capture the essential *entities (classes)*, the *responsibilities* of those entities (properties/methods), and the *relationships* between them.

**System Requirements**:
* Your system should be able to handle the following functionality:
  * A doctor can manage their list of available appointment slots.
  * A patient can book an appointment with a doctor for a specific time slot.
  * An appointment can be marked as "scheduled", "checked in", "in progress", "completed", or "cancelled".
* Your system must include at least three classes that are connected by relationships (associations), with at least one one-to-many relationship.

**Explanation Topics:** 
When you record your explanation, you will be asked to explain:
- How your system handles each of the system functionality requirements above: 
- Why you chose the specific relationships and class responsibilities.  
- At least one significant design decision you made and what alternatives or trade-offs you considered to arrive at your final design. 
  - Examples of significant decisions: where to store your data, how your system handles order status, which class is responsible for X, Y, or Z.

We recommend that you take notes as you create your system in the `system-design.md` file.

### Part 2: Create a UML Diagram

You should create this using a diagramming tool (we recommend [LucidChart](https://www.lucidchart.com/)). 

When you are done, click **Share** in the top right corner, turn on the **Shareable link** and then paste the link in the `system-design.md` file.

**UML Requirements**: Your UML Diagram _must_ have the following:

1. Model relationships using arrows and appropriate multiplicity notation:
   * Exactly one: `1` (e.g. an adoption application has exactly 1 Pet)
   * Zero or more (many): `0..*` (e.g. a shelter has 0 or more pets)

2. Annotate relationships with **association labels** to describe each relationship
   *  Example: "Shelter --creates many--> Applications"
   *  Example: "Application --references one--> Adopter"

3. Include detailed class definitions with:
   * **Properties** (attributes) and their **data types** (e.g. `name: String`)
   * **Methods** (behaviors) and their **named parameters** (e.g. `findPetById(id)`)

### Step 3: Record Your Explanation

1. Use **Loom** to record your screen. For instructions on downloading Loom, refer to the [Marcy GitBook](https://marcylabschool.gitbook.io/marcy-lab-school-docs/environment-setup/loom).
   
2. In your video, you must explain the **Explanation Topics** listed in part 1.

3. Prior to recording, we highly recommend that you write out the key points of your explanation in bullets in the `src/system.design.md` file. 
  
4. Be specific and use proper technical vocabulary:
   | ✅ Good Example                                                          | 🚫 Bad Example                |
   |--------------------------------------------------------------------------|------------------------------|
   | "instance property" or "instance method"                                 | "variable" or "function"     |
   | "Pet status is updated by invoking setStatus()"                          | "A Pet changes status"       |
   | "A shelter houses many pets"                                             | "pets are in a shelter"      |
   | "A donor submits an application by invoking shelter.createApplication()" | "An application is created"  |

5. Keep your video concise (roughly between 5-7 minutes)

6. Upload your video and add the link to the comment at the top of `src/modify-with-video.js`
