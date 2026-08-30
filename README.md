# Computational Approaches to Nim

 Python implementation exploring the Sprague-Grundy Theorem through simulation, ordinal approximation, and neural network learning. This repository accompanies the paper "Computational Approaches to Nim: Verifying the Sprague-Grundy Theorem and Training Neural Networks" in the file Nim__Michelle_Wu.pdf.

## Abstract

 Nim is a classical two-player combinatorial game. The Sprague-Grundy Theorem states that any finite impartial normal-play game is equivalent to a Nim pile of a specific size. By calculating the XOR sum at the current state, we are able to determine if a position is a winning position and play optimally. We found relatively little work that tests the theorem computationally or uses finite cases to explore ordinal variants. In this paper, we verify the theorem computationally: a recursive simulator based on the mex (minimum excluded value) definition predicts the winner of all 10,000 randomly generated games correctly. We then approximate ordinal piles with finite surrogates and find that game length grows linearly in the approximation size. Finally, we train a multi-layer perceptron to predict optimal moves from pile sizes alone; it reaches 89.77% accuracy without being given the XOR rule. This suggests that the network learned part of the strategy, although its accuracy was not high enough to show that it learned the exact XOR rule.

## Background

 Combinatorial game theory began in 1901 when Charles Bouton solved the game of Nim. In the 1930s, Roland Sprague and Patrick Grundy proved that every finite impartial normal-play game is equivalent to a single pile of Nim. A related and more recent question is whether a standard neural network can learn the bitwise-XOR structure behind the theorem from examples alone, without the rule being programmed in. This project combines both perspectives: a recursive simulator built from the mex definition (not the XOR shortcut) is used to verify finite Nim positions, apply to finite approximations of ordinal Nim, and train an MLP to predict winning moves directly from pile sizes. All three experiments are implemented in a single file, nim_simulator.py.
