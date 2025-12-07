# Battery Design Optimization Assignment
## CHEM 233 - Final Module: Electrochemistry and Engineering Applications

### Overview
In this assignment, you will systematically analyze battery design from first principles. You will examine all possible electrode combinations, determine which are viable (galvanic vs. electrolytic), and optimize battery systems for three specific applications.

**Motivating Question:** Why is a 1.5V D-cell battery physically larger than a 9V battery?

---

## Part 1: Systematic Electrochemical Analysis

### Step 1: Calculate Cell Voltages for ALL Combinations

**Objective:** Determine the theoretical voltage of every possible electrode pair.

**Formula:**
```
E°cell = E°cathode - E°anode
```

**Process:**
1. Take each material from your assigned set
2. Consider it as both anode and cathode in combination with every other material
3. Calculate E°cell for all combinations (you should get 12 total)
4. Classify each combination as:
   - **Galvanic** (E°cell > 0): Spontaneous, can provide energy
   - **Electrolytic** (E°cell < 0): Non-spontaneous, requires energy input

**Important:** Calculate voltages for ALL combinations, but only proceed with capacity/energy calculations for galvanic cells.

---

### Step 2: Calculate Capacity and Energy Density (Galvanic Cells Only)

**Objective:** Determine the energy storage characteristics of viable battery cells.

#### Mass Calculation
Use realistic molecular weights that reflect actual battery construction:
- **Anode (reducing agent):** Elemental molecular weight (pure metal)
- **Cathode (oxidizing agent):** Compound molecular weight (salt in solution)

```
Total Mass = (anode_coefficient × elemental_MW) + (cathode_coefficient × compound_MW)
```

#### Capacity Calculation
**Formula:**
```
Capacity (mAh/kg) = (n × 96,485 × 1000) / (3600 × total_mass_g)
```

Where:
- n = total electrons transferred (use LCM of half-reaction electrons)
- 96,485 = Faraday constant (C/mol)
- 1000 = conversion factor (g to kg)
- 3600 = conversion factor (s to h)
- total\_mass\_g = total mass of reactants per reaction (grams per mole)

#### Energy Density Calculation
**Formula:**
```
Energy Density (Wh/kg) = E°cell × Capacity / 1000
```

---

## Part 2: Application-Specific Design

### Step 3: Optimize for Three Applications

**Process:**
1. Use ONLY galvanic cells (E°cell > 0)
2. Select cells that meet voltage requirements (hard cutoff)
3. Calculate mass needed for each application

#### Applications:

**1. Medical Pacemaker**
- Target voltage: 3.0 V
- Current: 10 μA
- Runtime: 10 years (87,600 hours)
- Goal: Minimum weight

**2. LED Flashlight**
- Target voltage: 1.5 V
- Current: 400 mA
- Runtime: 2 hours
- Goal: Maximum capacity

**3. Portable Electronics**
- Target voltage: 3.7 V
- Current: 500 mA
- Runtime: 1 hour
- Goal: Balanced energy density

#### Mass Calculation for Applications
**Formula:**
```
Mass Needed (kg) = (Current_mA × Runtime_hours) / Capacity_mAh/kg
```

**Example:**
- Flashlight: (400 mA × 2 h) / 1000 mAh/kg = 0.8 kg

---

## Part 3: Analysis and Comparison

### Step 4: Engineering Trade-offs

**Analyze and discuss:**

1. **Voltage vs. Capacity Trade-off**
   - Which combinations give highest voltage?
   - Which combinations give highest capacity?
   - Why can't you maximize both simultaneously?

2. **Application Optimization**
   - Why do different applications require different battery designs?
   - How does current requirement affect optimal choice?
   - Why might pacemaker batteries be acceptable at several kg theoretically?

3. **Real-World Context**
   - How does your analysis explain the D-cell vs. 9V battery size difference?
   - What practical factors are ignored in theoretical calculations?
   - Why are real batteries much lighter than your calculations predict?

---
## Notes  
1. Some of your battery masses may seem unrealistic, but we're ignoring a lot of complexity here, so as long as your calculations are sound, trust your numbers.
2. We're ignoring things like overvoltage, the fact that voltages drop as the reactions proceed (reach equilibrium), mass of solvents in a "wet" cell, packaging constraints, environmental impacts, or safety.  However, your work here will provide a "first pass" look at this problem that would give ideas of where to investigate batteries that are actual feasible for the applications described.
3. Pay close attention to the need for series configurations.  For example, if you need 3.7V but your cell generates only 2.0V, you'll need two cells in series.  Be sure to account for this doubling (or tripling or whatever) in your density/capacity calculations.
4. I recommend using a spreadsheet, but it's not required.  Still, trust me, you'll be glad you did!


## Deliverable

A well written, succinct engineering-style report that has the following:

### Summary, Intro, and methodology
- Include an executive summary as before with the highlights of your analysis
- Introduce the problem briefly, including target applications - Describe how you arrived at your numbers.


### Required Tables

**Table 1: Complete Electrochemical Analysis**
- All 12 electrode combinations
- Cell voltage for each
- Cell type (Galvanic/Electrolytic)
- For galvanic cells only: capacity, energy density, balanced equation

**Table 2: Application Analysis**
- For each application: optimal cell choice
- System configuration (cells in series if needed)
- Mass required to meet runtime specifications
- Justification for choice


### Engineering Analysis

Write a brief analysis (1-2 paragraphs each) addressing:
1. Why D-cell batteries are larger than 9V batteries
2. Trade-offs between voltage, capacity, and energy density
3. How your would approach calculating the actual capacity of a battery given that voltages drop as the reactions approach equilibrium.

As usual, cite any sources you use for this analysis.

### Visuals
None required!  But feel free to add anything that you think might help or that fit your style.

---

## Key Formulas Reference

```
Cell Voltage:           E°cell = E°cathode - E°anode

Mass (mixed approach):  Total = anode_coeff × element_MW + cathode_coeff × compound_MW

Capacity:               (n × 96,485 × 1000) / (3600 × mass_g) [mAh/kg]

Energy Density:         E°cell × Capacity / 1000 [Wh/kg]

Runtime per kg:         Capacity / Current_mA [hours/kg]

Mass Needed:            (Current_mA × Runtime_h) / Capacity [kg]
```

---



### Expected Insights

By the end of this analysis, you should understand:
- Why battery design involves fundamental trade-offs
- How application requirements drive material selection
- The relationship between electrochemistry and practical engineering
- Why theoretical calculations provide limits rather than practical predictions

This systematic approach mirrors how battery engineers actually design energy storage systems for specific applications.
