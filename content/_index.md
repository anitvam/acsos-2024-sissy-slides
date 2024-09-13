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

# Multi-Paradigm Integration for the <span style="color: #AA0000">BDI</span> Resurgence

<br>


Danilo Pianini, **Martina Baiardi**, Samuele Burattini, and Giovanni Ciatto <br />
m.baiardi@unibo.it <br /><br />

<small>Department of Computer Science and Engineering (DISI)<br>
Alma Mater Studiorum — Università di Bologna <br>
Via dell’Università 50, 47522 Cesena (FC), Italy </small>

---

# BDI?

## Beliefs, Desires, Intentions

<br />

- It's a framework to model Multi-Agent Systems through *Goals*
    - Reduces the *abstraction gap* between *cognitive abstractions* and the abstractions of common paradigms
        - cognitive entities are **not functions** (as they would in *functional* programming)
        - **nor** they are *objects* (as they would in *OOP*)
        - **nor** they are **instructions** (as they would in *Imperative* programming)
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

<img src="images/paperz.png">

---

## Why did interest in BDI decrease?

### Hypothesis 1: paradigmatic issues

Unlikely: systems that use it were commonly proposed in the past

### Hypothesis 2: technological gaps

- Cumbersome interoperability with General Purpose Languages (*GPL*)
- Hard to mix-and-match paradigms as modern languages do (*FP*, *OOP*, *IP*, *LP*)
- Poor tooling (IDEs, code suggestions, syntax highlighters, linters...)
- Poor reuse mechanisms

### Hypothesis 2 + 1

**Gaps in technology accumulated** to the point that
**the paradigm became inconvenient**
compared to modern GPLs

### $\Rightarrow$ improve the technology to improve the paradigm to improve the technology to...

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

# Majority of BDI tools: Libraries

<br>
<br>

{{% multicol class="text-center" %}} {{< col class="col-75">}}

* Built for mainstream languages
* Subject to the *syntactic restrictions* of their host language
  * "True" AOP/BDI feeling hardly achieved

{{< /col >}}

{{< col class="col-25">}}

{{< fragment >}}
## <i class="fa-solid fa-arrow-right"></i> *custom language*
{{< /fragment >}}

{{< /col >}} {{% /multicol %}}

---

# AOP Custom Languages

<div>

<div class=" w-50 m-auto text-right" style="text-align: left">

<i class="fa-solid fa-check" style="color: green; margin-right: 10px"></i>
Great ergonomy for BDI AOP (made by purpose)

<i class="fa-solid fa-xmark" style="color: red; margin-right: 10px"></i>
BDI-specific, not multi-paradigm 

<i class="fa-solid fa-xmark" style="color: red; margin-right: 10px"></i>
Steep learning curve

<i class="fa-solid fa-xmark" style="color: red; margin-right: 10px"></i>
Require custom tooling - IDEs, code suggestions, syntax highlighters, linters...

<i class="fa-solid fa-xmark" style="color: red; margin-right: 10px"></i>
Small community

<i class="fa-solid fa-xmark" style="color: red; margin-right: 10px"></i>
High maintenance cost!

</div>

---

# A hybrid approach

{{< figure src="ergonomy.png" width="60%" >}} 

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

# Why kotlin?
<br>

{{% multicol %}}{{% col %}}
* Natively multi-paradigm (OOP + FP)
* Statically typed
  * With a good IDE, helps understanding what can be written where
* Direct support to internal DSLs
  * a.k.a "Type-safe builders" in the Kotlin documentation
* Support for multiplatform development
{{% /col %}}

{{< col class="text-center">}}

* Growing community
  * Strongly pushed by Google for Android
{{< figure src="android-kotlin.png" width="70%" >}}

{{% /col %}}{{% /multicol %}}


---

## Jakta: multi-paradigm AOP/BDI+OOP+FP


```kotlin
mas {                                                   // BDI specification
  fun allPlayers(team: String) =
    Regex("""<a\s(\X*?)\sdata-cy="player">(.*)<\/a>""") // Object-oriented regex library
        .findAll(URL("https://www.besoccer.com/team/squad/$team").readText())
        .map { team to it.groupValues[2] }              // Lambda expression (Functional style)

  listOf("napoli", "milan", "internazionale")           // Kotlin standard library
      .flatMap(::allPlayers)                            // Higher-order function (Functional style)
      .forEach { (team, player) ->                      // Destructuring declaration
          agent(player) {
              beliefs { fact { squad(team) } }
              goals { achieve(start) }
              plans {
                  +achieve(start) onlyIf { squad(S).fromSelf } then {
                      execute(print("Hello! I play for", S))
                  }
              }
          }
      }
}.start()
```


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

