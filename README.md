# Groceries

Where should you buy groceries? This applied math project minimizes grocery prices while accounting for travel time, checkout time, and item quality.

## Project Plan

1. Create a database of stores, their locations, and their prices.
   - Extension: Record per-ounce pricing and account for item sizes. For this project, I simply chose a common, medium size for each item.
2. Create a linear programming Excel sheet that minimizes price—accounting for travel time, checkout time, and item quality.
   - Extension: Account for other time consuming factors like store layout, parking availability, distance between nearby stores, and other subjective factors like customer service.
3. Use sensitivity analysis to answer questions like:
   - How much shorter would the checkout time at Walmart have to be for us to buy there?
   - How much less must we value our time in order to buy at Target v.s. Safeway?
   - How much closer must Walmart be for us to shop there instead of Safeway?
4. Implement that Excel sheet into a usable website.

### 1. Create a database of stores, their locations, and their prices.

#### Stores

- Walmart in Mountain View (Showers)
- Target in Mountain View (Showers)
- Costco in Mountain View (Rengstorff)
- Safeway in Palo Alto (Midtown)
- Walgreens in Palo Alto (Midtown)
- CVS in Palo Alto (Midtown)
- Trader Joe’s in Palo Alto (T&C)
- CVS in Palo Alto (T&C)

#### Items

- Milk (1/2 gal, lactose free, fat free)\*
- Eggs (12 white, grade A-AA)
- Flour (5 lb, all-purpose white)
- Bread (27 oz, Dave’s Killer Bread)
- Cheerios (18 oz, family size)\**
- Bananas (5 pc)
- Grapes (1.5-2.25-3 lb, green)
- Strawberries (1 lb)
- Saline Solution (24 oz)
- Lotion (16 oz, CeraVe Cream)
- Shampoo (Pantene Classic)
- Toilet Paper (12 rolls, Scott 1000s)

\*admittedly, at this point, it’s no longer milk
\**or the off-brand equivalent (to save $$$)

### 2. Create a linear programming Excel sheet that minimizes price—accounting for travel time, checkout time, and item quality.

**Evolutionary** - 48.859s ($13.80)
**GRG multitask** - 73.297s ($13.80)
**GRG nonlinear** - 0.125s ($20.71)

#### Ideally

- Constraints are linear
- Objectives are linear
- Use simplex method
- Find global optimal solution

#### Reality

- Constraints are linear
- Objectives are non-linear, non-smooth\*
- Use [evolutionary method](https://engineerexcel.com/excel-solver-solving-method-choose/)
- Find local optimal solution

\*non-smooth functions are not infinitely differentiable (e.g. cannot take 2nd derivative)

### 3. GRG nonlinear and evolutionary methods don’t have sensitivity analyses… sadly…
