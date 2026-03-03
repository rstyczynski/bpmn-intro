# Let's make pizza with BPMN

<p align="center">
  <img src="image/logo.jpg" alt="Pizza BPMN Logo" width="300" />
</p>

For a long time, I was looking for a good pizza recipe. I started before the internet era, asking friends how to make this tasty food. Finally, after years, I opened an Italian cookbook and voila - I was able to make my first good pizza bread. Of course, the secrets are hidden in small details that are easy to overlook. After many years, I have the impression that I know those secrets, and I am happy to share one more lesson discovered in my professional work: the importance of business process documentation with well-known standards.

## Introduction to BPMN

BPMN (Business Process Model and Notation) is a well-established standard for visually describing how a process works from start to finish. You can read it like a map: who does what, in what order, and what decisions change the path. BPMN helps you:

- understand the process without reading long technical text,
- see hand-offs between people or systems,
- spot branching points and timing behavior,
- discuss improvements with a shared vocabulary.

There is nothing better than an example, so let's take a look at a pizza bread-making process.

## Let's make pizza bread!

Imagine a family returning from a winter trip; they are on the road and will be back home the next day. They love homemade pizza and ask their loved ones at home to prepare this welcome dinner. The presented process describes both the request and the pizza-bread preparation. It is not a fully ready pizza yet - just the bread. The final step is done at home, when everyone is together, to serve freshly baked pizza.

<p align="center">
  <img src="model/pizza_2.1.0.svg" alt="Pizza bread making BPMN" width="600" />
</p>

The model is built in draw.io and is available [here](https://app.diagrams.net/?url=https://raw.githubusercontent.com/rstyczynski/bpmn-intro/refs/heads/main/model/models.drawio).

## How to read the pizza bread process

Start with these six elements:

- **Pools** separate organizational units with their own processes (here: `On the road`, `Home`) and communicate with each other using messages.
- **Events (circles):** mark when something starts, waits, or ends.
- **Lanes:** separate responsibilities (for example `Hungry guys`, `Kitchen owner`, `Chef`).
- **Tasks (rounded rectangles):** show concrete actions, for example mixing ingredients.
- **Gateways (diamonds):** split or join paths, such as choices (XOR), parallel work (AND), or one-or-more possibilities (OR).
- **Sequence flows (arrows):** show the order of execution.

This is enough to understand most of the model quickly, even before learning advanced BPMN features. Even with new elements, most of the model is intuitive.

## First steps

My advice is to focus on `pools` and `gateways`, which may be new concepts if you know only regular activity diagrams. Pools represent participants (for example, another team in the same company or an external partner/supplier). Gateways are more expressive than in a typical flowchart and are used to control branching and merging logic.

- **Choice** - XOR Gateway: exactly one path is selected based on a condition; when joining, one incoming path is enough to continue.
- **Parallel** - AND Gateway: all paths are started in parallel; when joining, all incoming paths must arrive before continuing.
- **One or more** - OR Gateway: one or many paths can be selected based on conditions; when joining, it waits only for the paths that were actually activated.

In practice, branching and merging gateways are usually used together, as shown in the pizza-bread process.

## Next steps

As an exercise, extend the model to a full pizza-making process.

## Why is it important to stick to BPMN?

You may say: "It's easy. I don't need to learn anything new - a simple activity flow (flowchart) is enough." That is partly true, but it is like my pizza-making learning curve: without a good method, it can take years of trial and error to reach the right level.

BPMN builds on 40+ years of process-modeling experience, including common pitfalls. There is no need to repeat those mistakes. It is easy to start with simple BPMN notation, and once you make the first step, more advanced use cases come naturally.

It is like learning math: `2+2` comes before `x`, `x^2`, and the Pythagorean theorem, and all of them come before `sin(x)`.

## Tools

There are many tools for BPMN modeling. Personally, I use one of the simplest: [draw.io](https://draw.io) - a universal business and IT diagramming tool that runs in the browser. Both browser and desktop versions are available.

Draw.io comes with rich palettes of modeling elements, such as UML and BPMN. From a behavioral perspective, beyond regular nodes and connectors, notice `view/tags`, which make it possible to logically group elements and show or hide them. In my model, you will notice tags for `process`, `frame`, and `comments`. Using tags makes modeling easier. Draw.io supports export to many formats, including SCG, JPG, which is used in this project.

The formal owner of the standard is [OMG](https://www.omg.org/spec/BPMN); however, its documents can be difficult to read. For a learning path, I recommend starting with the [CIB seven BPMN 2.0 Implementation Reference](https://docs.cibseven.org/manual/2.0/reference/bpmn20/) and then using the OMG [BPMN 2.0 examples](https://www.omg.org/cgi-bin/doc?dtc/10-06-02.pdf).

Enjoy making pizza with BPMN!

Enjoy modeling business processes with BPMN!
