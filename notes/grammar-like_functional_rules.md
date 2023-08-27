# Grammar-like Functional Rules for Representing Query Optimization Alternatives
## Ratings
- Time Consumed: 40min
- Degree of Mastery: 3/10
- Main topic: optimize strategies in Starburst

## Abstraction
Many researchers suggested using strategy rules to transform query execution plans into alternatives
or better plans. While this is kind of inefficient, since many rules may be elligible and still must be tested. So this paper introduced a constructive, "build block" approach.

## Concepts
1. LOLEPOP(LOw-LEvel Plan OPerator): terminals in our grammar, variation of the relational algebra. Each LOLEPOP is viewed as a function that operates on 1 or 2 tables and produces a single table as output.
2. QEP(query evaluation plan): a directed graph of LOLEPOPs.
3. STAR(STrategy Alternative Rules): a grammar-like set of parametrized production rules. A STAR defines a named, parametrized object(the nonterminal in our grammar), each of which
    - may have a condition of applicability
    - define a plan by referrencing one or more LOLEPOPs or other STARs, specifying arguments for there parameters.
4. SAP(Set of Alternative Plans for a stream).

## Essentials
This paper described how to construct - rather than to alter or to match - plans. The "build block" rules have two major advantages over plan transformation rules. They are more readily understood and can be more efficiently processed.
