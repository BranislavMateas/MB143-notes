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

# Podmínena pravdepodobnost
P(A|B) - aká je šanca, že sa stane A, ak sa stalo B?

Počítame pravdepodobnosť (A prienik B) a to delené P(B)

Imagine you're looking at the weather forecast for tomorrow. There's a 30% chance of rain overall for the day. We could write this as:
P(Rain) = 0.3
Now, a meteorologist tells you: "By the way, there's a cold front coming in tomorrow morning."
You ask: "Well, if this cold front is definitely coming, what's the chance of rain now?"
This is exactly what conditional probability answers. You're asking for the probability of rain GIVEN THAT there's a cold front. In math notation, this is:
P(Rain | Cold Front)
The vertical bar "|" simply means "given that" or "if we know this is true."
Let's say the meteorologist tells you that when cold fronts come in, it rains 60% of the time. This means:
P(Rain | Cold Front) = 0.6
This is higher than the original 30% chance because the cold front information has updated our expectations.

Toto nejde spočítať, keď máš len P(A) a P(B), v takom prípade potrebuješ bližší kontext.

does the order with  | matter?

Yes, the order in P(A|B) absolutely matters! P(A|B) and P(B|A) are generally different values that represent different conditional probabilities.
Let me explain with our weather example:
P(Rain|Cold Front) = "probability of rain, given that there's a cold front"
P(Cold Front|Rain) = "probability of a cold front, given that it's raining"
These are fundamentally different questions:

P(Rain|Cold Front) asks: "When cold fronts happen, how often does it rain?"

Maybe 60% of cold fronts bring rain, so P(Rain|Cold Front) = 0.6


P(Cold Front|Rain) asks: "When it rains, how often is there a cold front?"

Maybe 80% of rainy days involve cold fronts, so P(Cold Front|Rain) = 0.8



Even though they relate to the same events, they're asking different questions about the relationship between those events. It's similar to how "percentage of doctors who are women" and "percentage of women who are doctors" are very different statistics.
This difference is why we have Bayes' theorem, which lets us convert between P(A|B) and P(B|A):
P(A|B) = [P(B|A) × P(A)] / P(B)

To calculate P(A ∩ B) - the probability that both events A and B occur - you have two main approaches:
Method 1: Using the conditional probability formula
If you know the conditional probability P(A|B) and the probability of B, you can calculate:
P(A ∩ B) = P(A|B) × P(B)
For example, using our weather scenario:

If the probability of a cold front is P(B) = 0.4
And the probability of rain given a cold front is P(A|B) = 0.6
Then P(A ∩ B) = 0.6 × 0.4 = 0.24

Method 2: Using the conditional probability formula in reverse
Alternatively, if you know P(B|A) instead, you can use:
P(A ∩ B) = P(B|A) × P(A)
For example:

If the probability of rain tomorrow is P(A) = 0.3
And the probability of a cold front given that it rains is P(B|A) = 0.8
Then P(A ∩ B) = 0.8 × 0.3 = 0.24

