---
title: "Problem Solving and Search"
date: 2023-09-18 10:59:22
tags: [Inteligensi Buatan]
categories: []
---

## Agent and Envionment
---
* Actors adalah sebuah sistem yang berinteraksi dengan lingkungan.
* Lingkungan sendiri adalah segalanya yang diluar dari aktor (termasuk aktor
    lain)
* Aktor dapat berupa entitas fisik seperti robot, atau *software program*
    seperti chat bot. Sebaliknya Lingkungan dapat berupa ruangan fisik seperti
    ruangan, maupun virtual seperti simulasi komputer.
* Konsep rational agent, agent seharusnya berupaya melakukan tindakan yang
    benar agar berhasil, sedangkan kriteria keberhasilan perilaku agen disebut
    *Performace measure*

## PEAS (Performace measure, Environment, Actuators, Sensors)
---
* Ketika merancang sebuah agent, harus mendefinisikan lingkungan masalah (*task
    environment*), yakni:
1. Performace measure : apa saja komponen pengukur keberhasilan si agent?
2. Environment : kondisi apa aja yang ada disekitar agent:
3. Actuators : Apa saja yang bisa dilakukan si agent
4. Sensors: Apa saja yang menjadi input si agent

## Jenis Environment
---
* Fully obserable (vs. partially observable) : apakah semua informasi diketahui
* Deterministic : apakah next state di tentukan dari current state dan action
* Episodic : apakah tergantung pada pengalaman
* Static : apakah environment berubah ketika agent tidak bertindak
* Discrete
* Single agent (vs multiagent) : apakah agent bertindak sendiri

## Jenis-Jenis Agent
---
* Simple reflex agents: berdasarkan persepsi yang terakhir
* Model-based reflex agent: memiliki repersentasi internal tentang keadaan
    sekitar
* Goal-based agents: melakukan penilaian kuantitatif terhadap suatu keadaan
    lingkungan
* Learning agents: belajar dari pengalaman, meningkatkan kinerja.


### Summary
---
* A rational agent must have goals
* Sebuah task environment mendefinisikan PEAS ( *performance measure,
    environment, action dan sensors* ) 
* Agent funciton memetakan persepsi terhadap tindakan
* Agent program mengimplementasikan agent function

### Well-Define Problem and Solution
---
Problem dapat dirumuskan dengan 5 komponen
1. Initial state
2. Action: Successor Function
3. Goal Test
4. Path Cost (Optimal solution)

```yaml
8-Queen Problem
- State: Susunan 0,.., 8 ratu pada papan catur tanpa ada yang bersinggungan
- Initial State: Tidak ada ratu pada papan catur
- Successor Function: Masukan Ratu ke papan catur
- Goal Test: Tidak ada ratu yang saling serang
```

