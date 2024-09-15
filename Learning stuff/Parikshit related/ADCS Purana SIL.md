---
tags:
  - Evo-1
  - ADCS
  - Parikshit
  - "#Code"
  - "#Simulation"
aliases:
  - Akash aur Shubhakriti ka Fornication
Status: work-in-progress
---
__Date - 15-09-2024__

__Time - 11:13__


# *Main Content*☣
---
## Introduction

This documentation is just to have a basic explanation of what I myself understand of the old SIL made by the old seniors (aka Akash and Shubhakriti). I think that if we're gonna be having a meeting with Akash, we should at least have a very good insight into what exactly we're facing with this. I don't know how we got here, I don't know where it comes from, but I can figure out what it does based on the variable and function names, I just can't figure out where the formulas came from.
The reason for me making this document is just out of pure spite, I'm done listening to other people, feeling bad because their words make sense, and never actually going through with anything because of that. This is what happened in Parikshit, this is what happened during JEE and boards, and it's still happening. I'm done never taking action because I can never objectively come to a conclusion. Now, I'm just gonna figure out the number of sides, and then join the side with more of my friends lol. So, I'm technically making this document due to the reason of just knowing enough about the SIL so that I can say to Akash that we're not using it cause fuck him and his love story with Shubhakriti and fuck Ankit too.

## adcs_engine

This is where the `main()` function is. I think that function is just used for the main idea that is to just run it. There is also a `adcs_engine()` function:

``` C++
double **adcs_engine(int time, double**moi_satellite, double**prev_req_var)
```

This function basically initializes the adcs engine (or SIL). In this function, out of the parameters:
- `int time`: It's the Julian date of the current epoch.
- `double **moi_satellite`: The Moment of Inertia of the satellite.
- `double **prev_req_var`: the previous required variables, that they probably get from the OBC (on-board computer)
These parameters take arguments as a double pointer to a `double` variable....
Well, some of them do. Some take `int`, but yeah.
