# Smart Parcel Orientation & Sorting System

A browser-based educational digital artifact that demonstrates how abstract algebra can model parcel orientation and sorting decisions.

## Live demo
- [Main ParcelFlow dashboard](https://meerab00.github.io/Smart-Parcel-Sorting-System/)
- [Z4 Orientation Optimizer](https://meerab00.github.io/Smart-Parcel-Sorting-System/z4-lab.html)\n- [D4 Symmetry Checker](https://meerab00.github.io/Smart-Parcel-Sorting-System/d4-lab.html)\n- [Sn Parcel Sequence Optimizer](https://meerab00.github.io/Smart-Parcel-Sorting-System/sn-lab.html)

## Problem
Parcel-handling workflows need parcels to face a required orientation and be grouped into destination sequences. This prototype simulates those decisions and reports the operations involved.

## Mathematical model
- **Finite Abelian Group (Z4):** represents the four quarter-turn orientations. The required clockwise turn is `(target - current + 4) mod 4`.
- **Dihedral Group (D4):** represents the symmetries of a square parcel face: four rotations and four reflections. The interactive D4 lab demonstrates rotation and reflection operations. The main batch workflow currently calculates quarter-turn orientation only.
- **Permutation Group (Sn):** represents rearrangements of parcel positions. The sorting routine groups parcels by destination and reports the resulting permutation and inversion count (the minimum number of adjacent swaps needed to reach that order).

## Features
- Add and remove parcels with current and required orientations.
- Load a sample batch.
- Calculate the minimum quarter-turn direction.
- Sort parcels by destination and display the resulting permutation.
- Measure rotations, inversion count, and destination groups.
- Interactive D4 symmetry demonstration.
- Responsive dashboard for desktop and mobile.

## Run
Open `index.html` in a modern browser. No server, database, API key, or installation is required.

## Scope and limitations
This is a mathematical software simulation, not a physical conveyor, camera-based parcel recognizer, or industrial control system. Parcel orientation is entered manually. The main batch workflow currently assumes no flip is required; the separate D4 lab demonstrates the eight square symmetries interactively.

## Sample test
Load the six sample parcels and run the sorting algorithm. Expected results:
- Sorted destination sequence: PKG-1004, PKG-1003, PKG-1001, PKG-1005, PKG-1002, PKG-1006
- Total minimum quarter-turns: 7
- Resulting permutation (1-based): [4, 3, 1, 5, 2, 6]
- Inversion count: 6
- Destination groups: 4

## Authors
Student digital artifact project.
