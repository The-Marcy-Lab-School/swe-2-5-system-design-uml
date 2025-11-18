# swe-2-5-system-design-uml

**Table of Contents:**
- [Setup](#setup)
- [System Design Problem](#system-design-problem)
  - [Time Constraint](#time-constraint)
  - [Part 1: Design Your System](#part-1-design-your-system)
  - [Part 2: Create a UML Diagram](#part-2-create-a-uml-diagram)
  - [Step 3: Record Your Explanation](#step-3-record-your-explanation)

## Setup

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/how-tos/working-with-assignments#how-to-work-on-assignments).

Here are some useful commands to remember.

```sh
npm i                   # install dependencies
git checkout -b draft   # switch to the draft branch before starting

git add -A              # add a changed file to the staging area
git commit -m 'message' # create a commit with the changes
git push                # push the new commit to the remote repo
```

## System Design Problem

### Time Constraint

For this assignment, you will design a system based on the prompt below. This assignment is meant to simulate an interview (and your upcoming assessment) so **aim to spend approximately 2 hours on it total**, and up to 3 hours if you must.
* 20-30 min: Understanding requirements and sketching initial design
* 30-40 min: Creating the UML diagram in LucidChart
* 20-30 min: Writing bullet points for explanation
* 15-20 min: Recording and reviewing the Loom

Your goal should be to hone your intuition around good system design and this time constraint will force you to make decisions.

### Part 1: Design Your System

**Scenario**: You are tasked with designing a **Doctor's Appointment Management system**. Your system design should capture the essential *entities (classes)*, the *responsibilities* of those entities (properties/methods), and the *relationships* between them.

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

We recommend that you take notes as you create your system in the `system-design.md` file and use pen and paper to draw an initial sketch of your design.

### Part 2: Create a UML Diagram

As you approach finalizing your design, transition to [LucidChart](https://www.lucidchart.com/) to create your UML diagram. 

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
