---
title: Basic Electrical Theory
keywords: electrical, electronics, basics
sidebar: main_sidebar
permalink: main_basic_theory.html
folder: main
---
## Table of Contents
1. [Overview](#Overview)
2. [Current](#Current)
    1. [What is Charge?](#Charge)
    2. [Important Notes](#INC)
3. [Voltage](#Voltage)
4. [Power](#Power)
5. [Component Communication](#CC)
    1. [PWM](#PWM)
    2. [CAM](#CAM)
6. [Tips and General Knowledge](#T&G)
    1. [Ohm's Law](#Ohm)
    2. [Using a Multimeter](#Mult)
    3. [General Tips](#Gen)

## Overview <a name="Overview"></a>
Electricity, according to [dictionary.com](http://www.dictionary.com/browse/electricity), is the study of electric charges. It powers all electronics. It is a vast field, but for FRC purposes, you really just need to grasps these 3 concepts: *Voltage, Current, Power*

## Current <a name="Current"></a>
It is common sense that we know electricity flows. The word "current" is used to describe this flow of electricity. Just like how water flows through a river is water current, the flow of electricity through a wire is electric current.

Formally electric current is defined as the amount of charge traveling through a given cross section in a given amount of time. To make it less wordy, it means the flow of charge. **Remember current is the flow of charge, not electrons**.

### What is charge? <a name="Charge"></a>
Charge is the fundamental quantity of electricity. There are positive charges and negative charges. In an atom, the electrons have negative charge, and the protons have positive charge. By convention, people usually look at the movement of positive charge going through a wire as current. *However, that does not mean current is the movement of protons through the wire*.

Well then, if current is not the movement of protons through a wire, then how does a positive charge move?

We all know that positive attracts negative and vice versa. Therefore, when the robot is connected, the positive terminal of the battery attracts the electrons on the nearby atom, which causes the nearby atom to have a "gap" in its electron cloud, making the entire atom positive temporarily. Then this "positive" atom attracts the electrons in its nearby atom, repeating the process all the way until the end of the wire at the negative terminal of the battery. This creates an impression that some sort of positive charge carrier travels through the wire, but in reality, it is just that positive charged "gap" that is propagating through the wire. Since the gap goes from the positive terminal of the battery to the negative terminal, by convention, electric current flows from the positive end to the negative end.

### Important Notes <a name="INC"></a>
-Since current flows only one way, **never mix up the negative and the positive terminal of any electrical component!!!** (Seems silly, but believe me many people will make this dumb mistake)
-Current is expresses in units all *Amperes* or *Amps* or just *A* for short.
-Amperes is Coulombs per second, fitting the definition of current.
