# tippitytappity-design

tippitytappity is a program to practice typing


## Data model
 
```mermaid
classDiagram
  Word <|-- Name
  Word <|-- Item
  Word --> Character
TypingSession --> Word
class Character{
        - correct: bool
        - value: char
        - timeToType: float
  `     + isCorrect() bool
        + getVal() char
  }
class Word{
        - text: string
        - characters: vector~Character~
        + getLen() int
        + getAcc() float
        + getText() string
}
class Name{
        - origin: string
        + getOrigin() string
}
class Item{
        - category: string
        + getCategory() string
}
class TypingSession{
        - wordQueue: vector~Word~
        - currIndex: int
        + start()
        + nextWord() Word
        + submitUserInput(input: string)
}
```
