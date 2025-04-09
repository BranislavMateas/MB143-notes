# MB143-notes
----
# Pravděpodobnostní prostor

Pravděpodobnostní prostor je matematický základ pro modelování náhodných experimentů nebo situací, kde se vyskytuje náhodnost. Skládá se ze tří základních částí:

## Základní prostor (Ω)
### Toto je neprázdná množina, která obsahuje všechny možné výsledky náhodného experimentu.

## σ-algebra (A)
### Toto je kolekce podmnožin Ω (nazývaných jevy), která splňuje určité matematické vlastnosti. V podstatě určuje, kterým kolekcím výsledků můžete přiřadit pravděpodobnosti.

## Pravděpodobnostní míra (P)
### Toto je funkce, která přiřazuje pravděpodobnost (číslo mezi 0 a 1) každému jevu v σ-algebře.

## Příklad pro lepší pochopení:
Představme si hod mincí:
- Základní prostor (Ω): {Hlava, Orel} - všechny možné výsledky
- σ-algebra (A): {∅, {Hlava}, {Orel}, {Hlava, Orel}} - všechny možné podmnožiny Ω
- Pravděpodobnostní míra (P):
  - P(∅) = 0 (nemožný jev)
  - P({Hlava}) = 0,5 (pravděpodobnost padnutí hlavy)
  - P({Orel}) = 0,5 (pravděpodobnost padnutí orla)
  - P({Hlava, Orel}) = 1 (jistý jev)

## ! σ-algebra není vždy stejná jako potenční množina ! 
## ! σ-algebra je kolekce podmnožin (jevů) základního prostoru, kterým chceme přiřadit pravděpodobnost. !
## ! ∅ není v základnom prostore, pretože ten obsahuje len reálné možné stavy výsledku experimentu !
## ! Pravděpodobnost celého základního prostoru Ω je vždy 1 (nebo 100%). !
