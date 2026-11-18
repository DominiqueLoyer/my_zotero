---
title: "Intelligent agents :ch. 2"
item-type: "bookSection"
authors:
  - "Russell Stuart"
  - "Norvig Peter"
date: "2015"
year: "2015"
publication: "Artificial intelligence : A modern approach."
publisher: "Prentice- Hall"
tags:
  - "doi-fix:low-confidence"
  - "notion"
collections:
  - "Cours A24/DIC9001/Russell"
zotero-key: "7NSIEARN"
zotero-library: 1
zotero-uri: "zotero://select/library/items/7NSIEARN"
date-added: "2024-12-11 19:33:09"
date-modified: "2026-11-18 01:46:38"
---

# Intelligent agents :ch. 2

**Russell Stuart; Norvig Peter**

## Attachments

- Texte 11b Russell  Norvig 2015 ch. 2.pdf _(file not in repository: missing)_
- [Notion](notion://www.notion.so/russellstuartIntelligentAgentsCh2015-2c09fa248c5781d4901ed8029718e75b)

## Annotations

- **p. 1, highlight** “How well an agent can behave depends on the nature of the environment; some environments are more difficult than others”
- **p. 1, highlight** “An agent is anything that can be viewed as perceiving its environment through sensors”
- **p. 1, highlight** “SENSOR acting upon that environment through actuator”
- **p. 1, highlight** “A human agent has eyes, ears, and other organs for sensors and hands, legs, vocal tract, and so on for actuators. A robotic agent might have cameras and infrared range finders for sensors and various motors for actuators”
- **p. 1, highlight** “A software agent receives keystrokes, file contents, and network packets as sensory inputs and acts on the environment by displaying on the screen, writing files, and sending network packet”
- **p. 2, highlight** “agent’s behavior is described by the agent function that maps any given percept sequence to an action”
- **p. 2, highlight** “agent function for an artificial agent will be implemented by an agent program”
- **p. 2, highlight** “The agent function is an abstract mathematical description; the agent program is a concrete implementation, running within some physical system”
- **p. 2, highlight** “agent function”
- **p. 2, highlight** “if the current square is dirty, then suck; otherwise, move to the other square”
- **p. 3, highlight** “tool for analyzing systems, not an absolute characterization that divides the world into agents and non-agents”
- **p. 3, highlight** “rational agent is one that does the right thing”
- **p. 4, highlight** “definition of a rational agent:  For each possible percept sequence, a rational agent should select an action that is ex- pected to maximize its performance measure, given the evidence provided by the percept sequence and whatever built-in knowledge the agent ha”
- **p. 9, highlight** “chess is a competitive multiagent environment”
- **p. 9, highlight** “ta”
- **p. 9, highlight** “axi-driving environment”
- **p. 9, highlight** “partially cooperative multiagent environmen”
- **p. 9, highlight** “t”
- **p. 9, highlight** “communication often emerges as a rational behavior in multiagent environments”
- **p. 9, highlight** “randomized behavior is rational because it avoids the pitfalls of predictability.”
- **p. 9, highlight** “Deterministic vs. stochastic”
- **p. 9, highlight** “If”
- **p. 9, highlight** “f the next state of the environment is completely deter STOCHASTIC mined by the current state and the action executed by the agent, then we say the environment is deterministic; otherwise, it is stochastic.”
- **p. 10, highlight** “ully observable, deterministic environment”
- **p. 10, highlight** “we ignore uncertainty that arises purely from the actions of other agents in a multiagent environment;”
- **p. 10, highlight** “game can be deterministic even though each agent may be unable to predict the actions of the others”
- **p. 10, highlight** “partially observable,”
- **p. 10, highlight** “stochastic.”
- **p. 10, highlight** “environment is uncertain if it is not fully observable or not deterministic”
- **p. 10, highlight** “Episodic vs. sequential”
- **p. 10, highlight** “episodic task environment, the agent’s experience is  SEQUENTIAL divided into atomic episodes. In each episode the agent receives a percept and then performs a single action”
- **p. 10, highlight** “Crucially, the next episode does not depend on the actions taken in previous episodes”
- **p. 10, highlight** “In sequential environments, on the other hand, the current decision could affect all future decisions.3 Chess and taxi driving are sequential”
- **p. 10, highlight** “Episodic environments are much simpler than sequential environments because the agent does not need to think ahead”
- **p. 10, highlight** “Static vs. dynamic:”
- **p. 10, highlight** “Static environments are easy to deal with because the agent need not keep looking at the world while it is deciding on an action, nor need it worry about the passage of time. Dynamic environments, on the other hand, are continuously asking the agent what it wants to do; if it hasn’t decided yet, that counts as deciding to do nothing. If the environment itself does not change with the passage of time but the agent’s performance score does, then we say the environment is  SEMIDYNAMIC  DISCRETE semidynamic.”
- **p. 11, highlight** “Discrete vs. continuous”
- **p. 11, highlight** “For example, the chess environment has a finite number of distinct states (excluding the clock). Chess also has a discrete set of percepts and actions. Taxi driving is a continuous-state and continuoustime problem: the speed and location of the taxi and of the other vehicles sweep through a range of continuous values and do so smoothly over time. Taxi-driving actions are also continuous (steering angles, etc.). Input from digital cameras is discrete, strictly speak- ing, but is typically treated as representing continuously varying intensities and locations.”
- **p. 11, highlight** “Known vs. unknown”
- **p. 11, highlight** “agent’s (or designer’s) state of knowledge about the “laws of physics” of the environment. In a known environment, the outcomes (or outcome probabilities if the environment is stochastic) for all actions are given. Obviously, if the environment is unknown, the agent will have to learn how it works in order to make good decisions.”
- **p. 11, highlight** “not the same as the one between fully and partially observable environments. It is quite possible for a known environment to be partially observable—for example, in solitaire card games, I know the rules but am still unable to see the cards that have not yet been turned over. Conversely, an unknown environment can be fully observable—in a new video game, the screen may show the entire game state but I still don’t know what the buttons do until I try them”
- **p. 11, highlight** “As one might expect, the hardest case is partially observable, multiagent, stochastic, sequential, dynamic, continuous, and unknown. Taxi driving is hard in all these senses, except that for the most part the driver’s environment is known. Driving a rented car in a new country with unfamiliar geography and traffic laws is a lot more exciting.”
- **p. 12, highlight** “The job of AI is to design an agent program that implements the agent function— the mapping from percepts to actions”
- **p. 13, highlight** “run on some sort of computing device with physical sensors and actuators—we call this the architecture:  agent = architecture + program”
- **p. 13, highlight** “The agent programs that we design in this book all have the same skeleton: they take the current percept as input from the sensors and return an action to the actuators”
- **p. 19, highlight** “utility”
- **p. 20, highlight** “maximize its utility”
- **p. 20, highlight** “goals are inadequate but a utility-based agent can still make rational decisions”
- **p. 20, highlight** “utility provides a way in which the likelihood of success can be weighed against the importance of the goals.”
- **p. 23, highlight** “In a sense, the performance standard distinguishes part of the incoming percept as a reward (or penalty) that provides direct feedback on the quality of the agent’s behavior.”
- **p. 24, highlight** “search and game-playing (Chapters 3–5), Hidden Markov models (Chapter 15), and Markov decision processes (Chapter 17) all work with atomic representations”
- **p. 24, highlight** “factored representations, we can also represent uncertainty—for example, ignorance about the amount of gas in the tank can be represented by leaving that attribute blank.”
- **p. 24, highlight** “Many important areas of AI are based on factored representations, including constraint satisfaction algorithms (Chapter 6), propositional logic (Chapter 7), planning (Chapters 10 and 11), Bayesian networks (Chapters 13–16), and the machine learning al- gorithms in Chapters 18, 20, and 21”
- **p. 24, highlight** “Structured representations underlie relational databases and first-order logic (Chapters 8, 9, and 12), first-order probability models (Chapter 14), knowledge-based learning (Chapter 19) and much of natural language understanding (Chapters 22 and 23). In fact, almost everything that humans express in natural language concerns objects and their relationships”
- **p. 24, highlight** “the axis along which atomic, factored, and structured repre- sentations lie is the axis of increasing expressiveness”
- **p. 24, highlight** “for example, the rules of chess can be written in a page or two of a structuredrepresentation language such as first-order logic but require thousands of pages when written in a factoredrepresentation language such as propositional logic.”
- **p. 24, highlight** “first-order logic”
- **p. 24, highlight** “propositional logic”
- **p. 24, highlight** “To gain the benefits of expressive representations while avoiding their drawbacks, intelligent systems for the real world may need to operate at all points along the axis simultaneously”
- **p. 25, highlight** “The agent function for an agent specifies the action taken by the agent in response to any percept sequence”
- **p. 25, highlight** “The agent program implements the agent function. There exists a variety of basic agent-program designs reflecting the kind of information made explicit and used in the decision process”
- **p. 25, highlight** “Simple reflex agents respond directly to percepts, whereas model-based reflex agents maintain internal state to track aspects of the world that are not evident in the current percept. Goal-based agents act to achieve their goals, and utility-based agents try to maximize their own expected “happiness.”  • All agents can improve their performance through learning.”
- **p. 25, highlight** “practical reasoning—goes back at least as far as Aristotle’s Nicomachean Ethics. Practical reasoning was also the subject of McCarthy’s (1958) influential paper “Programs with Common Sense.””
- **p. 25, highlight** “The fields of robotics and control theory are, by their very nature, concerned principally with physical agents. The concept of a controller in control theory is identical to that of an agent in AI. Perhaps sur- prisingly, AI has concentrated for most of its history on isolated components of agents— question-answering systems, theorem-provers, vision systems, and so on—rather than on whole agents. The discussion of agents in the text by Genesereth and Nilsson (1987) was an influential exception. The whole-agent view is now widely accepted and is a central theme in recent texts (Poole et al., 1998; Nilsson, 1998; Padgham and Winikoff, 2004; Jones, 2007).”
- **p. 26, highlight** “A paper by Jon Doyle (1983) predicted that rational agent design would come to be seen as the core mission of AI, while other popular topics would spin off to form new disciplines.”
- **p. 26, highlight** “dynamic programming”
- **p. 26, highlight** “Reflex agents were the primary model for psychological behaviorists such as Skinner (1953)”
- **p. 26, highlight** “who attempted to reduce the psychology of organisms strictly to input/output or stim- ulus/response mappings”
- **p. 26, highlight** “Goal-based agents are presupposed in everything from Aristotle’s view of practical rea- soning to McCarthy’s early papers on logical AI. Shakey the Robot (Fikes and Nilsson, 1971; Nilsson, 1984) was the first robotic embodiment of a logical, goal-based agent. A full logical analysis of goal-based agents appeared in Genesereth and Nilsson (1987), and a goal-based programming methodology called agent-oriented programming was developed by Shoham (1993)”
- **p. 26, highlight** “The goal-based view of agents also dominates the cognitive psychology tradition in the area of problem solving, beginning with the enormously influential Human Problem Solv- ing (Newell and Simon, 1972) and running through all of Newell’s later work (Newell, 1990).”

---

[Open in Zotero](zotero://select/library/items/7NSIEARN)
