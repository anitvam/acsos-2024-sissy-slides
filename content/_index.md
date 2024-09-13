+++
title = "Multi-Paradigm Integration for the BDI Resurgence"
outputs = ["Reveal"]

+++

# Multi-Paradigm Integration for the BDI Resurgence

<br>


Danilo Pianini, **Martina Baiardi**, Samuele Burattini, and Giovanni Ciatto <br />
m.baiardi@unibo.it <br /><br />

<small>Department of Computer Science and Engineering (DISI)<br>
Alma Mater Studiorum — Università di Bologna <br>
Via dell’Università 50, 47522 Cesena (FC), Italy </small>

---

## Context
#### Autonomic Computing

<br/>

{{% multicol %}}{{% col %}}

<img src="images/autonomic-diagram.svg" width="100%" />

<div class="mx-5 text-center">

## *<i class="fa-solid fa-arrow-up"></i> MAPE-K* 
Reference <u>model</u> for *Autonomic* and *self-\** systems design. 

</div>

{{% /col %}}{{% col  %}}

<div class="mx-5 text-center">

{{% fragment %}}

<img src="images/bdi-diagram.svg" width="100%" />

## *<i class="fa-solid fa-arrow-up"></i> BDI* 
Reference <u>framework</u> (*AgentSpeak(L)*) for *Multi-Agent Systems*. 

{{% /fragment %}}

</div>

{{% /col %}}{{% /multicol %}}

{{% fragment %}}
<div class="position-absolute">
<iframe src="https://giphy.com/embed/g01ZnwAUvutuK8GIQn" width="100%" height="100%" frameBorder="0" class="fixed-top" allowFullScreen></iframe>

<div class="fixed-top " style="color:white">

<h2 style="color:white"> Why isn't BDI common in autonomic loops? </h2>

</div>

</div>
{{% /fragment %}}

---

# The idea is not new
## It simply disappeared

grafico.

---

## Beliefs, Desires, Intentions

<br />

- It's a framework to model Multi-Agent Systems through *Goals*
  - *Imperative Paradigm* and *Functional Paradigm* are suboptimal to do so 
  - Huge *abstraction gap* between instruction and notion representation
- BDI tries to minimise this gap in the abstraction
  - Mimicking human-level notions such as *beliefs*, *desires* and *intentions*


---

## Beliefs, Desires, Intentions

<br />

Agents are modeled through three main abstractions:
- *Beliefs*: mental state of the agent, that changes over time.
- *Desires*: motivational state of the system.
- *Intentions*: deliberative state of the agent.

<div>
<br />

<small style="text-align: left"> 
--- <br/>
[1] Bratman, Michael. "Intention, plans, and practical reason." (1987) <br />
[2] Anand S. Rao and Michael P. Georgeff. "BDI agents: From theory to practice." (1995) <br />
[3] Anand S. Rao. "Agentspeak(l): BDI agents speak out in a logical computable language." (1996) 
</small>
</div>

---

# BDI Agent Programming Languages
{{% fragment %}}

### ... some of them

{{% /fragment %}}

<br />

{{< figure src="images/AOPlang.svg" width="50%" >}}

<br />

<div>
<small style="text-align: left"> 
[1] Collier, R.W., Russell, S.E., Lillis, D.. "Reflecting on agent programming with AgentSpeak(L). I" (2015) <br />
[2] Hindriks, K.V.. "Programming rational agents in GOAL." (2009) <br />
[3] Pokahr, A., Braubach, L., Lamersdorf, W.. "Jadex: A BDI reasoning engine." (2005) <br />
[4] Bordini, R.H., Hübner, J.F., Wooldridge, M.J.. "Programming Multi-Agent Systems in AgentSpeak using Jason." (2007) <br />
[5] D’Urso, F., Longo, C.F., Santoro, C.. "Programming intelligent iot systems with a python-based declarative tool." (2019) <br />
[6] Palanca, J., Rincon, J.A., Carrascosa, C., Julián, V., Terrasa, A.. "A flexible agent architecture in SPADE." (2022)
</small>
</div>

---

## Why did interest in BDI decrease?

BDI frameworks didn't follow latest technological developments:
- Interoperability with other General Purpose Languages (*GPL*), improving modularity of a system implementation
- Seamless adoption of the most suitable paradigm (*FP*, *OOP*, *IP*, *LP*)
- Integration with existing development tools (IDEs, code suggestions, syntax highlighters, linters...)

---

# JaKtA: <br> <u>Ja</u>son-like <u>K</u>o<u>t</u>lin <u>A</u>gents [1]

Internal Domain-Specific Language (DSL) implemented in Kotlin

* Multi-paradigm support: OOP + FP + BDI AOP
* Hosted on a mainstream language: gentle learning curve
  * Great learning resources for Kotlin
  * Significantly large community for help
* Reuses the entire existing Kotlin toolchain
  * Developed and *maintained* by the language maintainers and the community
  * Maintenance is greatly reduced
* Good ergonomy

<br />
<br />

<div>
<small style="text-align: left"> 
---<br/>
[1] Baiardi, M., Burattini, S., Ciatto, G., & Pianini, D. (2023, September). JaKtA: BDI Agent-Oriented Programming in Pure Kotlin. 
</small>
</div>

---

## Future work
JaKtA is still in its early stages, in the future we plan to: 
* Provide stable tools to emulate dynamic environments (**Simulation**)
* Expose BDI abstractions within the debugger for helping bug inspection (**Debug**)
* Experiment JaKtA integration with other tools by experimenting pactical use cases (for example: drone swarm coordination) 

---

# try jakta
<br>

[github.com/jakta-bdi/jakta-examples](https://github.com/jakta-bdi/jakta-examples)

<img src="images/qr-code.svg" width="20%" />

