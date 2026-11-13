# Smart Parcel Orientation & Sorting System

A browser-based educational digital artifact that demonstrates how abstract algebra can model parcel orientation and sorting decisions.

## Problem
Parcel-handling workflows need parcels to face a required orientation and be grouped into destination sequences. This prototype simulates those decisions and reports the operations involved.

## Mathematical model
- **Finite Abelian Group (Z4):** represents the four quarter-turn orientations. The required clockwise turn is `(target - current + 4) mod 4`.
- **Dihedral Group (D4):** represents the symmetries of a square parcel face: four rotations and four reflections. The current prototype models quarter-turn orientation and explains reflection as a supported symmetry; the batch workflow currently assumes no flip is required.
- **Permutation Group (Sn):** represents rearrangements of parcel positions. The sorting routine groups parcels by destination, and reports the resulting permutation and inversion count (the minimum number of adjacent swaps).

## Features
- Add and remove parcels with current and required orientations.
- Load a sample batch.
- Calculate the minimum quarter-turn direction.
- Sort parcels by destination and display the resulting permutation.
- Measure rotations, inversion count, and destination groups.
- Responsive dashboard for desktop and mobile.

## Run
Open `index.html` in a modern browser. No server, database, API key, or installation is required.

## Scope and limitations
This is a mathematical software simulation, not a physical conveyor, camera-based parcel recognizer, or industrial control system. Parcel orientation is entered manually. The current version assumes parcels are represented by a square face for the D4 symmetry model. A later version can add an explicit flip/reflection selector and track D4 elements as pairs (rotation, reflection).

## Test example
Load the six sample parcels and run the sorting algorithm. The dashboard reports the quarter-turn operations, destination order, resulting permutation, and inversion count.

## Authors
Student digital artifact project.
