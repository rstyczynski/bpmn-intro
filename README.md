# Let's make pizza with BPMN

<p align="center">
  <img src="image/logo.jpg" alt="Pizza BPMN Logo" width="300" />
</p>

For a long time, I was looking for a good pizza recipe. I started before the internet era, asking friends how to make this tasty food. Finally, after years, I opened an Italian cookbook and voila - I was able to make my first good pizza bread. Of course, the secrets are hidden in small details that are easy to overlook. After many years, I have the impression that I know those secrets, and I am happy to share one more discovered in my professional work: the importance of business process documentation with well-known standards.

## Introduction to BPMN

BPMN (Business Process Model and Notation) is a well-established standard for visually describing how a process works from start to finish. You can read it like a map: who does what, in what order, and what decisions change the path. BPMN helps you:

- understand the process without reading long technical text,
- see hand-offs between people or systems,
- spot branching points and timing behavior,
- discuss improvements with a shared vocabulary.

There is nothing better than an example, so let's take a look at a pizza bread-making process.

## Let's make pizza bread!

<p align="center">
  <img src="model/pizza_1.0.0.jpg" alt="Pizza bread making BPMN" width="600" />
</p>

## How to read the pizza bread process

Start with these six elements:

- **Pools** separate organization units with own processes (here: `On the road`, `Home`); communicates with others always using messages.
- **Events (circles):** mark when something starts, waits, or ends.
- **Lanes:** separate responsibilities (for example `Hungry guys`, `Kitchen owner`, `Chef`).
- **Tasks (rounded rectangles):** show concrete actions, for example mixing ingredients.
- **Gateways (diamonds):** split or join paths, such as choices (XOR). parallel work (AND), or one ore more possibilities (OR).
- **Sequence flows (arrows):** show the order of execution.

This is enough to understand most of the model quickly, even before learning advanced BPMN features. Even with new elements majority of the model are intuitive.

## First step

My advice is to focus on `pools` and `gateways`, which may be new concepts if you know only regular activity diagrams. Pools represent participants (for example, another team in the same company or an external partner/supplier). Gateways are more expressive than in a typical flowchart and are used to control branching and merging logic.

- **Choice** - XOR Gateway: exactly one path is selected based on a condition; when joining, one incoming path is enough to continue.
- **Parallel** - AND Gateway: all paths are started in parallel; when joining, all incoming paths must arrive before continuing.
- **One or more** - OR Gateway: one or many paths can be selected based on conditions; when joining, it waits only for the paths that were actually activated.

In practice, branching and merging gateways are usually used together, as shown in the pizza-bread process.

## Why is it important to stick to BPMN?

You may say: "It's easy. I don't need to learn anything new - a simple activity flow (flowchart) is enough." That is partly true, but it is like my pizza-making learning curve: without a good method, it can take years of trial and error to reach the right level.

BPMN builds on 40+ years of process-modeling experience, including common pitfalls. There is no need to repeat those mistakes. It is easy to start with simple BPMN notation, and once you make the first step, more advanced use cases come naturally.

It is like learning math: `2+2` comes before `x`, `x^2`, and the Pythagorean theorem, and all of them come before `sin(x)`.

For formal BPMN 2.0 element definitions and coverage, use the [CIB seven BPMN 2.0 Implementation Reference](https://docs.cibseven.org/manual/2.0/reference/bpmn20/).

Enjoy making pizza with BPMN!

Enjoy making business processes with BPMN!
