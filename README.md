# Credit Card Validation and Detection

Before a credit card is submitted to a financial institution, it generally makes sense to run some simple reality checks on the number. The numbers are a good length and it's common to make minor transcription errors when the card is not scanned directly.

The first check people often do is to validate that the card matches a known pattern from one of the accepted card providers. Some of these patterns are:

      +============+=============+===============+
      | Card Type  | Begins With | Number Length |
      +============+=============+===============+
      | AMEX       | 34 or 37    | 15            |
      +------------+-------------+---------------+
      | MasterCard | 51-55       | 16            |
      +------------+-------------+---------------+
      | Visa       | 4           | 13 or 16      |
      +------------+-------------+---------------+

Writing code to detect these card types is simple enough, but additionally, card numbers are generated so that they all validate against the [Luhn Check](https://fr.wikipedia.org/wiki/Formule_de_Luhn#Algorithme).



Lets write some code to detect and identify card types.

## Story 1 - Detect card type

    As a user
    When I provide a card number
    The card type is detected

## Story 2 - Luhn validity

    As a user
    When I provide a card number
    It is validated against the luhn algorithm

