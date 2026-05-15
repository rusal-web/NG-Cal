# Borrowing Power Reality Check: The Impact of the May 2026 Budget

## Overview
This repository contains a single-file, interactive HTML/JS web application designed to proxy and stress-test Australian mortgage borrowing capacities under the rules introduced in the May 2026 Budget. 

The calculator mechanically demonstrates the massive gap in borrowing power by contrasting maximum loan sizes for **Established Post-2027 (No Negative Gearing)** properties against **New Build / Grandfathered (With Negative Gearing)** properties.

## Features
* **Three-Tiered Lender Logic:** Calculates exact scenarios simultaneously across Major Banks (3.0% assessment buffer), Preferred Lenders (2.5% buffer), and Specialist Lenders (2.0% buffer).
* **Advanced Goal-Seeking Algorithm:** Uses a custom iterative JavaScript loop to dynamically calculate usable tax refunds, net rental losses, and maximum borrowing capacity for negatively geared properties.
* **Strict Manual Inputs:** Uses precise user-defined Monthly Living Expenses (bypassing dynamic HEM estimates) to ensure highly predictable and stable math across all lender tiers.
* **Integrated Tax Engine:** Incorporates strict Australian Tax Brackets and a flat 2.0% Medicare Levy.
* **Responsive UI:** Built with Tailwind CSS, featuring dynamic thousands-separator formatting for user inputs and a clean, scannable comparison UI.

## Tech Stack
* **Markup/Styling:** HTML5, CSS3 (Tailwind CSS via CDN)
* **Logic:** Vanilla JavaScript (ES6)
* **Architecture:** Zero-dependency, single-file application.

## Installation & Local Usage
Because this is a single-file application with no backend or external build dependencies, running it is instant:
1. Clone this repository to your local machine.
2. Open the `.html` file directly in any modern web browser (Chrome, Safari, Edge, Firefox).

## Mathematical Assumptions & Logic
* **Rent Shading:** A flat 20% shade (0.80 multiplier) is applied to all expected rental income.
* **Input Sanitization:** The JS engine actively strips comma formatting dynamically as the user types to prevent `NaN` math errors.
* **IO Periods:** Selecting an Interest Only (IO) period compresses the Principal & Interest (P&I) repayment into the remaining loan term, accurately reflecting APRA assessment requirements.

## Disclaimer
*This calculator is an educational proxy tool designed to illustrate the mechanical impact of the May 2026 Budget. The formulas have been calibrated against aggregate market data with an estimated Standard Deviation (SD) of ±6% to ±9% depending on the borrower's exact tax bracket, chosen IO term, and specific lender policies. It does not constitute financial advice. Actual loan approvals are subject to comprehensive lender-specific HEM, DTI, and credit assessments.*
